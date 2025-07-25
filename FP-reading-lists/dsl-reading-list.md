# DSLs

## stuff

http://www.cs.ox.ac.uk/jeremy.gibbons/publications/fp4dsls.pdf Functional Programming for Domain-Specific Languages 
http://cs448h.stanford.edu/DSEL-Little.pdf hudak
https://www.andres-loeh.de/HaskellForDSLs.pdf Loh
https://github.com/mchakravarty/hoas-conv
https://wiki.haskell.org/Embedded_domain_specific_language
https://www.reddit.com/r/haskell/comments/2e8d53/whats_the_best_practice_for_building_a_dsl_in/
https://skillsmatter.com/skillscasts/2872-haskell-for-embedded-domain-specific-languages
http://cacm.acm.org/magazines/2011/7/109910-dsl-for-the-uninitiated/fulltext
https://www.reddit.com/r/haskell/comments/2dh0sd/denotational_design_from_meanings_to_programs_by/
http://lambda-the-ultimate.org/node/2438
http://okmij.org/ftp/tagless-final/course/lecture.pdf
https://gist.github.com/PkmX/182c6c5444b695d9a794
http://homepages.inf.ed.ac.uk/slindley/papers/unembedding.pdf

Two approaches to representing variables in a typed term language implemented as a GADT are (1) to use higher-order abstract syntax (HOAS) or to use de Bruijn indices.. Both approaches are convenient for manipulating terms as they require no explicit alpha conversion and avoid name capture during substitution. Nevertheless, there are trade offs between the two. In particular, the HOAS representation doesn't support comparing variable names and the de Bruijn representation is inconvenient for humans to read and write. For a more detailed discussion, see for example Conor McBride and James McKinna's I am not a number: I am a free variable, where they discuss a mixed representation using de Bruijn indices for bound variables and variables of the meta-language for free variables.

The tension between the HOAS and de Bruijn representation also has relevance for the design and implementation of embedded domain specific languages (EDSLs) — aka internal languages. When an internal includes higher-order functions, it is usually most convenient for the user to use the function abstraction mechanisms of the host language. However, to execute or compile the internal language, de Bruijn notation is often more convenient; at least, if optimisations are performed.

http://www2.hh.se/staff/vero/dsl/printL1.pdf
http://www2.hh.se/staff/vero/dsl/printL2.pdf
http://www2.hh.se/staff/vero/dsl/printL3.pdf
http://www2.hh.se/staff/vero/dsl/printL4.pdf
http://www2.hh.se/staff/vero/dsl/printL5.pdf
http://www2.hh.se/staff/vero/dsl/printL6.pdf

Typed compilation to tagless-final HOAS The embedded DSL is now higher-order: it is simply-typed lambda-calculus with the fixpoint and constants — essentially, PCF. We no longer use staging. Rather, we compile to tagless-final representation, which can be interpreted by different interpreters. Regardless of the number of interpretations of a term, the type checking happens only once. We build our own Dynamics to encapsulate typed terms and represent their types. 

https://www.haskell.org/communities/11-2009/report.pdf
https://en.wikipedia.org/wiki/Programming_Computable_Functions

https://mail.haskell.org/pipermail/haskell-cafe/2009-October/067425.html

https://blog.cppcabrera.com/posts/56-writing-a-search-dsl-1.html

http://gallium.inria.fr/~naxu/research/dsel.pdf

Sharing and recursion are common problems when implementing DSLs. Often some kind of observable sharing is requested that requires a deep embedding.

