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

