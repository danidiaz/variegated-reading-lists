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

[The GHC strictness analyzer, unboxing, and the worker-wrapper transformation - Tweag](https://www.reddit.com/r/haskell/comments/108tzle/lexi_lambda_the_ghc_strictness_analyzer_unboxing/). [The Worker/Wrapper Transformation (Extended Version)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=4a74a66a02a229d10eee49f324a3e72afc488e77). [The Worker/Wrapper Transformation](https://ku-fpg.github.io/practice/workerwrapper/). [Mechanising the worker/wrapper transformation](https://www.isa-afp.org/browser_info/current/AFP/WorkerWrapper/outline.pdf)




