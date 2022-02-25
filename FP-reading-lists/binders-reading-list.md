# Binders

## papers

[Lambda Calculus Notation with Nameless Dummies](http://alexandria.tue.nl/repository/freearticles/597619.pdf)

[Names For Free](http://www.cse.chalmers.se/~bernardy/NamesForFree.pdf)

[I am not a Number—I am a Free Variable](http://www.cs.ru.nl/~james/RESEARCH/haskell2004.pdf)

[Higher-Order Abstract Syntax](http://www.cs.cmu.edu/~fp/papers/pldi88.pdf)

[Bananas in Space](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.64.4921&rep=rep1&type=pdf)

[Revisiting catamorphisms over datatypes with embedded functions](https://digitalcommons.ohsu.edu/cgi/viewcontent.cgi?article=1253&context=csetech)

[Programs from Outer Space](http://citeseer.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.2763)

> Fortunately, a year later Leonidas Fegaras and Tim Sheard realized that the main use of the 'unfold step' above was to just undo the damage caused by the fold step and that a full inverse wasn't needed

> The problem the reduces to the question of how to define place. Fegaras and Sheard were willing (and able) to change every functor to include an extra member name Place and then define as part of each catamorphism that cata f (Place x) = x. They then ensured that Place wasn't abused by the programmer by a complicated type system that we really don't have access to in Haskell. 

> We revisit the work of Paterson and of Meijer & Hutton, which describes how to construct catamorphisms for recursive datatype definitions that embed contravariant occurrences of the type being defined. Their construction requires, for each catamorphism, the definition of an anamorphism that has an inverse-like relationship to that catamorphism. We present an alternative construction, which replaces the stringent requirement that an inverse anamorphism be defined for each catamorphism with a more lenient restriction. The resulting construction has a more efficient implementation than that of Paterson, Meijer, and Hutton and the relevant restriction can be enforced by a Hindley-Milner type inference algorithm. We provide numerous examples illustrating our method.


[Boxes Go Bananas](http://www.seas.upenn.edu/~sweirich/papers/itabox/icfp-published-version.pdf) [slides](https://www.cis.upenn.edu/~sweirich/talks/bgb.pdf) [extended version](https://works.bepress.com/stephanie_weirich/4/)

> One fix, as noted by Washburn and Weirich is to quantify over the a with an explicit forall when working with the Fegaras/Sheard catamorphism. This has the nice side effect that it prevents illegal uses of 'Place'. Moreover, that explicit quantifier allows you to use different catamorphisms over the term.

> Weirich and Washburn's encoding as an elimination form protect the user from bad case analysis by denying you the ability to inspect terms with case at all. 

> In other words, the only thing you can do to a term is apply a catamorphism to it. They even say as much somewhere in the paper.

> No sweat, we can go rederive all of the other stuff thats defined in terms of catamorphism, right? paramorphisms, zygomorphisms, histomorphisms, generalized catamorphisms, and then we can do anything we want, right? Unfortunately, here is where we run out of steam.

> A catamorphism isn't strong enough to encode general recursion without fmap. In order to rederive general recursion from a catamorphism you need at least a paramorphism. Normally we can define a paramorphism in terms of our catamorphism with the use of fmap, but as we are working over merely an exponential functor we do not have fmap!

> Depending on how bad we want to be, we can get out of the Washburn/Weirich or Fegaras/Sheard sandboxes and into one of the others. Though curiously we can't get back out of the Meijer/Hutton-style unless we have a full Functor.

> We do not claim that this encoding will solve all of the problems
with programming using higher-order abstract syntax. In particular,
algorithms that require the explicit manipulation of the names of
bound variables remain outside the scope of this implementation
technique.

> Using cata to implement operations such as eval is convenient because the pattern of recursion is already
specified. None of eval, evalAux or unevalAux are recursively defined.

[Parametric Higher-Order Abstract Syntax for Mechanized Semantics](http://adam.chlipala.net/papers/PhoasICFP08/PhoasICFP08.pdf) [slides](http://adam.chlipala.net/papers/PhoasICFP08/PhoasICFP08Talk.pdf)

[The Locally Nameless Representation](http://www.chargueraud.org/research/2009/ln/main.pdf)

[Lambda calculus cooked four ways](http://foswiki.cs.uu.nl/foswiki/pub/USCS/InterestingPapers/AugustsonLambdaCalculus.pdf)

[Scrap your nameplate](http://homepages.inf.ed.ac.uk/jcheney/publications/cheney05icfp.pdf)

[Using Circular Programs for Higher-Order Syntax](http://www.cse.chalmers.se/~emax/documents/axelsson2013using.pdf)

[Abstract Syntax Graphs for Domain Specific Languages](https://www.andres-loeh.de/ASGDSL/) explains PHOAS [reddit](https://www.reddit.com/r/haskell/comments/85een6/sharing_from_phoas_multiple_interpreters_from_free/)

[Engineering Formal Metatheory](https://www.cis.upenn.edu/~bcpierce/papers/binders.pdf)

[De Bruijn Monads](https://fpfm.github.io/Slides_Maggesi.pdf) [reddit](https://www.reddit.com/r/dependent_types/comments/68t2g3/de_bruijn_monads_slides_pdf/)

[Type-and-Scope Safe Programs and Their Proofs](https://gallais.github.io/pdf/cpp2017.pdf)

> A programmer implementing an embedded language with
bindings has a wealth of possibilities. However, should she
want to be able to inspect the terms produced by her users
in order to optimise or even compile them, she will have to
work with a deep embedding. 

[A Locally Nameless Theory of Objects](http://www-sop.inria.fr/oasis/SAFA/Safa2010/01_Henrio_SAFA2010_final.pdf)

[Locally Nameless Permutation Types](http://edsko.net/pubs/lnpt.pdf)

[Functional Programming with Structured Graphs](https://www.cs.utexas.edu/~wcook/Drafts/2012/graphs.pdf)

> To provide a convenient and expressive programming interface, structured
graphs use a binding representation based on parametric higherorder
abstract syntax (PHOAS)

[Parametric Compositional Data Types](https://pdfs.semanticscholar.org/7a21/fe9119ba6864180c2f4e97d87a7a91ecd0f7.pdf)

[A Parallel Intermediate Representation for Embedded Languages]()

> The HOAS allows Nikola to express let-sharing
and λ-sharing, two kinds of optimisations for minimising recomputation of
common subexpressions and for reducing the final code-size.

[Binders Unbound](http://www.seas.upenn.edu/~sweirich/papers/icfp11.pdf) [post](https://byorgey.wordpress.com/2011/03/28/binders-unbound/)

> Atoms are often taken to be strings, but any countably infinite set with decidable equality will do.

> Stephanie Weirich, Tim Sheard and I recently submitted a paper to ICFP entitled Binders Unbound. (You can read a draft here.) It’s about our kick-ass, I mean, expressive and flexible library, unbound (note: GHC 7 required), for generically dealing with names and binding structure when writing programs (compilers, interpreters, refactorers, proof assistants…) that work with syntax. Let’s look at a small example of representing untyped lambda calculus terms. This post is working Literate Haskell, feel free to save it to a .lhs file and play around with it yourself!

[Monadic presentations of lambda terms using generic inductive types](http://www.cs.nott.ac.uk/~psztxa/publ/csl99.pdf) [twitter](https://twitter.com/Iceland_jack/status/1002764494249000961)

[A Type Theory for Defining Logics and Proofs](https://www.cs.mcgill.ca/~bpientka/papers/cocon-short.pdf). Talks about HOAS.

[Everybody’s Got To Be Somewhere](https://arxiv.org/pdf/1807.04085.pdf). [twitter](https://twitter.com/Iceland_jack/status/1123938329832173569). [repo](https://github.com/pigworker/EGTBS). [pdf](worker/EGTBS/blob/master/EGTBS.pdf).

[Secrets of the Glasgow Haskell Compiler inliner](https://www.microsoft.com/en-us/research/wp-content/uploads/2002/07/inline.pdf). [question](https://www.reddit.com/r/haskell/comments/i1b8q9/monthly_hask_anything_august_2020/g07sofo/).

> Another well-known approach to the name-capture problem to use de Bruijn numbers [dB80]. Apart from being
entirely unreadable, this approach suffers from the disad- vantage that when pushing a substitution inside a lambda,
the entire range of the substitution must have its de Bruijn
numbers adjusted. That operation can be carried out lazily, to avoid a complexity explosion when pushing a substitution
inside multiple lambdas, but that means yet more administration.

[Using Circular Programs for Higher-Order Syntax](https://www.researchgate.net/publication/262241181_Using_Circular_Programs_for_Higher-Order_Syntax_Functional_pearl). [A simple alternative to De Bruijn indexing, from ICFP 2013](http://pchiusano.github.io/2014-06-20/simple-debruijn-alternative.html). [A simple alternative to De Bruijn indexing, from ICFP 2013](https://www.reddit.com/r/haskell/comments/28vfd0/a_simple_alternative_to_de_bruijn_indexing_from/cifbbkd/).

## posts

[Bound](http://www.slideshare.net/ekmett/bound-making-de-bruijn-succ-less)

[Bound](https://www.schoolofhaskell.com/user/edwardk/bound) [strongly-typed bound](https://www.reddit.com/r/haskell/comments/7r0jkt/using_bound_with_mutually_recursive_expression/) [video](https://www.youtube.com/watch?v=7mUxp-xrcUw) [more](https://www.reddit.com/r/haskell/comments/7qxyaf/capture_avoiding_substitution_with_support_for/) [even more](https://www.reddit.com/r/haskell/comments/7sj5jt/extremely_strongly_typed_syntax_trees/dt5uz5p/)

[PHOAS For Free](https://www.fpcomplete.com/user/edwardk/phoas) [more](https://pay.reddit.com/r/haskell/comments/7t4bes/bananas_for_lets_and_lambdas/)

[Rotten Bananas](http://comonad.com/reader/2008/rotten-bananas/)

> In other words, to use the Meijer/Hutton catamorphism to write a pretty printer, you have to write a parser as well; to use it to eval, you must also be able to reify values back into programs.

[Higher-order abstract syntax](https://en.wikipedia.org/wiki/Higher-order_abstract_syntax)

[Parametric HOAS](http://adam.chlipala.net/papers/PhoasICFP08/PhoasICFP08Talk.pdf)

[A Type-theoretic Foundation for Programming with Higher-order Abstract Syntax and First-class Substitutions](http://lambda-the-ultimate.org/node/3627)

[Name binding blog](https://namebinding.wordpress.com)

[Separate positive and negative occurrences of PHOAS variables in presence of recursive binders](http://stackoverflow.com/questions/24369954/separate-positive-and-negative-occurrences-of-phoas-variables-in-presence-of-rec)

[Using Circular Programs for Higher-Order Syntax](https://www.reddit.com/r/haskell/comments/4ni32l/what_are_common_patterns_for_building_dsls/)

[https://pay.reddit.com/r/haskell/comments/4rynuq/directed_acyclic_graphs_and_phoas/](https://pay.reddit.com/r/haskell/comments/4rynuq/directed_acyclic_graphs_and_phoas/)

[An amazing functional](http://math.andrej.com/2010/07/29/an-amazing-functional/)

[total phoas transformation](https://www.reddit.com/r/haskell/comments/5ueisr/total_phoas_transformation/)

[phoas normalization](https://www.reddit.com/r/haskell/comments/5unefp/phoas_normalization/)

[binders unbound 2011](https://hackage.haskell.org/package/unbound)

[A Scope Safe Universe of Syntaxes with Binding, Their Semantics and Proofs](https://www.reddit.com/r/dependent_types/comments/65ijd9/a_scope_safe_universe_of_syntaxes_with_binding/)

[Let Idris Take Care Of You: Variable Binding](https://crunchytype.wordpress.com/2017/05/07/let-idris-take-care-of-you-variable-binding/)

[Dependable Types 2: Correctness by Construction](http://www.tomharding.me/2018/01/27/dependable-types-2/)

[Is nameless representation worth the trouble?](https://www.reddit.com/r/haskell/comments/4rvssi/is_nameless_representation_worth_the_trouble_why/)

> The main goal of pretty much any story for binders isn't about saving memory, it's primarily about ensuring that we don't write unhygienic programs or program transformations, often with a secondary goal of providing fast/easy alpha-equivalence.

> Using explicit names it's all too easy to break hygiene: allowing a variable to be used outside the scope in which it's bound, allowing binders to capture things they shouldn't, etc. As a particular example, correctly implementing capture-avoiding substitution is far trickier than expected. So the primary goal of any variable binding story (de Bruijn levels, de Bruijn indices, locally nameless, HOAS,...) is to get rid of these problems.

[Type 'Int' does not match type 'Int'](http://blog.discus-lang.org/2016/06/type-int-does-not-match-type-int.html)

> Compiler engineering is full of traps of representation.

[Differences between HOAS and FOAS](https://stackoverflow.com/questions/21771353/differences-between-hoas-and-foas) 

[Why GADTs are awesome: implementing System F using HOAS](https://www.reddit.com/r/haskell/comments/rk0uf/why_gadts_are_awesome_implementing_system_f_using/)

[Separate positive and negative occurrences of PHOAS variables in presence of recursive binders](https://stackoverflow.com/questions/24369954/separate-positive-and-negative-occurrences-of-phoas-variables-in-presence-of-rec)

[CH = PH](http://wadler.blogspot.com.es/2012/10/ch-ph_9.html)

> Two representations for lambda calculus terms are the Church representation, due to Thierry Coquand (left) and Gerard Huet (middle), let's call it CH, and PHOAS, due to Adam Chlipala (right), let's call it PH.  Here is a Haskell program giving both encodings, and showing they are interconvertible.  The CH representation is called finally tagless by Carette, Kiselyov, and Shan, which is not the most perspicuous name; Atkey, Lindley, and Yallop point out the idea goes back to Coquand and Huet; PH was introduced by Chlipala.

[Converting a HOAS term GADT into a de Bruijn term GADT](https://github.com/danidiaz/hoas-conv)

> Atkey, Sam Lindley & Jeremy Yallop had independently developed the same method and were about to publish it in a paper entitled Unembedding Domain-Specific Languages

[parsing for PHOAS expressions](https://stackoverflow.com/questions/19415621/parsing-for-phoas-expressions)

> I'll show how to convert between a named, a de-Bruijn, and a PHOAS representation of lambda terms. It's relatively easy to fuse that into the parser if you absolutely want to, but it's probably better to parse a named representation first and then convert.

[Phoas in scala - Boxes go bananas for less](https://stackoverflow.com/questions/23989856/phoas-in-scala-boxes-go-bananas-for-less)

[HOAS in write you a Haskell](http://dev.stephendiehl.com/fun/evaluation.html#higher-order-abstract-syntax-hoas)

>  Since all the machinery is wrapped up inside of Haskell's implementation even simple operations like pretty printing and writing transformation passes can be more difficult. This form is a good form for evaluation, but not for transformation.

[Library Hoas - cdpt](http://adam.chlipala.net/cpdt/html/Hoas.html)

> In the context of Haskell, Washburn and Weirich introduced a technique called parametric HOAS, or PHOAS. By making a slight alteration in the spirit of weak HOAS, we arrive at an encoding that addresses all three of the complaints above: the encoding is legal in Coq, exotic terms are impossible, and it is possible to write any syntax-deconstructing function that we can write with first-order encodings. The last of these advantages is not even present with HOAS in Twelf. In a sense, we receive it in exchange for giving up a free implementation of capture-avoiding substitution.

[HOAS in HN](https://news.ycombinator.com/item?id=12300407)

> It is nice for languages where it is a first-class concept (e.g. Twelf, which is a logic/theorem language), but it gets complicated very quickly if you want to do AST transformations.

> HOAS is a form of embedding a language L with binders into a language L-Base also with binders and functions, but such that L-binders are handled by functions in L-Base and the problem of defining capture-avoiding substitution for L-terms is reduced to reusing L-Base's capture-avoiding substitution. (NB L = L-Base is possible but not required.)

> HOAS is neat, but (simplifying a bit) prevents you from making inductive definitions on L terms. There are various ways of getting around this shortcoming, the most principled one is probably the nominal approach of A. Pitts et al. Another problem with HOAS is that the representation may contain 'junk'. That means there are L-Base terms that do not represent L-programs.

> It's quite ingenious but it's not as convenient as locally nameless representation for working underneath binders.

[How I learned to stop worrying and love de Bruijn indices](http://blog.discus-lang.org/2011/08/how-i-learned-to-stop-worrying-and-love.html)

[Turning bottom-up into top-down with Reverse State](http://blog.ielliott.io/topsy-turvy-reverse-state/)

[HOAS in Rust](https://stackoverflow.com/questions/51182640/is-it-possible-to-represent-higher-order-abstract-syntax-in-rust)

[Is it possible to normalize affine λ-calculus terms using PHOAS in Agda?](https://stackoverflow.com/questions/51845828/is-it-possible-to-normalize-affine-%CE%BB-calculus-terms-using-phoas-in-agda)

[A well-typed suspension calculus](https://mazzo.li/posts/suspension.html)

[de bruijn in a tweet](https://twitter.com/pigworker/status/1068897189227913223)

[Sometimes when I feel sad I implement a dependently typed lambda calculus.](https://twitter.com/rob_rix/status/1069080429578412033)

[binders in Java](https://twitter.com/lukaseder/status/1093440886183288832)

[unbound-generics in case expressions](https://www.reddit.com/r/haskell/comments/ck3qfe/unboundgenerics_case_expressions/)

[localy nameless](https://boarders.github.io/posts/locally-nameless/). 

[codebruijn](https://twitter.com/kmett/status/1190721234071240704) [more](https://twitter.com/kmett/status/1190848342701432833)

[converting HOAS to FOAS](https://www.reddit.com/r/haskell/comments/54pq7g/problem_about_converting_hoas_to_foas/  
)

[I am not a number, I am a classy hack](https://mazzo.li/epilogue/index.html%3Fp=773.html)

> In this post, I’ll discuss some of the issues which have driven us to a de Bruijn indexed representation of values, where once we used Haskell functions to model Epigram functions.

> Remark. Whilst this is a higher-order representation of values, it is not and should not be described as ‘higher-order abstract syntax’: on the one hand, free variables have a concrete first-order representation; on the other hand, the functions in Can are permitted to analyse and compute with their arguments by pattern matching on canonical value forms. Repeat. It is not HOAS. It is an untyped approximation to a Kripke-model construction, which morally goes by structural recursion on types.

[does HOAS suck?](https://twitter.com/rob_rix/status/900895905137741824)

[Semantics for de Bruijn levels](https://stackoverflow.com/questions/59789814/semantics-for-de-bruijn-levels)

[hoas and traversable tweet](https://twitter.com/rob_rix/status/1239956043909730306). [another HOAS tweet](https://twitter.com/rob_rix/status/1241180296327897091)

[A Generic Abstract Syntax Model for Embedded Languages](https://www.reddit.com/r/haskell/comments/fbfhum/monthly_hask_anything_march_2020/fl6b2vt/)

[variadic lambda construction](https://twitter.com/rob_rix/status/1243277159562698762)

[Is it possible to convert a HOAS function to continuation passing style?](https://stackoverflow.com/questions/62201446/is-it-possible-to-convert-a-hoas-function-to-continuation-passing-style)

[monadic presentations of lambda terms using generalized inductive types](http://www.cs.nott.ac.uk/~psztxa/publ/csl99.pdf). [tweet](https://twitter.com/completelysound/status/1282321814828580872).

> Syntaxes with binding form a monad indexed by the variable representation:
> 4.4

[What are the performance characteristics of HOAS/tagless final?](https://www.reddit.com/r/haskell/comments/hubilz/what_are_the_performance_characteristics_of/)

[What representations but de Bruijn are there to avoid the ill-defined capture-avoiding substitution?](https://twitter.com/xcycl/status/1297582896031522816)

[HOAS & staged computation](https://twitter.com/rob_rix/status/1310545241741590528) 

[tweet about co-debrujin](https://twitter.com/haskell_cat/status/1313470736850399233)

[Writing efficient free variable traversals](https://twitter.com/rob_rix/status/1313797892696682498). [more](https://twitter.com/rob_rix/status/1313797892696682498).

[more about bound](https://twitter.com/kmett/status/1355435021260128259)

[a HOAS encoding of a subset of the XLA core ops with completely statically tracked shape information](https://twitter.com/lexi_lambda/status/1373171721176547331)

[context contains patterns, not variables](https://twitter.com/rob_rix/status/1375610727004782592)

[even more about bound](https://twitter.com/DiazCarrete/status/1387388824234364928)

> No real-world implementation of a functional language uses term substitution for beta reduction! Instead, the standard practice is to have environment machines, closures, and a separation of immutable code from value environments
> CEK, SECD & STG machines

[Nominal: An efficient and easy-to-use library for defining datatypes with binders, and automatically handling bound variables and alpha-equivalence](https://twitter.com/DiazCarrete/status/1387389569637789696). [A New Approach to Abstract Syntax
with Variable Binding](https://www.cl.cam.ac.uk/~amp12/papers/newaas/newaas-jv.pdf).

[the implementation of (dependent) type systems](https://twitter.com/agdakx/status/1390014025484972036). [a bibliography of publications that discuss implementation of dependent type systems](https://twitter.com/agdakx/status/1390699639515631619).

[data structures that represent only closed terms](https://stackoverflow.com/questions/67748283/is-it-possible-to-write-a-data-structure-or-data-structures-that-represent-only)

[Namespaced De Bruijn indices](https://www.haskellforall.com/2021/08/namespaced-de-bruijn-indices.html).

[Skipping the binder bureaucracy with mixed embeddings in a semantics course (Functional Pearl)](https://twitter.com/Jose_A_Alonso/status/1425745900836737024?s=03). [video](https://www.youtube.com/watch?v=C2HFRlj7qT8&list=PLyrlk8Xaylp5ed_Yhg2oTdVhrtVohVaoa&index=26).

[You Could Have Invented De Bruijn Indices](https://golem.ph.utexas.edu/category/2021/08/you_could_have_invented_de_bru.html)

[lambda calculus cooked n-ways](https://github.com/sweirich/lambda-n-ways)

[Implementing Hindley-Milner with the unification-fd library](https://twitter.com/Jose_A_Alonso/status/1436449406522302468)

[Bottom-up rewriting with smart constructors, hereditary substitution & normalization by evaluation](https://twitter.com/JulesJacobs5/status/1442217029432451075)

[Do you want to define syntax with binders in Agda but have no idea whether to use de Bruijn indices, nominal sets, HOAS, or yet something else?](https://jesper.sikanda.be/posts/1001-syntax-representations.html) [tweet](https://twitter.com/agdakx/status/1456666363821531142)

[A type- and scope-safe universe of syntaxes with binding](https://www.cambridge.org/core/journals/journal-of-functional-programming/article/abs/type-and-scopesafe-universe-of-syntaxes-with-binding-their-semantics-and-proofs/8A0865F34313BA65F4FE46D4522B4568)

[Why capture-avoiding substitution is typically first introduced in untyped lambda-calculus with applicative order reduction, where no capture can actually happen if the top-level term is closed?](https://twitter.com/ilyasergey/status/1488765108201222145) Twitter thread. [applicative order reduction](https://opendsa-server.cs.vt.edu/OpenDSA/Books/PL/html/ReductionStrategies.html).

> refactorings, call-by-name, and full reduction are good examples why [CAS] matters

> But call-by-name also doesn't need C.A.S. if terms are closed and reduction order is outermost-first, right?

> I introduce naïve substitution first, then explain CAsubst later when making out-of-order reductions ("refactorings", contextual equivalence, etc).

[Categorical semantics of functional type theory with explicit substitutions, formalized in Agda](https://twitter.com/elpin1al/status/1489886363826946055)

[Using Circular Programs for Higher-Order Syntax](https://twitter.com/Iceland_jack/status/1493995166302146560)

[informal type theory](https://twitter.com/jonmsterling/status/1497122894429646849)

## software

[bound](http://hackage.haskell.org/package/bound)

[unbound](https://hackage.haskell.org/package/unbound)

[nom](http://hackage.haskell.org/package/nom)

## videos

[Unembedding Domain-specific Languages](https://vimeo.com/6685910)

[Devon Stewart - Higher Order Abstract Syntax](https://www.youtube.com/watch?v=d36y3NYmxH8)

[Phil Freeman - Embedded DSLs in Haskell](https://www.youtube.com/watch?v=8DdyWgRYEeI) [slides](https://github.com/paf31/haskell-slides/tree/master/hoas)

[Binding Types à la carte](https://skillsmatter.com/skillscasts/12385-binding-types-a-la-carte).

[Type theory elaboration implementation](https://www.youtube.com/playlist?list=PL2ZpyLROj5FOt99f_KCxARvd1hDqKns5b). Playlist related to [elaboration-zoo](https://github.com/AndrasKovacs/elaboration-zoo)

[Practical Normalization by Evaluation for EDSLs](https://www.youtube.com/watch?v=7sQ22-kMCqc). [reddit](https://www.reddit.com/r/haskell/comments/pnec00/haskell_symposium_2021_practical_normalization_by/).

[How to implement the lambda calculus, quickly](https://twitter.com/DiazCarrete/status/1480178086658383874)

