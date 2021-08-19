http://manishearth.github.io/blog/2017/01/14/stop-ascribing-meaning-to-unicode-code-points/ Let’s Stop Ascribing Meaning to Code Points.

Breaking Our Latin-1 Assumptions http://manishearth.github.io/blog/2017/01/15/breaking-our-latin-1-assumptions/ 

UAX #29: Unicode Text Segmentation https://unicode.org/reports/tr29/ 

https://github.com/unicode-rs/unicode-segmentation https://github.com/unicode-rs/unicode-segmentation

Iterators which split strings on Grapheme Cluster or Word boundaries, according to the Unicode Standard Annex #29 rules.

 http://site.icu-project.org/home

ICU is a mature, widely used set of C/C++ and Java libraries providing Unicode and Globalization support for software applications. ICU is widely portable and gives applications the same results on all platforms and between C/C++ and Java software.

http://userguide.icu-project.org/          

http://userguide.icu-project.org/boundaryanalysis

http://userguide.icu-project.org/boundaryanalysis#TOC-Character-Boundary

https://stackoverflow.com/questions/40878804/how-to-count-grapheme-clusters-or-perceived-emoji-characters-in-java

https://engineering.linecorp.com/en/blog/the-7-ways-of-counting-characters/

https://softwareengineering.stackexchange.com/questions/13207/string-class-based-on-graphemes

https://news.ycombinator.com/item?id=13832831
Emoji.length == 2 

