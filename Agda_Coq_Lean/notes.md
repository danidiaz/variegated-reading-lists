[HISTORY OF INTERACTIVE THEOREM PROVING](http://www.cl.cam.ac.uk/~jrh13/papers/joerg.pdf)

[Data Structures and Functional Programming](http://www.cs.cornell.edu/courses/cs3110/2017fa/)

[Proof general](https://proofgeneral.github.io/) [documentation](http://proofgeneral.inf.ed.ac.uk/htmlshow.php?title=Proof+General+user+manual&file=releases%2FProofGeneral%2Fdoc%2FProofGeneral%2FProofGeneral_2.html#Features-of-Proof-General)

> Without using electric terminator, you can trigger processing the text up to the current position of the point with the key C-c C-RET, or just up to the next command with C-c C-n. We show the rest of the example in Isabelle with semi-colons, but these will not appear in the final text.

> A proof script is a sequence of commands which constructs definitions, declarations, theories, and proofs in a proof assistant. Proof General is designed to work with text-based interactive proof assistants, *where the mode of working is usually a dialogue between the human and the proof assistant*.

[Data Types as Inductively Defined Mathematical Collections](https://coq.inria.fr/tutorial/2-induction)

[CIC, Gallina, Ltac, Vernacular](http://adam.chlipala.net/cpdt/html/Cpdt.StackMachine.html)

    Coq is actually based on an extension of CIC called Gallina. The text after the
    := and before the period in the last code example is a term of Gallina. Gallina
    includes several useful features that must be considered as extensions to CIC.
    The important metatheorems about CIC have not been extended to the full breadth
    of the features that go beyond the formalized language, but most Coq users do
    not seem to lose much sleep over this omission.  Next, there is Ltac, Coq's
    domain-specific language for writing proofs and decision procedures. We will
    see some basic examples of Ltac later in this chapter, and much of this book is
    devoted to more involved Ltac examples.  Finally, commands like Inductive and
    Definition are part of the Vernacular, which includes all sorts of useful
    queries and requests to the Coq system. Every Coq source file is a series of
    vernacular commands, where many command forms take arguments that are Gallina
    or Ltac programs. (Actually, Coq source files are more like trees of vernacular
    commands, thanks to various nested scoping constructs.)

[Vernacular grammar](http://web.mit.edu/cpitcla/www/coq-rst/gallina-specification-language.html#the-vernacular)

[more on induction principles](http://www.cs.cornell.edu/~clarkson/courses/csci6907/2014sp/terse/MoreInd.html)

[mutual induction](https://github.com/coq/coq/wiki/Mutual-Induction) [more](http://article.gmane.org/gmane.science.mathematics.logic.coq.club/1695)

[tactics index](https://coq.inria.fr/refman/tactic-index.html)

[Coq standard library](https://coq.inria.fr/distrib/current/stdlib/)

[Coq.Init.Prelude](https://coq.inria.fr/library/Coq.Init.Prelude.html)

[Why does Coq have Prop?](https://cstheory.stackexchange.com/questions/21836/why-does-coq-have-prop)

> Prop  is very useful for program extraction because it allows us to delete parts of code that are useless.

> But there are genuine design decisions one has to make when using Prop. 

> it is a design question which things to put in Prop. You need to know what the user wants, and he tells you what he wants by using Prop.

[Coq : Back To Basics](http://www.alpheccar.org/content/71.html)

> In Coq, we have two sorts : Set and Prop. A type of sort Set is a specification and a proof of a specification is a program. A type of sort Prop is a proposition.

> Why do we need a sort Prop ? With Set, we already have the proof-as-program correspondence and the type-as-proposition.

> From an algorithmic point of view, tactics can be dangerous since you have no control on the algorithm which is generated. This kind of type driven development is better for proofs.

> the Omega library used for inequalities 

[Prop_or_Set](https://github.com/coq/coq/wiki/Prop_or_Set)

> If your type could have two or more distiguishable objects, put it in Set otherwise put it in Prop. 

[Coq: Prop versus Set in Type(n)](https://stackoverflow.com/questions/29322534/coq-prop-versus-set-in-typen)

[What is different between Set and Type in Coq? [closed]](https://cs.stackexchange.com/questions/80729/what-is-different-between-set-and-type-in-coq)

[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)

[Inside Coq’s Type System 1](https://www.labri.fr/perso/casteran/CoqArt/Tsinghua/C5.pdf)

[My unusual hobby](https://www.stephanboyer.com/post/134/my-unusual-hobby)

[COQ LTAC 101](http://lthms.xyz/blog/coq-ltac-101)

[Company-coq](https://github.com/cpitclaudel/company-coq)

> A collection of extensions for Proof General's Coq mode.

[Intermediate Coq: "Programming In The Large" Roadmap](https://www.reddit.com/r/Coq/comments/7fpuut/intermediate_coq_programming_in_the_large_roadmap/)

    Between Software Foundations and Adam Chlipala's books, there is an enormous amount of excellent introductory material for "programming in the small" in Coq. On the other hand, whenever I try to write a Coq project of non-trivial size, I run into all sorts of issues. They include:

    When should I use modules vs. typeclasses?
    Is using setoids everywhere instead of eq overkill?
    When should I use reflection?
    When should I use refine?
    When should I use Program (Russell)?
    What options should I set? Implicit Arguments seems to be consensus, are there others?
    What set of libraries should I default to?
    ...and, while I'm at it, here are some "coding in the small" things I can't figure out:

    How do I make coinduction non-painful?
    How do I use hints properly?
    Any insight is greatly appreciated.

    How do I make coinduction non-painful?
    
[Paco: A Coq Library for Parameterized Coinduction](https://plv.mpi-sws.org/paco/)

    Have you tried the Paco approach? You don't have to go full Mendler style (co)-recursion, actually using open co-inductive types and the corresponding co-induction principle are already fairly useful.

    Also, don't use co-inductive types defined as inductive ones. They're fundamentally broken, you should rely on primitive records when doing coinduction (up to the fact they're currently still somewhat buggy, but this is not a foundational issue).

[Approximating Inductive Types in Coq](https://gmalecha.github.io/reflections/2016/approximating-inductive-types)

[Is Agda without K less powerful?](https://stackoverflow.com/questions/39264130/is-agda-without-k-less-powerful/39266672#39266672)

> The situation with Martin-Löf type theory and Axiom K is in some ways analogous to Euclidean geometry and the parallel postulate. With the parallel postulate more theorems can be proven, but those are only about Euclidean spaces. Without the parallel postulate provable theorems are true of non-Euclidean spaces too, and one has the freedom to add explicitly non-Euclidean axioms.

> Axiom K seems intuitive, since we defined Agda's propositional equality with a single refl constructor. Why even bother with the mysterious non-refl equality proofs whose existence we can't disprove without K?

[Can I extract a Coq proof as a Haskell function?](https://stackoverflow.com/questions/13334863/can-i-extract-a-coq-proof-as-a-haskell-function)

> Thanks to Prof. Pierce's summer 2012 video 4.1 as Dan Feltey suggested, we see that the key is that the theorem to be extracted must provide a member of Type rather than the usual kind of propositions, which is Prop.

[The Logic of Coq](https://github.com/coq/coq/wiki/The-Logic-of-Coq)

[Proof irrelevance / Axiom K](https://github.com/coq/coq/wiki/CoqAndAxioms)

[What is Axiom K?](https://stackoverflow.com/questions/39239363/what-is-axiom-k/39256457)

> When investigating the identity type in his thesis, Thomas Streicher introduced a new eliminator for the identity type which he called K (as the next letter in the alphabet after J, the standard eliminator for the identity type). It states that any proof p of an equality of the form x = x is itself equal to the trivial proof refl. From this, it follows that any two proofs p and q of any equation x = y are equal, hence the alternative name "uniqueness of identity proofs". What's remarkable is that he proved that this does not follow from the standard rules of type theory. I recommend reading Dan Licata's article on the homotopy type theory blog if you want to understand why not, he explains it much better than I could.

> Conor McBride showed in his thesis ("Dependently typed functional programs and their proofs (2000)") that K is the only thing that dependent pattern matching really adds to dependent type theory.

[Just Kidding: Understanding Identity Elimination in Homotopy Type Theory](https://homotopytypetheory.org/2011/04/10/just-kidding-understanding-identity-elimination-in-homotopy-type-theory/)

> Several current proof assistants, such as Agda and Epigram, provide uniqueness of identity proofs (UIP): any two proofs of the same propositional equality are themselves propositionally equal.

> On the other hand, Coq does not provide uniqueness of identity proofs (but nor does it allow you to define higher-dimensional types that contract it, except by adding axioms).

> Here’s where things get confusing: UIP is not a consequence of J, as shown by the first higher-dimensional interpretation of type theory, Hofmann and Streicher’s groupoid interpretation. This gives a model of type theory that validates J, but in which UIP does not hold. UIP can be added as an extra axiom, such as Streicher’s K:

[Axiom K at ncatlab](https://ncatlab.org/nlab/show/axiom+K)

> Propositionally extensional type theory has some of the attributes of intensional type theory, and many type theorists use “extensional type theory” to refer only to the definitional version.

> In type theory, the axiom K is an axiom that when added to intensional type theory turns it into extensional type theory — or more precisely, what is called here “propositionally extensional type theory”.

> We can add as an axiom the “uniqueness of identity proofs” (axiom UIP) property that any two inhabitants of the same identity type IdA(x,y) Id_A(x,y) are themselves equal (in the corresponding higher identity type).

> An alternative to adding this axiom is to allow the kind of dependent pattern matching present in Agda and Epigram, which allow you to define K.

[The Coq FAQ](https://github.com/coq/coq/wiki/The-Coq-FAQ) [talking with the rooster](https://github.com/coq/coq/wiki/Talkin'-with-the-Rooster)

[Learning set theory through Coq (part 1)](http://coqmath.blogspot.com.es/2015/01/learning-set-theory-through-coq-part-1.html)

[GADTs vs Inductive Datatypes](https://www.cs.purdue.edu/sss/projects/tycon/2014/04/09/Coq-Basics.html)

> Notice that it looks quite similar to Haskell definition, with type variables explicated. An empty list in explicitly typed haskell is VNil Int, whereas in Coq, it is vnil int. However, unlike Haskell, where there is term-type-kind hierarcy, Coq has full dependent types with infinite hierarchy of universes. One consequence of this is that we will frequently see arrows mapping members of one universe to members of a different universe.

[Require, Import, Require Import](https://stackoverflow.com/questions/47973317/require-import-require-import)

[Vernacular Commands Index](https://coq.inria.fr/refman/command-index.html) [Variable](https://coq.inria.fr/refman/gallina.html#hevea_command5)

[What is the difference between “definition” and “inductive” in Coq?](https://cs.stackexchange.com/questions/12047/what-is-the-difference-between-definition-and-inductive-in-coq)

> Fixpoint is similar to Definition, but allows a recursive definition (like let rec in ML). It's in fact syntactic sugar for Definition plus the explicit fixpoint combinator fix, but definitions made using Fixpoint are easier to read and write.

[In Coq, what does it mean to have an inductive type where the right-hand side of “:” is Prop?](https://cs.stackexchange.com/questions/81657/in-coq-what-does-it-mean-to-have-an-inductive-type-where-the-right-hand-side-of?rq=1)

> Every time you prove something, Coq builds the proof object and verifies that it's well-formed. It's rare to write down constructions in Prop, you'd usually let a tactic do it for you, but the objects always exist under the hood. (End a proof with Defined. instead of Qed. and run Print mytheorem to see the proof object for mytheorem. It can get big, but it's sometimes instructive to look at that for small proofs.)

[How to define set in coq without defining set as a list of elements](https://stackoverflow.com/questions/36588263/how-to-define-set-in-coq-without-defining-set-as-a-list-of-elements)

> The are basically four possible choices to be made when defining sets in Coq depending on your constraints on the base type of the set and computation needs

[How to define finite set of N elements in Coq?](https://stackoverflow.com/questions/42871971/how-to-define-finite-set-of-n-elements-in-coq/42872889#42872889)

[Does ssreflect assume excluded middle?](https://stackoverflow.com/questions/34520944/does-ssreflect-assume-excluded-middle/35051026#35051026)

> In standard Coq, le is encoded as an inductive type, whereas in ssreflect it's a computational function leq: nat -> nat -> bool.

> Using the leq function for proofs is more "efficient" for the following reason: imagine you want to prove that 102 < 203. Using the standard Coq definition, you will have to build a large proof term, you must explicitly encode every step of the proof.

> ssreflect is only concerned with decidable types: types where equality can be decided, ... This means that for any two elements of the type T, you can get a constructive (in Set, not in Prop like the excluded middle) proof that they are either equal or different.

[Ordered seq in Coq/SSreflect](https://stackoverflow.com/questions/44731224/ordered-seq-in-coq-ssreflect?rq=1)

[What is the difference between “Qed” and “Defined”?](https://stackoverflow.com/questions/25478682/what-is-the-difference-between-qed-and-defined)

> There is some concept of "opacity" which Qed enforces but Defined does not.

[How is Coq's parser implemented?](https://stackoverflow.com/questions/43184660/how-is-coqs-parser-implemented)

> this notation system is very powerful and it was probably one of the reasons of Coq's success. In practice, this is a source of much complication in the source code.

[v8.7.1](https://github.com/coq/coq/blob/V8.7.1/CHANGES)

    New tactics: Variants of tactics supporting existential variables eassert,
    eenough, etc. by Hugo Herbelin; Tactics extensionality in H and
    inversion_sigma by Jason Gross; specialize with accepting partial bindings
    by Pierre Courtieu.
    
    Cumulative Polymorphic Inductive Types, allowing
    cumulativity of universes to go through applied inductive types, by Amin
    Timany and Matthieu Sozeau.
    
    The SSReflect plugin by Georges Gonthier,
    Assia Mahboubi and Enrico Tassi was integrated (with its documentation in
    the reference manual) by Maxime Dénès, Assia Mahboubi and Enrico Tassi.

[Programs as Proofs](http://ilyasergey.net/pnp/pnp.pdf)

[Types classes in Coq](https://www.irif.fr/~sozeau/research/coq/classes.en.html) [Class vernacular](https://coq.inria.fr/refman/type-classes.html)

[What's the difference between ADTs, GADTs, and inductive types?](https://cstheory.stackexchange.com/questions/10594/whats-the-difference-between-adts-gadts-and-inductive-types)

[Haskell for Coq programmers](http://blog.ezyang.com/2014/03/haskell-for-coq-programmers/)

[A Tutorial on [Co-]Inductive Types in Coq](https://coq.inria.fr/distrib/current/files/RecTutorial.pdf)

[COQ documentation](https://coq.inria.fr/refman/index.html)

[Why haven't newer dependently typed languages adopted SSReflect's approach?](https://stackoverflow.com/questions/49477427/why-havent-newer-dependently-typed-languages-adopted-ssreflects-approach)

> Firstly, where possible predicates are expressed as boolean-returning functions rather than inductively defined datatypes.

> Secondly, datatypes with invariants are defined as dependent records containing a simple datatype plus a proof of the invariant

> A common anti-pattern in dependently-typed languages and Coq in particular is to encode such algebraic properties into the definitions of the datatypes and functions themselves (a canonical example of such approach are length-indexed lists). While this approach looks appealing, as it demonstrates the power of dependent types to capture certain properties of datatypes and functions on them, it is inherently non-scalable, as there will be always another property of interest, which has not been foreseen by a designer of the datatype/function, so it will have to be encoded as an external fact anyway. This is why we advocate the approach, in which datatypes and functions are defined as close to the way they would be defined by a programmer as possible, and all necessary properties of them are proved separately.

[How do we overcome the compile time and runtime gap when programming in a Dependently Typed Language?](https://stackoverflow.com/questions/48128884/how-do-we-overcome-the-compile-time-and-runtime-gap-when-programming-in-a-depend)

> we can still reason symbolically on the unknowns  n,m and argue that vn ++ vm has that type, involving n+m, even if we do not yet know what n+m actually is.

[Keeping information when using induction?](https://stackoverflow.com/questions/4519692/keeping-information-when-using-induction)

>  There is a general trick, which is to selectively rewrite the structured parameter to a variable, keeping the equality in the environment.

[What does V stand for in the Coq file extension?](https://stackoverflow.com/questions/7963528/what-does-v-stand-for-in-the-coq-file-extension)

[Coq in a hurry](https://cel.archives-ouvertes.fr/file/index/docid/459139/filename/coq-hurry.pdf)

[On representations of permutations](https://stackoverflow.com/questions/17430023/on-representations-of-permutations)

[A Short Course on Interactive Proofs in Coq/Ssreflect.](https://github.com/ilyasergey/pnp)

[Finding bugs in Haskell code by proving it](https://www.joachim-breitner.de/blog/734-Finding_bugs_in_Haskell_code_by_proving_it)

[Formal Reasoning in Coq — a Beginner's Guide](https://raywang.tech/2017/09/25/formal-reasoning-in-coq/)

[Naive Coq](https://github.com/readablesystems/cs260r-17/blob/master/naivecoq.md)

[Tricks you wish the Coq manual told you](https://github.com/tchajed/coq-tricks)

[POPL 2016: Programs and Proofs in the Coq Proof Assistant](http://www.cis.upenn.edu/~rrand/popl_2016/)

[Some questions about binary number representations (ZArith)](https://www.reddit.com/r/dependent_types/comments/9g50eq/some_questions_about_binary_number/)

[Bishop's work on type theory](https://groups.google.com/forum/#!topic/homotopytypetheory/WhMsxFlek5I) [reddit](https://www.reddit.com/r/dependent_types/comments/8h2zx2/on_bishops_invention_of_type_theory/)

# Papers

[Generating Good Generators for Inductive Relations](https://www.cis.upenn.edu/~llamp/pdf/GeneratingGoodGenerators.pdf)

[Total Haskell is reasonable Coq](https://arxiv.org/pdf/1711.09286.pdf)

[One Monad to Prove Them All](https://arxiv.org/pdf/1805.08059.pdf)

> We follow her on her journey when she learns about concepts like free monads
and containers as well as basics and restrictions of proof assistants like Coq. These concepts are well-known
individually, but their interplay gives rise to a solution for Mona’s problem that has not been presented before

[Verifying Monoidal String Matching in Liquid Haskell and Coq](https://arxiv.org/pdf/1711.09286.pdf)

[a ssreflect tutorial](https://hal.inria.fr/inria-00407778/document)

[Reification by Parametricity Fast Setup for Proof by Reflection, in Two Lines of Ltac](https://people.csail.mit.edu/jgross/personal-website/papers/2018-reification-by-parametricity-itp-draft.pdf)

[Functional Pearl: Theorem Proving for All](http://www.cs.nott.ac.uk/~pszgmh/tpfa.pdf)

[Mtac2: Typed Tactics for Backward Reasoning in Coq](https://icfp18.sigplan.org/event/icfp-2018-papers-mtac2-typed-tactics-for-backward-reasoning-in-coq)

[Demostración asistida por ordenador](https://twitter.com/Jose_A_Alonso/status/1025755820653518848)

[POPL 2016](http://www.cis.upenn.edu/~rrand/popl_2016/)

[Towards Mac Lane’s Comparison Theorem for the (co)Kleisli Construction in Coq](https://www.cicm-conference.org/2018/infproc/paper11.pdf)

[certified algorithms for program slicing](https://tel.archives-ouvertes.fr/tel-01874620/document)

[C-path monad](https://twitter.com/_sofia_af/status/1083088976813150213)

# Slides

[TheMathematical Components library principles and design choices](http://ssr.msr-inria.inria.fr/doc/tutorial-itp13/slides.pdf)

[INF551 - Computational Logic: Artificial Intelligence in Mathematical Reasoning](http://www.enseignement.polytechnique.fr/informatique/INF551/) [The theory of sets](http://www.enseignement.polytechnique.fr/informatique/INF551/lecture6.pdf)



# Videos

[How to use Coq with Proof General](https://www.youtube.com/watch?v=l6zqLJQCnzo)

[How to use CoqIDE](https://www.youtube.com/watch?v=7sk8hPWAMSw)

[Leibniz Equality implies Coq's Equality](https://www.youtube.com/watch?v=1E8-LQ4l1HQ)

[A first proof with Coq (Frobenius rule)](https://www.youtube.com/watch?v=z861PoZPGqk)

at [here](https://youtu.be/z861PoZPGqk?t=122):

> we submit this to Coq (C-c C-n)

[Introductory Proof: Commutativity of Addition in Coq](https://www.youtube.com/watch?v=OaIn7g8BAIc)

[Introduction to Coq by Kimball Germane](https://www.youtube.com/watch?v=ngM2N98ppQE)

[Software foundations in Coq 0.1 - Benjamin Pierce](https://www.youtube.com/watch?v=KKrD4JcfW90) [full list](https://www.cs.uoregon.edu/research/summerschool/summer12/curriculum.html)

[quote from here](https://youtu.be/KKrD4JcfW90?t=1073)

> the tactics language is a programming language in which you are imperatively manipulating a lambda term

> you propose a theorem and then go into a different mode

[Introduction to the Coq Proof Assistant - Andrew Appel](https://www.youtube.com/watch?v=3WBUHEVr56c)

[The dual Frobenius rule, part 2](https://www.youtube.com/watch?v=XCsUZhx9OHg)

At [here](https://youtu.be/XCsUZhx9OHg?t=481)

> implication is just a special case of forall.

Maybe that's why `intro` works for both?

[Coming Soon: Machine-Checked Mathematical Proofs in Everyday Software and Hardware Development](https://media.ccc.de/v/34c3-9105-coming_soon_machine-checked_mathematical_proofs_in_everyday_software_and_hardware_development)

[Functional Geekery Episode 101 – Adam Chlipala](https://www.functionalgeekery.com/episode-101-adam-chlipala/)

[awesome Coq](https://github.com/coq-community/awesome-coq#readme)

## Code

[Ensemble facts](https://github.com/antalsz/hs-to-coq/blob/8f84d61093b7be36190142c795d6cd4496ef5aed/examples/intervals/Ensemble_facts.v)

[Insertion sort](http://www.enseignement.polytechnique.fr/informatique/INF551/TD/TD5/aux/Insert_Sort.v)

[Mathematical Components](https://math-comp.github.io/math-comp/)

[hs-to-coq](https://github.com/antalsz/hs-to-coq/blob/8f84d61093b7be36190142c795d6cd4496ef5aed/examples/intervals/Proofs.v)

[state as comonad](http://lpaste.net/361413) [reddit](https://www.reddit.com/r/haskell/comments/7ojy6x/the_comonadreader_the_state_comonad/dsa51hh/)

[parity nat list](https://cstheory.stackexchange.com/a/10604/13730)

[Cours du Coq](https://t.co/YWt1vqUhgF).

[Discrete math in Coq](http://www.cs.pomona.edu/~michael/courses/csci054s18/book/)

[advent of coq 2018](https://github.com/Lysxia/advent-of-coq-2018)

[safety in programming languages](https://www2.ccs.neu.edu/racket/pubs/tr99-352.pdf). [Size-Change Termination as a Contract](https://arxiv.org/abs/1808.02101). [termination tweet](https://twitter.com/ShriramKMurthi/status/1136630749711519746)

[Proving tree algorithms for succinct data structures](https://www.xuanruiqi.com/assets/succinct.pdf)

[jscoq](https://news.ycombinator.com/item?id=20212266)

[An Introduction to Programming and Proving with Dependent Types in Coq](http://adam.chlipala.net/papers/CpdtJFR/CpdtJFR.pdf)

[sqrt(2) is irrational](https://www.youtube.com/watch?v=bTLc_9buWLQ)

[Survery of category theory in Coq](https://coq.discourse.group/t/survey-of-category-theory-in-coq/371)

[Equations Reloaded (also: ChunkableMonoid)](http://delivery.acm.org/10.1145/3350000/3341690/icfp19main-p204-p.pdf)

[Learn Coq in Y](https://twitter.com/SandMouth/status/1190290926603620352)

[Programming with dependent types in Coq: inductive families and dependent patter-matching.](https://twitter.com/Jose_A_Alonso/status/1221155592808599554)

[the nature of tactics](https://twitter.com/jjcarett2/status/1351367688711532544)