[Abstracting definitional interpreters](https://arxiv.org/pdf/1707.04755.pdf)

> First, the interpreter is written in an open recursive style; the evaluator
does not call itself recursively, instead it takes as an argument a function
ev—shadowing the name of the function ev being defined—and ev (the argument) is
called instead of self-recursion. This is a standard encoding for recursive
functions in a setting without recursive binding. It is up to an external
function, such as the Y-combinator, to close the recursive loop. This open
recursive form is crucial because it allows intercepting recursive calls to
perform “deep” instrumentation of the interpreter

[Program reduction: a win for recursion schemes](http://www.well-typed.com/blog/2018/03/oop-in-haskell/) [reddit](https://www.reddit.com/r/haskell/comments/82wf06/new_blog_post_object_oriented_programming_in/)

[Backpack for initial and final encodings](https://qfpl.io/posts/backpack-for-initial-and-final-encodings/)

> We’re going to use open recursion and a dash of laziness to write our evaluator.

[Explicit memoization can be elegant; a response to "DP in Haskell"](https://www.reddit.com/r/haskell/comments/8hrbr5/explicit_memoization_can_be_elegant_a_response_to/)

[compositional zooming](http://www.well-typed.com/blog/2018/09/compositional-zooming/). [reddit](https://www.reddit.com/r/haskell/comments/9cvtc0/new_blog_post_compositional_zooming_for_statet/).

[Packrats Parse in Packs](https://github.com/gasche/icfp2017-papers)

> We present a novel but remarkably simple formulation of formal language grammars in Haskell as functions mapping a record of production parsers to itself

[Hyperfunctions](https://doisinkidney.com/posts/2021-03-14-hyperfunctions.html). [hypertypes](https://github.com/lamdu/hypertypes). [hyperfunctions as games](https://www.reddit.com/r/haskell/comments/m5lb97/hyperfunctions/gr5e8ip/). [tweet](https://twitter.com/riz0id/status/1414475358766837761). [Algebras for Weighted Search](https://doisinkidney.com/pdfs/algebras-for-weighted-search.pdf). [Hyperfunctions have sort of stacklike behavior](https://www.reddit.com/r/haskell/comments/oj5br4/any_good_uses_for_logict_extended_with_shift_and/h50qd8l).

> On the other hand, BFS player 1's behavior looks extremely complex, and involves dreaming up some entirely new hypothetical other player, and thinking about what that other player would have done, as well.

[an answer of mine on SO](https://stackoverflow.com/questions/67782579/easiest-way-to-debug-visualize-recursive-function-calls-in-haskell/67787958#67787958)

[Getting To The (Fixed) Point](https://rebeccaskinner.net/posts/2021-06-09-getting-to-the-fixed-point.html)

[Memoizing fixpoint operator](https://wiki.haskell.org/Memoization#Memoizing_fix_point_operator). 

[Functional Pearl: The Decorator Pattern in Haskell](http://web.cecs.pdx.edu/~ntc2/haskell-decorator-paper.pdf)

> An arity-generic decorator needs to solve two problems: intercept recursive calls and handle functions of any arity uniformly

> a well-typed call-tracing decorator

[loop-unrolling pass using futumorphisms ](https://twitter.com/luctielen/status/1432217874781855747)

[tangle: Heterogenous memoisation monad](https://www.reddit.com/r/haskell/comments/qpebqx/tangle_heterogenous_memoisation_monad/). [Löb and möb: strange loops in Haskell](https://www.reddit.com/r/haskell/comments/qq7tki/l%C3%B6b_and_m%C3%B6b_strange_loops_in_haskell/).

> loeb relies on recursion and laziness, which is neat but doesn't work well with effects and strict data structures. Hence I decided to implement memoisation explicitly using lenses.

[Applying File Changes with `fix` and GADTs](https://www.reddit.com/r/haskell/comments/qsexqr/applying_file_changes_with_fix_and_gadts/)

[Memoization](https://wiki.haskell.org/Memoization). [SO](https://stackoverflow.com/questions/141650/how-do-you-make-a-generic-memoize-function-in-haskell). [Representable-tries vs. Memo-trie](https://www.reddit.com/r/haskell/comments/si8tv7/representabletries_vs_memotrie/).

[Monadic Memoization Mixins](https://www.cs.utexas.edu/~wcook/Drafts/2006/MemoMixins.pdf). [monad-memo: Memoization monad transformer](https://hackage.haskell.org/package/monad-memo).

[simulate mutual recursion with Higher-Order Functions + fix combinator](https://twitter.com/ChShersh/status/1492812492757778435)

[Lenses for Tree Traversals Redux](https://www.reddit.com/r/haskell/comments/vaurfc/lenses_for_tree_traversals_redux/)

[quines and metaprogramming](https://www.youtube.com/watch?v=Rnji4rZT51s&list=PLxxF72uPfQVRQXih84omWRmacz1lwejc6&index=6). [links](https://www.reddit.com/r/haskell/comments/xzo8ge/comment/irs91j6/).

[catamorphisms are optics with a trivial backward pass.](catamorphisms are optics with a trivial backward pass.)

> the residual

[Haskell can have a little Inheritance as a Treat](https://tarmean.github.io/OpenRec)


