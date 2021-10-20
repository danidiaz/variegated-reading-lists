# Finally tagless style

## papers

[Finally tagless, partially evaluated](http://okmij.org/ftp/tagless-final/JFP.pdf)

[Finally, Safely-extensible and Efficient Language-integrated Query](http://logic.cs.tsukuba.ac.jp/~kam/paper/pepm2016a.pdf)

[De Bruijn-index, finally tagless](http://okmij.org/ftp/tagless-final/course/PE-dB.html)

> What makes partial evaluation of De Bruijn-indexed terms P repr h a so difficult is that their type includes the environment h with the types of the free variables that may occur in the term. The two key operations of partial evaluation, substitution for free variables and weakening, do change the environment h. (The type a of the embedded expression of course stays the same.) Furthermore, these operations have to adjust the De Bruijn indices in a complex way. 

[Effects Without Monads: Non-determinism -- Back to the Meta Language](https://arxiv.org/abs/1905.06544)

## posts

[Reducing boilerplate in finally tagless style](https://www.reddit.com/r/haskell/comments/4416gn/reducing_boilerplate_in_finally_tagless_style/)

[Typed Tagless Interpretations and Typed Compilation](http://okmij.org/ftp/tagless-final/)

[From object algebras to finally tagless interpreters](https://oleksandrmanzyuk.wordpress.com/2014/06/18/from-object-algebras-to-finally-tagless-interpreters-2/)

[Writing search DSL in Haskell](https://www.youtube.com/watch?v=JxC1ExlLjgw)

[Tagless Staged Interpreters for Simpler Typed Languages](http://lambda-the-ultimate.org/node/2438)

Typing dynamic typing [1](http://www.haskell.org/pipermail/haskell-cafe/2006-October/019160.html) [2](http://www.haskell.org/pipermail/haskell-cafe/2006-October/019161.html) [3](http://www.haskell.org/pipermail/haskell-cafe/2006-November/019193.htm)

[Mutual Recursion in Final Encoding](http://aherrmann.github.io/programming/2016/05/28/mutual-recursion-in-final-encoding/).

[A very simple technique for making DSLs extensible](http://pchiusano.github.io/2014-06-12/extensible-dsls.html)

[Simple lambda calculus DSL using GADTs in OCaml](https://stackoverflow.com/questions/22676975/simple-lambda-calculus-dsl-using-gadts-in-ocaml)

[Optimizing Tagless Final](https://lukajcb.github.io/blog/functional/2018/01/03/optimizing-tagless-final.html)

[the architecture of beam](https://www.reddit.com/r/haskell/comments/9tlcw8/joining_sql_tables_in_haskell/)

> Beam uses a finally tagless style which abstracts away the AST representation. The AST in the core module is used for testing. That’s it. The individual backends co opt the typeclasses in the core module to provide a custom representation. 

[Introduction to Tagless Final](https://serokell.io/blog/2018/12/07/tagless-final). Great article! [reddit](https://www.reddit.com/r/haskell/comments/a40z4t/blog_introduction_to_tagless_final/).

[Dino](https://www.reddit.com/r/haskell/comments/bbkh6o/dino_a_convenient_tagless_edsl/)

[tagless with discipline](https://medium.com/iterators/tagless-with-discipline-testing-scala-code-the-right-way-e74993a0d9b1)

[Final tagless encodings have little to do with typeclasses](https://www.reddit.com/r/haskell/comments/nmj8hz/final_tagless_encodings_have_little_to_do_with/). [more](https://twitter.com/trupill/status/1398167586056118274).

[Initial and final encodings of free monads](https://blog.poisson.chat/posts/2021-10-20-initial-final-free-monad.html)

## slides

[Haskell for EDSLs](http://www.andres-loeh.de/HaskellForDSLs.pdf)

[pragmatic object oriented tagless final](http://w.pitula.me/presentations/2019-07-lxscala/#/)

## videos

[Finally Tagless DSLs and MTL](https://www.youtube.com/watch?v=JxC1ExlLjgw)

[The Death of Final Tagless](https://skillsmatter.com/skillscasts/13247-scala-matters). [Beautiful, Simple, Testable Functional Effects for Scala](http://degoes.net/articles/zio-environment). [tweet](https://twitter.com/jdegoes/status/1100499303087423488). [zio thread](https://giuliohome.wordpress.com/2019/02/27/tagless-final-architecture/). [Interview](https://scala.love/effectful-episode-with-john-de-goes/). [more zio](https://twitter.com/jdegoes/status/1101205364014542850). [final tagless seen alive](https://blog.softwaremill.com/final-tagless-seen-alive-79a8d884691d). [not dead yet](https://www.reddit.com/r/hascalator/comments/ayhz79/finally_tagless_not_quite_dead_yet/). [tweet](https://twitter.com/Odomontois/status/1101082500347166720). [tweet](https://twitter.com/Odomontois/status/1100626349327335425). [stuff](https://twitter.com/jdegoes/status/1104309396941799425). [laws](https://twitter.com/MxLambda/status/1106073953129373697).

