[Reimplementing graphmod as a source plugin: graphmod-plugin](http://mpickering.github.io//posts/2018-08-09-source-plugin-graphmod.html) [reddit](https://www.reddit.com/r/haskell/comments/95r8uj/reimplementing_graphmod_as_a_source_plugin/)

[Specifying how a plugin affects recompilation](http://mpickering.github.io/posts/2018-08-10-plugins-recompilation.html) [reddit](https://www.reddit.com/r/haskell/comments/967o6k/specifying_how_a_plugin_affects_recompilation/)

[GHCi in GHCi](https://mgsloan.com/posts/ghcinception/) [reddit](https://www.reddit.com/r/haskell/comments/92szf7/ghc_inside_ghci/)

[Building GHC: The Stages](https://medium.com/@zw3rk/building-ghc-the-stages-2c6cf6fc4b29)

[Comprehensive overview of using the Build System](https://ghc.haskell.org/trac/ghc/wiki/Building/Using)

[hlint as a source plugin](https://github.com/ocharles/hlint-source-plugin) [reddit](https://www.reddit.com/r/haskell/comments/96f97x/hlint_as_a_ghc_source_plugin_proof_of_concept/)

[GHC Hacking Newcomer Guide](https://www.youtube.com/watch?v=s9DkByHSdOg).

[an index of different resources about GHC plugins](http://mpickering.github.io/plugins.html)

[The Thoralf plugin: for your fancy type needs](https://dl.acm.org/citation.cfm?id=3242754)

[write your own GHC typechecker plugins](https://skillsmatter.com/skillscasts/12388-write-your-own-ghc-type-checker-plugins).

[GHC API Improvement Status](https://ghc.haskell.org/trac/ghc/wiki/GhcApiStatus)

[Type Theory Behind Glasgow Haskell Compiler Internals](https://www.youtube.com/playlist?list=PLvPsfYrGz3wspkm6LVEjndvQqK6SkcXaT)

[stages](https://ghc.haskell.org/trac/ghc/wiki/Building/Architecture/Idiom/Stages)

> Stage 1 does not support interactive execution (GHCi) and Template Haskell. The reason being that when running byte code we must dynamically link the packages, and only in stage 2 and later can we guarantee that the packages we dynamically link are compatible with those that GHC was built against (because they are the very same packages).

[Contributing to GHC 2: Basic Hacking and Organization](https://mmhaskell.com/blog/2018/6/18/contributing-to-ghc-2-basic-hacking-and-organization)

> So why did we need to build the compiler twice, wouldn’t the stage 1 compiler and the stage 1 package database have been enough? That’s a good question! We need to build the stage 2 compiler with the stage 1 compiler using the stage 1 package database (the one we will ship with the stage 2 compiler). As such, the compiler is built with the identical libraries that it ships with. When running / interpreting byte code, we need to dynamically link packages and this way we can guarantee that the packages we link are identical to the ones the compiler was built with. This it is also the reason why we don’t have GHCi or Template Haskell support in the stage 1 compiler.

[reddit hask anythin comment](https://www.reddit.com/r/haskell/comments/a1u9qj/monthly_hask_anything_december_2018/eciwz4e)

[Writing Custom Optimization Passes](https://www.reddit.com/r/haskell/comments/brrrpk/writing_custom_optimization_passes_reasonably/). [faking fundeps](https://www.reddit.com/r/haskell/comments/bsreix/faking_fundeps_with_typechecker_plugins/)

[ghc name supply](https://www.reddit.com/r/haskell/comments/c1zqbo/taking_a_look_at_how_ghc_creates_unique_ids/)

[ghc hacking using Nix](https://twitter.com/vbhvsgr/status/1141437007253725184). [another tweet](https://twitter.com/vbhvsgr/status/1142593445149761536).

[Hunting leaks with GDB](https://lukelau.me/haskell/posts/leak/)

[Build GHC with stack and hadrian](https://blog.shaynefletcher.org/2019/06/build-ghc-with-stack-and-hadrian.html).

[working with source plugins](http://mpickering.github.io/papers/working-with-source-plugins.pdf)

[custom Setup.hs](https://www.reddit.com/r/haskell/comments/c7gvaw/monthly_hask_anything_july_2019/etr51qa)

[ghc-source-gen](https://hackage.haskell.org/package/ghc-source-gen)

[Writing efficient free variable traversals](https://www.haskell.org/ghc/blog/20190728-free-variable-traversals.html). [reddit](https://www.reddit.com/r/haskell/comments/cj6bkj/ghc_blog_writing_efficient_free_variable/)

[contributor's cheat sheet](https://twitter.com/serokell/status/1164903883329757184)

[Haskell compilation pipeline and STG language: nice dive into STG types, current GHC API usage to compile haskell, attempt at .Net compiler](https://www.reddit.com/r/haskell/comments/d4dny6/haskell_compilation_pipeline_and_stg_language/)

["Eventful GHC" (debugging / profiling Haskell via the GHC eventlog)](https://twitter.com/welltyped/status/1176500000513245184)

[Gazing into the Void: Understanding Space (Leaks)](https://skillsmatter.com/skillscasts/14173-gazing-into-the-void-understanding-space-leaks)

https://ghc-compiler-notes.readthedocs.io/en/latest/

[Embracing a mechanized formalization gap](https://www.cis.upenn.edu/~sweirich/papers/verifying-ghc-extended.pdf)

> In GHC, scopes are represented by VarSets. These VarSets
are implemented by finite maps from uniques to Vars. Querying whether a variable is contained within this set is done
by checking whether the unique of the variable is in the
domain of the map. However, that query doesn’t ensure
that the same variable is stored in the set, only one with
the same unique. Thus, we require a stronger property: not
only should the variable stored in the set have the same
unique, but it should also be the “same” variable in the sense
of almostEqual, shown below. In that way, all of the occurrences of that variable in the expression will be forced to
have the same meta-information

[compile ghc in one line](https://twitter.com/availablegreen/status/1189955310515105792)

[Recompilation Avoidance](https://gitlab.haskell.org/ghc/ghc/wikis/commentary/compiler/recompilation-avoidance)

[Developing GHC for a Living](https://serokell.io/blog/developing-ghc-for-a-living). [GHC dev](https://ghc.dev/).

> I put together https://ghc.dev/, a cheatsheet to help anyone get started with contributing to GHC. 

[GHC.Hs module](https://twitter.com/smdiehl/status/1245329283704381440)

[DWARF support in GHC (part 1)](http://www.well-typed.com/blog/2020/04/dwarf-1/)

[Simon Hafner- Up to Your Elbows in GHC- λC 2019](https://www.youtube.com/watch?v=kPcD7uvDF6Y&list=PL7DZ7q3nEWhzT6OVc5laZqqGAa5mlqKjF&index=16)

[haskell / GHC symbol cheat sheet](https://github.com/takenobu-hs/haskell-symbol-search-cheatsheet)

[GHC Dev getting started material](https://www.reddit.com/r/haskell/comments/gr5xc8/ghc_dev_getting_started_material/)

[Write a GHC extension in 30 minutes by Richard Eisenberg](https://www.youtube.com/watch?v=bhhE2DxbrJM)

[On "simple" constraints for typechecker plugins by Nicolas Frisby](https://www.youtube.com/watch?v=sE1qWyQWWVY&list=PLiU7KJ5_df6aZbNfh_TUJt-6w9N3rYkTX&index=3&t=0s)

[Function Calls](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/rts/haskell-execution/function-calls). [whole-program specialization](https://www.reddit.com/r/haskell/comments/h8xiq8/z%C3%BCrich_friends_of_haskell_effects_for_less_alexis/fuyq6j3/). [effects for less - known vs unkown calls](https://youtu.be/0jI-AlWEwYI?t=2322)

> A known call is a call of a function whose binding site is statically visible:
> The function is bound at top level in this module; or,
> The function is bound at top level in another module, and optimisation is on, so we can see the details (notably arity) of the function in the module's interface file; or,
> The function is bound by a let binding that encloses the call.

> higher order functions make unknown calls (?)

[Haskell to Core: Understanding Haskell Features Through Their Desugaring](https://www.youtube.com/watch?v=fty9QL4aSRc&feature=youtu.be). [post](https://serokell.io/blog/haskell-to-core)

[What do ghc's FUN_1_0, FUN_0_1, etc closure types mean?](https://stackoverflow.com/questions/63582381/what-do-ghcs-fun-1-0-fun-0-1-etc-closure-types-mean)

[That's how the STG machine works, except thinnings can only appear at functions and thunks.](https://twitter.com/andrasKovacs6/status/1299405064310792192)

[Creating new backends for GHC?](https://www.reddit.com/r/haskell/comments/iq6jt5/creating_new_backends_for_ghc/)

[Systems Haskell](https://www.reddit.com/r/haskell/comments/ir3hmr/compiling_systems_haskell_resourcesexamples/)

[Introduction to Haskell execution and garbage collection internals](https://www.youtube.com/watch?v=vvLDerKtUWE)

[Debugging an assertion failure in GHC](https://www.youtube.com/watch?v=65GWGc5LNxc)

[-ddump-timings](https://stackoverflow.com/questions/65171404/is-there-a-way-to-see-the-compile-times-of-each-module)

[STG](https://www.reddit.com/r/haskell/comments/ku1zsm/nextgen_haskell_compilation_techniques/gir7tzo/?utm_source=reddit&utm_medium=web2x&context=3)

> The obvious point to connect to GHC codegen is STG, because Core is too restricted by its specific (and weak) type system, and Cmm is too low-level to be convenient. For example, Agda can compile to Haskell, but because the Haskell type system is weak in comparison, the code output is a horrid mess where almost everything is wrapped in unsafeCoerce, and this can be very poorly optimized by GHC. STG in contrast has a type system which only represents memory layouts and basic operational features, so it's a lot more flexible.

[bracket has interrumptible cleanup](https://gitlab.haskell.org/ghc/ghc/-/issues/18899)

[reworking of GHC's errors](https://twitter.com/TechnoEmpress/status/1359130608354668544) nice architectural choice to avoid cyclic dependencies

[GHC activities report: December–January 2020/2021](https://www.well-typed.com/blog/2021/02/ghc-2020-12-2021-01/)

[GHC Hacking Newcomer Guide](https://twitter.com/bgamari/status/1006171802140364800)

[Hacking on GHC - First Steps (2021)](https://cptwunderlich.github.io/2021/04/21/ghc-hacking-first-steps.html)

[Understanding Memory Usage with eventlog2html and ghc-debug](https://www.youtube.com/watch?v=6Ljv5FHGXDM)

[Dependency Analysis of Haskell Declarations](https://www.youtube.com/watch?v=jNbb5JVuq-o)

[how to contribute to ghc?](https://www.reddit.com/r/haskell/comments/oe4j3a/ghc_how_it_works_how_can_i_try_to_contribute_to_it/h4476z9)

[avoiding quadratic ghc core code size for modules containing large records](https://www.reddit.com/r/haskell/comments/p81t7v/new_blog_post_and_library_avoiding_quadratic_ghc/)

> Perhaps aiming for linear cost however is not necessary. We saw in the section on GHC generics that if we are careful how we set things up, we can generate code that is O(n log n) in size. Similar techniques can be applied in libraries such as generics-sop as well, provided that we are careful at every step; for example, the use of type-level lists should be avoided and we should be using type-level (balanced) trees instead.

[How does GHC implement functions under the hood?](https://www.reddit.com/r/haskell/comments/p7xq7e/how_does_ghc_implement_functions_under_the_hood/)

> The spineless tagless g machine paper linked above is amazing and if you want to understand how Haskell is evaluated it is probably the best thing to read. It is the missing link between lazy thunk and push function pointer plus arguments onto heap.

> There are also some interesting details which have changed since, like partial applications. How to make a fast curry: push/enter vs eval/apply is a great introduction on this - but after skimming over it contains less details on thunks than I remembered. 

[Persistent Software Transactional Memory in Haskell](https://twitter.com/Iceland_jack/status/1429253494314307588)

[UnliftedDatatypes in GHC 9.2.1](https://www.reddit.com/r/haskell/comments/p9m2kz/announce_ghc_921rc1_is_now_available/ha0l4jp)

> Modern branch prediction gets rid of most of the overhead of dead code from superfluous forcing

[Masking Asynchronous Exceptions](https://coot.me/posts/mask.html). [Interruptible or uninterruptible cleanup, issue in safe-exceptions package.](https://github.com/fpco/safe-exceptions/issues/3). [Uninterruptible closeFdWith merge request #4942](https://gitlab.haskell.org/ghc/ghc/-/merge_requests/4942). [Dealing with Asynchronous Exceptions during Resource Acquisition](https://www.well-typed.com/blog/2014/08/asynchronous-exceptions/). very tricky case.

[the STG machine and unboxed values](https://stackoverflow.com/questions/70740815/stg-machine-unboxed-values-handling)

[Haskell's secret sauce for a fast FFI](https://www.reddit.com/r/haskell/comments/s5ughh/what_is_haskells_secret_sauce_for_a_fast_ffi/)


## Compiling in Ubuntu

> $ cabal install --installdir /home/someguy/.local/bin --install-method=copy happy
> $ cabal install --installdir /home/someguy/.local/bin --install-method=copy alex
> $ sudo apt-get install autoconf autotools-dev automake happy
> # then follow the instructions in ghc.dev

[Induction without core-size blow-up a.k.a. Large records: anonymous edition](https://well-typed.com/blog/2021/10/large-records-part-2/)

[Bidirectional Type Checking](https://www.youtube.com/watch?v=utyBNDj7s2w)

[Ghc pipeline: type checking/elaboration and translation to Core](https://discourse.haskell.org/t/ghc-pipeline-type-checking-elaboration-and-translation-to-core/3749)

Stuff about the heap:

> There are actually a bunch of different kinds of heap objects in GHC; a lot of them are special primitive values like a few kinds of primitive arrays, mutable variables, concurrency primitives, but at the top there are several for closures, thunks, partial applications, indirections, and a couple I don’t know what exactly they mean.
> 
> However, AFAIU every object has entry code, which in the case of an evaluated constructor does almost nothing.

[Stock, Stock1 modifiers](https://gitlab.haskell.org/ghc/ghc/-/issues/20770). [meta-patterns](https://www.reddit.com/r/haskell/comments/r7bte7/metapatterns_abstracting_over_the_class_instance/). [proposal](https://github.com/ghc-proposals/ghc-proposals/pull/461)

[OS memory usage](https://twitter.com/ghc_commits/status/1468185116132397060)

[A specification for typed template Haskell](https://arxiv.org/abs/2112.03653v1)

[type-level sharing](https://twitter.com/welltyped/status/1471782671768555522)

[Christmas story](https://github.com/zw3rk/mobile-core-log/blob/master/LOG.md)

[CAFs](https://wiki.haskell.org/Constant_applicative_form) and [PAPs](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/rts/storage/heap-objects). [internal error: PAP object entered!](https://gitlab.haskell.org/ghc/ghc/-/issues/16066)

> for a Partial Application (PAP), there's no entry code. These can only be applied to more arguments using the generic apply functions, as for functions.

> unlifted objects cannot be evaluated, and therefore have no entry code.

[generated code](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/compiler/generated-code)

> The closure will store a pointer to x's closure (as it is a free variable of the lambda), along with a pointer to an info table.  That info table will contain information relevant to a function value, recording information such as the fact that it has an arity of 1 (i.e. the binding for y), and the pointer to the entry code for the function \y -> y + x itself. This entry code will implement the addition by combining the closure for the free variable x (taken from the closure) with the stack-passed y variable's closure.

[code gen](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/compiler/code-gen)

[A Haskell Compiler](https://www.scs.stanford.edu/16wi-cs240h/slides/ghc-compiler.html)

[type-checking plugins, part iii: writing a type-checking plugin](https://www.tweag.io/blog/2022-02-17-tcplugins-3/)

[conditional coding](https://blockscope.com/posts/2022-02-23-iffy-diffy.html)

[What does the GHC source mean by "zonk"?](https://stackoverflow.com/questions/31889048/what-does-the-ghc-source-mean-by-zonk)

[Hacking on GHC Has Never Been Easier! (2019)](https://vaibhavsagar.com/blog/2019/06/22/easy-ghc-hacking/)

[Incremental GHC builds with Recursive Nix (2019) (video)](https://www.youtube.com/watch?v=BFZwLbdWw8w) [ghc-nix](https://github.com/ocharles/ghc-nix)

[Word64/Int64 use Word64#/Int64#](https://gitlab.haskell.org/ghc/ghc/-/wikis/migration/9.4#word64int64-use-word64int64)

> Before 9.4, Int64/Word64 were wrappers for Int#/Word# on 64-bit architectures and for Int64#/Word64# on 32-bit architectures. Now the latter are always used (Int64#/Word64#). Users of the unboxed values must use Int64#/Word64# primops on every architecture. 

[ffi](https://www.reddit.com/r/haskell/comments/tthrq0/monthly_hask_anything_april_2022/i5dpir1/)

[Writing a GHC Plugin + Preprocessor for the first time](https://brandonchinn178.github.io/blog/2022/07/11/writing-a-ghc-plugin-and-preprocessor-for-the-first-time.html)

[PROFILING NON-CPU TIME IN HASKELL](https://www.tweag.io/blog/2022-07-28-timestats/)

[sharing is caring (about leaks)](https://www.reddit.com/r/haskell/comments/xptedd/linearity_and_eventual_uniqueness/)

[Improvements in observability in GHC 9.6](https://www.youtube.com/watch?v=vCv1vnY87NI&list=PLxxF72uPfQVRQXih84omWRmacz1lwejc6&index=7)

[ghcjs and asterius](https://www.reddit.com/r/haskell/comments/xtph0p/comment/iqv5mcq/). [more](https://www.reddit.com/r/haskell/comments/y7wuil/status_of_ghcjs_for_larger_projects/).

[about the rapier](https://www.reddit.com/r/haskell/comments/y8o9ot/understanding_the_rapier_algorithm_of_the_ghc/)

[a comparison between GHC and Racket compilation models](https://www.youtube.com/watch?v=H0ATppFmt2o)

[Profiling Memory Usage With eventlog2html and ghc-debug](https://www.youtube.com/watch?v=nIyaC3JtlyQ)

[ffi stuff](https://www.reddit.com/r/haskell/comments/zj0ted/should_raw_library_bindings_drop_the_namespace/)

[Type variables in patterns](https://arxiv.org/pdf/1806.03476.pdf)

[From delimited continuations to algebraic effects in Haskell](https://www.reddit.com/r/haskell/comments/101bcx9/from_delimited_continuations_to_algebraic_effects/)

[How can I remove all the boilerplate introduced by Trees That Grow?](https://stackoverflow.com/questions/75268118/how-can-i-remove-all-the-boilerplate-introduced-by-trees-that-grow)

[Cabal upload revisions? and some philosphical points](https://discourse.haskell.org/t/cabal-upload-revisions-and-some-philosphical-points/3772)

[Interface Files with Core Definitions](https://well-typed.com/blog/2023/02/interface-files-with-core/)

[Anonymous or large records with OverloadedRecordDot and OverloadedRecordUpdate](https://www.reddit.com/r/haskell/comments/11l3ks8/welltyped_blog_anonymous_or_large_records_with/)

[Working with Haskell CallStack](https://www.parsonsmatt.org/2023/05/11/working_with_haskell_callstack.html)

[backtrace proposal](https://github.com/ghc-proposals/ghc-proposals/pull/330)

[module-level build parallelism (-j) in #GHC vs package-level build parallelism  (-j) in #Cabal](https://discourse.haskell.org/t/ghcs-j-n-flag-useful-enough-to-be-a-default/6333/3)

> passing -j4 —ghc-option=-j4 to cabal can lead to 16 modules being compiled at the same time

[TESTING CONTROL-FLOW TRANSLATIONS IN GHC](https://www.tweag.io/blog/2023-06-01-translation-testing/)

> Cmm’s control flow is expressed through unconditional branches, conditional branches, and Switch. WebAssembly’s control flow is expressed through multiple syntactic forms: blocks, if statements, loop statements, return, and some multipurpose br forms. 

[deriving template haskell instances](https://twitter.com/Iceland_jack/status/1668293311868596225)

[COVERAGE-GUIDED FUZZING OF HASKELL PROGRAMS FOR CHEAP](https://www.tweag.io/blog/2023-06-15-ghc-libfuzzer/)

[Videos from the GHC Contributor’s Workshop](https://discourse.haskell.org/t/videos-from-the-ghc-contributors-workshop/6961)

[the Staged Working group](https://mail.haskell.org/pipermail/ghc-devs/2023-June/021253.html)

[type sharing, type level let](https://discourse.haskell.org/t/about-type-sharing-mostly-and-records-desugaring-mostly/7016/3)

[The GHC Packaging Ecosystem - Duncan Coutts - 2023 GHC Contributor's Workshop](https://www.youtube.com/watch?v=XfTinQPjDQw). [slides](https://haskell.foundation/assets/other/Duncan%20Coutts%20-%20GHC%20Tool%20Ecosystem.pdf)

[An Exceptional Actor System](https://arxiv.org/abs/2307.11194)

[using HIE files for tooling](https://hachyderm.io/@DiazCarrete/110867148360522034)

[the GHC renamer](https://www.youtube.com/watch?v=1ClZ0ySPHtI)

[ghc-debug implementation details](https://ghc.gitlab.haskell.org/ghc-debug/). [link to code](https://gitlab.haskell.org/ghc/ghc-debug/-/blob/master/common/src/GHC/Debug/Types/Closures.hs)

> Closures are represented by the DebugClosure pap string s b type

[interesting tidbit](https://gitlab.haskell.org/ghc/ghc/-/blob/master/compiler/GHC/StgToJS.hs)

> -- THUNK =
> --  { f  = returns the object reduced to WHNF
> --  , m  = ?
> --  , d1 = ?
> --  , d2 = ?
> --  }
> --
> -- FUN =
> --  { f  = function itself

[entry code for thunks?](https://www.scs.stanford.edu/14sp-cs240h/slides/ghc-compiler.html)

soo both FUN and THNK closures contain the free variables?

> [thunks] Differ from function closure in that they can be updated

[GHC Heap Objects](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/rts/storage/heap-objects#heap-objects)

> All heap objects have the same basic layout, embodied by the type StgClosure in Closures.h

> The closure type is a constant describing the kind of closure this is (function, thunk, constructor etc.).

> Valid closure kinds are CON (constructor), FN (manifest function), PAP (partial application), BH (black hole) and THK (thunk).

> FUN: functions with their free variables as payload
> THUNK: suspensions with their free variables as payload
> PAP: partial application to a FUN. FUN closure and already applied arguments as payload.

[making a fast curry](https://www.cs.tufts.edu/comp/150FP/archive/simon-peyton-jones/eval-apply-jfp.pdf)

> [about heap objects] Of these, FUN , PAP and CON objects are values, and cannot be evaluated any
further

[Writing efficient free variable traversals](https://www.haskell.org/ghc/blog/20190728-free-variable-traversals.html)

[lazy evaluation: haskell lazy evaluation illustrated](https://github.com/takenobu-hs/lazy_evaluation)

[good SO answer](https://stackoverflow.com/questions/6048194/good-introductory-text-about-ghc-implementation)

[Reducing Haddock's Memory Usage](https://www.reddit.com/r/haskell/comments/15umlnr/welltyped_blog_reducing_haddocks_memory_usage/). [Understanding memory usage with eventlog2html and ghc-debug](https://well-typed.com/blog/2021/06/zurihac-2021-advanced-track-materials/#understanding-memory-usage-with-eventlog2html-and-ghc-debug-by-matthew-pickering-and-ben-gamari). [thunks](https://github.com/well-typed/memory-usage-zurihac-2021#thunks-and-partial-applications) [saved closures](https://youtu.be/6Ljv5FHGXDM?t=2632). [saveClosures](https://hackage.haskell.org/package/ghc-debug-stub-0.5.0.0/docs/GHC-Debug-Stub.html#v:saveClosures)

> Thunks and partial function applications are represented similarly to data constructor applications, with captured free variables taking the place of the constructor fields. For instance, the program

[A First Look at Info Table Profiling](https://well-typed.com/blog/2021/01/first-look-at-hi-profiling-mode/)

> With -hi and -finfo-table-map we’ll get useful source locations for thunks but not for evaluated closures. Hence the -fdistinct-constructor-tables compile time option which creates distinct info tables per usage of data constructors.

[Rethinking Static Reference Tables in GHC](https://simonmar.github.io/posts/2018-06-22-New-SRTs.html). [Tracing the compilation of Hello Factorial! (2011)](http://blog.ezyang.com/2011/04/tracing-the-compilation-of-hello-factorial/). [Note [What are these SRTs all about?]](https://ghc-compiler-notes.readthedocs.io/en/latest/notes/compiler/stgSyn/CoreToStg.hs.html#note-what-are-these-srts-all-about)

[GHC Runtime - Stack and Heap](http://www.mchaver.com/posts/2017-06-09-ghc-runtime-heap-and-stack.html)

> Entry Code: code that will evaluate the closure. However, in the case of functions, the entry code will apply the function to the arguments given in registers or on the stack.

[A Haskell Compiler](https://www.scs.stanford.edu/14sp-cs240h/slides/ghc-compiler.html)

> Thunk closures
> Payload contains the free variables of the expression
> Differ from function closure in that they can be updated
> Entry code is the code for the expression

[Use bidirectional typechecking for types and type patterns](https://gitlab.haskell.org/ghc/ghc/-/issues/23639)

[Laziness in Haskell — Part 4: Thunks](https://www.youtube.com/watch?v=wC9cpQk7WWA). Interesting insights into STG case/let and allocations.

[strict-wrapper](https://www.reddit.com/r/haskell/comments/167o1d3/comment/jys612f/)

[ZuriHac 2016 - Low-level Haskell: An Interactive Tour Through the STG](https://www.youtube.com/watch?v=-MFk7PIKYsg)

[A GHC plugin for OpenTelemetry build metrics](https://www.haskellforall.com/2023/10/a-ghc-plugin-for-opentelemetry-build.html)

[coercion optimizer](https://gitlab.haskell.org/ghc/ghc/-/issues/8095#note_530602)

[coffee compiler club](https://www.youtube.com/watch?v=pYNgu7dG0Tc)

[zonkTyVarOcc](https://oleg.fi/gists/posts/2023-10-17-more-traverals-and-more-cabal-sat.html#fn1)

[The GHC strictness analyzer, unboxing, and the worker-wrapper transformation - Tweag](https://www.reddit.com/r/haskell/comments/108tzle/lexi_lambda_the_ghc_strictness_analyzer_unboxing/). [The Worker/Wrapper Transformation (Extended Version)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=4a74a66a02a229d10eee49f324a3e72afc488e77). [The Worker/Wrapper Transformation](https://ku-fpg.github.io/practice/workerwrapper/). [Mechanising the worker/wrapper transformation](https://www.isa-afp.org/browser_info/current/AFP/WorkerWrapper/outline.pdf). [The Worker-Wrapper Transformation Getting it right and making it better](https://eprints.nottingham.ac.uk/46840/1/thesis.pdf)

[Laziness in Haskell — Part 4: Thunks](https://www.youtube.com/watch?v=wC9cpQk7WWA). [demand signatures](https://ghc.gitlab.haskell.org/ghc/doc/users_guide/using-optimisation.html#ghc-flag--fstrictness) 

Essential reading! Covers: 

- the importance of demand analysis
- the assymmetry between laziness in arguments vs. laziness in results which is exacerbated by the "open world" of separate compilation
- how exporting vs not exporting a function might influence optimizations, because of the above.
- the importance of using strictness annotations for forbidding unusual, nonsensical usage patterns that harm optimization. 

[really cool use of RULEs for efficient Text use](https://discourse.haskell.org/t/overloadedstringdefault-proposal/8182/27). [higher order patterns in rewrite rules](https://github.com/ghc-proposals/ghc-proposals/blob/master/proposals/0555-template-patterns.rst). [semantics](https://downloads.haskell.org/ghc/latest/docs/users_guide/exts/rewrite_rules.html?highlight=rewrite%20rules#semantics).

> By using more powerful matching, we solve the long-standing problem of fusing concatMap under stream fusion. In turn, this could potentially make stream fusion general enough to replace foldr/build fusion in base.

[propriocept](https://hachyderm.io/@DiazCarrete/111516126716263577)

[More Fixpoints! (Functional Pearl)](https://www.youtube.com/watch?v=MEvSkuWvCO0)

[Confusion about the operational semantics of the let binding (LET rule) in the STG language](https://discourse.haskell.org/t/confusion-about-the-operational-semantics-of-the-let-binding-let-rule-in-the-stg-language/8286)

[Suggesting Valid Hole Fits for Typed-Holes in Haskell - aka zonk zonkitty zonk](https://www.mpg.is/papers/gissurarson2018suggesting-msc.pdf)

[When "blocked indefinitely" is not indefinite](https://well-typed.com/blog/2024/01/when-blocked-indefinitely-is-not-indefinite/)

[get-tested](https://hachyderm.io/@hecate@merveilles.town/111796213904272607) GitHub actions matrix generator

[Haskell checklist](https://hachyderm.io/@DiazCarrete/111767157009948297)

[Eras profiling for GHC](https://www.well-typed.com/blog/2024/01/ghc-eras-profiling/)

> You might start by looking at what has been allocated: which types of closures and which constructors are contributing significantly to the problem. Then perhaps it’s prudent to look at why a closure has been allocated by the info table provenance information. This will tell you from which point in the source code your allocations are coming from. But if if you then turned to investigate when a closure was allocated during the lifecycle of your program, you end up being stuck.

[time-ghc-modules can draw treemaps](https://www.reddit.com/r/haskell/comments/1aqg2q6/ann_timeghcmodules_can_draw_treemaps_now/)

[-fprefer-byte-code](https://twitter.com/mattoflambda/status/1780273199000744208)

[Improvements to the ghc-debug terminal interface](https://www.well-typed.com/blog/2024/04/ghc-debug-improvements/)

[Getting your Haskell executable statically linked without Nix](https://hasufell.github.io/posts/2024-04-21-static-linking.html)

[Multiple Component support for cabal repl](https://well-typed.com/blog/2023/03/cabal-multi-unit/). [motivation](https://jade.fyi/blog/cabal-test-dev-trick/). [more](https://stackoverflow.com/questions/67312833/fast-haskell-rebuildtest-with-file-watch-using-cabal-ghcid). [multiple home units](https://discourse.haskell.org/t/well-typed-blog-making-ghci-compatible-with-multiple-home-units/12328).

[Fault-tolerant GHC compiler pipeline](https://github.com/haskellfoundation/tech-proposals/blob/f79c2940f36e05bf587fb6b9b7ee0dce09f041f0/proposals/0000-fault-tolerant-ghc.md)

[GHC notes (there's an HLS plugin for them)](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/coding-style#2-using-notes)

> A commit message describes a change; a comment or a Note describes a state

[GHC’s type checker can operate either in checking mode or inference mode.](https://discourse.haskell.org/t/typeabstractions-in-ghc-9-10/9530/7)

[Live Reloading GUI From Scratch](https://discourse.haskell.org/t/live-reloading-gui-from-scratch/9569)

[Objects with special collection routines in GHC's GC](https://well-typed.com/blog/2018/05/ghc-special-gc-objects/)

[TH compilation](https://discord.com/channels/280033776820813825/280036215477239809/1244366119473647647)

["running typed splices in the zonker"](https://discord.com/channels/280033776820813825/280036215477239809/1244366377645637763)

[th improvements](https://discourse.haskell.org/t/what-is-your-recent-ghc-9-4-experience-using-template-haskell/9615/18). [reification](https://gitlab.haskell.org/ghc/ghc/-/issues/24021#reification)

[LIQUID HASKELL THROUGH THE COMPILERS](https://www.tweag.io/blog/2024-05-30-lh-upgrades/)

[Choreographing a dance with the GHC specializer (Part 1)](https://well-typed.com/blog/2024/04/choreographing-specialization-pt1/)

> The extra allocations required to pass these implicit dictionary arguments and apply selectors to them do result in a measurable overhead, albeit one that is insignificant for most intents and purposes. As we will see, the real cost of ad-hoc polymorphism comes from the optimizations it prevents rather than the overhead it introduces.

> all specializations that GHC generates are prefixed by $s

> The above transformation really is all that the GHC specializer does to our programs. It may not be immediately clear why this optimization is a meaningful optimization at all. That is because specialization is an enabling optimization: The real benefit comes from the optimizations that it enables later in the pipeline, such as inlining.

> GHC will only potentially attempt automatic specialization in exactly one scenario: An overloaded call at a concrete, statically known type is encountered (we’ll refer to such calls as “specializable” calls from now on).

> Instead of specializing, GHC decided to eliminate the call entirely by inlining f [so GHC must sometimes choose between inlining and specialization?]

> GHC prefers inlining over specialization, when possible, since inlining eliminates calls and doesn’t require creation of new bindings. [...]  when a specializable call is deemed too costly to inline, GHC will still attempt to specialize it.

> Interestingly, the Core terms for foo and its specialization f_$sf are alpha-equivalent to the terms we arrived at when GHC inlined the call and applied worker/wrapper instead2, with the specialization playing the same role as the worker.

[Choreographing a dance with the GHC specializer (Part 2)](https://well-typed.com/blog/2024/06/choreographing-specialization-pt2/)

[-fpolymorphic-specialisation](https://downloads.haskell.org/ghc/latest/docs/users_guide/using-optimisation.html#ghc-flag-fpolymorphic-specialisation)

[INLIN(E)ing: A case study](https://mpickering.github.io/posts/2017-05-17-inlining-case-study.html)

[GHC and Cabal: the big picture](https://discourse.haskell.org/t/ghc-and-cabal-the-big-picture/9968)

["packages and components are concept relative to how source code is distributed; while all GHC ever loads are units"](https://discourse.haskell.org/t/ghc-and-cabal-the-big-picture/9968/13)

[See the GHC team's working conventions regarding how to contribute a patch to GHC. First time contributors are encouraged to get started by just sending a Merge Request.](https://gitlab.haskell.org/ghc/ghc#getting-the-source). [How to contribute a patch to GHC](https://gitlab.haskell.org/ghc/ghc/-/wikis/working-conventions/fixing-bugs). [documentation changes](https://gitlab.haskell.org/ghc/ghc/-/wikis/working-conventions/documentation-changes).

[Object linking and GHC explained](https://discourse.haskell.org/t/object-linking-and-ghc-explained/9999)    

[diff-package-api](https://discourse.haskell.org/t/maintain-a-golden-test-of-your-packages-api-with-diff-package-api-and-print-api/9997/3)

[haskell-ci](https://github.com/haskell-CI/haskell-ci)

[ghciwatch](https://www.reddit.com/r/haskell/comments/1eaca5d/announcing_ghciwatch_10_a_ghcid_successor/)

[combinator compiler](https://www.youtube.com/watch?v=uMurx1a6Zck)

[record update drama](https://discord.com/channels/280033776820813825/280036215477239809/1285881240334897174)

[Static-ls v1.0 announcement](https://www.reddit.com/r/haskell/comments/1fqs6r8/staticls_v10_announcement_mercury/)

[Hell](https://discourse.haskell.org/t/hell-shell-scripting-in-haskell-based-language/8339/7)

[ghc wasm TH ghci](https://www.tweag.io/blog/2024-11-21-ghc-wasm-th-ghci/). [previous explanation of cross-compilation issues](https://www.tweag.io/blog/2020-11-25-asterius-th/). [the external interpreter](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/compiler/external-interpreter). [-fexternal-interpreter](https://downloads.haskell.org/ghc/latest/docs/users_guide/ghci.html#ghc-flag--fexternal-interpreter).

[ghc splices proposal](https://github.com/ghc-proposals/ghc-proposals/pull/682). [why not run splices on the host?](https://github.com/ghc-proposals/ghc-proposals/pull/682#issuecomment-2481123324). [gitlab](https://gitlab.haskell.org/ghc/ghc/-/issues/24339).

[experience with modern TH](https://discourse.haskell.org/t/what-is-your-recent-ghc-9-4-experience-using-template-haskell/9615/4)

[Interface Files with Core Definitions for faster TH](https://well-typed.com/blog/2023/02/interface-files-with-core/)

> Adding Core definitions to interface files makes it possible to defer the choice of backend (between no code, static object code, dynamic object code, bytecode) until more is known about the necessary targets. In particular:

> Cabal pessimises build times by building both static and dynamic objects under the assumption that you will eventually need dynamic objects to run Template Haskell splices. With the Core definitions at hand, we can delay this choice until we know for sure we need to do the work.

> Linking many large object files, which happens once per splice, can be very expensive compared to linking bytecode.

[let-bind more types to save space](https://gitlab.haskell.org/ghc/ghc/-/issues/20264)

[debuggable](https://www.well-typed.com/blog/2024/12/debuggable/)

[Multiple home units and Backpack together](https://gitlab.haskell.org/ghc/ghc/-/issues/20890). [driver: Do not store indefinite backpack instantiations in the EPS](https://gitlab.haskell.org/ghc/ghc/-/merge_requests/13735).

doctests: semember that the command can have a --build-depends argument.

[Exported for tests only: Precise control over API visibility with custom warnings](https://www.reddit.com/r/haskell/comments/1hqdpu3/exported_for_tests_only_precise_control_over_api/)

[Uploading](https://hackage.haskell.org/upload) Haddocks manually:

```
cabal haddock --haddock-for-hackage --haddock-hyperlink-source --haddock-quickjump --enable-documentation    
cabal upload -d --publish /home/danidiaz/cauldron/dist-newstyle/cauldron-0.6.1.0-docs.tar.gz
```

Oromolu

```
ormolu --mode inplace $(git ls-files '*.hs')
```

[running TH decls in ghci](https://www.reddit.com/r/haskell/comments/1hqrafl/comment/m5drvg8/)

[we have build-foldr fusion that can't fuse zip, and stream fusion that can't fuse concatMap](https://discord.com/channels/280033776820813825/280036215477239809/1325576477013708882)

[naming newtype accessors after the data they hold](https://bsky.app/profile/fullmoon.id/post/3lf6b43fq3c24)

[when to be strict](https://www.reddit.com/r/haskell/comments/1i2w4iq/comment/m7jmgse/)

> You never know when someone might want to write code that ties a knot someplace you didn't anticipate.

[cabal-hooks](https://www.well-typed.com/blog/2025/01/cabal-hooks/)

[church encoding](https://old.reddit.com/r/haskell/comments/1b1c71b/how_does_church_encoding_in_parser_combinator/ksey0dn/)

[entity component system](https://discourse.haskell.org/t/aztecs-v0-6-a-modular-game-engine-and-ecs-for-haskell/11447/7?u=danidiaz)

[Explicit Level Imports awarded best paper at TFP 2025](https://www.well-typed.com/blog/2025/04/explicit-level-imports/). [video](https://www.youtube.com/watch?v=-T5FirDusSs&list=PLQpeDZt0_xQfpBPdVV3hUZ3_pDxmYhsbr&index=14)

[Quasiquoting for Fun, Profit, Expressions and Patterns](https://www.reddit.com/r/haskell/comments/1khryl8/quasiquoting_for_fun_profit_expressions_and/)

[You should be using Hackage tokens](https://taylor.fausak.me/2025/06/11/hackage-tokens/)

[Draft: introduce cast zapping as an alternative to coercion zapping](https://gitlab.haskell.org/ghc/ghc/-/merge_requests/14387)

[rename modules in cabal-add](https://discourse.haskell.org/t/cabal-add-extend-cabal-build-depends-from-the-command-line/7911/21)

[inlining experiments](https://era.ed.ac.uk/handle/1842/43690)

[GADTs That Can Be Newtypes and How to Roll 'Em](https://gist.github.com/LSLeary/dd52b3086eb153e3c99e578f19eec1ee)

[Intensional Analysis of Typed Template Haskell Quotations](https://www.youtube.com/watch?v=RbBoLq8AmAA)

[What we have learned about memory profiling in the last 5 years](https://www.youtube.com/watch?v=8i8HJiBI0lo)

[Template Haskell, a case study in (in)stability](https://www.youtube.com/watch?v=TCvDq6ScaDg)

[Making GHCi compatible with multiple home units](https://www.youtube.com/watch?v=0tOciI7lMEE)

[henforcer](https://www.youtube.com/watch?v=PEAiqBHVHC0&t=2589s)

[RFC: Introduce a serialisable bytecode format and corresponding “bytecode” way](https://discourse.haskell.org/t/rfc-introduce-a-serialisable-bytecode-format-and-corresponding-bytecode-way/12678). [link](https://gitlab.haskell.org/ghc/ghc/-/issues/26298).

[Save memory and CPU with an interning cache](https://www.reddit.com/r/haskell/comments/1mou96j/save_memory_and_cpu_with_an_interning_cache/)

[Embedding Microhs](https://www.reddit.com/r/haskell/comments/1n5kawz/new_blog_post_embedding_microhs/)

[typed template haskell ~ staged programming](https://discourse.haskell.org/t/microhs-and-hackage/12916/42?u=danidiaz)

> Staged Programming: Ability to separate a program into different stages, where prior stages generate later stages.

> “Template Haskell” metaprogramming: The ability to perform intensional syntax analysis and construction.

[Better Haskell stack traces via user annotations](https://www.well-typed.com/blog/2025/09/better-haskell-stack-traces/)

[Per-component dependency solving](https://github.com/haskell/cabal/issues/4087)

[GHC optimization and fusion](https://markkarpov.com/tutorial/ghc-optimization-and-fusion). [test - Disable implicit fusion rules](https://github.com/haskell/text/pull/348).

[Higher Order Patterns for Rewrite Rules](https://pure.tudelft.nl/ws/portalfiles/portal/221833630/3677999.3678275.pdf)

> Since the introduction of fold/build fusion, a new flavor of short-cut
> fusion, called stream fusion [1], has gained
> traction in the literature. Stream fusion is based on unfolds rather than
> folds, which gives it the ability to fuse functions with multiple lists as
> input, such as zip

> Rewrite rules are written in Haskell proper, but matching
> happens at a point in the compilation pipeline where the
> program has been desugared into a small intermediate representation called Core. Rewrite rules are desugared as well

[haskell to core](https://serokell.io/blog/haskell-to-core)

[Allow expressions in SPECIALISE pragmas](https://github.com/ghc-proposals/ghc-proposals/blob/master/proposals/0493-specialise-expressions.rst)

[best practices for development](https://github.com/alexfmpe/semantic-satiation/blob/main/src/Posts/002-cheaper.md)

[next steps for reinstallable base](https://discourse.haskell.org/t/what-are-the-next-steps-for-reinstallable-base/13319)

[The Subtle Footgun of TVar (Map _ _)](https://discourse.haskell.org/t/the-subtle-footgun-of-tvar-map/13429)

[--with-repl and doctest](https://github.com/haskell/cabal/blob/master/release-notes/Cabal-3.16.0.0.md)

> Add --with-repl flag to specify alternative REPL program #9115 #10996

> Added a new --with-repl command-line option that allows specifying an alternative program to use when starting a REPL session, instead of the default GHC.

> This is particularly useful for tools like doctest and hie-bios that need to intercept the REPL session to perform their own operations. Previously, these tools had to use --with-ghc which required them to proxy all GHC invocations, including dependency compilation, making the implementation more complex.

> before: cabal repl lib:dani-sqlite --with-ghc=doctest --repl-options='-w -Wdefault'

> now (?): cabal repl --with-repl=doctest