Oleg in Haskell-Cafe about Designing DSL with explicit sharing (was: I love purity, but it's killing me)
Koen Classen: Observable Sharing for Functional Circuit Description
Andy Gill: Type-Safe Observable Sharing
Tom Lokhorst AwesomePrelude presentation (video)
Leandro Lisboa Penz Haskell eDSL Tutorial - Shared expenses
Bruno Oliveira and William Cook: Functional Programming with Structured Graphs
Emil Axelsson and Koen Claessen: Using Circular Programs for Higher-Order Syntax
Oleg Kiselyov: Implementing explicit and finding implicit sharing in embedded DSLs

An obvious way to relief the tension between the representations is to use HOAS in the surface representation of the internal language and to convert that to the de Bruijn representation before optimisation and execution. However, the conversion is not entirely straight forward for a strongly typed internal language with typed intermediate representations and type-preserving transformations between those representations.

http://www.iro.umontreal.ca/~monnier/tcm.pdf

[Implementing Explicit and Finding Implicit Sharing in Embedded DSLs](http://arxiv.org/pdf/1109.0784.pdf)

[I love purity, but it's killing me](https://mail.haskell.org/pipermail/haskell-cafe/2008-February/039639.html)

[Simple and Compositional Reification of Monadic Embedded Languages](http://www.cse.chalmers.se/~joels/writing/bb.pdf) 

[https://www.reddit.com/r/haskell/comments/4ck2yh/compilation_as_a_typed_edsltoedsl_transformation/](https://www.reddit.com/r/haskell/comments/4ck2yh/compilation_as_a_typed_edsltoedsl_transformation/)

[The Difference Between Shallow and Deep Embedding](http://alessandrovermeulen.me/2013/07/13/the-difference-between-shallow-and-deep-embedding/)

[Certifying Machine Code Safety: Shallow versus Deep Embedding](https://www21.in.tum.de/~nipkow/pubs/tphols04.html)

[Shallow versus Deep Embeddings](http://cstheory.stackexchange.com/questions/1370/shallow-versus-deep-embeddings)

[Embedded domain specific language (links)](https://wiki.haskell.org/Embedded_domain_specific_language)

[using an opaque/abstract data type to remove power from a monadic interface](https://www.reddit.com/r/haskell/comments/kntpkm/monthly_hask_anything_january_2021/gkr4h2x/)

[Practical Normalization by Evaluation for EDSLs](https://twitter.com/Iceland_jack/status/1496855129844330498). [pdf](http://www.cse.chalmers.se/~russo/publications_files/haskell21.pdf)

> Often, eDSL designers face a choice between either adding complex features to an eDSL or keeping the core eDSL simple and exploiting the host language to construct programs.

> Should the eDSL support pairs in expressions (Exp (a, b)), or should it use pairs of expressions ((Exp a, Exp b))? 

> Should the eDSL support functions (Exp (Int → Int)) directly or should it instead rely on Haskell functions (Exp Int → Exp Int) to build programs?

> Normalization by Evaluation (NbE) [9], is a program specialization technique that offers a solution to this problem by making specialization automatic, without the need for manual stage separation.

> In programming language semantics, normalisation by evaluation (NBE) is a
> style of obtaining the normal form of terms in the λ-calculus by appealing to
> their denotational semantics. A term is first interpreted into a denotational
> model of the λ-term structure, and then a canonical (β-normal and η-long)
> representative is extracted by reifying the denotation. Such an essentially
> semantic approach differs from the more traditional syntactic description of
> normalisation as a reductions in a term rewrite system where β-reductions are
> allowed deep inside λ-terms.

>  NbE’s ability to aggressively reduce arithmetic expressions even in the presence of unknown values

> A normal form in NbE only needs to be some canonical element in the
> equivalence class of expressions identified by the equations, but it is often
> helpful to think of it as an expression that cannot be reduced further by
> applying the 𝛽 laws by orienting them from left to right, and has a canonical
> shape as dictated by the 𝜂 law.

> addition and multiplication must be performed when both the operands are
> available as lifted integer values. In the absence of either, such as in Add
> (Lift 2) (Var "x"), the expression cannot be reduced further, and must be
> considered to be in normal form

[Introduction to Normalization by Evaluation (Favonia video)](https://www.youtube.com/watch?v=atKqqiXslyo). [reification seems related to eta rules](https://youtu.be/atKqqiXslyo?t=312) 

> Good example of sorting as a form of "normalization".

> The evaluation and reification phases become intertwined because the expansion during reification could trigger delayed evaluation.

[Supercompilation and Normalisation by Evaluation](https://www.researchgate.net/publication/48991563_Supercompilation_and_Normalisation_by_Evaluation)

> It has been long recognised that partial evaluation is related to proof normalisation. Normalisation by evaluation, which has been presented for theories with simple types, has made this correspondance formal.

> Supercompilation is a program transformation technique which performs a superset of the simplications performed by partial evaluation 

[Partial evaluation, normalization by evaluation, multi-stage programming, supercompilation](http://lists.seas.upenn.edu/pipermail/types-announce/2021/009633.html)

[These notes are a collection of literate programs that demonstrate how to derive a normalization procedure from an evaluator or interpreter](https://davidchristiansen.dk/tutorials/nbe/)

> When we have a collection of equations over syntax, the syntax can be seen as divided into various “buckets,” where each expression in a bucket is αβ-equivalent to all the others in its bucket. One way to check whether two expressions are in the same bucket is to assign each bucket a representative expression and provide a way to find the bucket representative for any given expression. 

> it is much easier to implement an evaluator with environments than it is to correctly implement substitution, which is surprisingly subtle.

> When reducing under λ, there will also be variables that do not have a value in the environment. To handle these cases, we need values that represent neutral expressions. 

> Apply a function, potentially attaching more arguments to a neutral expression.

> We can now work with values that are neutral, but every neutral value begins with a neutral variable, and those are not introduced anywhere. Additionally, our values are clearly not the normal forms of expressions. The second step in implementing a normalizer is to write a procedure to convert the values back into their representations as syntax—a process referred to as reading back or quoting value into syntax.

> There are a number of ways in which type systems might not be syntax-directed. One way is that there might be insufficient information in the program to determine the type. For example, languages like ML in which all types can be inferred typically require a type checking algorithm that looks very little like the rules. Another alternative is to require that programs be annotated with types in enough locations to allow the type rules to follow the annotations. Another way in which type systems frequently fail to be syntax-directed is by having a complicated notion of type equality or subsumption, which makes it so that the type checker at each step could either transform a type or follow the program’s syntax. These are not the only ways in which types might fail to be syntax-directed, but they occur frequently.

> Bidirectional type checking is a technique for making type systems syntax-directed that adds only a minimal annotation burden. Typically, only the top level of an expression or any explicit redexes need to be annotated. Additionally, bidirectional type checking provides guidance for the appropriate places to insert checks of type equality or subsumption.

> Hi. Newbie question. While reading "Checking Dependent Types with
> Normalization by Evaluation" I encountered the passage: it is much easier to
> implement an evaluator with environments than it is to correctly implement
> substitution, which is surprisingly subtle.  In what way does an "evaluator
> with environments" avoids the need for substitution? Where can I find a
> comparison of the "evaluator" approach and the one based in substitutions,
> which I guess means doing beta reductions? 

> An evaluator with environments can just look up the value of a variable in
> the environment when it hits the variable case.  Substitution, on the other
> hand, has to deal with capture avoidance issues.  Another part of the trick,
> though, is that before putting a var:value pair in to the environment you
> either a) force value to be fully evaluated already, as in an eager eval
> style b) also associate value with (a copy of) the already-current
> environment, the one it was intended to be evaluated in Doing either of those
> means you never have to think about capture-avoidance or name collisions-
> values are always evaluated in the context they were supposed to be,
> shadowing just means putting an extra binding at the front of the
> environment.

> normal forms are more than just expressions that do not contain redexes. To
> be a normal form is to be the canonical representative of the equivalence
> class induced by the equality judgment, such that comparing normal forms for
> α-equivalence is sufficient to decide whether two expressions are equal.

> One technique for solving this is extending normalization by evaluation to
> take types into account. Reductions still occur in the evaluator, as before,
> but the typed version of the read-back procedure takes the types into account
> to perform η-expansion.

> Typed normalization by evaluation is far from the only way to implement
> conversion checking for dependent types. Indeed, normalization by evaluation
> has a number of characteristics that make it only suitable for certain
> theories: it η-expands expressions as many times as possible, but η-expansion
> is not valid for some theories (including Coq’s Calculus of Constructions)
> and which furthermore can consume a lot of memory if retained; also, it fully
> normalizes terms when it may have been possible to determine they were
> identical by an immediate α-equivalence check. Because NbE with higher-order
> closures re-uses the implementation language’s functions, achieving laziness
> in a strict implementation language requires additional work.

[Normalization by Evaluation Dependent Types and Impredicativity—Abel (PDF)](https://www.cse.chalmers.se/~abela/habil.pdf)

> Normalization by evaluation (NbE) is a technique to compute the normal form
> of a lambda-term, i. e., an expression of a pure functional programming
> language. While evaluation is only concerned with computing closed
> expressions, normalization also applies to function bodies, thus, needs to
> compute with open expressions containing free variables. NbE reduces
> normalization to evaluation of expressions in a residualizing model, i. e., a
> computational structure that has extra base values which are unknowns or
> computations blocked by unknowns.

[The essential part of NbE is the separation of syntax and values](https://cstheory.stackexchange.com/questions/48952/what-technique-is-used-to-implement-type-checking-for-coc)

> The specification of values is obtained from the specification of syntax by
> replacing binders with metalanguage functions or closures. Evaluation goes
> from syntax to values and performs β-reduction (but not necessarily
> η-conversions). Then, conversion checking can be implemented on values,
> proceeding purely structurally, except where we want syntax-directed
> η-checking in the manner specified in ATAPL.

[What are the advantages of normalization by evaluation over traditional reduction-based normalization?](https://proofassistants.stackexchange.com/questions/196/what-are-the-advantages-of-normalization-by-evaluation-over-traditional-reductio)

> Eta-equivalences such as M≡(λx.Mx) are quite difficult to implement with a
> reduction-only algorithm. There are various reasons for this, such as the
> fact that if you want to reduce λx.Mx to M you need to check that x doesn't
> occur in M, and if you want to expand M to λx.Mx you need to have type
> information present to know that M has a function-type. I won't say it's
> impossible, but normalization-by-evaluation is a clean, generalizable, and
> easy-to-reason-about family of algorithms that perform both β-reduction and
> η-expansion in a type-directed way.

[Elementary Tutorial on Normalization-by-Evaluation](https://okmij.org/ftp/tagless-final/NBE.html)

> There may be some who peer beyond symbols, who view them as shadows of real things, who look for intuitions behind the seemingly arbitrary rules and seek to grasp the meaning of the game.

[Normalization and Partial Evaluation](http://hjemmesider.diku.dk/~andrzej/papers/NaPE.pdf)

> We first present normalization by evaluation for a combinatory version of
> G¨odel System T. Then we show normalization by evaluation for typed lambda
> calculus with β and η conversion. Finally, we introduce the notion of binding
> time, and explain the method of type-directed partial evaluation for a small
> PCF-style functional programming language. We give algorithms for both
> call-by-name and call-by-value versions of this language

> In lambda calculus “evaluation” means normalization of a closed term, usually
of base type.

> It is important here to contrast (a) normalization and partial evaluation and
> (b) the evaluation of a complete program. In (a) there are still unknown
> (dynamic) inputs, whereas in (b) all the inputs are known.

## papers

[Using Circular Programs for Higher-Order Syntax](http://www.cse.chalmers.se/~emax/documents/axelsson2013using.pdf)

[Implementing Explicit and Finding Implicit Sharing in Embedded DSLs](http://okmij.org/ftp/tagless-final/sharing/sharing.pdf)

[Type-Safe Observable Sharing in Haskell](http://www.ittc.ku.edu/~andygill/papers/reifyGraph.pdf)

[An Image Processing Language: External and Shallow/Deep Embeddings](http://www.macs.hw.ac.uk/~rs46/papers/rwdsl2016/rwdsl-2016.pdf)

[Fizzbuzz in Haskell by embedding a DSL](https://themonadreader.files.wordpress.com/2014/04/fizzbuzz.pdf)

[Strongly Typed Term Representations in Coq](https://people.mpi-sws.org/~gil/publications/typedsyntaxfull.pdf)

[Finally, Safely-Extensible and Efficient Language-Integrated Query](http://okmij.org/ftp/meta-programming/quel.pdf)

[A Self-Hosting Evaluator using HOAS](http://www.ccs.neu.edu/racket/pubs/scheme2006-b.pdf)

[Typed Self-Representation](http://www.informatik.uni-marburg.de/~kos/papers/pldi142_rendel1.pdf)

[Breaking Through the Normalization Barrier: A Self-Interpreter for F-omega](http://compilers.cs.ucla.edu/popl16/popl16-full.pdf)

[Church and Curry: Combining Intrinsic and Extrinsic Typing](http://www.cs.cmu.edu/~fp/papers/andrews08.pdf)

[Church Encoding of Data Types Considered Harmful for Implementations](https://ifl2014.github.io/submissions/ifl2014_submission_13.pdf) linked from [this](https://www.reddit.com/r/haskell/comments/61zs2l/regarding_dsls_what_are_the_recommended_use_cases/) interesting reddit discussion.

> (P)HOAS and its ilk are a tool to simplify the representation of variable binders and the operation of term substitution. (bound, a great library, has an altogether different approach to solving this problem.) Phenomenally useful if variable binding and term substitution are important in your DSL - ie, your DSL looks something like lambda calculus - but quite useless for imperative languages where variables are declared and then written and read.

[Tagless Staged Interpreters for Typed Languages](https://www.cs.rice.edu/~taha/publications/conference/icfp02.pdf)

[Abstracting Definitional Interpreters](http://david.darais.com/assets/papers/abstracting-definitional-interpreters/adi.pdf). [video](https://twitter.com/jeanqasaur/status/1407107972371673088). [tweet](https://twitter.com/wilton_quinn/status/1413816658758537217).

[Sound and Reusable Components for Abstract Interpretation](https://svenkeidel.de/papers/analysis-components.pdf)

[Type Soundness Proofs with Definitional Interpreters](https://www.cs.purdue.edu/homes/rompf/papers/amin-popl17a.pdf)

[Engineering Definitional Interpreters](https://www.cs.tufts.edu/~nr/pubs/interps.pdf)

[Tagging, Encoding, and Jones Optimality](https://pdfs.semanticscholar.org/a46e/8b573d826f3a2da246d1e80108031f7daa53.pdf)

[The Structure and Performance of Efficient Interpreters](https://www.jilp.org/vol5/v5paper12.pdf) apparently [obsolete?](https://news.ycombinator.com/item?id=13990592)

[Compiling to categories](http://conal.net/papers/compiling-to-categories/) "The general technique appears to provide a compelling alternative to deeply embedded domain-specific languages."

[Type-safe observable sharing in Haskell](https://pdfs.semanticscholar.org/4838/bd0a91b3058b467fa31ad9e0810121b46388.pdf)

[Observable Sharing for Functional Circuit Description](https://pdfs.semanticscholar.org/0d2c/c9ee73d9398fd273845a26b3ed79af5ebf29.pdf)

[Stream Processing for Embedded Domain Specific Languages](http://www.cse.chalmers.se/~emax/documents/aronsson2015stream.pdf)

[Effect Handlers in Scope](http://www.cs.ox.ac.uk/people/nicolas.wu/papers/Scope.pdf)

[Abstracting Definitional Interpreters](https://arxiv.org/pdf/1707.04755.pdf) [github](https://github.com/josefs/AbstractingDefinitionalInterpreters)

[Compositional Soundness Proofs of Abstract Interpreters](https://www.student.informatik.tu-darmstadt.de/~xx00seba/publications/arrow-abstract-interp.pdf)

[Collapsing Towers of Interpreters](https://www.cs.purdue.edu/homes/rompf/papers/amin-popl18.pdf) [HN](https://news.ycombinator.com/item?id=15626816) [lobsters](https://lobste.rs/s/yj31ty/collapsing_towers_interpreters)

[Writing CEK-style interpreters (or semantics) in Haskell](http://matt.might.net/articles/cek-machines/) [reddit](https://www.reddit.com/r/haskell/comments/7f3xux/writing_cekstyle_interpreters_or_semantics_in/)

[Functional EDSLs for Web Applications](https://ekblad.cc/pubs/thesis.pdf) [reddit](https://www.reddit.com/r/haskell/comments/85e97q/haskell_phd_thesis_functional_edsls_for_web/)

> Haste, Selda

[(Re-)Creating sharing in Agda’s GHC backend](https://macsphere.mcmaster.ca/bitstream/11375/22177/2/Perna_Natalie_201706_MSc.pdf)

[Strongly Typed Term Representations in Coq](https://link.springer.com/article/10.1007/s10817-011-9219-0)

> There are two approaches to formalizing the syntax of typed object languages in a proof assistant or programming language. The extrinsic approach is to first define a type that encodes untyped object expressions and then make a separate definition of typing judgements over the untyped terms. The intrinsic approach is to make a single definition that captures well-typed object expressions, so ill-typed expressions cannot even be expressed. Intrinsic encodings are attractive and naturally enforce the requirement that metalanguage operations on object expressions, such as substitution, respect object types. The price is that the metalanguage types of intrinsic encodings and operations involve non-trivial dependency, adding significant complexity. This paper describes intrinsic-style formalizations of both simply-typed and polymorphic languages, and basic syntactic operations thereon, in the Coq proof assistant. The Coq types encoding object-level variables (de Bruijn indices) and terms are indexed by both type and typing environment. One key construction is the boot-strapping of definitions and lemmas about the action of substitutions in terms of similar ones for a simpler notion of renamings. In the simply-typed case, this yields definitions that are free of any use of type equality coercions. In the polymorphic case, some substitution operations do still require type coercions, which we at least partially tame by uniform use of heterogeneous equality.

[intrinsically-typed definitional interpreters for imperative languages](http://pure.tudelft.nl/ws/files/39919546/34370649.pdf)

> A definitional interpreter defines the semantics of an object language in terms of the (well-known) semantics of a host language, enabling understanding and validation of the semantics through execution. Combining a definitional interpreter with a separate type system requires a separate type safety proof. An alternative approach, at least for pure object languages, is to use a dependently-typed language to encode the object language type system in the definition of the abstract syntax. Using such intrinsically-typed abstract syntax definitions allows the host language type checker to verify automatically that the interpreter satisfies type safety. Does this approach scale to larger and more realistic object languages, and in particular to languages with mutable state and objects?

> In this paper, we describe and demonstrate techniques and libraries in Agda that successfully scale up intrinsically-typed definitional interpreters to handle rich object languages with non-trivial binding structures and mutable state. While the resulting interpreters are certainly more complex than the simply-typed λ-calculus interpreter we start with, we claim that they still meet the goals of being concise, comprehensible, and executable, while guaranteeing type safety for more elaborate object languages.

[Folding Domain−Specific Languages: Deep and Shallow Embeddings - Gibbons](http://www.cs.ox.ac.uk/publications/publication7584-abstract.html)

[Abstracting Definitional Interpreters](https://arxiv.org/abs/1707.04755)

[A Generic Abstract Syntax Model for Embedded Languages](https://www.cs.tufts.edu/~nr/cs257/archive/emil-axelsson/paper.pdf)

> But the real insight of this story is a replaying of an insight from Reynold's landmark paper, Definitional Interpreters for Higher-Order Programming Languages, in which he observes definitional interpreters enable the defined-language to inherit properties of the defining-language. We show the same holds true for definitional abstract interpreters. Remarkably, we observe that abstract definitional interpreters can inherit the so-called "pushdown control flow" property, wherein function calls and returns are precisely matched in the abstract semantics, simply by virtue of the function call mechanism of the defining-language. 

[Embedding F](http://homepages.inf.ed.ac.uk/slindley/papers/embedding-f.pdf) [tweet](https://twitter.com/Iceland_jack/status/994762622212993024) [gist](https://gist.github.com/Icelandjack/223763d397723efe0bc92e10b60c69fc) type-level lambdas

> This millennium has seen a great deal of research into embedded
domain-specific languages. Primarily, such languages are simplytyped.
Focusing on System F, we demonstrate how to embed polymorphic
domain specific languages in Haskell and OCaml. We exploit
recent language extensions including kind polymorphism and
first-class modules

[Lightweight Modular Staging: A Pragmatic Approach to Runtime Code Generation and Compiled DSLs](https://infoscience.epfl.ch/record/150347/files/gpce63-rompf.pdf) [Haskell example](https://gist.github.com/mpickering/b6935a63717129cc33b77774c126168a)

[Alchemy: A Language and Compiler for Homomorphic Encryption Made easY](http://web.eecs.umich.edu/~cpeikert/pubs/alchemy.pdf) look at the appendix

> The difficulty of using HOAS with effectful generators has long
been recognized in the literature as a thorny problem,

[Intrinsically-Typed Definitional Interpreters for Imperative Languages](http://casperbp.net/store/intrinsicallytyped.pdf). [Intrinsically Typed Definitional Interpreters: The Good, The Bad, and The Ugly](https://conf.researchr.org/event/plnl-2018/plnl-2018-papers-intrinsically-typed-definitional-interpreters-the-good-the-bad-and-the-ugly). [video](https://www.youtube.com/watch?v=8gT13KSZNRk).

[Generic Monadic Constructs for Embedded Languages](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.447.3499&rep=rep1&type=pdf). Feldspar?

[Lambda: the Ultimate Sublanguage](https://www.cl.cam.ac.uk/~jdy22/papers/lambda-the-ultimate-sublanguage.pdf). [tweet](https://twitter.com/thompson_si/status/1132206867961339905)

[Scoping Monadic Relational Database Queries](https://ekblad.cc/pubs/selda-paper.pdf)

[From Definitional Interpreter to Symbolic Executor](http://casperbp.net/store/from-definitional-interpreter-to-symbolic-executor.pdf)

[Towards Secure IoT Programming in Haskell](http://nachivpn.me/haski.pdf)

> Haski is designed after the synchronous programming language Lustre

> our design does not require any modifications to GHC or the use of compiler plug-ins. Instead, Haski
uses embedding techniques by leveraging advanced type-level
features of GHC such as GADTs [Peyton Jones et al. 2006],
data kinds [Yorgey et al. 2012], existential types, and pattern
synonyms [Pickering et al. 2016].

[going functional on exotic trades](https://arbitrary.name/papers/fpf.pdf)

> The Functional Payout Framework, fpf, is a Haskell application that uses an
> embedded domain specific functional language to represent and process exotic
> financial derivatives.  Whereas scripting languages for pricing exotic
> derivatives are common in banking, fpf uses multiple interpretations to not
> only price such trades, but also to analyse the scripts to provide lifecycle
> support and more.

> The lifecycle of exotic trades involves many different people in different
> rˆoles, including structurers, salespeople, quantitative analysts (“quants”),
> risk management teams and traders. Structurers create new ideas for trades
> and variations on existing ones. Their aim is to find novel and effective
> ways to meet the client’s requirements. The structurers then develop and test
> a prototype implementation.  Salespeople support interaction with the
> customer, and write a term sheet that describes the option using a
> combination of prose and mathematical notation. The quants provide
> mathematical modelling expertise.


## blog

[Resource-AWare Feldspar](https://github.com/Feldspar/raw-feldspar/blob/master/README.md)

[Compilation as a Typed EDSL-to-EDSL Transformation](http://fun-discoveries.blogspot.com.es/2016/03/compilation-as-typed-edsl-to-edsl.html)

[Combining deep and shallow embedding of domain-specific languages](http://www.sciencedirect.com/science/article/pii/S1477842415000500)

[Yet another explanation of intrinsic encoding](http://okmij.org/ftp/formalizations/#intrinsic)

[The parsing/typechecking problem for intrinsic encodings (?)](http://lambda-the-ultimate.org/node/2438#comment-36667) and [another take](http://lambda-the-ultimate.org/node/2438#comment-58396).

[De-serialization and type-checking](http://okmij.org/ftp/tagless-final/course/course.html#type-checking)

[parsing for PHOAS expressions](http://stackoverflow.com/questions/19415621/parsing-for-phoas-expressions)

[Typed Tagless-Final Linear Lambda Calculus](https://www.schoolofhaskell.com/user/mutjida/typed-tagless-final-linear-lambda-calculus) great resource! tagless final + HOAS (?)

[Embedding, deep and shallow](http://composition.al/blog/2015/06/02/embedding-deep-and-shallow/)

[Domain-specific Languages and Code Synthesis Using Haskell](https://queue.acm.org/detail.cfm?id=2617811)

[Lessons learned building a toy compiler](https://jaseemabid.github.io/2017/07/04/compiler.html)

[A small (<500 LOC) programming language capable of proving theorems about its own terms](https://www.reddit.com/r/haskell/comments/7zohb5/a_small_500_loc_programming_language_capable_of/)

[Backpack for initial and final encodings](http://qfpl.io/posts/backpack-for-initial-and-final-encodings/) [reddit](https://www.reddit.com/r/haskell/comments/84k7yk/backpack_for_initial_and_final_encodings/)

[Duplicator Interpreter with HOAS](https://stackoverflow.com/questions/43648182/duplicator-interpreter-with-hoas)

[Sharing in Haskell EDSLs](https://jtobin.io/sharing-in-haskell-edsls)

[Writing A GraphQL DSL In Kotlin](https://alediaferia.com/2019/03/18/writing-graphql-dsl-kotlin/)

[Parsing Typed eDSL](https://serokell.io/blog/parsing-typed-edsl). [reddit](https://www.reddit.com/r/haskell/comments/c19gw5/article_parsing_typed_edsl/erccrz8).

> It's well-known™ that this sort of 'intrinsically-typed' AST (where the AST is indexed by types/contexts) does not scale to dependently-typed object languages. As soon as your type contexts are telescopes instead of lists (i.e., types in the context can refer to other types in the context), you need induction-recursion and it gets unpleasant.

> A completely valid point; I still think a indexed AST is preferred for correctness, particularly between phases. They definitely quite more time/dedication to complete though -- telescopes are much harder to deal with than lists.

[Move DSL](https://twitter.com/b1ackd0g/status/1141793530488053760)

[Building a Friendly and Safe EDSL with IxState and TypeLits](https://free.cofree.io/2020/02/29/dsl/)

[Combining Deep and Shallow Embedding of Domain-Specific Languages](http://www.cse.chalmers.se/~josefs/publications/svenningsson2015combining.pdf). [reddit](https://www.reddit.com/r/haskell/comments/l644p9/combining_deep_and_shallow_embedding_of/).

["There is at least some similarity between synthetic mathematics and domain specific embedded programming languages"](https://ncatlab.org/nlab/show/synthetic+mathematics#relation_to_computer_science)

## slides

[Combining deep and shallow embeddings: a tutorial](http://www.cse.chalmers.se/~josefs/DSLTutorial/tutorialSlides.html)

[Building Small Native Languages with Haskell](http://dev.stephendiehl.com/paris.pdf)

[compiling a fifty year journey](http://www.cs.nott.ac.uk/~pszgmh/fifty.pdf) [material](https://github.com/pa-ba/McCarthy-Painter)

[DSLs for non-programmers are a hoax](https://artur-martsinkovskyi.github.io//2019/dsls-are-hoax/). [reddit](https://www.reddit.com/r/programming/comments/bssesw/dsls_for_nonprogrammers_are_a_hoax_amblog/). [hn](https://news.ycombinator.com/item?id=20007813).

[kotlin DSLs](https://fr.slideshare.net/nfrankel/devfest-santo-domingo-kotlin-dsl)

[More about NbE](http://www.cse.chalmers.se/~abela/talkEAFIT2017.pdf)

> normalization: Bring an expression with unkowns into a canonical form.
> Unknowns = free variables.
> Checking equality by comparing canonical forms. 

> Evaluation
> Compute the value of an expression relative to an environment.
> Environment assigns values to free variables of expressions

> Normalization by Evaluation (NbE)
> Adapt an interpreter to simplify expressions with unknowns.

> Interpreters can be turned into normalizers in a systematic way.

> Normalization-by-evaluation has helped to understand η-equality

[Normalization by Evaluation for Martin-Lof Type Theory (2018)](https://jozefg.github.io/papers/2018-logsem-slides.pdf)

> The most common alternatives to NbE are based on rewriting

> Original idea: normalize programs using the ambient semantic universe.

> [...] Many presentations now use a different semantic model: syntax. [?]

> Construct a syntax in which all expressions are canonical.

> Divided between neutrals, normals, values, closures

> Need to include neutrals with type information to allow η-expansions later.

> We need type information to know whether η-expansion is necessary now that we
> have neutrals of all types.  In the domain-theoretic or intrinsic formulation
> this was baked in as we disallowed such neutrals.

> Inject/reflect a term context into an environment. [?]

## videos

[Type-Safe Observable Sharing in Haskell](https://vimeo.com/6679785)

https://skillsmatter.com/skillscasts/2872-haskell-for-embedded-domain-specific-languages

[Strongly Typed Domain Specific Embedded Languages](http://www.infoq.com/presentations/Strongly-Typed-DSEL-Lennart-Augustsson)

[Everything Old is New Again: Quoted Domain Specific Languages](https://www.youtube.com/watch?v=DlBwJ4rvz5c)

[Implementing Domain Specific Languages with LLVM](https://www.youtube.com/watch?v=1Hwnagof1Wo)

[Phil Freeman - Embedded DSLs in Haskell](https://www.youtube.com/watch?v=8DdyWgRYEeI)

[Building a language, in Haskell, with an LLVM backend](https://www.youtube.com/watch?v=I51TRpl1qic)

[Philip Wadler on Reynolds’s ‘Definitional Interpreters for Higher-Order Programming Languages’](https://skillsmatter.com/skillscasts/8261-papers-we-love-meetup)

[Creating an approachable Haskell-like DSL](http://cufp.org/2016/creating-an-approachable-haskell-like-dsl.html)

[Zeldspar - The Road to Epiphany](https://www.youtube.com/watch?v=GY5SxLkVyp4)

[07 The Highs and Lows of Opimising DSLs](https://www.youtube.com/watch?v=vewEILtqF7E)

[SMT for DSLs: a Tutorial](https://www.reddit.com/r/haskell/comments/6s1oce/cody_roux_smt_for_dsls_a_tutorial/)

[Traversing Syxtax Trees](https://twanvl.nl/blog/haskell/traversing-syntax-trees)

[Algebraic Design of DSLs](https://skillsmatter.com/skillscasts/10749-algebraic-design-of-dsls)

[Statically Typed Interpreters - λC 2017](https://www.youtube.com/watch?v=Ci2KF5hVuEs&list=PL7DZ7q3nEWhx5bgmpAgqArzrh0pL-tc3P&index=78) [assets](https://github.com/lambdaconf/lambdaconf-2017-assets)

[An EDSL for KDB/Q: Rationale, Techniques and Lessons Learned](https://skillsmatter.com/skillscasts/10770-an-edsl-for-kdb-q-rationale-techniques-and-lessons-learned)

[Ryan Newton - DSL Embedding in Haskell 1/2](https://www.youtube.com/watch?v=VIX4_XI3JAE)

[Ryan Newton - DSL Embedding in Haskell 2/2](https://www.youtube.com/watch?v=O6hDhrBRUYI)

[dsldiss-2015](https://www.youtube.com/channel/UCfrkueNadcqDv-YXFmn_CdA)

[ICFP 2014: Folding Domain-Specific Languages: Deep and Shallow Embeddings - Jeremy Gibbons](https://www.youtube.com/watch?v=xS7TJrrhYe8)

[UoY CS - Folding Domain-Specific Languages - Prof. Jeremy Gibbons](https://www.youtube.com/watch?v=crMTryrqkog)

[Stitch: The Sound Type-Indexed Type Checker](https://www.youtube.com/watch?v=XJ8hm3Tq2k8) [reddit](https://www.reddit.com/r/haskell/comments/8lkv6l/richard_eisenberg_speaks_on_dependent_types/)

[Chris Laffra - Little Languages](https://www.youtube.com/watch?v=G166wZyfR9M)

[Refunctionalization of Abstract Abstract Machines](https://www.youtube.com/watch?v=8IexRC-DrOs). [paper](https://dl.acm.org/citation.cfm?doid=3243631.3236800).\

[Direct Reflection for Free!](http://www.cs.princeton.edu/~ckorkut/papers/direct-nyplse.pdf).

[staged abstract interpreters](https://www.youtube.com/watch?v=3ZxbF4sLPxw&feature=youtu.be)

[the power of Kotlin DSLs](https://twitter.com/nicolas_frankel/status/1212027675457605640)

[writing a DSL in Lua](https://news.ycombinator.com/item?id=22223542)

[Lorentz: Implementing Smart Contract eDSL in Haskell(https://www.reddit.com/r/haskell/comments/f098r7/lorentz_implementing_smart_contract_edsl_in/)

[PaSe: An Extensible and Inspectable DSL for Micro-Animations](https://arxiv.org/abs/2002.02171)

[A DSL for fluorescence microscopy](https://twitter.com/Jose_A_Alonso/status/1227472519835373576)

[A Generic Abstract Syntax Model for Embedded Languages (slides)](https://pdfs.semanticscholar.org/bcd1/c773a1ba9869605954a74cfd71bbdc58523b.pdf)

[BinderAnn: Automated reification of source annotations for monadic EDSLs](https://twitter.com/Jose_A_Alonso/status/1227729275756990464)

[Haskell is a Great Host](https://skillsmatter.com/skillscasts/13780-keynote-gabriele-keller)

[Techniques for Implementation of Symbolically
Interpretable Haskell EDSLs](http://syrcose.ispras.ru/2020/submissions/SYRCoSE_2020_paper_09_81.pdf)

[strongly typed system F in ghc](https://twitter.com/Iceland_jack/status/1275051807442644994)

[On Adding Pattern Matching to Haskell-based Deeply Embedded Domain Specific Languages](https://www.youtube.com/watch?v=RaHdxf0UK0E). [reddit](https://www.reddit.com/r/haskell/comments/l5h9so/on_adding_pattern_matching_to_haskellbased_deeply/).

[Choosing is Losing: How to combine the benefits of shallow and deep embeddings through reflection](https://arxiv.org/abs/2105.10819). [tweet](https://twitter.com/jjcarett2/status/1399480878619897857).

[Your program is a language](https://twitter.com/LiquidSloshalot/status/1471522697507217419?t=iwGRJEwV7mIg232qUAKDyA&s=03)

[A DSL for finite types and enumeration in Agda](https://www.youtube.com/watch?v=sFyy9sssK50)

[ZuricHac 2022 DSL Workshop slides](https://twitter.com/trupill/status/1536385902209015811)

[Investigating the performance of the implementations of embedded languages in Haskell](https://twitter.com/Jose_A_Alonso/status/1550017816778121217)

## Software

[Data-reify for observable sharing](http://hackage.haskell.org/package/data-reify)

[hnix](https://github.com/jwiegley/hnix)

> hnix is essentially a catamorphic lambda calculus interpreter. Using a functor fixed point to encode expression trees yields some very useful flexibility.

[duet](https://github.com/duet-lang/duet) [reddit](https://pay.reddit.com/r/haskell/comments/8lt6au/github_duetlangduet_duet_language_main/)

[Embedded Pattern Matching](https://www.reddit.com/r/haskell/comments/phx4me/embedded_pattern_matching/)

> we are essentially hiding from the user that they are working on syntax trees representing the computation of values, rather than computing on values directly

[smalltt: Demo for high-performance type theory elaboration](https://www.reddit.com/r/haskell/comments/rheykz/github_andraskovacssmalltt_demo_for/)

[There are good reasons for building domain-specific programming languages by *deep* embedding](https://twitter.com/PTOOP/status/1557787709875228672?t=aiHKYiQCqALZbxCXbeI-NA&s=03)

> In my experience, in the end it always turns out that you need to go deep. 

> I *instinctively* go deep. It’s the lesson my father taught me. Getting away with shallow is transient. If you go deep, you can look around the corner at what *else* is possible.

[musings on DSL languages](https://www.reddit.com/r/haskell/comments/12loreg/crem_compositional_representable_executable/)

[Java DSL trick: static methods within lambdas](https://javalin.io/blog/static-methods-within-lambdas). [example DSL](https://twitter.com/helpermethod/status/1656546416871759873).

[convert linear subset of the haskell to any DSL that is also a symmetric monoidal category](https://www.reddit.com/r/haskell/comments/13mit4v/code_generation_with_haskell_itself_as_the_dsl/)

[Building Search DSLs with Django](https://danlamanna.com/posts/building-search-dsls-with-django/)

[siren song](https://www.reddit.com/r/haskell/comments/1b33c1d/the_siren_song_of_domainspecific_languages/)

[Which Interpreters are Faster, AST or Bytecode?](https://stefan-marr.de/2023/10/ast-vs-bytecode-interpreters/). [hn](https://news.ycombinator.com/item?id=37951343).

[Simple and compositional reification of monadic embedded languages](https://dl.acm.org/doi/10.1145/2544174.2500611)

[YulCat is a symmetric monoidal category (SMC), using linear-smc package 1, one can convert between linear functions and YuLCat:](https://discourse.haskell.org/t/ann-yolc-a-haskell-powered-safe-expressive-fun-language-for-ethereum/11145)

[Shallowly Embedded Functions](https://trendsfp.github.io/abstracts/paper-007.pdf). [Functional programs: conversions between deep and shallow embeddings](https://www.cl.cam.ac.uk/~mom22/itp12-embeddings.pdf)

[hell](https://github.com/chrisdone/hell). [a tour of Hell](https://chrisdone.com/posts/tour-of-hell/)

[resources on normalization by evaluation (NbE)](https://www.reddit.com/r/haskell/comments/1lnfbmd/a_collection_of_resources_about/)