This is most definitely not a solved problem, because graphemes (visual symbols) are a poor way to deal with unicode in the real world. Pretty much all systems either deal with the length in bytes (if they're old-style C), in code units / byte pairs (if they're UTF-16 based, like windows, java and javascript), or in unicode code points (if they're UTF-8 based, like every proper system should be). Dealing with the length in visual symbols is actually pretty much impossible in practice because databases won't let you define field lengths in graphemes.

The way things compose: bytes combine into code points (unicode numbers), and code points combine into graphemes (visual symbols). In UTF-16 for legacy compatibility reasons with UCS-2, code points decompose into code units (byte pairs), and high code points, which need a lot of bits to represent their number, need two code units (4 bytes) instead of one.

Java and JavaScript are UTF-16 based, so they measure length in code units and not code points. An emoji code point can be a low or high number depending on when it was added. Low numbers can be stored in two bytes, high numbers need four bytes. So an emoji can have length 1 or 2 in UTF-16. However, when moving to the database it will typically be stored in UTF-8, and the field length will be code points, not code units. So, that emoji will have a length of 1 regardless of whether it is low or high. You don't notice this as a problem because app-level field length checks will return a bigger number than what the database perceives, so no field length limits are exceeded.

There isn't any such thing as "characters" in code. In documentation when they say "characters" usually they mean bytes, code units or code points. Almost never do they mean graphemes, which is intuitively what people think they mean. The bottom line is two-fold: (A) always understand what is meant in documentation by "length in characters", because it almost never means the intuitive thing, and (B) don't try to use graphemes as your unit of length, it won't work in practice.

https://wiki.sei.cmu.edu/confluence/display/java/STR01-J.+Do+not+assume+that+a+Java+char+fully+represents+a+Unicode+code+point

The char data type is based on the original Unicode specification, which defined characters as fixed-width 16-bit entities. The Unicode Standard has since been changed to allow for characters whose representation requires more than 16 bits. The range of Unicode code points is now U+0000 to U+10FFFF. The set of characters from U+0000 to U+FFFF is called the basic multilingual plane (BMP), and characters whose code points are greater than U+FFFF are called supplementary characters. Such characters are generally rare, but some are used, for example, as part of Chinese and Japanese personal names. To support supplementary characters without changing the char primitive data type and causing incompatibility with previous Java programs, supplementary characters are defined by a pair of Unicode code units called surrogates. According to the Java API [API 2014] class Character documentation (Unicode Character Representations):

The Java platform uses the UTF-16 representation in char arrays and in the String and StringBuffer classes. In this representation, supplementary characters are represented as a pair of char values, the first from the high-surrogates range, (\uD800-\uDBFF), the second from the low-surrogates range (\uDC00-\uDFFF).

A char value, therefore, represents BMP code points, including the surrogate code points, or code units of the UTF-16 encoding. An int value represents all Unicode code points, including supplementary code points. The lower (least significant) 21 bits of int are used to represent Unicode code points, and the upper (most significant) 11 bits must be zero. Similar to UTF-8 (see STR00-J. Don't form strings containing partial characters from variable-width encodings), UTF-16 is a variable-width encoding. Because the UTF-16 representation is also used in char arrays and in the String and StringBuffer classes, care must be taken when manipulating string data in Java. In particular, do not write code that assumes that a value of the primitive type char (or a Character object) fully represents a Unicode code point. Conformance with this requirement typically requires using methods that accept a Unicode code point as an int value and avoiding methods that accept a Unicode code unit as a char value because these latter methods cannot support supplementary characters.

https://htmlpreview.github.io/?https://github.com/unicode-org/icu/blob/maint/maint-67/icu4c/readme.html

https://unicode-org.github.io/icu-docs/#/icu4c/


https://bollu.github.io/mathemagic/declarative/index.html https://news.ycombinator.com/item?id=23231361

 

https://apps.timwhitlock.info/unicode/inspect?s=e%CC%81 unicode inspector

 

é <- this one is two codepoints

é <- this one isn’t

 

I thought it would be useful to share my personal list of scripts that break our Latin-1 assumptions. This is a list I mentally check against whenever I am attempting to reason about text. I check if I’m making any assumptions that break in these scripts. Most of these concepts are independent of Unicode; so any program would have to deal with this regardless of encoding.

I again recommend going through eevee’s post, since it covers many related issues. Awesome-Unicode also has a lot of random tidbits about Unicode.

 
https://en.wikipedia.org/wiki/Arabic_alphabet#Table_of_basic_letters


https://www.gutenberg.org/catalog/

https://en.wikipedia.org/wiki/Devanagari_(Unicode_block)

https://stackoverflow.com/questions/6805311/combining-devanagari-characters

http://unicode.org/faq/char_combmark.html

http://unicode.org/faq/

 

http://www.unicode.org/versions/Unicode6.0.0/ch04.pdf

https://en.wikipedia.org/wiki/Unicode_block

 

4. Grapheme clusters: how many of what end users might consider "characters". In this example, the Devanagari syllable "ni" must be composed using a base character "na" (न) followed by a combining vowel for the "i" sound ( ि), although end users see and think of the combination of the two "नि" as a single unit of text. In this sense, the example string can be thought of as containing 4 “characters” as end users see them. A default grapheme cluster is specified in UAX #29, Unicode Text Segmentation, as well as in UTS #18, Unicode Regular Expressions.

 

The choice of which count to use and when depends on the use of the value, as well as the tradeoffs between efficiency and comprehension. For example, Java, Windows, and ICU use UTF-16 code unit counts for low-level string operations, but also supply higher level APIs for counting bytes, characters, or denoting boundaries between grapheme clusters, when circumstances require them. An application might use these to, say, limit user input based on a number of "screen positions" using the user-perceived "character" (grapheme cluster) count. Or the application might have an internal limit based on storage allocation in a database field counted in bytes. This approach allows for efficient low-level processing, with allowance for higher-level usage. However, for a very high-level application, such as word-processing macros, grapheme clusters alone may be sufficient.

 

https://emojipedia.org/

https://blog.emojipedia.org/what-the-2021-unicode-delay-means-for-emoji/

 

https://emojipedia.org/emoji-zwj-sequence/

https://emojipedia.org/eye-in-speech-bubble/

https://emojipedia.org/emoji-flag-sequence/

https://blog.emojipedia.org/emoji-zwj-sequences-three-letters-many-possibilities/

 

https://en.wikipedia.org/wiki/Unicode_block

A Unicode block is one of several contiguous ranges of numeric character codes (code points) of the Unicode character set that are defined by the Unicode Consortium for administrative and documentation purposes. Typically, proposals such as the addition of new glyphs are discussed and evaluated by considering the relevant block or blocks as a whole.

Each block is generally, but not always, meant to include all the glyphs used by one or more specific languages, or in some general application area such as mathematics, surveying, decorative typesetting, social forums, etc.

Unicode blocks are identified by unique names, which use only ASCII characters and are usually descriptive of the nature of the symbols, in English; such as "Tibetan" or "Supplemental Arrows-A". (When comparing block names, one is supposed to equate uppercase with lowercase letters, and ignore any whitespace, hyphens, and underbars; so the last name is equivalent to "supplemental_arrows__a" and "SUPPLEMENTALARROWSA".[1]

Blocks are pairwise disjoint, that is, they do not overlap. The starting code point and the size (number of code points) of each block are always multiples of 16; therefore, in the hexadecimal notation, the starting (smallest) point is U+xxx0 and the ending (largest) point is U+yyyF, where xxx and yyy are three or more hexadecimal digits. (These constraints are intended to simplify the display of glyphs in Unicode Consortium documents, as tables with 16 columns labeled with the last hexadecimal digit of the code point.[1]) The size of a block may range from the minimum of 16 to a maximum of 65,536 code points.

Every assigned code point has a glyph property called "Block", whose value is a character string naming the unique block that owns that point.[2] However, a block may also contain unassigned code points, usually reserved for future additions of characters that "logically" should belong to that block. Code points not belonging to any of the named blocks, e.g. in the unassigned planes 3–13, have the value block="No_block".[1]

 

https://unicode.org/emoji/charts/full-emoji-list.html unicode emojis, grapheme clusters


https://stackoverflow.com/questions/40878804/how-to-count-grapheme-clusters-or-perceived-emoji-characters-in-java

https://users.rust-lang.org/t/how-to-iterate-over-emojis-grapheme-clusters/14254

https://users.rust-lang.org/t/how-to-iterate-over-emojis-grapheme-clusters/14254/4

https://hsivonen.fi/string-length/ <- this is awesome!!!!!

https://blog.jonnew.com/posts/poo-dot-length-equals-two but, is that true?

https://stackoverflow.com/questions/54369513/how-to-count-the-correct-length-of-a-string-with-emojis-in-javascript

 

For example, the character encoding scheme ASCII comprises 128 code points in the range 0hex to 7Fhex, Extended ASCII comprises 256 code points in the range 0hex to FFhex, and Unicode comprises 1,114,112 code points in the range 0hex to 10FFFFhex. The Unicode code space is divided into seventeen planes (the basic multilingual plane, and 16 supplementary planes), each with 65,536 (= 216) code points. Thus the total size of the Unicode code space is 17 × 65,536 = 1,114,112.

 

Why is Java’s primitive “char” designed to respond to 1 code unit of UTF-16 instead of 1 grapheme or 1 code point? Because when Java was first designed, Unicode’s entire code points were defined in 16 bit.

The concept of “encoding every character in 16 bits” was something that the original designers of Unicode were proud enough to include in their design principles.(Not long after Java was announced, Unicode was expanded beyond 16 bits. As of Unicode 7.0, It is defined as U+10FFFF, or 17*65536=1,114,112.) Meanwhile, MySQL or Oracle’s “utf8” charset is more closer to CESU-8 than it is to UTF-8, possibly requiring more space. When encoding in UTF-8, charsets “AL32UTF8” (Oracle) or “utf8mb4” (MySQL) must be used. Swift, one of the most recent programming languages, is defined so that a character type is expressed as 1 grapheme.

 

https://en.wikipedia.org/wiki/Plane_(Unicode)

Planes are further subdivided into Unicode blocks, which, unlike planes, do not have a fixed size. The 308 blocks defined in Unicode 13.0 cover 26% of the possible code point space, and range in size from a minimum of 16 code points (fifteen blocks) to a maximum of 65,536 code points (Supplementary Private Use Area-A and -B, which constitute the entirety of planes 15 and 16). For future usage, ranges of characters have been tentatively mapped out for most known current and ancient writing systems.[4]

 

https://www.w3.org/International/articles/definitions-characters/

UTF-32

From Wikipedia, the free encyclopedia

Jump to navigationJump to search

UTF-32 (32-bit Unicode Transformation Format) is a fixed-length encoding used to encode Unicode code points that uses exactly 32 bits (four bytes) per code point (but a number of leading bits must be zero as there are far fewer than 232 Unicode code points).[citation needed] UTF-32 is a fixed-length encoding, in contrast to all other Unicode transformation formats, which are variable-length encodings. Each 32-bit value in UTF-32 represents one Unicode code point and is exactly equal to that code point's numerical value.

The main advantage of UTF-32 is that the Unicode code points are directly indexed. Finding the Nth code point in a sequence of code points is a constant time operation. In contrast, a variable-length code requires sequential access to find the Nth code point in a sequence. This makes UTF-32 a simple replacement in code that uses integers that are incremented by one to examine each location in a string, as was commonly done for ASCII.

The main disadvantage of UTF-32 is that it is space-inefficient, using four bytes per code point, including 11 bits that are always zero. Characters beyond the BMP are relatively rare in most texts, and can typically be ignored for sizing estimates. This makes UTF-32 close to twice the size of UTF-16. It can be up to four times the size of UTF-8 depending on how many of the characters are in the ASCII subset.

 


Though a fixed number of bytes per code point seems convenient, it is not as useful as it appears. It makes truncation easier but not significantly so compared to UTF-8 and UTF-16 (both of which can search backwards for the point to truncate by looking at 2–4 code units at most).

It is extremely rare[citation needed] that code wishes to find the Nth code point without earlier examining the code points 0 to N–1. For instance, XML parsing cannot do anything with a character without first looking at all preceding characters.[4] So an integer index that is incremented by 1 for each character can be replaced with an integer offset, measured in code units and incremented by the number of code units as each character is examined. This removes the perceived speed advantages[citation needed] of UTF-32.

 

Each hexadecimal digit represents four binary digits, also known as a nibble, which is half a byte. For example, a single byte can have values ranging from 00000000 to 11111111 in binary form, which can be conveniently represented as 00 to FF in hexadecimal.

 

In the Unicode standard, a plane is a continuous group of 65,536 (216) code points. There are 17 planes, identified by the numbers 0 to 16, which corresponds with the possible values 00–1016 of the first two positions in six position hexadecimal format (U+hhhhhh). Plane 0 is the Basic Multilingual Plane (BMP), which contains most commonly used characters. The higher planes 1 through 16 are called "supplementary planes".[1] The very last code point in Unicode is the last code point in plane 16, U+10FFFF. As of Unicode version 13.0, seven of the planes have assigned code points (characters), and five are named.

The limit of 17 planes is due to UTF-16, which can encode 220 code points (16 planes) as pairs of words, plus the BMP as a single word.[2] UTF-8 was designed with a much larger limit of 231 (2,147,483,648) code points (32,768 planes), and can encode 221 (2,097,152) code points (32 planes) even under the current limit of 4 bytes.[3]

The 17 planes can accommodate 1,114,112 code points. Of these, 2,048 are surrogates (used to make the pairs in UTF-16), 66 are non-characters, and 137,468 are reserved for private use, leaving 974,530 for public assignment.

 

https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/

 

Every platonic letter in every alphabet is assigned a magic number by the Unicode consortium which is written like this: U+0639.  This magic number is called a code point. The U+ means “Unicode” and the numbers are hexadecimal. U+0639 is the Arabic letter Ain. The English letter A would be U+0041. You can find them all using the charmap utility on Windows 2000/XP or visiting the Unicode web site.

 

 

There is no real limit on the number of letters that Unicode can define and in fact they have gone beyond 65,536 so not every unicode letter can really be squeezed into two bytes, but that was a myth anyway.

 

Well, technically, yes, I do believe it could, and, in fact, early implementors wanted to be able to store their Unicode code points in high-endian or low-endian mode, whichever their particular CPU was fastest at, and lo, it was evening and it was morning and there were already two ways to store Unicode. So the people were forced to come up with the bizarre convention of storing a FE FF at the beginning of every Unicode string; this is called a Unicode Byte Order Mark and if you are swapping your high and low bytes it will look like a FF FE and the person reading your string will know that they have to swap every other byte. Phew. Not every Unicode string in the wild has a byte order mark at the beginning.

 

Almost every stupid “my website looks like gibberish” or “she can’t read my emails when I use accents” problem comes down to one naive programmer who didn’t understand the simple fact that if you don’t tell me whether a particular string is encoded using UTF-8 or ASCII or ISO 8859-1 (Latin 1) or Windows 1252 (Western European), you simply cannot display it correctly or even figure out where it ends. There are over a hundred encodings and above code point 127, all bets are off.



https://en.wikipedia.org/wiki/Universal_Character_Set_characters

The UCS uses surrogates to address characters outside the initial Basic Multilingual Plane without resorting to more than 16 bit byte representations. There are 1024 "high" surrogates (D800–DBFF) and 1024 "low" surrogates (DC00–DFFF). By combining a pair of surrogates, the remaining characters in all the other planes can be addressed (1024 × 1024 = 1048576 code points in the other 16 planes). In UTF-16, they must always appear in pairs, as a high surrogate followed by a low surrogate, thus using 32 bits to denote one code point.

 

http://unicode.org/faq/char_combmark.html

 

https://en.wikipedia.org/wiki/Duplicate_characters_in_Unicode

https://en.wikipedia.org/wiki/Unicode_equivalence

Unicode equivalence is the specification by the Unicode character encoding standard that some sequences of code points represent essentially the same character. This feature was introduced in the standard to allow compatibility with preexisting standard character sets, which often included similar or identical characters.

 

Unicode provides two such notions, canonical equivalence and compatibility. Code point sequences that are defined as canonically equivalent are assumed to have the same appearance and meaning when printed or displayed. For example, the code point U+006E (the Latin lowercase "n") followed by U+0303 (the combining tilde "◌̃") is defined by Unicode to be canonically equivalent to the single code point U+00F1 (the lowercase letter "ñ" of the Spanish alphabet). Therefore, those sequences should be displayed in the same manner, should be treated in the same way by applications such as alphabetizing names or searching, and may be substituted for each other. Similarly, each Hangul syllable block that is encoded as a single character may be equivalently encoded as a combination of a leading conjoining jamo, a vowel conjoining jamo, and, if appropriate, a trailing conjoining jamo.

 

The standard also defines a text normalization procedure, called Unicode normalization, that replaces equivalent sequences of characters so that any two texts that are equivalent will be reduced to the same sequence of code points, called the normalization form or normal form of the original text. For each of the two equivalence notions, Unicode defines two normal forms, one fully composed (where multiple code points are replaced by single points whenever possible), and one fully decomposed (where single points are split into multiple ones).

 

https://hackage.haskell.org/package/text-utf8

 

https://www.smashingmagazine.com/2012/06/all-about-unicode-utf8-character-sets/

The High Surrogate (U+D800–U+DBFF) and Low Surrogate (U+DC00–U+DFFF) codes are reserved for encoding non-BMP characters in UTF-16 by using a pair of 16-bit codes: one High Surrogate and one Low Surrogate. A single surrogate code point will never be assigned a character.

 

https://en.wikipedia.org/wiki/UTF-16#U+10000_to_U+10FFFF


https://en.wikipedia.org/wiki/Category:Unicode_formatting_code_points

 

All characters satisfying a given condition, using properties defined in the Unicode Character Database [UCD]:               https://unicode.org/reports/tr41/tr41-26.html#UCD

https://unicode.org/reports/tr29/

https://www.gutenberg.org/catalog/

 

https://www.win.tue.nl/~aeb/linux/uc/nfc_vs_nfd.html

Roughly speaking, NFC is the short form, fully composed, like U+1F85, and NFD is the long form, fully decomposed, in some well-defined order, like U+03B1 U+0314 U+0301 U+0345. (These are the two non-lossy normal forms



The rules for grapheme clusters can be easily converted into a regular expression, as in Table 1b, Combining Character Sequences and Grapheme Clusters. It must be evaluated starting at a known boundary (such as the start of the text), and it will determine the next boundary position. The resulting regular expression can also be used to generate fast, deterministic finite-state machines that will recognize all the same boundaries that the rules do.

 

https://hackage.haskell.org/package/text

Currently the text library uses UTF-16 as its internal representation which is neither a fixed-width nor always the most dense representation for Unicode text. We're currently investigating the feasibility of changing Text's internal representation to UTF-8 and if you need such a Text type right now you might be interested in using the spin-off packages text-utf8 and text-short.