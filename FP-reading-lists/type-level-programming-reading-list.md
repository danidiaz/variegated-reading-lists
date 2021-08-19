# Type-level programming

## Papers

[Dependently typed programming with singletons](http://www.cis.upenn.edu/~eir/papers/2012/singletons/paper.pdf)

[How to keep your neighbours in order](https://personal.cis.strath.ac.uk/conor.mcbride/Pivotal.pdf)

[Self Types for Dependently Typed Lambda Encodings](https://fermat.github.io/document/papers/rta-tlca.pdf) and the [SO question](http://stackoverflow.com/questions/43123504/what-is-the-exact-difference-between-fix-and-self-on-the-calculus-of-constructio)

[A tutorial implementation of a dependently typed lambda calculus](https://www.andres-loeh.de/LambdaPi/LambdaPi.pdf)

[Higher-Order Dynamic Pattern Unification for Dependent Types and Records](https://pdfs.semanticscholar.org/0b74/a70ccad7829ad522337f0d3aa2106a59d4ee.pdf)

[A Unification Algorithm for COQ Featuring Universe Polymorphism and Overloading](https://people.mpi-sws.org/~beta/papers/unicoq.pdf)

[Contrained type families - preprint](http://cs.brynmawr.edu/~rae/papers/2017/partiality/partiality.pdf)

[Programming Examples Needing Polymorphic Recursion](http://itrs04.di.unito.it/papers/hk.pdf)

[Staged Generic Programming - in metaocaml](https://www.cl.cam.ac.uk/~jdy22/papers/staged-generic-programming.pdf)

[Constrained type families](https://arxiv.org/abs/1706.09715)

[Quantified class constraints](http://i.cs.hku.hk/~bruno/papers/hs2017.pdf) [Reddit](https://www.reddit.com/r/haskell/comments/6me3sv/quantified_class_constraints_pdf/) [Another very good exposition](https://ryanglscott.github.io/2018/03/04/how-quantifiedconstraints-can-let-us-put-join-back-in-monad/) [Reddit](https://www.reddit.com/r/haskell/comments/8257mz/how_quantifiedconstraints_can_let_us_put_join/)

[the power of Pi](https://cs.ru.nl/~wouters/Publications/ThePowerOfPi.pdf)

[Safe API Design with Ghosts of Departed Proofs](https://github.com/matt-noonan/gdp-paper/releases/download/june-2018-draft/gdp.pdf) [reddit](https://www.reddit.com/r/haskell/comments/8qn0wr/safe_api_design_with_ghosts_of_departed_proofs/). [who authorized these ghosts?](https://www.reddit.com/r/haskell/comments/co966h/who_authorized_these_ghosts/).

> Writing APIs with enforced preconditions, that give the user plenty of flexibility in constructing arguments to prove that the preconditions are met.

[Keep Your Laziness in Check](http://very.science/pdf/StrictCheck_arxiv.pdf) [reddit](https://www.reddit.com/r/haskell/comments/8uzqgr/icfp_18_preprint_keep_your_laziness_in_check/) the appendix describes a way to implement variadic currying.

[LiquidHaskell: Experience with Refinement Types in the Real World](http://goto.ucsd.edu/~nvazou/real_world_liquid.pdf) [twitter](https://twitter.com/puffnfresh/status/1031838964812922880)

[Interactive Programs and Weakly Final Coalgebras in Dependent Type Theory](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.63.8185&rep=rep1&type=pdf)

[agdarsec - Total Parser Combinators](https://gallais.github.io/pdf/agdarsec18.pdf). [more](https://gallais.github.io/blog/instrumenting-agdarsec).

[Proving tree algorithms for succinct data structures](http://jssst.or.jp/files/user/taikai/2018/PPL/ppl3-3.pdf)

[Saint: an API-generic Type-safe Interpreter](http://www.cse.chalmers.se/~patrikj/papers/Algehed_Jansson_et_al_Saint_TFP2018.pdf). [source](http://www.cse.chalmers.se/~myreen/tfp2018/program.html).

[Implementing Modal Dependent Type Theory](https://jozefg.github.io/papers/implementing-modal-dependent-type-theory-2019.pdf)

[Dependently Typed Haskell in Industry (Experience Report)](http://www.davidchristiansen.dk/pubs/dependent-haskell-experience-report.pdf)

[Intrinsically-Typed Definitional Interpreters for Linear, Session-Typed Languages](https://eelcovisser.org/publications/2020/RouvoetPKV20-preprint.pdf). [for imperative languages](https://dl.acm.org/citation.cfm?id=3158104)

[FUNCTIONAL PEARLS Heterogeneous binary random-access lists](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/CC82B2E79DC5CCAD57E0AC5DF0D43DEC/S0956796820000064a.pdf/heterogeneous_binary_randomaccess_lists.pdf) [tweet](https://twitter.com/Iceland_jack/status/1248729811104813059)

[Generic Programming of all Kinds](https://stackoverflow.com/questions/61439601/kind-polymorphism-in-closed-type-families)

[type your matrices for great good](https://github.com/bolt12/tymfgg-pearl/)

[Optimizing Generics Is Easy!](http://dreixel.net/research/pdf/ogie.pdf)

[A Specification for Typed Template Haskell](https://mpickering.github.io/papers/specification-typed-th.pdf) [tweet](https://twitter.com/DiazCarrete/status/1289543755842740226). [slides](https://kosmikus.org/zero-overhead-abstractions-in-haskell-using-staging.pdf)

[Multi-stage Programs in Context](https://mpickering.github.io/papers/multi-stage-programs-in-context.pdf)

[Staged Sums of Products](https://www.andres-loeh.de/StagedSOP/staged-sop-paper.pdf). [video](https://vimeo.com/449627298)

[Staged Selective Parser Combinators](https://icfp20.sigplan.org/details/icfp-2020-papers/20/Staged-Selective-Parser-Combinators). [video at 28:00](https://www.youtube.com/watch?v=i9wgeX7e-nc&list=PLyrlk8Xaylp4fOgwO5RUTrpgSA_HRjDMW&index=3)

[Eliminating Bugs with Dependent Haskell (Experience Report)](https://research.fb.com/wp-content/uploads/2020/08/Eliminating-Bugs-with-Dependent-Haskell-Experience-Report.pdf)

## Books

[Dependent Types at Work](http://www.cse.chalmers.se/~peterd/papers/DependentTypesAtWork.pdf) looks like a good introduction to Agda for people with Haskell experience.

> G¨odel system T is very important in the history of ideas that led to the CurryHoward isomorphism and Martin-L¨of type theory. Roughly speaking, G¨odel system T is the simply typed kernel of Martin-L¨of’s constructive type theory, and Martin-L¨of type theory is the foundational system out of which the Agda language grew. The relationship between Agda and Martin-L¨of type theory is much like the relationship between Haskell and the simply typed lambda calculus. Or perhaps it is better to compare it with the relationship between Haskell and Plotkin’s PCF [30]. Like G¨odel system T, PCF is based on the simply typed lambda calculus with truth values and natural numbers. However, an important difference is that PCF has a fixed point combinator which can be used for encoding arbitrary general recursive definitions. As a consequence we can define non-terminating functions in PCF.

[DEPENDENT TYPES IN HASKELL: THEORY AND PRACTICE](http://cs.brynmawr.edu/~rae/papers/2016/thesis/eisenberg-thesis-draft.pdf) Richard A. Eisenberg's thesis.

[Identity in HOTT](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)

[Programs and Proofs Mechanizing Mathematics with Dependent Types](http://ilyasergey.net/pnp/)

[A specification for dependent types in Haskell](http://dl.acm.org/citation.cfm?id=3110275)

[On dependent types and intuitionism in programming mathematics](https://arxiv.org/abs/1709.01810)

[POPLMark Reloaded: Strong Normalization for STLC proven via logical relations in the Kripke style formulation (pdf)](https://www.reddit.com/r/dependent_types/comments/71qbhi/poplmark_reloaded_strong_normalization_for_stlc/)

[Singleton types here Singleton types there Singleton types everywhere](https://www.iro.umontreal.ca/~monnier/comp-deptypes.pdf)

[Formal Verification of Spacecraft Control Programs Using a Metalanguage for State Transformers](https://arxiv.org/pdf/1802.01738.pdf)

[Handling Recursion in Generic Programming Using Closed Type Families](http://staff.mmcs.sfedu.ru/~ulysses/Papers/2018-TFP-dgp-recursion.pdf)

[Equivalences for free: univalent parametricity for effective transport](https://dl.acm.org/citation.cfm?id=3236787)

[Ornamental Algebras, Algebraic Ornaments](http://plv.mpi-sws.org/plerg/papers/mcbride-ornaments-2up.pdf). [The Essence of Ornaments](https://pages.lip6.fr/Pierre-Evariste.Dagand/stuffs/journal-2013-catorn-jfp/paper.pdf). [so question](https://stackoverflow.com/questions/27624145/does-agda-treat-records-and-datatypes-differently-for-the-purposes-of-terminatio).

> Dependent types thus provide not only a new ‘axis of diversity’ — indexing — for data structures,
but also new abstractions to manage and exploit that diversity. I

[Generic programming of all kinds](https://github.com/VictorCMiraldo/victorcmiraldo.github.io/blob/845e74b59aee5a322b6cdd1e45355db16a30d8af/data/hask2018_draft.pdf)

[sums of products for mutually recursive families](https://github.com/VictorCMiraldo/victorcmiraldo.github.io/blob/845e74b59aee5a322b6cdd1e45355db16a30d8af/data/tyde2018_draft.pdf). [tweet](https://twitter.com/Iceland_jack/status/1043937784904523776). [slides](https://github.com/VictorCMiraldo/victorcmiraldo.github.io/blob/845e74b59aee5a322b6cdd1e45355db16a30d8af/data/tyde2018_slides.pdf).

[Generic Deriving of Generic Traversals](https://arxiv.org/abs/1805.06798). [slides](https://github.com/kcsongor/talks/blob/master/ICFP18/generic-lens.pdf).

[All source material for Thinking with Types](https://www.reddit.com/r/haskell/comments/a5w1qm/ann_all_source_material_for_thinking_with_types/).

[C O M P I L I N G W I T H D E P E N D E N T T Y P E S - Bowman](https://www.williamjbowman.com/resources/wjb-dissertation.pdf).

[Sums of Products for Mutually Recursive Datatypes](https://victorcmiraldo.github.io/data/tyde2018_draft.pdf)

[Game Semantics of Martin-Lof Type Theory](https://arxiv.org/pdf/1905.00993.pdf)

[Extensible Type-Directed Editing](http://cattheory.com/extensibleTypeDirectedEditing.pdf)

[What is type theory,  precisely?](https://twitter.com/andrejbauer/status/1305464399231094784). [A general definition of dependent type theories](https://arxiv.org/pdf/2009.05539.pdf)

## Posts

[Practical Dependent Types in Haskell: Type-Safe Neural Networks](https://blog.jle.im/entry/practical-dependent-types-in-haskell-1.html) [reddit](https://pay.reddit.com/r/haskell/comments/4l199z/practical_dependent_types_in_haskell_type_safe/)

[Defunctionalization for the win](https://typesandkinds.wordpress.com/2013/04/01/defunctionalization-for-the-win/). [Defunctionalizing Arithmetic to an Abstract Machine](https://www.philipzucker.com/defunctionalizing-arithmetic-to-an-abstract-machine/).

[What are type families?](https://typesandkinds.wordpress.com/2015/09/09/what-are-type-families/)

[Better Data Types a la Carte -- with injectivity guaranteed by construction](https://www.reddit.com/r/haskell/comments/52p09a/better_data_types_a_la_carte_with_injectivity/)

[trying fancy type stuff: is it possible to write slice for Fixed-Length vectors?](https://www.reddit.com/r/haskell/comments/54u4lm/trying_fancy_type_stuff_is_it_possible_to_write/)

[How to write a Monoid instance for something that depends on parameters](http://stackoverflow.com/questions/39674555/haskell-how-to-write-a-monoid-instance-for-something-that-depends-on-paramete)

[Data families vs Injective type families](http://stackoverflow.com/questions/39707115/data-families-vs-injective-type-families)

[Quotient types for programmers](https://pay.reddit.com/r/haskell/comments/54xdvz/quotient_types_for_programmers/)

[Pattern Matching on Type Constructors?](https://pay.reddit.com/r/haskell/comments/54zcop/pattern_matching_on_type_constructors/) type families allow Prolog-like non-linear matches

[How can quotient types help safely expose module internals?](http://stackoverflow.com/questions/23596225/how-can-quotient-types-help-safely-expose-module-internals)

[Typesafe Printf with TypeInType](https://www.reddit.com/r/haskell/comments/55bvt4/typesafe_printf_with_typeintype/)

[working my way through Data.Type.Equality...my head	hurts](https://mail.haskell.org/pipermail/haskell-cafe/2015-January/117719.html)

[Decidable Propositional Equality in Haskell](http://hackage.haskell.org/package/base-4.9.0.0/docs/Data-Type-Equality.html)

[Simpler, Easier!](http://augustss.blogspot.com.es/2007/10/simpler-easier-in-recent-paper-simply.html)

[A Functional Programmer's Guide to Homotopy Type Theory](https://pay.reddit.com/r/haskell/comments/55xo01/a_functional_programmers_guide_to_homotopy_type/)

[HoTT](https://pay.reddit.com/r/haskell/comments/561muo/suggestion_the_more_experienced_typetheory/)

[Elaborator reflection](http://docs.idris-lang.org/en/latest/reference/elaborator-reflection.html)

[Dependent type checking without substitution](https://github.com/AndrasKovacs/tcbe/blob/master/nosubst.md) see also this [minimal implementation of the calculus of constructions](https://www.reddit.com/r/haskell/comments/62gnhp/my_particular_take_in_a_minimalist_simple_fast/)

[verified instances in Haskell](https://www.reddit.com/r/haskell/comments/62uv6g/verify_your_typeclass_instances_in_haskell_today/)

[Type Systems as Macros.](http://www.ccs.neu.edu/home/stchang/popl2017/) [LtU](http://lambda-the-ultimate.org/)

[dependent regexes talk by Stephanie Weirich](https://www.youtube.com/watch?v=GgD0KUxMaQs) [code](https://github.com/sweirich/dth/tree/master/popl17) (Reddit)[https://pay.reddit.com/r/haskell/comments/66p7s7/the_influence_of_dependent_types_stephanie_weirich/]

[Type inference for polymorphic recursion is undecidable](http://stackoverflow.com/questions/40247339/polymorphic-recursion-syntax-and-uses)

[Is it possible to declare FromJSON instance for my weird enum-like type?](https://stackoverflow.com/questions/44159807/is-it-possible-to-declare-fromjson-instance-for-my-weird-enum-like-type)

[Idiomatic boolean equality usage (singletons)](https://stackoverflow.com/questions/38290067/idiomatic-boolean-equality-usage-singletons)

> Don't use Booleans! I seem to keep repeating myself on this point: Booleans are of extremely limited usefulness in dependently-typed programming and the sooner you un-learn the habit the better. An Elem s ss ~ True context promises to you that s is in ss somewhere, but it doesn't say where. This leaves you in the lurch when you need to produce an s-value from your list of ss. One bit is not enough information for your purposes.

[Is there any connection between `a :~: b` and `(a :== b) :~: True`?](https://stackoverflow.com/questions/37923470/is-there-any-connection-between-a-b-and-a-b-true/37925725#37925725)

[Checking if one type-level list contains another](https://stackoverflow.com/questions/38209817/checking-if-one-type-level-list-contains-another/38221146#38221146)

> There seems to be an obsession with Boolean type families that's endemic to the Haskell community. Don't use them! You're making more work for yourself than necessary when it comes to using the result of such a test.

[So: what's the point?](https://stackoverflow.com/questions/33270639/so-whats-the-point)

[Dependent types in Haskell: Progress Report](https://typesandkinds.wordpress.com/2016/07/24/dependent-types-in-haskell-progress-report/)

[Decidable Propositional Equality in Haskell](https://typesandkinds.wordpress.com/2012/12/01/decidable-propositional-equality-in-haskell/)

[Tradeoffs of dependent types](https://www.reddit.com/r/haskell/comments/3zc81v/tradeoffs_of_dependent_types_xpost_from_ridris/) food for thought

There are two different notions of equality applicable to singletons: Boolean equality and propositional equality.

- Boolean equality is implemented in the type family (:==) (which is actually a synonym for the type family (==) from Data.Type.Equality) and the class SEq. See the Data.Singletons.Prelude.Eq module for more information.

- Propositional equality is implemented through the constraint (~), the type (:~:), and the class SDecide. See modules Data.Type.Equality and Data.Singletons.Decide for more information.

[Generic unification](https://ro-che.info/articles/2017-06-17-generic-unification)

> The unification-fd package by wren gayle romano is the de-facto standard way to do unification in Haskell. You’d use it if you need to implement type inference for your DSL, for example.

[music composition meets dependent types](https://www.reddit.com/r/haskell/comments/6holdz/mezzo_music_composition_meets_dependent_types/)

[generic-lens - Generically derive lenses for accessing fields of data types (with no Template Haskell)](https://www.reddit.com/r/haskell/comments/6glkpq/genericlens_generically_derive_lenses_for/) does records-sop allow something like this as well?

[justified containers](https://www.reddit.com/r/haskell/comments/6qu04u/justify_your_existence_with_justifiedcontainers/)

[Encode state transitions in types using linear types](https://www.reddit.com/r/haskell/comments/6rbk45/encode_state_transitions_in_types_using_linear/)

[Fixed-Length Vector Types in Haskell (an Update for 2017)](https://www.reddit.com/r/haskell/comments/6w0uvb/an_update_to_my_fixedlength_vector_types_in/)

[Type Level Merge Sort (Haskell)](https://www.athiemann.net/2017/08/31/mergesort.html)

[Uses of row polymorphism in Purescript](https://pay.reddit.com/r/haskell/comments/6xkqk7/why_has_row_polymorphism_not_made_it_into_haskell/dmh8j35/)

[dtt tiny language](https://hydraz.club/posts/2017-09-08.html)

[Coinduction in Coq and Isabelle](https://www.joachim-breitner.de/blog/726-Coinduction_in_Coq_and_Isabelle) [reddit](https://www.reddit.com/r/dependent_types/comments/6zbdmj/coinduction_in_coq_and_isabelle/)

[A hands-on introduction to cubicaltt](https://www.reddit.com/r/dependent_types/comments/713xop/a_handson_introduction_to_cubicaltt/)

[Dependent Pairs in Haskell - λC 2017](https://www.youtube.com/watch?v=PNkoUv74JQU) [slides](http://reasonablypolymorphic.com/some1-like-you/#/title)

[Structures of Arrays, Functors, and Continuations](https://github.com/rampion/conkin/blob/master/README.md#readme) [reddit](https://www.reddit.com/r/haskell/comments/78xxql/structures_of_arrays_functors_and_continuations/)

[Better Data Types a la Carte](http://reasonablypolymorphic.com/blog/better-data-types-a-la-carte) [reddit](https://www.reddit.com/r/haskell/comments/52p09a/better_data_types_a_la_carte_with_injectivity/) [earlier](https://mail.haskell.org/pipermail/haskell-cafe/2008-July/045613.html)

> Eliminating overlapping instances with type families is a known trick. In this case, we need a type family to compute a Nat index of the occurrence of a type in a lifted list, then dispatch the class instances on the computed index. This is used in freer and monad-classes, plus there's a version of this in compdata with paths to tree nodes instead of indices.

[Type-Directed Code Generation](http://reasonablypolymorphic.com/blog/type-directed-code-generation)

[Finite-State Machines, Part 2: Explicit Typed State Transitions](https://wickstrom.tech/finite-state-machines/2017/11/19/finite-state-machines-part-2.html)

[Indexed monads](https://github.com/pigworker/so-pigworker/blob/b3acb4a402ccf726fe835f94101505869745899b/markdown/indexed-monad.md)

[Finding bugs in Haskell code by proving it](https://www.joachim-breitner.de/blog/734-Finding_bugs_in_Haskell_code_by_proving_it) [and a compiler](https://dbp.io/essays/2018-01-16-how-to-prove-a-compiler-correct.html) [reddit](https://www.reddit.com/r/haskell/comments/7rlij4/how_to_prove_a_compiler_correct_using_hstocoq/)

[Deriving Bifunctor with Generics](http://kcsongor.github.io/generic-deriving-bifunctor/) [reddit](https://www.reddit.com/r/haskell/comments/7n981q/deriving_bifunctor_with_generics/)

[Haskell and dependent pairs](http://www.vittoriozaccaria.net/#/blog/2018/01/27/what-i-whish-i-knew-haskell-and-dependent-pairs.html) [reddit](https://www.reddit.com/r/haskell/comments/7tbw7d/what_i_whish_i_knew_haskell_and_dependent_pairs/)

[GADTs are weak approximations of inductive families from dependently typed languages](https://stackoverflow.com/a/21189680/1364288)

[Free Lenses for Higher-Kinded Data](http://reasonablypolymorphic.com/blog/free-lenses) [reddit](https://www.reddit.com/r/haskell/comments/88hnhm/free_lenses_for_higherkinded_data_reasonably/) [reddit](https://www.reddit.com/r/haskell/comments/884pe0/higherkinded_data_reasonably_polymorphic/) [another post](http://reasonablypolymorphic.com/blog/hkd-not-terrible) [reddit](https://www.reddit.com/r/haskell/comments/89okc1/hkd_less_terrible_than_you_might_expect/)

[Haskell-cafe Selda, type operators and heterogeneous lists](https://mail.haskell.org/pipermail/haskell-cafe/2018-April/128927.html)

[Heterogeneous lists with dependent types in Haskell](http://blog.poisson.chat/posts/2018-06-06-hlists-dependent-haskell.html) [reddit](https://www.reddit.com/r/haskell/comments/8p32ga/heterogeneous_lists_with_dependent_types_in/) [twitter](https://twitter.com/etorreborre/status/1004434826873769984)

[Proving commutativity of type level addition of natural numbers](https://stackoverflow.com/questions/50787796/proving-commutativity-of-type-level-addition-of-natural-numbers)

[Smart constructors that cannot fail](https://markkarpov.com/post/smart-constructors-that-cannot-fail.html) [reddit](https://www.reddit.com/r/haskell/comments/8rj1gy/smart_constructors_that_cannot_fail/)

[Type-safe tic tac toe](https://twitter.com/mstk/status/1008290541971259392)

[Functional Typelevel Programming in Scala](https://github.com/dotty-staging/dotty/blob/add-transparent/docs/docs/typelevel.md) [HN](https://news.ycombinator.com/item?id=17469890)

[pigworker tweet](https://twitter.com/pigworker/status/1023509070542721024)

> A recurring method in dependently typed programming is to program with data structures that enforce coherence of their indices, even though they contain no bits themselves...leaving said data-bearing indices entirely implicit.

[htree](https://github.com/i-am-tom/learn-me-a-haskell#htree) [tweet](https://twitter.com/am_i_tom/status/1031971184030765056)

[matching on types](https://twitter.com/Iceland_jack/status/1036265501499056130). [The universe pattern](https://www.youtube.com/watch?v=AWeT_G04a0A)

[Binomial heaps](https://jaspervdj.be/posts/2018-09-04-binomial-heaps-101.html#fn1)

> I think it is fairly common in Haskell for a developer to play around with different ways of representing a certain thing until you converge on an elegant representation. This is many, many times more important when we are dealing with dependently-typed Haskell.

> Inelegant and awkward data representations can make term-level programming clunky. Inelegant and awkward type representations can make type-level programming downright infeasible due to the sheer amount of lemmas that need to be proven.

> It took me a good amount of time to put the different pieces together in my head. It is not only a matter of proving the lemma: restructuring the code in childrenToForest_go leads to different lemmas you can attempt to prove, and figuring out which ones are feasible is a big part of writing code like this.

[Checking Dependent Types with Normalization by Evaluation: A Tutorial](http://davidchristiansen.dk/tutorials/nbe/)

[Singletons of singletons (emulating complex pi types in Haskell)](https://stackoverflow.com/questions/52399035/singletons-of-singletons-emulating-complex-pi-types-in-haskell).

[Variable-arity zipWith in terms of Applicative ZipList](https://gist.github.com/Icelandjack/e4c86ba4d6219ad9e44a68f99319b3fa). [reddit](https://www.reddit.com/r/haskell/comments/aaik7t/blog_variablearity_zipwith_in_terms_of/).

[Constraints.org](https://gist.github.com/Icelandjack/5afdaa32f41adf3204ef9025d9da2a70).

[particularities of type families](https://www.reddit.com/r/haskell/comments/54zcop/pattern_matching_on_type_constructors/d86h7d5)

[Interpreter for System T Combinator Language](https://stackoverflow.com/questions/53996638/haskell-interpreter-for-system-t-combinator-language)

(Typeable — A long journey to type-safe dynamic type representation)[https://medium.com/@hgiasac/typeable-a-long-journey-to-type-safe-dynamic-type-representation-9070eac2cf8b]

[a minimal singe-file example of dependently typed elaboration with holes and pattern unification](https://twitter.com/andrasKovacs6/status/1081563050057056257)

[Proving m + (1 + n) == 1+ (m + n) in Dependent Haskell](https://stackoverflow.com/questions/54236422/proving-m-1-n-1-m-n-in-dependent-haskell).

[Hide one of the type params of a multi-param typeclass in a function signature](https://stackoverflow.com/questions/54331107/hide-one-of-the-type-params-of-a-multi-param-typeclass-in-a-function-signature).

[overtyping microservices](https://gist.github.com/i-am-tom/20bc844acba06c7be83537c0df084455)

[flag, a tagged bool](https://www.reddit.com/r/haskell/comments/b463wp/flag_a_tagged_bool/)

[Proving Addition is Commutative in Haskell using Singletons](http://www.philipzucker.com/proving-addition-is-commutative-in-haskell-using-singletons/).

[How to think about types: Insights from a personal journey](http://www.cs.cmu.edu/~fp/talks/plmw19-talk.pdf)

[on the arity of type families](https://www.reddit.com/r/haskell/comments/btxt2j/on_the_arity_of_type_families_ryan_scott/)

> I'm not sure in which context this usage arose (Coq? Twelf? LF? Earlier? Anyone know?), but I tend to think of the terms parameter and index as having a slight difference in meaning.

[Singletons of Singletons for embedding System F-omega in Haskell](https://twitter.com/Iceland_jack/status/1083020606252204036)

[authenticated data structures, generically](https://github.com/adjoint-io/auth-adt). [tweet](https://twitter.com/haroldcarr/status/1140754437314682881)

[making ghosts of departed proofs easier to use](https://twitter.com/christopherdone/status/1192810405921480706)

[unordered effects](https://www.reddit.com/r/haskell/comments/ej8fme/unordered_effects/)

[Four ways to partially apply constraint tuples](https://ryanglscott.github.io/2019/11/30/four-ways-to-partially-apply-constraint-tuples/)

[alternatives to rewrite rules](https://github.com/gelisam/typelevel-rewrite-rules#alternatives)

[Ghost Hunting the Perfect API ( with departed proofs )](https://slides.com/anthony-1/deck-1c0c6a#/)

[Guarded Computational Type Theory](https://arxiv.org/abs/1804.09098)

[Describing Microservices using Modern Haskell (Experience Report)](https://www.47deg.com/assets/pdf/mu-haskell-hs-2020.pdf)

[Unpack your Existentials](https://www.parsonsmatt.org/2020/10/13/unpack_your_existentials.html)

[Functional Pearl: Witness me - Constructive arguments must be guided with concrete witness](https://twitter.com/Jose_A_Alonso/status/1375750477200175106). [Interesting CS trend: evidence](https://twitter.com/jjcarett2/status/1378359466492637187). [Linear Logic for Constructive Mathematics](https://golem.ph.utexas.edu/category/2018/05/linear_logic_for_constructive.html).

[pipelining in a session type framework](https://twitter.com/me_coot/status/1401226817617465345)

[Classless GHC.Generic with Type.Reflection](https://www.reddit.com/r/haskell/comments/ojlutn/classless_ghcgeneric_with_typereflection/)

## Tutorials

[Applying Type-Level and Generic Programming in Haskell](https://www.cs.ox.ac.uk/projects/utgp/school/andres.pdf) [Updated version](https://github.com/kosmikus/SSGEP/raw/master/LectureNotes.pdf) [reddit](https://www.reddit.com/r/haskell/comments/86rv65/is_there_a_reasonably_comprehensive_introductory/dw7fex1/)

[Liquid Haskell Tutorial](https://liquid.kosmikus.org/)

## Videos

[ZuriHac 2016: Generic (and type-level) Programming with Generics-sop](https://www.youtube.com/watch?v=sQxH349HOik)

[Coding for Types: The Universe Patern in Idris](https://www.youtube.com/watch?v=AWeT_G04a0A)

[SuperRecord: Practical Anonymous Records for Haskell](https://www.youtube.com/watch?v=Nh0XD2hPV8w)

[Type-Safe GraphQL Servers with GADTs](https://www.youtube.com/watch?v=jaKcEGkItsY)

[A Little Taste of Dependent Types](https://www.youtube.com/watch?v=1BWYy2-WM-o)

[cubical adventures](https://www.youtube.com/watch?v=W5-ulP_JzNc)

[dependent types in haskell](https://skillsmatter.com/skillscasts/12195-keynote-dependent-types-in-haskell).

[Shapeless](https://twitter.com/CodeMeshIO/status/1072899241172000768). [video](https://www.youtube.com/watch?v=xG00ivPa9hk).

[Why are type-families (over-)used in Haskell bindings to REST APIs?](https://www.reddit.com/r/haskell/comments/9zd8nf/why_are_typefamilies_overused_in_haskell_bindings/).

["one of the few good uses of Boolean type families"](https://stackoverflow.com/questions/38290067/idiomatic-boolean-equality-usage-singletons#comment64008188_38290067). [Avoid overlapping instances with closed type families](https://kseo.github.io/posts/2017-02-05-avoid-overlapping-instances-with-closed-type-families.html). [Avoiding Overlapping Instances with Closed Type Families (GHC/AdvancedOverlap)](https://stackoverflow.com/questions/39599346/avoiding-overlapping-instances-with-closed-type-families-ghc-advancedoverlap).

[n](http://oleg.fi/gists/posts/2018-12-29-reviewN.html). [variable arity](https://www.reddit.com/r/haskell/comments/aaik7t/blog_variablearity_zipwith_in_terms_of/). [more](https://stackoverflow.com/a/53973908/1364288).

[visible kind application example](https://www.reddit.com/r/haskell/comments/abxem5/experimenting_with_kleisli_instance_of/)

[DataKind unions](https://stackoverflow.com/questions/55556060/restrict-pattern-matching-to-subset-of-constructors)

[Typed Protocols, Session Type Framework for Applications](https://www.youtube.com/watch?v=j8gza2L61nM)

[BOB Summer 2019 - Peter Thiemann, Types for Protocols](https://www.youtube.com/watch?v=weOaECxYX6o)

[Whatever happened to "open data types and open functions"?](https://www.reddit.com/r/haskell/comments/d3qdql/whatever_happened_to_open_data_types_and_open/)

[System F in Agda, for fun and profit](https://iohk.io/en/research/library/papers/system-f-in-agdafor-fun-and-profit/)

[Datatype-Generic Programming by Andres Löh - Advanced Track @ ZuriHac 2020](https://www.youtube.com/watch?v=pwnrfREbhWY&list=PLiU7KJ5_df6aZbNfh_TUJt-6w9N3rYkTX&index=6&t=0s)

[STORM framework ](https://twitter.com/RanjitJhala/status/1415388341869056000)

[GHC curiosities: Equality constraints in kinds](https://ryanglscott.github.io/2021/08/01/equality-constraints-in-kinds/)

[CBPV doesn't distinguish data/code using kinds [...] the kind-based approach is a good one](https://www.reddit.com/r/haskell/comments/ox5j50/zero_cost_io_take_two/h7lox6b/). [Unboxed types in GHC](https://www.reddit.com/r/haskell/comments/oxqwju/richard_eisenberg_unboxed_types_in_ghc/).

