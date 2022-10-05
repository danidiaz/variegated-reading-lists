[Main.Documentation](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=Main.Documentation)

[Data](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=ReferenceManual.Data)

>  Logicians and theoretical computer scientists may find it helpful to think of an indexed datatype as a set of judgements given by inference rules. 

[Brutal [Meta]Introduction to Dependent Types in Agda](https://oxij.org/note/BrutalDepTypes/)

> There are loads of idiosyncratic features in both, so I mention only a couple
of general things which are most relevant to me. Agda: much stronger and more
robust inference & unification, HoTT compatibility, modules, universe
polymorphism, rewrite pragmas. Idris: far more usable program compilation &
code backends.

>  Agda uses oversimplified lexer that splits tokens by spaces, parentheses, and braces

> When programming with dependent types, a predicate on A becomes a function from A to types, i.e. A → Set. If a : A satisfies the predicate P : A → Set then the function P returns a type with each element being a proof of P a, in a case a doesn’t satisfy P it returns an empty type.

> The magic of dependent types makes the type of the second argument of div2e change every time we pattern match on the first argument n.

> Unification is the most important (at least with pattern matching on inductive datatypes involved) and easily forgotten aspect of dependently typed programming.

> In datatype declarations things before a : are called “parameters”, things after the colon but before a Set are called “indexes”.

> Decidable propositions are the glue that make your program work with the real world.

[Difference between type parameters and indices?](https://stackoverflow.com/questions/24600256/difference-between-type-parameters-and-indices)

> Parameters are merely indicative that the type is somewhat generic, and behaves parametrically with regards to the argument supplied.

> Indices on the other hand may affect which inhabitants you may find in the type! That's why we say they index a family of types, that is, each index tells you which one of the types (within the family of types) you are looking at (in that sense, a parameter is a degenerate case where all the indices point to the same set of "shapes").

> This is why, when you define inductive families, usually you can define the parameters for the entire type, but you have to specify the indices for each constructor (since you are allowed to specify, for each constructor, what indices it lives at).

> zero != n of type Nat

> There’s no direct analogue to case in Agda, with construction allows pattern matching on intermediate expressions (just like Haskell’s case), but (unlike case) on a top level only. Thus with effectively just adds a “derived” argument to a function. Just like with normal arguments, pattern matching on a derived argument might change some types in a context.

[Parameters vs Indices](http://people.inf.elte.hu/divip/AgdaTutorial/Sets.Parameters_vs_Indices.html)

[Agda Vim editing](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=Main.VIMEditing)

[Programming Language Theory in Agda](https://wenkokke.github.io/sf/)

[Declarative GUIs: Simple, Consistent, and Verified](http://www.cs.swan.ac.uk/~csetzer/articles/PPDP18/PPDP18adelsbergerSetzerWalkingshawAccepted.pdf)

[Quick Guide to Editing, Type Checking and Compiling Agda Code](https://agda.readthedocs.io/en/v2.5.4.1/getting-started/quick-guide.html)

> tip: one can "Give" (C-SPC) while having ? inside the goal

> To enter a subscript in the Emacs mode, type "\_1".

> Commands working with types [like C-d] can be prefixed with C-u to compute type without further normalisation and with C-u C-u to compute normalised types.

[Library Management](https://agda.readthedocs.io/en/latest/tools/package-system.html). [agda-stdlib](https://github.com/agda/agda-stdlib).

[writing Unicode chars in Emacs](https://agda.readthedocs.io/en/latest/tools/emacs-mode.html#unicode-input)

[compilers](https://agda.readthedocs.io/en/v2.5.4.1/tools/compilers.html)

> Note that pattern matching on an Integer is slower than on an unary natural number. Code that does a lot of unary manipulations and doesn’t use builtin arithmetic likely becomes slower due to this optimization. If you find that this is the case, it is recommended to use a different, but isomorphic type to the builtin natural numbers.

> Typical examples of erasable types are the equality type and the accessibility predicate used for well-founded recursion

> The erasure means that equality proofs will (mostly) be erased, and never looked at, and functions defined by well-founded recursion will ignore the accessibility proof.

[built-ins](https://agda.readthedocs.io/en/v2.5.4.1/language/built-ins.html#built-ins)

[Instrumenting Total Parsers Written in agdarsec](https://gallais.github.io/blog/instrumenting-agdarsec). [paper](https://gallais.github.io/pdf/agdarsec18.pdf). [github](https://github.com/gallais/agdarsec). [earlier paper](http://www.cse.chalmers.se/~nad/publications/danielsson-parser-combinators.html)

[Working only with classical logic?](https://www.reddit.com/r/agda/comments/7epmgv/working_only_with_classical_logic/)

[Is Agda without K less powerful?](https://stackoverflow.com/questions/39264130/is-agda-without-k-less-powerful)

[What is Axiom K?](https://stackoverflow.com/questions/39239363/what-is-axiom-k/39256457)

[Problem solving PLFA exercises](https://www.reddit.com/r/agda/comments/991g8i/beginner_problem_solving_plfa_exercises/)

[Assisting Agda's termination checker](https://stackoverflow.com/questions/19642921/assisting-agdas-termination-checker). [Total definition of Gcd in Idris](https://stackoverflow.com/questions/50663750/total-definition-of-gcd-in-idris). [MiniAgda: Integrating Sized and Dependent Types](https://arxiv.org/pdf/1012.4896.pdf).

> I would like to offer a slightly different answer than the ones given above. In particular, I want to suggest that instead of trying to somehow convince the termination checker that actually, no, this recursion is perfectly fine, we should instead try to reify the well-founded-ness so that the recursion is manifestly fine in virtue of being structural.


[Libraries and other developments](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=Main.Libraries)

[Auto in Agda](http://www.staff.science.uu.nl/~swier004/publications/2015-mpc.pdf)

> The Coq proof assistant has two distinct language fragments. Besides the
programming language Gallina, there is a separate tactic language for writing
and programming proof scripts. Together with several highly customizable tactics,
the tactic language Ltac can provide powerful proof automation [Chlipala,
2013]. Having to introduce a separate tactic language, however, seems at odds
with the spirit of type theory, where a single language is used for both proof
and computation. Having a separate language for programming proofs has its
drawbacks: programmers need to learn another language to automate proofs,
debugging Ltac programs can be difficult, and the resulting proof automation
may be inefficient

[open type-level proofs](https://stackoverflow.com/questions/27219660/open-type-level-proofs-in-haskell-idris/)

proving stuff:

>  Proof by induction isn't just flailing about, you know? The trick is
      to pick the case analysis that provokes the "stuck" programs to do a
      step of computation. Then the same reasoning that justifies the
      termination of the program will justify the induction in a proof
      about it.
      
[cubical types for dummies](https://www.reddit.com/r/dependent_types/comments/8fqipe/cubical_types_for_dummies_draft/). [cubical adventures](https://www.youtube.com/watch?v=W5-ulP_JzNc).

[The Agda's New Sorts](https://jesper.sikanda.be/posts/agdas-new-sorts.html)

[An agda proposition used in the type — what does it mean?](https://stackoverflow.com/questions/18296161/an-agda-proposition-used-in-the-type-what-does-it-mean)

[How to compare two sets in Agda?](https://stackoverflow.com/questions/30794282/how-to-compare-two-sets-in-agda)

[Agda exercises](http://www.cse.chalmers.se/~peterd/papers/AgdaExercises.pdf)

[Built-ins](https://agda.readthedocs.io/en/v2.5.4.1/language/built-ins.html#built-ins)

> module Agda.Builtin.Equality

> While it is possible to define your own versions of the built-in types and bind them using BUILTIN pragmas, it is recommended to use the definitions in the Agda.Builtin modules. These modules are installed when you install Agda and so are always available. For instance, built-in natural numbers are defined in Agda.Builtin.Nat. The standard library and the agda-prelude reexport the definitions from these modules.

[Browse the standard library as clickable HTML](https://agda.github.io/agda-stdlib/README.html)

[universes](https://pigworker.wordpress.com/2015/01/09/universe-hierarchies/). [more on universes](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=ReferenceManual.UniversePolymorphism). [worlds](https://pigworker.wordpress.com/2014/12/31/worlds/).

[function notation](http://wiki.portal.chalmers.se/agda/pmwiki.php?n=ReferenceManual.Functions#Notation)

[Why haven't newer dependently typed languages adopted SSReflect's approach?](https://stackoverflow.com/questions/49477427/why-havent-newer-dependently-typed-languages-adopted-ssreflects-approach)

> There are two conventions I've found in Coq's SSReflect extension that seem particularly useful but which I haven't seen widely adopted in newer dependently-typed languages (Lean, Agda, Idris).

> Firstly, where possible predicates are expressed as boolean-returning functions rather than inductively defined datatypes. This brings decidability by default, opens up more opportunities for proof by computation, and improves checking performance by avoiding the need for the proof engine to carry around large proof terms. The main disadvantage I see is the need to use reflection lemmas to manipulate these boolean predicates when proving.

> A dependently typed datastructure in which the invariant is part of its type. One advantage of SSReflect's approach is that it allows reuse, so that for instance many of the functions defined for seq and proofs about them can still be used with tuple (by operating on the underlying seq), whereas with Idris' approach functions like reverse, append and the like need to be rewritten for Vect. Lean actually has a SSReflect style equivalent in its standard library, vector, but it also has an Idris-style array which seems to have an optimised implementation in the runtime.

> So SSReflect's approach is not perfect. The other one is too. Is there anything that improves upon both? Yes, Ornaments (see Ornamental Algebras, Algebraic Ornaments and The essence of ornaments). You can easily get Vec from List by applying the corresponding ornamental algebra, but I can't say how much code reuse you'll get from it and whether types will drive you nuts or not. I heard people actually use ornaments somewhere.

[Ornamental Algebras, Algebraic Ornaments](http://plv.mpi-sws.org/plerg/papers/mcbride-ornaments-2up.pdf). [The Essence of Ornaments](https://pages.lip6.fr/Pierre-Evariste.Dagand/stuffs/journal-2013-catorn-jfp/paper.pdf). [Datatypes of Datatypes](https://www.cs.ox.ac.uk/projects/utgp/school/conor.pdf).

> I see types as an external rationalisation imposed upon the raw stuff of computation

> the equational theory of open terms (conceived as functions from
valuations of their variables) will always be to some extent beyond the ken of the
computer.

> The remedy for our inevitable disappointment with judgmental equality is to
define a notion of evidence for equality

> we have declared
that the equality predicate for closed terms is whatever judgmental equality
we happen to have chosen. We have sealed our disappointment in, but we have
gained the abilty to prove useful equations on open terms.

> repurpose the existing data declaration as mere sugar for the definition of the corresponding code, and to ensure that those codes carry enough information (e.g., about constructor names, implicit argument conventions,
and so forth) to sustain the readability

[Proving properties of programs by structural induction](http://www.cse.chalmers.se/edu/year/2010/course/DAT140_Types/Burstall.pdf).

[Don't use Booleans!](https://stackoverflow.com/questions/38290067/idiomatic-boolean-equality-usage-singletons)

> That said, you should still be able to recover the information you threw away and extract a HasElem x xs value from a context of Elem x xs ~ True. It's tedious, though - you have to search the list for the item (which you already did in order to evaluate Elem x xs!) and eliminate the impossible cases.

> So does give you the same information as Disjoint — you just need to extract it. Basically, if there is no inconsistency between disjoint and Disjoint, then you should be able to write a function So (disjoint s) -> Disjoint s using pattern matching, recursion and impossible cases elimination.

[Agda Tips](https://doisinkidney.com/posts/2018-09-20-agda-tips.html). [more on reddit](https://www.reddit.com/r/agda/comments/9hepvt/agda_beginnerish_tips_tricks_pitfalls/)

> If you’ve got a hole in your program, you can put the cursor in it and press SPC-m-a (in spacemacs), and Agda will try and find the automatic solution to the problem. For a while, I didn’t think much of this feature, as rare was the program which Agda could figure out. Turns out I was just using it wrong! Into the hole you should type the options for the proof search: enabling case-splitting (-c), enabling the use of available definitions (-r), and listing possible solutions (-l).

> Often, a program will not be obviously terminating (according to Agda’s termination checker). The first piece of advice is this: don’t use well-founded recursion. It’s a huge hammer, and often you can get away with fiddling with the function (try inlining definitions, rewriting generic functions to monomorphic versions, or replacing with-blocks with helper functions), or using one of the more lightweight techniques out there.

> When combining prescriptive and descriptive indices, ensure both are in constructor form. Exclude defined functions which yield difficult unification problems.

> This is exactly the problem inspect solves: it runs your function, giving you a result, but also giving you a proof that the result is equal to running the function.

> This one is a little confusing, because Agda’s notion of “irrelevance” is different from Idris’, or Haskell’s. In all three languages, irrelevance is used for performance: it means that a value doesn’t need to be around at runtime, so the compiler can elide it.

> In dependently typed languages, this isn’t a distinction we can rely on. The line between runtime entities and compile-time entities is drawn elsewhere, so quite often types need to exist at runtime. As you might guess, though, they don’t always need to. The length of a length-indexed vector, for instance, is completely determined by the structure of the vector: why would you bother storing all of that information at runtime? This is what Idris recognizes, and what it tries to remedy: it analyses code for these kinds of opportunities for elision, and does so when it can. Kind of like Haskell’s fusion, though, it’s an invisible optimization, and there’s no way to make Idris throw a type error when it can’t elide something you want it to elide.

[Three Tricks to make Termination Obvious](https://gallais.github.io/blog/termination-tricks.html)

[Canonical Structures in Agda using REWRITE](https://gallais.github.io/blog/canonical-structures-REWRITE.html)

The Agda archives.

https://lists.chalmers.se/pipermail/agda/

https://lists.chalmers.se/pipermail/agda/2018/009985.html

https://lists.chalmers.se/pipermail/agda/2018/009986.html

https://lists.chalmers.se/pipermail/agda/2018/009950.html IO examples

https://lists.chalmers.se/pipermail/agda/2018/010031.html

https://lists.chalmers.se/pipermail/agda/2018/010158.html

https://lists.chalmers.se/pipermail/agda/2018/010159.html

https://lists.chalmers.se/pipermail/agda/2018/010195.html

https://lists.chalmers.se/pipermail/agda/2018/010263.html

https://lists.chalmers.se/pipermail/agda/2018/010305.html

> Level polymorphism bloats almost every definition in the Standard Prelude

> Indeed; to give another little data point, my personal experience is that I use --type-in-type with Agda almost always, and check predicativity by hand (usually not that hard, if you aren't doing something which will obviously be bad). I suspect a lot of people work this way, so as far as the social force is concerned, the solution which is eventually adopted in Agda X might need to be not much more bureaucratic than this
 
https://lists.chalmers.se/pipermail/agda/2018/010267.html
https://lists.chalmers.se/pipermail/agda/2018/010276.html [Agda] The joys and sorrows of abstraction

[Implicit generalization](https://people.inf.elte.hu/divip/AIMXXVIII.pdf)

[Keeping Formal Verification in Bounds](https://doisinkidney.com/posts/2018-11-20-fast-verified-structures.html).

[Agda Beginner(-ish) Tips, Tricks, and Pitfalls](https://doisinkidney.com/posts/2018-09-20-agda-tips.html) [Total Combinations](https://doisinkidney.com/posts/2018-10-16-total-combinations.html)

[Graphs are to categories as lists are to monoids](https://alhassy.github.io/PathCat/).

[Univalent Categories A formalization of category theory in Cubical Agda](http://publications.lib.chalmers.se/records/fulltext/256404/256404.pdf).

[Resources for Teaching with Formal Methods](https://avigad.github.io/formal_methods_in_education/).

[Automatically And Efficiently Illustrating Polynomial Equalities in Agda](https://www.reddit.com/r/dependent_types/comments/ajqtg6/automatically_and_efficiently_illustrating/). [tweet](https://twitter.com/copumpkin/status/1088846373720592384).

[Generic Zero-Cost Reuse for Dependent Types](https://arxiv.org/pdf/1803.08150.pdf)

> pendently typed languages are well known for having a problem with code reuse. Traditional non-indexed
algebraic datatypes (e.g. lists) appear alongside a plethora of indexed variations (e.g. vectors). Functions are
often rewritten for both non-indexed and indexed versions of essentially the same datatype, which is a source
of code duplication.

[Finger Trees in Agda](https://doisinkidney.com/posts/2019-02-25-agda-fingertrees.html)

[filter in Agda](https://twitter.com/acid2/status/1102926423487062017)

[Permutations By Sorting](https://doisinkidney.com/posts/2019-03-24-permutations-by-sorting.html)

[Introduction to Univalent Foundations of Mathematics with Agda](https://homotopytypetheory.org/2019/03/20/introduction-to-univalent-foundations-of-mathematics-with-agda/)

[Introductory Agda sessions](https://twitter.com/dregntael/status/1123586006408679430)

[tactic arguments](https://agda.readthedocs.io/en/latest/language/implicit-arguments.html#tactic-arguments)

[agda quality code](https://twitter.com/scottfleischman/status/1146133657427406848)

[Automatically and E!ciently Illustrating Polynomial Equalities in Agda](https://doisinkidney.com/pdfs/bsc-thesis.pdf)

[tips for matrices in agda](https://twitter.com/laMudri/status/1153970508683075584)

[(Programming Languages) in Agda = Programming (Languages in Agda)](https://www.youtube.com/watch?v=4rETh3TZO44)

[Vectors and Matrices in Agda](https://personal.cis.strath.ac.uk/james.wood.100/blog/html/VecMat.html)

[From type theory to setoids and back](https://arxiv.org/abs/1909.01414)

[improvements to the with construct](https://twitter.com/anormalform/status/1173162307100303360)

[Lazily exploring a directory (co)tree to find a file with a given basename, in Agda](https://twitter.com/anormalform/status/1174061234917924866)

[a cheatsheet to Agda demonstrating how to use Haskell for sideffects](https://www.reddit.com/r/haskell/comments/ddcsvv/subverting_agda_using_haskell_a_cheatsheet_to/)

[Introduction to Univalent Foundations of Mathematics with Agda](https://arxiv.org/abs/1911.00580) Martín Hötzel Escardó

[ a pretty slick way to get computation to do more for us. I guess it's what ssreflect was always getting at, in a way](https://twitter.com/laMudri/status/1196171890605404160)

[Three Equivalent Ordinal Notation Systems in Cubical Agda](https://personal.cis.strath.ac.uk/fredrik.nordvall-forsberg/papers/ord_cpp2020.pdf)

[Hack your type theory with rewrite rules](https://jesper.sikanda.be/posts/hack-your-type-theory.html), [also in Haskell](https://www.reddit.com/r/haskell/comments/ek8an8/ann_typelevelrewriterules01/).

[Equality of functions in Agda](https://armkeh.github.io/blog/EqualityOfFunctions.html)

[equality in mechanized mathematics](https://artagnon.com/articles/equality)

[Agda vs Coq vs Idris](https://www.reddit.com/r/haskell/comments/f6f5yk/agda_vs_coq_vs_idris/)

[Agda 2.6.1 has been released!](https://www.reddit.com/r/haskell/comments/fjk3up/agda_261_has_been_released/)

[Type-based formal verification ](https://www.youtube.com/watch?v=JboZel47XU0&feature=emb_logo)

[agda resources](https://twitter.com/razvan_panda/status/1256192729467490304)

Brigitte Pientka: Mechanizing Meta-Theory in Beluga https://vimeo.com/423668919

[ZuricHac](https://www.youtube.com/watch?v=x0R5h190Yts)

[Competing inheritance paths in dependent type theory: a case study in functional analysis](https://twitter.com/Jose_A_Alonso/status/1272559944143953922)

[Agda editor support](https://twitter.com/ndm_haskell/status/1272521576383238144)

[Leibniz Equality is Isomorphic to Martin-Lof¨
Identity, Parametrically](https://jesper.sikanda.be/files/leibniz-equality.pdf)

[tactics](https://twitter.com/jjcarett2/status/1276859006552813575)

[inference in agda](https://www.reddit.com/r/haskell/comments/jo4a6u/inference_in_agda/)

[about fin (Idris)](https://blog.cofree.coffee/2020-12-22-finally-modular-arithmetic/). [reddit](https://www.reddit.com/r/haskell/comments/kigwzh/modular_arithmetic_with_fin_in_idris/ggqzo4k/?utm_source=reddit&utm_medium=web2x&context=3).

[the nature of tactics](https://twitter.com/jjcarett2/status/1351367688711532544)

[The Agda universal algebra library and Birkhoff's theorem in Martin-Löf dependent type theory](https://twitter.com/Jose_A_Alonso/status/1354005494017486850)

[induction-recursion and universes](https://twitter.com/andrasKovacs6/status/1363900515147481089)

[The Agda Universal Algebra Library, Part 1: Foundation](https://arxiv.org/abs/2103.05581)

[ISRM-LOGRAC-2022-02-17 First steps with Agda](https://www.youtube.com/watch?v=0hsYR4bgDE8)

["1 + (–1) = 0 in π₁(S¹)" but in cubical Agda](https://twitter.com/kisonecat/status/1499061783171985412)

[Using Agda's Induction (Recursion) Library](https://twitter.com/jeremysiek/status/1512083784455254017?t=nEu64THloev4-rnxDaTVjg&s=03)

[HoTTEST-Summer-School](https://github.com/martinescardo/HoTTEST-Summer-School/tree/main/Agda/Lecture-Notes)

[reasonable Agda is correct Haskell](https://twitter.com/agdakx/status/1554044242846257153)

[Practical Generic Programming over a Universe of Native Datatypes (video)](https://twitter.com/agdakx/status/1577566371050815490)



