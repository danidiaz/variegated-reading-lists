[Nix](https://nixos.org/nix/)

[Nix discourse](https://discourse.nixos.org/)

[Is there much difference between using nix-shell and docker for local development?](https://discourse.nixos.org/t/is-there-much-difference-between-using-nix-shell-and-docker-for-local-development/807)

> You need to see a Docker image as a snapshot of a machine. It will stay like it is and thus anything you do with it will keep working. However, making changes to such an image is where nondeterminism seeps in. Docker images are built using shell commands, usually it contains commands like apt-get update, apt-get install ... or wget .... These fetch information from outside sources, but because the outside sources change over time will result in different files being fetched at different times. In addition, there are no checks that the files that are being fetched are actually the ones you intended to download for your Docker image. So, Docker images will stay the same, but building the Docker image will result in a different result each time you build it. No guarantees there. Nix is different in the sense that the build process itself is resttricted so that no outside sources can change without that change being detected. Builds will result in functionally the same thing each time it is run. That also makes making changes safer, as a change requires a rebuild.

> Another area that nix-shell is better is composability. You can potentially maintain common nix expressions among your many projects, and the shared build dependencies will only need to be built once. This could potentially greatly speed up your ability to work on a lot of small projects, if the alternative is you have to build a separate Docker container for each one.

> With Docker, you can share and cache the layers of containers, but you have to figure out how to order your layers to maximize sharing, and sometimes it is not possible to get all the sharing you need because two dependencies are kind of at the same layer.

[Nix, Docker and Haskell](https://cs-syd.eu/posts/2018-07-14-nix-docker-haskell)

[cachix](https://cachix.org/)

> Nix builds a package in isolation from your system. This ensures that build process is reproducible and doesn’t have undeclared dependencies, so if a package is built on one machine, it will build identically on another machine.

[Setting Up A Private Nix Cache](http://softwaresimply.blogspot.com/2018/07/setting-up-private-nix-cache.html)

[Nix compiling Haskell packages instead of downloading from Hydra](https://www.reddit.com/r/haskell/comments/45ijv2/nix_compiling_haskell_packages_instead_of/)

[Snack: incremental Nix builds for Haskell](https://www.reddit.com/r/haskell/comments/91f5r7/snack_incremental_nix_builds_for_haskell/)

[How I develop with Nix](https://ocharles.org.uk/blog/posts/2014-02-04-how-i-develop-with-nixos.html)

http://cache.nixos.org/
 
[Nix command reference](https://nixos.org/nix/manual/#part-command-ref)

[Nixos docker image](https://hub.docker.com/r/nixos/nix)

[Getting Started Haskell Project with Nix](https://maybevoid.com/posts/2019-01-27-getting-started-haskell-nix.html) tried this

> Comparing to Stack, Nix also have the advantage that we can host private Haskell packages, or even private distributions with Nix. The expressiveness of Nix makes it possible to add or remove packages, apply private patches to packages, use upstream or unpublished packages, and pin some packages to specific versions. When working on multi-language projects, Nix also makes it easy to integrate Haskell projects to a larger system and manage them as a whole.

[Haskell Nix Vim](http://www.tpflug.me/2019/01/14/haskell-nix-vim/)

[hacking on GHC but on Nix](https://www.reddit.com/r/haskell/comments/7n0eaa/what_about_hacking_on_ghc_but_on_nix/)

[all hies](https://github.com/Infinisil/all-hies)

[GHC HEAD with Nix](https://mpickering.github.io/posts/2018-01-05-ghchead-nix.html)

[Various ways to use gch in nix-shell](https://medium.com/@wizzup/various-ways-to-use-ghc-in-nix-shell-bcceae4a0397)

[Stack Nix integration](https://docs.haskellstack.org/en/stable/nix_integration/)

[Gabriel Gonzalez’s guide to using Haskell with Nix](https://github.com/Gabriel439/haskell-nix)

> Nix is a language-independent build tool. This means you can use Nix to also build and customize non-Haskell dependencies (like gtk). This uniform language simplifies build tooling and infrastructure.

> Both Nix and stack use curated package sets instead of version bounds for dependency management. stack calls these package sets "resolvers" whereas Nix calls these package sets "channels". Nix provides stable channels with names like NixOS-18.09 (analogous to stack's LTS releases) and then an unstable channel named nixpkgs-unstable (analogous to stack's nightly releases)

[Nixpkgs guide to the Haskell infrastructure](https://nixos.org/nixpkgs/manual/#users-guide-to-the-haskell-infrastructure)

[Nix integration with Cabal](https://cabal.readthedocs.io/en/latest/nix-integration.html)

[User's guide to the Haskell infrastructure](https://nixos.org/nixpkgs/manual/#users-guide-to-the-haskell-infrastructure)

[Cabal - Nix local build overview](https://www.haskell.org/cabal/users-guide/nix-local-build-overview.html)

[Make Cabal v3 Nix-friendly](https://github.com/haskell/cabal/issues/5858). [nix integration](https://www.haskell.org/cabal/users-guide/nix-integration.html?highlight=nix).

> However, I'm also a member of another group of users: those who make heavy use of Nix. For a number of reasons, Nix is very popular amongst the Haskell community, and nixpkgs builds a huge number of Haskell packages. And many of the industrial users are quite tightly wedded to it - for things like cross-compilation there are few compelling alternatives.

> Now, most people using Nix to build Haskell packages do use Cabal. nixpkgs uses the lower-level Setup.hs machinery, but of course that still depends heavily on Cabal as a library.

[A truly reproducible scientific paper](https://mozillafoundation.github.io/2017-fellows-sf/re-papers/). [hn](https://news.ycombinator.com/item?id=16356556)

[Is `cabal2nix` the (only) recommend way to convert/create small Haskell project as of today?](https://discourse.nixos.org/t/is-cabal2nix-the-only-recommend-way-to-convert-create-small-haskell-project-as-of-today/2971)

> cabal2nix converts Haskell projects to nix expressions based on the currently available package set in nixpkgs. This usually follows stackage. If your Haskell project works with this, then it is probably the most convenient way to get started. You get the benefit of using the binary cache, so you don’t even need to build much.

> It quickly gets frustrating when your dependencies don’t match what is available in the default package set. You begin to start needing to override the packages to get the exact dependencies you want, and this can quickly get out of hand.

> I’ve recently been playing with https://github.com/input-output-hk/haskell.nix 5 which take the approach of conjuring up the package set you need using cabals solver (or stacks). It then builds a nix expression which matches exactly what cabal or stack would do at that point in time, and allows you to reproduce it whenever. This is much easier to work with as you can just use your normal tools to come up with the build plan, and simply use nix for caching and reproducibility (check in the generated nix files much like you would a cabal lock file).

[The papercut thread](https://discourse.nixos.org/t/the-papercut-thread-post-your-small-annoyances-confusions-here/3100)

[Backport ghc-8.6.5 to 19.03](https://discourse.nixos.org/t/backport-ghc-8-6-5-to-19-03/3040)

https://discourse.nixos.org/t/why-not-use-yaml-for-configuration-and-package-declaration/1333

https://discourse.nixos.org/t/declarative-package-management-for-normal-users/1823

https://discourse.nixos.org/t/nixos-pain-points-newbie-gone-intermediate-experience-report/452

> “to pin or not to pin”: when staying with a NixOS release, I quickly started to miss newer packages; when following nightly, I was afraid of things breaking and the config being not really reproducible; I tried to reasearch nixpkgs pinning, but didn’t manage to find a lot about this (reportedly doable, but haven’t found good examples I would be able to reuse);

https://vaibhavsagar.com/blog/2018/05/27/quick-easy-nixpkgs-pinning/

> This might be desirable in many cases, but for us it means a lot of waiting for no benefit. We can avoid this by pinning nixpkgs to a known-good commit. One way to do this is by setting the NIX_PATH environment variable, which is where Nix looks for the location of nixpkgs. We could do this as follows:

> cabal2nix converts Haskell projects to nix expressions based on the currently available package set in nixpkgs. This usually follows stackage. If your Haskell project works with this, then it is probably the most convenient way to get started. You get the benefit of using the binary cache, so you don’t even need to build much.

> I’ve recently been playing with https://github.com/input-output-hk/haskell.nix 5 which take the approach of conjuring up the package set you need using cabals solver (or stacks). It then builds a nix expression which matches exactly what cabal or stack would do at that point in time, and allows you to reproduce it whenever. This is much easier to work with as you can just use your normal tools to come up with the build plan, and simply use nix for caching and reproducibility (check in the generated nix files much like you would a cabal lock file).

[Nix hash collision](https://twitter.com/stdlib/status/1136629930060636162)

[Nix pills](https://nixos.org/nixos/nix-pills/)

Nix non-determinism https://gitlab.haskell.org/ghc/ghc/issues/4012 https://nixos.org/nix-dev/2015-June/017429.html

[What is nix-instantiate good for ? What is a store-derivation?](https://stackoverflow.com/questions/31490262/what-is-nix-instantiate-good-for-what-is-a-store-derivation)

[Nix PhD thesis](https://nixos.org/~eelco/pubs/phd-thesis.pdf)

> From the thesis: "Nix expressions are [...] translated to [...] store derivations, which encode single component build actions. [Just as] compilers generally do the bulk of their work on simpler intermediate representations of the code being compiled, rather than on a full-blown language with all its complexities. [...] Nix expressions are first translated to store derivations that live in the Nix store and that each describe a single build action with all variability removed. These store derivations can then be built, which results in derivation outputs that also live in the Nix store." 

[scripting with nix](http://chriswarbo.net/projects/nixos/scripting_with_nix.html)

[Environments with Nix Shell - Learning Nix pt 1](https://www.sam.today/blog/environments-with-nix-shell-learning-nix-pt-1/)

[Failing to Learn Nix](https://push.cx/2018/nixos)

[not feeling worthwhile on the desktop](https://www.reddit.com/r/NixOS/comments/7cgvk7/nixos_is_not_feeling_worthwhile_on_the_desktop/)

[remote Nix shells](https://freux.fr/orgposts/remoteshell.html)

[nix-instantiate man page](https://www.mankier.com/1/nix-instantiate). [nix-store man page](https://www.mankier.com/1/nix-store). [nix-env man page](https://www.mankier.com/1/nix-env)

[HN Nix misgivings](https://news.ycombinator.com/item?id=16443323). [HN on Nix 2.0 release](https://news.ycombinator.com/item?id=16442893). [more misgivins](https://hands-on.cloud/why-you-should-never-ever-use-nix-os/)

> Needing to pass `-A` to a lot of commands to use them the "right way" smells of a poorly thought out design.

> Nix isolates packages, such that updating one package has no impact on any other packages (with unavoidable exceptions like the graphics driver, presumably).

> You're right that package isolation isn't much of a problem on non-rolling distros. One of the benefits of Nix is that you get some of the stability and predictability of an LTS distro with the freshness of a rolling distro when desired, without having to deal with package conflicts.

> Incidentally, Nix doesn't need to be used in a deterministic manner. In fact, I don't think most desktop users of Nix care too much about determinism for most packages they run. I certainly don't; I'm happy to follow along with whatever arrives in my channel. Nix has features that support determinism, and I'm certainly glad they exist for when I end up needing them, but they're not necessarily why people use Nix.

[How we use Nix at IOHK](https://iohk.io/blog/how-we-use-nix-at-iohk/)

[how does nix know what binary a machine needs?](https://stackoverflow.com/questions/30945027/how-does-nix-know-what-binary-a-machine-needs)

[managuing rust dependencies with Nix](https://www.hadean.com/blog/managing-rust-dependencies-with-nix-part-i)

[NIX + BAZEL = FULLY REPRODUCIBLE, INCREMENTAL BUILDS](https://www.tweag.io/posts/2018-03-15-bazel-nix.html)

[Overlays](https://nixos.wiki/wiki/Overlays)

> Overlays provide a method to extend and change nixpkgs. They replace constructs like packageOverride and overridePackages.

[NixOS: The DOs and DON’Ts of nixpkgs overlays](https://blog.flyingcircus.io/2017/11/07/nixos-the-dos-and-donts-of-nixpkgs-overlays/) with [video](https://www.youtube.com/watch?v=6bLF7zqB7EM&feature=youtu.be&t=39m50s)

[NixCon](https://www.youtube.com/channel/UCjqkNrQ8F3OhKSCfCgagWLg/videos)

[Nixpkgs Overlays – A place for all excluded packages](https://www.youtube.com/watch?v=W85mF1zWA2o)

> the ability to compose different modules

> NixOS: declarative, composable. Nixpgs: not declarative, not composable (before overlays)

[Introduction to Nix](https://www.youtube.com/watch?v=D5Gq2wkRXpU)

[scons (not Nix)](https://news.ycombinator.com/item?id=20138448)

["Nix does a lot of fixpoints"](https://www.youtube.com/watch?v=1yOfr9f7nJk&t=2352)

[Dhall and bidirectional type checking](https://www.reddit.com/r/haskell/comments/5go3sb/dhall_a_nonturingcomplete_configuration_language/)

[complex setup](https://twitter.com/nomeata/status/1137838054390095873). [generating package sets for Cabal projects](https://input-output-hk.github.io/haskell.nix/user-guide/cabal-projects/)

[GHC user guide: packages](https://downloads.haskell.org/~ghc/latest/docs/html/users_guide/packages.html)

[phases](https://nixos.org/nixpkgs/manual/#sec-stdenv-phases)

[How to install java in NixOS?](https://unix.stackexchange.com/questions/403846/how-to-install-java-in-nixos). [issue](https://github.com/NixOS/nixpkgs/issues/19690). [issue](https://github.com/NixOS/nixpkgs/issues/47223).

[Using Nix and CI for great good!](https://medium.com/plapadoo/using-nix-and-ci-for-great-good-8a9162fed313)

[Graal VM packages wanted](https://discourse.nixos.org/t/graal-vm-packages-wanted/2485)

[Learning to love Nix](https://cdagostino.io/posts/2017-07-28-learning-to-love-nix.html)

[another take on Docker vs Nix](https://news.ycombinator.com/item?id=15480487)

[NixOS channels, profiles and packages](https://stackoverflow.com/questions/47953868/nixos-channels-profiles-and-packages)

> nix-env -q will only report packages that are installed into imperative 'environments', like those created by nix-env -i.

> nix-env is a tool for imperative package management that is a thin layer over the otherwise declarative and immutable Nix system. The profiles mechanism provides a means for mutability and nix-env creates manifest.nix in the profile to record the set of packages that are in the environment.

[Quick and Easy Nixpkgs Pinning](https://vaibhavsagar.com/blog/2018/05/27/quick-easy-nixpkgs-pinning/)

[What does the <nixpkgs> string / value mean in Nix?](https://stackoverflow.com/questions/47379654/what-does-the-nixpkgs-string-value-mean-in-nix/47388602#47388602)
 
> Note that the Nix search path is impractical in many situations. You can only pass it from the outside, and it easily creates impurity. In my experience, problems are better solved with explicit argument passing or the functions relating to fix-points like callPackage and the overlay system.

[Self and super in nix overlays](https://stackoverflow.com/questions/52401177/self-and-super-in-nix-overlays/52402289#52402289)

[Can I replicate what nix-build does with nix-shell and cabal build?](https://stackoverflow.com/questions/52249028/can-i-replicate-what-nix-build-does-with-nix-shell-and-cabal-build)

> In general, you are not guaranteed that the output of nix-build and the same steps in a nix-shell will equivalent.

> nix-shell can be invoked without the --pure flag, so that many more environment variables will be set (this lets you use GUI applications for example)

[Where is `callPackage` defined in the Nixpkgs repo (or how to find Nix lambda definitions in general)?]()

> nix repl can tell you the location where a lambda is defined.

[not exactly Nix related but](https://twitter.com/alexellisuk/status/1138847795266428929)

[Nix .defexpr](https://github.com/NixOS/nix/issues/487)

[mutable NIX_PATH stuff, channel stuff, and the inconsistent plethora of CLI tools](https://twitter.com/programmerdude/status/1051476179906113537)

[Getting started with Nix](https://qfpl.io/posts/nix/getting-started-with-nix/)

[Nix by example](https://medium.com/@MrJamesFisher/nix-by-example-a0063a1a4c55)

[porcelain commands from 2.0](https://nixos.org/nix/manual/#ssec-relnotes-2.0)

[Compare Nix derivations using nix-diff](http://www.haskellforall.com/2017/)

> These *.drv files use the ATerm file format and are Nix-independent. Conceptually, Nix is just a domain-specific language for generating these ATerm files. 

[Nix cookbook](https://github.com/domenkozar/nix-cookbook)

[Nix function parameters](https://nixos.org/nixos/nix-pills/nixpkgs-parameters.html)

> https://nixos.org/nixos/nix-pills/nixpkgs-parameters.html
> In this case, nix does a trick:
> If the expression is a derivation, well build it.
> If the expression is a function, call it and build the resulting derivation.

[Nix + Cabal example](https://twitter.com/puffnfresh/status/1139377913155821569)

[nix-env -qa not showing latest packages](https://stackoverflow.com/questions/33883861/nix-env-qa-not-showing-latest-packages?rq=1)

[nix for cross-compiling](https://twitter.com/grhmc/status/1138921028019785728)

[Packaging a Haskell library for artefact evaluation using nix](http://mpickering.github.io/posts/2018-09-19-nix-artefacts.html)

[Nix cookbook](https://nix-cookbook.readthedocs.io/en/latest/index.html)

## Videos

[Intro to Nix](https://www.youtube.com/watch?v=D5Gq2wkRXpU)

[Py Munich](https://www.youtube.com/watch?v=Gv8OELicQzU)

[Using Nix as a build tool - Part 1](https://www.youtube.com/watch?v=ova4dZhzxAQ)

[Nix the functional Package Manager and NixOS the declarative Linux distribution](https://www.youtube.com/watch?v=dQLO5CWuGVk)

[Nix: Under the hood by Gabriel Gonzalez](https://www.youtube.com/watch?v=GMQPzv3Sx58)

[Nix as HPC package management system](https://www.youtube.com/watch?v=s5iY3CsdSfQ)

[Configuration management for your house](https://www.youtube.com/watch?v=0pqdOnQKMKE)

[Nix: The Purely Functional Package Manager](https://www.youtube.com/watch?v=w2E1C8u_uY0)

[Introduction to NixOS](https://www.youtube.com/watch?v=tl9I-R83lKo).

[Nix Flake MVP](https://gist.github.com/edolstra/40da6e3a4d4ee8fd019395365e0772e7)

[Example of default.nix for use with nix-build](https://gist.github.com/vaibhavsagar/212273a6af6896fb79dd2c866b03ce5a). [tweet](https://twitter.com/vbhvsgr/status/1139918593360048128).

[Putting your own derivations in Nix Profile](https://qiita.com/kimagure/items/8b4df59236717e54a2bc)

```
nix-store --query --deriver $(readlink -f $(which vim))
nix-env --query --drv-path --file '<nixpkgs>' vim
```

[Setting up a C++ project environment with nix](https://blog.galowicz.de/2019/04/17/tutorial_nix_cpp_setup/). [Managing libraries with Nix](https://blog.galowicz.de/2019/04/17/tutorial_nix_cpp_setup/)

[Haskell Nix tip](https://twitter.com/BoshenBoshen/status/1140798905937883137)

[Nix like](https://twitter.com/dysinger/status/1141796787683905536)

[Backup using Nix](https://twitter.com/domenkozar/status/1143497330806677504)

[more on Cabal Nix integration](https://twitter.com/emi1ypi/status/1143972703491280899)

[Package Management Walkthrough: apt, yum, dnf, pkg](https://lowendbox.com/blog/package-management-walkthrough-apt-yum-dnf-pkg/)

[Optimising Docker Layers for Better Caching with Nix](https://grahamc.com/blog/nix-and-layered-docker-images)

[Generic Level Polymorphic N-ary Functions](https://gallais.github.io/pdf/tyde19.pdf)

[Nix typeclasses](https://twitter.com/typeclasses/status/1151928000432267264)

[Flakes – Proposed mechanism to package Nix expressions into composable entities](https://news.ycombinator.com/item?id=20486462)

> I’d love for a way to write nix expressions that easily lead to reproducible builds. Of course this is possible right now next, but requires substantial legwork to pin Nixpkgs version or add SHA for every tarball. 

[Functional DevOps in a Dysfunctional World](https://vaibhavsagar.com/blog/2019/07/04/functional-devops/index.html)

[arion](https://github.com/hercules-ci/arion#docker-image-from-dockerhub). [tweet](https://twitter.com/domenkozar/status/1163368707235753984).

> Arion is a tool for building and running applications that consist of multiple docker containers using NixOS modules. It has special support for docker images that are built with Nix, for a smooth development experience and improved performance.

[stop using docker/containers as a replacement for reproducible build tools (like nix)](https://twitter.com/vamchale/status/1161290339472289792)

[another nix+haskell tweet](https://twitter.com/ChShersh/status/1163874632174329856)

[nix-copy-closure](https://vaibhavsagar.com/blog/2019/08/22/industrial-strength-deployments/)

[Using Nix for Repeatable Python Environments | SciPy 2019 | Daniel Wheeler](https://www.youtube.com/watch?v=USDbjmxEZ_I)

[python section of NixOS docs](https://github.com/NixOS/nixpkgs/blob/master/doc/languages-frameworks/python.section.md)

[article about Nix and Haskell](https://github.com/cdepillabout/post-about-nix-and-haskell/blob/master/2019-08-03-q-and-as-about-nix-for-haskellers.md)

[how to fix broken #Haskell packages in #Nix](https://www.youtube.com/watch?time_continue=2&v=KLhkAEk8I20)

[ociTools in NixOS](https://spacekookie.de/blog/ocitools-in-nixos/)

[#Nix code that can be used to find or build all reverse dependencies of a given #Haskell package.](https://twitter.com/cdepillabout/status/1171271332253839366)

[nix on small computers](https://www.reddit.com/r/haskell/comments/d86sqc/my_experience_with_haskell_on_raspberry_pi_4b_4gb/f18rsd0/)

[nix at shopify](https://twitter.com/domenkozar/status/1177169378607079424)

[some of the most commonly useful things about the nix repl](https://twitter.com/jusrin00/status/1179423225379467264)

https://twitter.com/ProgrammerDude/status/1188184013556604928

[Building our project using Nix for - JS, Statically (Musl + integer-simple), IHaskell notebook, Reflex webapp](https://www.reddit.com/r/haskell/comments/dnso4k/building_our_project_using_nix_for_js_statically/)

[testing Cabal packages](https://twitter.com/GabrielG439/status/1195383865608507392)

[Nix recipes for Haskellers](https://www.srid.ca/haskell-nix.html)

[recursive Nix](https://twitter.com/acid2/status/1201107254382084096)

[authoring Nix derivations](https://twitter.com/GabrielG439/status/1205508846967373824)

[recursive Nix](https://twitter.com/domenkozar/status/1207707582275686400)

[Incremental GHC builds with Recursive Nix](https://www.youtube.com/watch?v=BFZwLbdWw8w)

[Recursive Nix #13](https://github.com/NixOS/nix/issues/13). [This allows Nix builders to call Nix to build derivations, with some limitations](https://github.com/NixOS/nix/pull/3205)

[Eelco Dolstra - content-addressable store](https://www.youtube.com/watch?v=8M6yvJC00J4&feature=youtu.be&t=782)

> the holy grail for many years

> non-root users could install stuff from unverified binary caches

[NixCon](https://www.youtube.com/channel/UCjqkNrQ8F3OhKSCfCgagWLg/videos?view=0&sort=dd&flow=grid)

[The runtime dependencies are a subset of the build-time dependencies that Nix determines automatically by scanning the generated output for the hash part of each build-time dependencies' store path.](https://stackoverflow.com/a/34837585/1364288)

[nix for bash scrips](https://twitter.com/shajra/status/1208495950270017536)

[NixOS for developers](https://lobste.rs/s/jevfaf/nixos_for_developers)

> It’s good the author addresses the value of pinning channels, such as nixpkgs. Otherwise the dependencies aren’t really deterministic as nix will use the latest version.

[thoughts on Nix](https://lobste.rs/s/tp6o0q/thoughts_on_nix)

[experiences with Haskell and Nix](https://www.reddit.com/r/haskell/comments/ewm9ia/nix_and_haskell_in_production_share_your/)

[haskell nix doubt](https://twitter.com/tylerweir/status/1225147834598666240)

[I was Wrong about Nix](https://christine.website/blog/i-was-wrong-about-nix-2020-02-10) mentions Nix with Go, construction of docker images. Tools niv, dive, vgo2nix

I Was Wrong about Nix https://news.ycombinator.com/item?id=22295102 https://www.reddit.com/r/programming/comments/f23oox/i_was_wrong_about_nix/ http://lethalman.blogspot.com/2016/04/cheap-docker-images-with-nix_15.html

[How I start: Nix](https://lobste.rs/s/lktf6u/how_i_start_nix)

[Running a haskell script without GHC](https://gist.github.com/monadplus/4bd19ccf19681e82d013c290fd21e663)

https://www.reddit.com/r/haskell/comments/fp0g4n/nix_haskell_development_2020_howto/ pin nixpkgs

[Building a reproducible blog with Nix](https://blog.ysndr.de/posts/internals/2020-04-10-built-with-nix/)

[Erase your darlings: immutable infrastructure for mutable systems](https://news.ycombinator.com/item?id=22856199)

[NixOS – Building a web app with functional programming](https://news.ycombinator.com/item?id=22877355)

[My experience with NixOS](https://news.ycombinator.com/item?id=22877355)

[Nix documentation shouldn't even mention the existence of nix-env. It's a complete anti-pattern.](https://twitter.com/ProgrammerDude/status/1250520991308152832)

[society if Nix were typed](https://twitter.com/evertedsphere/status/1251144652381540352)

[nix yubykey](https://twitter.com/ProgrammerDude/status/1253670978141421570)

[My NixOS Desktop Flow](https://news.ycombinator.com/item?id=22984639)

[Nix as a Homebrew replacement](https://twitter.com/burkelibbey/status/1255165901365825536)

[ghcide and nix](https://twitter.com/a_cowley/status/1256079226412896256)

[A Gentle Introduction to the Nix Family (2019)](https://news.ycombinator.com/item?id=23087197)

[tweet](https://twitter.com/mitchellh/status/1258844671503024128)

[NIX FLAKES, PART 1: AN INTRODUCTION AND TUTORIAL](https://www.tweag.io/posts/2020-05-25-flakes.html)

[A Nix terminology primer by a newcomer](https://stephank.nl/p/2020-06-01-a-nix-primer-by-a-newcomer.html). [HN](https://news.ycombinator.com/item?id=23377292)

[Getting ghcide into nixpkgs](https://mpickering.github.io/ide/posts/2020-06-05-ghcide-and-nixpkgs.html)

[other package mangers](https://news.ycombinator.com/item?id=23439980)

[Nix(OS) Thoughts](https://blog.qtp2t.club/posts/2020-06-20-nix-nixos-thoughts/)

[Python with Nix](https://lobste.rs/s/tjgvzi/development_with_nix_python)

[NixOS: How it works and how to install it!](https://www.youtube.com/watch?time_continue=1&v=oPymb2-IXbg&feature=emb_logo)

[nix flakes 1](https://www.tweag.io/blog/2020-05-25-flakes/) [2](https://www.tweag.io/blog/2020-06-25-eval-cache/) [3](https://www.tweag.io/blog/2020-07-31-nixos-flakes/)

[When and how should default.nix, shell.nix and release.nix be used?](https://stackoverflow.com/questions/44088192/when-and-how-should-default-nix-shell-nix-and-release-nix-be-used)

[stuff about nix-shell](https://nixos.org/nix/manual/#name-2)

> If path is not given, nix-shell defaults to shell.nix if it exists, and default.nix otherwise.

[creating your Nix channel](https://lucperkins.dev/blog/nix-channel/)

[good video](https://twitter.com/a_cowley/status/1301185763913142272)

[TOWARDS A CONTENT-ADDRESSED MODEL FOR NIX](https://www.tweag.io/blog/2020-09-10-nix-cas/). [cachix interview](https://twitter.com/domenkozar/status/1300466293821370369)

https://haskell4nix.readthedocs.io/

[Distributing Haskell programs in a multi-platform zip file](https://www.joachim-breitner.de/blog/776-Distributing_Haskell_programs_in_a_multi-platform_zip_file)

[Creating a Haskell development environment with LSP on NixOS](https://jkuokkanen109157944.wordpress.com/2020/11/10/creating-a-haskell-development-environment-with-lsp-on-nixos/)

[Ubuntu 20.10 now packages Nix](https://twitter.com/ProgrammerDude/status/1347977911870095360)

[Scrive Nix Workshop](https://scrive.github.io/nix-workshop/)

[DERIVATION OUTPUTS IN A CONTENT-ADDRESSED WORLD](https://www.tweag.io/blog/2021-02-17-derivation-outputs-and-output-paths/)

[Offloading NixOS builds to a faster machine](https://sgt.hootr.club/molten-matter/nix-distributed-builds/)

[overlays based on recursive knots](https://discourse.haskell.org/t/whats-all-the-hype-with-nix/2593/13) 
 
[Nix: An idea whose time has come](https://news.ycombinator.com/item?id=30384121)

[haskell.nix depends heavily on what is commonly called "import from derivation" or IFD.](https://stackoverflow.com/a/71034842/1364288). [materialization](https://input-output-hk.github.io/haskell.nix/tutorials/materialization.html). 

> These can not be evaluated without building bar and somePackage.

> haskell.nix does have a feature that lets you avoid such expressions altogether. They've called it materialization.

[It’s the hardest learning curve of probably in tech I’ve ever learned](https://about.sourcegraph.com/blog/dev-tool-time-mitchell-hashimoto/)

[All New Repls are Powered By Nix](https://blog.replit.com/powered-by-nix). [lobsters](https://lobste.rs/s/jzpd65/all_new_repls_are_powered_by_nix)

[lib.attrsets.attrVals](https://nixos.org/manual/nixpkgs/stable/)

[Chapter 13. Callpackage Design Pattern](https://nixos.org/guides/nix-pills/callpackage-design-pattern.html)

> note from the example above that the intersectAttrs returns a set whose names are the intersection, and the attribute values are taken from the second set.

[How to Learn Nix, Part 26: An infinite list of functions](https://ianthehenry.com/posts/how-to-learn-nix/an-infinite-list-of-functions/)

[NixOs manual](https://nixos.org/manual/nix/stable/introduction.html)

[What does a question mark mean in the head of a Nix function definition?](https://stackoverflow.com/questions/56406588/what-does-a-question-mark-mean-in-the-head-of-a-nix-function-definition)

[Nix (builtins) & Nixpkgs (lib) Functions](https://teu5us.github.io/nix-lib.html)

[operators](https://nixos.org/manual/nix/stable/expressions/language-operators.html)

[Nix Expression Language](https://nixos.wiki/wiki/Nix_Expression_Language)

[When and how should default.nix, shell.nix and release.nix be used?](https://stackoverflow.com/questions/44088192/when-and-how-should-default-nix-shell-nix-and-release-nix-be-used)

> default.nix is used as a default file when running nix-build, and shell.nix is used as a default file when running nix-shell

> Next, default.nix isn't used only for nix-build. For example, <nixpkgs/lib/default.nix> is used as aggregator for functions, and doesn't contain derivations. So not every default.nix is supposed to be "built" (but if default.nix is an attribute set of derivations, it will be buildable, and nix-build will build all of them).

> Next, nix-shell will use default.nix if no shell.nix is found.

> Next, default.nix is used as default file when importing directory. So if you write x = import ./some/directory;, then ./some/directory/default.nix will be imported.

> And finally, there are two common formats for derivations in default.nix: derivation, and callPackage derivation. You can't nix-build the latter. 

Small victory: make ed available to nix-shell inside repl.it. [Development environment with nix-shell](https://nixos.wiki/wiki/Development_environment_with_nix-shell). 

>  if you don't (or you don't want to) have a package definition you can still use a nix-shell to provide a reproducible development environment

    { pkgs ? import <nixpkgs> {} }:
      pkgs.mkShell {
        # nativeBuildInputs is usually what you want -- tools you need to run
        nativeBuildInputs = [ pkgs.buildPackages.ed ];
    }

Here's a variant without buildPackages:

    { pkgs ? import <nixpkgs> {} }:
      pkgs.mkShell {
        # nativeBuildInputs is usually what you want -- tools you need to run
        nativeBuildInputs = [ pkgs.ed pkgs.sqlite ];
    }

> For Flakes-based projects (flake.nix file in project root), we replace nix-shell with nix develop

[what are the arguments of mkShell?](https://discourse.nixos.org/t/mkshell-vs-buildenv/681)

[Use `buildInputs` or nativeBuildInputs` for `nix-shell`?](https://discourse.nixos.org/t/use-buildinputs-or-nativebuildinputs-for-nix-shell/8464)

> for nix-shell, most people use a shell.nix + mkShell. In which case it doesn’t really matter as nix-shell doesn’t really make distinctions between them

> In general though, nativeBuildInputs is useful for cross-compilation as commands from those derivations will be available on the hostPlatform and execute at build time. Whereas buildInputs will likely be the architecture of the targetPlatform, so the derivation can link against those inputs (and be used at run-time). 

[overrides](https://ryantm.github.io/nixpkgs/using/overrides/)

> The function override is usually available for all the derivations in the nixpkgs expression (pkgs).

> It is used to override the arguments passed to a function.

[How is overrideAttrs different from override?](https://www.reddit.com/r/NixOS/comments/cn6nt4/how_is_overrideattrs_different_from_override/)

> override overrides arguments of a function (i.e. the dependencies of a package), and overrideAttrs overrides the package definition itself. 

[overrideAttrs vs. overrideDerivation](https://nixos.org/manual/nixpkgs/stable/#sec-pkg-override)

> Note that separateDebugInfo is processed only by the stdenv.mkDerivation function, not the generated, raw Nix derivation. Thus, using overrideDerivation will not work in this case, as it overrides only the attributes of the final derivation. It is for this reason that overrideAttrs should be preferred in (almost) all cases to overrideDerivation, i.e. to allow using stdenv.mkDerivation to process input arguments, as well as the fact that it is easier to use (you can use the same attribute names you see in your Nix code, instead of the ones generated (e.g. buildInputs vs nativeBuildInputs), and it involves less typing).

> You should prefer overrideAttrs in almost all cases

[Inputs Design Pattern](https://nixos.org/guides/nix-pills/inputs-design-pattern.html#inputs-design-pattern)

[Scrive Nix Workshop](https://scrive.github.io/nix-workshop/index.html)

[Experiment Packaging: Don’t Repeat Yourself](https://nix-tutorial.gitlabpages.inria.fr/nix-tutorial/experiment-packaging.html). 

[how Nix can help in the making of repeatable experiments](https://nix-tutorial.gitlabpages.inria.fr/nix-tutorial/index.html)

[FAQ/Pinning Nixpkgs](https://nixos.wiki/wiki/FAQ/Pinning_Nixpkgs). [more pinning](https://scrive.github.io/nix-workshop/03-nix-basics/04-import.html#pinning-nixpkgs). 

> Nix 2.0 introduces new builtins, fetchTarball and fetchGit, which make it possible to fetch a specific version of nixpkgs without depending on an existing one

> Pinning nixpkgs is highly encouraged when developing Nix modules. Without pinning, your users may run your modules on a version of nixpkgs that is several months old.

> We will go through in a later chapter on how to use niv to automate the management of pinned remote Nix packages.

[Quick and Easy Nixpkgs Pinning (2018)](https://vaibhavsagar.com/blog/2018/05/27/quick-easy-nixpkgs-pinning/)

> I love Nix because it makes packaging and using software so easy. For example, here’s a first stab at an expression that makes a recent version of Pandoc available in a nix-shell (be warned, this will take a while the first time!)

> Barring an event like the garbage collection of the Nix store or a change in the expression above, we would like to never rebuild this package again.

>  If we later update this by running $ nix-channel --update and any of the transitive dependencies of our expression are updated, this will cause a rebuild because Nix will rightly detect that the inputs have changed.

> What happens if we want to update the pinned version? One workflow I’ve seen suggested is to update the rev, change one character in the sha256, and let the Nix error message tell you the correct hash to use. I think we can do better than this.

[What is buildPackages in Nix?](https://stackoverflow.com/questions/67540620/what-is-buildpackages-in-nix)

> After googling this expression I get very random results about people using this for compiling many languages

> This looks like a package set to explicitly reference all packages built on the host during cross-compilation 

[After a year of using NixOS, stdenv.mkDerivation is still something of a mystery to me. I only know how to use it by copying examples from other packages](https://github.com/NixOS/nixpkgs/issues/18678)

[The complexity of the dependencies and hooks infrastructure has increased, over time, to support cross compilation.](https://nixos.org/guides/nix-pills/basic-dependencies-and-hooks.html)

> Once you learn the core concepts, you will be able to understand the extra complexity. 

[The propagatedBuildInputs Attribute](https://nixos.org/guides/nix-pills/basic-dependencies-and-hooks.html#idm140737319457488)

> The buildInputs covers direct dependencies, but what about indirect dependencies where one package needs a second package which needs a third? Nix itself handles this just fine, understanding various dependency closures as covered in previous builds. But what about the conveniences that buildInputs provides, namely accumulating in pkgs environment variable and inclusion of pkg/bin directories on the PATH? For this, stdenv provides the propagatedBuildInputs

[Nix Flakes: Packages and How to Use Them](https://christine.website/blog/nix-flakes-2-2022-02-27)

[Nix + Docker, a match made in heaven (video)](https://youtu.be/WP_oAmV6C2U?t=2616). [Functional programming and Nix for reproducible, immutable infrastructure (video)](https://www.youtube.com/watch?v=mKXLAbrKrno).

[Chapter 16. Nixpkgs Parameters](https://nixos.org/guides/nix-pills/nixpkgs-parameters.html#nixpkgs-parameters)

[direnv – unclutter your .profile](https://direnv.net/)

[Intro to Flakes](https://www.youtube.com/watch?v=K54KKAx2wNc)

[Nix - A One Pager](https://github.com/tazjin/nix-1p)

> Nix has three major things that could be considered its standard library and while there's a lot of debate to be had about this point, you still need to know all three.

[Nixery - inherit](https://nixery.dev/nix-1p.html#inherit-keyword)

[with](https://discourse.nixos.org/t/what-is-the-added-benefit-of-let-in-compared-to-plain-with-with-rec/14248/5)

> with foo is considered a bad design error of the language by some of us, and we consider the excessive use of with pkgs throughout tutorials and examples not only unidiomatic but also misleading.

> Also, remember that let and function arguments win over with.

> foo: let foo = 1; in foo always returns 1, while foo: with { foo = 1; }; foo is equivalent to x: x.

[Nix (builtins) & Nixpkgs (lib) Functions](https://teu5us.github.io/nix-lib.html)

[nmattia/niv: Easy dependency management for Nix projects](https://github.com/nmattia/niv)

[The hard part of type-checking Nix](https://www.haskellforall.com/2022/03/the-hard-part-of-type-checking-nix.html)

[a tour of Nix—further reading](https://nixcloud.io/tour/?id=34)

[Nix: Under the hood](https://www.youtube.com/watch?v=GMQPzv3Sx58)

[How to Learn Nix](https://ianthehenry.com/posts/how-to-learn-nix/). [An introduction to nix-shell](http://ghedam.at/15978/an-introduction-to-nix-shell). [A minimal nix-shell](https://fzakaria.com/2021/08/02/a-minimal-nix-shell.html). []()

[Writing a split derivation](https://nixos.org/manual/nixpkgs/stable/#sec-multiple-outputs-)

> a derivation that produces multiple outputs

> the whole machinery is triggered by defining the outputs attribute to contain the list of desired output names (strings). 

[Rpath, or why lld doesn’t work on NixOS](https://news.ycombinator.com/item?id=30688815)

[Haskell.nix—alternative Haskell infrastructure](https://input-output-hk.github.io/haskell.nix/reference/library.html)

[From nix-env to home-manager](https://www.youtube.com/watch?v=PmD8Qe8z2sY)

[Almost Perfect Dotfiles Management w/ nix, home-manager and flakes](https://www.youtube.com/watch?v=CDzgNxoAlnA)

[Hacking Your First Package](https://nix-tutorial.gitlabpages.inria.fr/nix-tutorial/first-package.html)

[Nix parallelism & Import From Derivation](https://fzakaria.com/2020/10/20/nix-parallelism-import-from-derivation.html). [Import From Derivation](https://nixos.wiki/wiki/Import_From_Derivation)

[IMPLEMENTING A CONTENT-ADDRESSED NIX](https://www.tweag.io/blog/2021-12-02-nix-cas-4/)    

[nix store make-content-addressable](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-store-make-content-addressable.html)

> This command converts the closure of the store paths specified by
> installables to content-addressed form. Nix store paths are usually
> input-addressed, meaning that the hash part of the store path is computed
> from the contents of the derivation (i.e., the build-time dependency graph). 

> By contrast, in a content-addressed path, the hash part is computed from the contents of the path.

[Contributing to Nix documentation](https://nixos.wiki/wiki/Contributing_to_Nix_documentation)


[Here’s a short overview of the different ways to produce a derivation with the Haskell stuff in Nixpkgs](https://discourse.nixos.org/t/why-are-these-derivations-so-different/18257/3)

> Just like stdenv, haskellPackages provides a mkDerivation function. haskellPackages also provides a callPackage function that works similarly to the top-level callPackage. If you dig through the above files, you’ll find that they are defined here:

> This generic Haskell builder is effectively a wrapper around stdenv.mkDerivation for specifically building Haskell packages.

> If you pass this function (or file) to haskellPackages.callPackage, it knows how to automatically find the arguments for Haskell packages like aeson, lens, etc. It also knows to fall back to looking for packages in the top-level Nixpkgs for things that aren’t Haskell libraries. So things like fetchgit, lib, etc will be pulled from the top-level Nixpkgs.

> It is admittedly somewhat confusing that haskellPackages.mkDerivation and stdenv.mkDerivation are named the same, but (completely) different functions (as well as callPackage).

> haskellPackages.callCabal2nix internally uses IFD 1, with all its advantages and disadvantages.

[Import From Derivation](https://nixos.wiki/wiki/Import_From_Derivation). [why have intermediate representation (derivations)?](https://blog.hercules-ci.com/2019/08/30/native-support-for-import-for-derivation/)

> All in all, derivation files save us computation compared to evaluating more than once.

> Acceptable uses of IFD include importing a pinned nixpkgs and automation around lock files. Such uses vastly improve your development workflow, outweighing the slight disadvantages of IFD.

[Status of lang2nix approaches](https://discourse.nixos.org/t/status-of-lang2nix-approaches/14477)

> the approaches to package applications which during their normal build process interact with online repos (Maven, NPM, Cargo, …) to compute the list of dependencies.

> [recursive Nix] replaces IFD with a more distributed build-friendly approach

> would be more pure if we maintain (or convince upstream to do) immutable snapshots of online packages repositories and allow network access only to particular immutable snapshots from within non-fixed-output derivations.


[What is the best dev workflow around nix-shell?](https://discourse.nixos.org/t/what-is-the-best-dev-workflow-around-nix-shell/418)

> a tension between the style nixpkgs expects and the style conducive to development

[Pro-IFD and Anti-IFD](https://discourse.nixos.org/t/another-simple-flake-for-haskell-development/18164/8)

> Pro-IFD: These are people that generally think IFD should be used for packaging things. Most Haskellers fall into this camp (given tools like haskell.nix and callCabal2nix), as well as users of the other FOO2nix tools.

> One unfortunate part of callCabal2nix is that cabal2nix is written in Haskell, so IFD must be used to build the resulting derivation. IFD can often be slower than just doing things with native Nix, and it is not allowed in Nixpkgs.

> This repo provides a callCabal2nixWithoutIFD function that is written in Nix, so it doesn't have either of the above downsides. Cabal files are parsed in Nix directly, so IFD is not needed.

[Eelco Dolstra - the Nix roadmap (NixCon 2018)—content-addressable store](https://www.youtube.com/watch?v=8M6yvJC00J4&t=782s). [needs binary reproducibility](https://youtu.be/8M6yvJC00J4?t=981)

Benefits: deduplication, prevent rebuilds from irrelevant changes.

Without ca, irrelevant changes not only require rebuilds, they take space in the Nix store as well!

> to make this work properly, it really needs perfect binary reproducibility

[Why are there so many ways to reference lib and do they matter?](https://discourse.nixos.org/t/why-are-there-so-many-ways-to-reference-lib-and-do-they-matter/2920)

> The lib in the NixOS module arguments comes from the module system itself and is the preferred way to reference it in NixOS. It’s the only one that doesn’t depend on pkgs and therefore doesn’t lead to infinite recursion when you use it to define modules themselves (which might define overlays, which can influence pkgs). 

[Nix flakes (NixCon 2019)](https://www.youtube.com/watch?v=UeBX7Ide5a0)

[An overview of language support in Nix (NixCon 2019)](https://www.youtube.com/watch?v=nXDumHZI2zg). [comparison of approaches](https://youtu.be/nXDumHZI2zg?t=1071). [snack](https://github.com/nmattia/snack)

> SNACK IS UNMAINTAINED!! It was a fun proof of concept but I don't have the time to take it further.

[Motivation for haskell.nix](https://input-output-hk.github.io/haskell.nix/motivation.html)

The Haskell builder in nixpkgs builds a package sequentially, first the library then the executables and finally the tests. It then executes the tests before the package is considered done. The upshot of this is that packages are only considered done if the test-suites passed. The downside is that if you have to compile multiple packages the likelihood of them failing is low, you have unnecessarily serialized your build. In a more aggressive setting libraries could start building as early as their dependent libraries are built. 

[Practical Nix Flakes](https://serokell.io/blog/practical-nix-flakes)

[Super-Simple Haskell Development with Nix](https://discourse.nixos.org/t/super-simple-haskell-development-with-nix/14287/3)

> Use Nix to get GHC, cabal, and system deps. Then use cabal to download and build all Haskell dependencies:
> The big disadvantage here is that you’re not building any of your Haskell dependencies with Nix, so you don’t get reproducbility, caching, etc.

[How to Setup a Haskell Programming Environment with Nix](https://lambdablob.com/posts/nix-haskell-programming-environment/)

[haskell-packges.nix from Nixpkgs](https://github.com/NixOS/nixpkgs/blob/master/pkgs/top-level/haskell-packages.nix)

[Nixpkgs User’s Guide How to install Haskell packages](https://haskell4nix.readthedocs.io/nixpkgs-users-guide.html)

> The name haskellPackages is really just a synonym for haskell.packages.ghcXYZ (where XYZ is current default GHC version in Nixpkgs),

[Advanced dependency management](https://github.com/Gabriel439/haskell-nix/blob/main/project4/README.md)

[Nixery – Docker images on the fly with Nix](https://news.ycombinator.com/item?id=31079144)

[How Nix and NixOS Get So Close to Perfect](https://news.ycombinator.com/item?id=31139829)

[Nix flakes, and how to convert to them](https://lobste.rs/s/0qifor/nix_flakes_how_convert_them)

[nix-shell, but make it lovely](https://lobste.rs/s/kgnkey/nix_shell_make_it_lovely)

[about flakes](https://twitter.com/GabriellaG439/status/1551724803509276673)

## From discourse

> Is there a way to somehow use allow-newer with haskell packages in nix? I have quite a few dependencies that haven't bumped their version constraints in cabal, so they're all broken.
> For the Haskell stuff in Nixpkgs, there is a doJailbreak function that can be applied to individual packages to allow them to try to build with newer dependencies. You can see some examples of it being used if you grep for doJailbreak in Nixpkgs  pkgs/development/haskell-modules/configuration-common.nix.


I don't think there is a single resource that is recommended above all others, but the [following might be some good reading](https://discord.com/channels/568306982717751326/747637197548552193/948048649290670080):

- Nixpkgs Haskell manual: https://haskell4nix.readthedocs.io/
- A high-level intro to using Nix for Haskellers: https://github.com/cdepillabout/post-about-nix-and-haskell/blob/master/2019-08-03-q-and-as-about-nix-for-haskellers.md
- a quick summary of the main approaches of using Nix to build Haskell stuff: https://discourse.nixos.org/t/super-simple-haskell-development-with-nix/14287/3

[__functor](https://nixos.org/manual/nix/stable/expressions/language-values.html). [how do functors work?](https://github.com/NixOS/nixpkgs/issues/11233). [How to undestand functors in the Nix expression language?](https://stackoverflow.com/questions/50994791/how-to-undestand-functors-in-the-nix-expression-language)

> A set that has a __functor attribute whose value is callable (i.e. is itself a function or a set with a __functor attribute whose value is callable) can be applied as if it were a function, with the set itself passed in first 

[Use `buildInputs` or nativeBuildInputs` for `nix-shell`?](https://discourse.nixos.org/t/use-buildinputs-or-nativebuildinputs-for-nix-shell/8464)

[mkShell needs documentation](https://discourse.nixos.org/t/use-buildinputs-or-nativebuildinputs-for-nix-shell/8464). [impl](https://github.com/NixOS/nixpkgs/blob/master/pkgs/build-support/mkshell/default.nix#L35)

    stdenv.mkDerivation ({
      inherit name;

      buildInputs = mergeInputs "buildInputs";
      nativeBuildInputs = packages ++ (mergeInputs "nativeBuildInputs");
      propagatedBuildInputs = mergeInputs "propagatedBuildInputs";
      propagatedNativeBuildInputs = mergeInputs "propagatedNativeBuildInputs";

      shellHook = lib.concatStringsSep "\n" (lib.catAttrs "shellHook"
        (lib.reverseList inputsFrom ++ [ attrs ]));

[Inspecting Nix lambda function named arguments](https://ops.functionalalgebra.com/2018/04/18/inspecting-nix-lambda-named-arguments/)

[evaluating functions](https://twitter.com/DiazCarrete/status/1556199663132459008)

[nix docs](https://nixos.org/manual/nix/stable/expressions/derivations.html) vs. [nixpg docs](https://nixos.org/manual/nixpkgs/stable/#sec-using-stdenv)

> To build a package with the standard environment, you use the function stdenv.mkDerivation, instead of the primitive built-in function derivation, e.g.

[types of derivations](https://book.divnix.com/ch04-00-derivations.html#types-of-derivations)

> Fixed Output Derivations (FODs)
These are the "leaves" of any build closure, in that, they do not refer to other derivations. These derivations are defined by their content. These derivations are easily differientiated because they will contain a sha256 (or other hash) which is used to enforce that an artifact is reproducible.

> One critical difference from evaluated derivations is that Fixed-Output derivations are able to have access to the network while fetching contents. This "impurity" is offset by enforcing that the hash matches, and reproducibility is delegated to the process which fetchs the assets.

> Many of the fetch* utilities in nixpkgs and nix's builtins will create FODs.

[Nix parallelism & Import From Derivation](https://fzakaria.com/2020/10/20/nix-parallelism-import-from-derivation.html)

[Using PostgreSQL in a nix-shell](https://mgdm.net/weblog/postgresql-in-a-nix-shell/). [Postgresql/Postgis inside nix-shell with sqitch and default postgres user](https://gist.github.com/gusmacaulay/9dc5793439750912458f3c6a8945de7d). [Nix Recipe: Setup Postgresql](https://zeroes.dev/p/nix-recipe-for-postgresql/). [Unable to setup postgres in nix-shell](https://discourse.nixos.org/t/unable-to-setup-postgres-in-nix-shell/14813/2). [trap](https://www.ludovicocaldara.net/dba/bash-tips-7-cleanup-on-exit/)

[Nix Flakes in Production: What, Why and How](https://www.youtube.com/watch?v=o1Y7rWrPEO8)

[How to correctly cache build-time dependencies using Nix](https://www.haskellforall.com/2022/10/how-to-correctly-cache-build-time.html)

[Release 2.8 (2022-04-19)](https://nixos.org/manual/nix/stable/release-notes/rl-2.8.html). [video](https://www.youtube.com/watch?v=ypFLcMCSzNA).

[Difference between `fetchgit` and `fetchGit`](https://discourse.nixos.org/t/difference-between-fetchgit-and-fetchgit/3619)

[devenv.lib.mkShell](https://twitter.com/sridca/status/1608119023857815554)

[zero to nix](https://lobste.rs/s/kf3xym/introducing_zero_nix)

[terraform-nixos-ng: Modern terraform support for NixOS](https://www.haskellforall.com/2023/01/terraform-nixos-ng-modern-terraform.html). [nixos-rebuild](https://www.haskellforall.com/2023/01/announcing-nixos-rebuild-new-deployment.html).

[The hakyll-nix-template Tutorial](https://robertwpearce.com/the-hakyll-nix-template-tutorial.html)

[flake-parts](https://flake.parts/). [Modularize your #Haskell #Nix code using flake-parts and haskell-flake.](https://twitter.com/sridca/status/1624504046307487752)

[zero-to-nix](https://zero-to-nix.com/)

[some notes on using nix](https://lobste.rs/s/eru89e/some_notes_on_using_nix)

[Nix journey part 0: Learning and reference materials](https://news.ycombinator.com/item?id=34987042)

[devenv 0.6](https://lobste.rs/s/a1jo3a/devenv_0_6_generating_containers_instant)

[NixOS in production](https://lobste.rs/s/bbbjfz/nixos_production). [update (Terraform, Integration Testing, CI/CD](https://x.com/GabriellaG439/status/1832494289982820731).

[Quick VMs with NixOS](https://galowicz.de/2023/03/13/quick-vms-with-nixos/)

[Flake Parts in Devenv.sh](https://flake.parts/). [tweet](https://twitter.com/domenkozar/status/1637060871984672769).

[Moving stuff around with Nix](https://determinate.systems/posts/moving-stuff-around-with-nix)

[Nix glossary](https://nixos.org/manual/nix/stable/glossary.html#gloss-closure)

> For a package, the closure of its derivation is equivalent to the build-time dependencies, while the closure of its output path is equivalent to its runtime dependencies.

[nix shell vs nix develop](https://www.reddit.com/r/NixOS/comments/r15hx4/nix_shell_vs_nix_develop/). [good post](https://blog.ysndr.de/posts/guides/2021-12-01-nix-shells/)

> The nix command aims to collect most common commands such as nix-build, nix-copy-closure, nix-env, … as subcommands of one common program. Unsurprisingly, this does not spare nix-shell.

> Yet, unlike some of the other commands which received a more or less one-to-one replacement it is not so easy with nix-shell. This command was actually broken up into multiple commands with different semantics: nix shell, nix develop and nix run. 

[How to write a Nix derivation (using Nix as a make replacement)](https://www.youtube.com/watch?v=bbW6kgB5F2M)

[Support arbitrary fetching of files as Flake inputs](https://github.com/NixOS/nix/issues/5979). [solved here](https://github.com/NixOS/nix/pull/6548)

[How to Learn Nix, Part 47: New and unimproved shells](https://ianthehenry.com/posts/how-to-learn-nix/nix-develop/). [Straightforward way to determine if inside a nix shell](https://github.com/NixOS/nix/issues/6677)

[legacyPackages in flakes](https://discourse.nixos.org/t/using-nixpkgs-legacypackages-system-vs-import/17462/5). [input follows](https://discourse.nixos.org/t/recommendations-for-use-of-flakes-input-follows/17413).

[my first flake](https://gist.github.com/danidiaz/dad21332cc27dbe87d6307f5884dec94)

> it depends on the flake, if the rust overlay for instance just exposes an overlay then you won’t need the follows since the overlay will be applied to your “main” nixpkgs input anyways, I don’t think flake-compat depends on nixpkgs at all, flake-utils claims to be pure nix and thus shouldn’t require nixpkgs either.

> So, in general, you have to reason about each individual case, which, in general, requires some knowledge of the internals of each.

> nix flake metadata will list a graph so you know which follows need to be added:

[follows](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-flake.html#flake-references)

> Most flakes provide their functionality through Nixpkgs overlays or NixOS modules, which are composed into the top-level flake's nixpkgs input; so their own nixpkgs input is usually irrelevant.

[Deploying NixOS using Terraform](https://nix.dev/tutorials/deploying-nixos-using-terraform)

[NixOS: The Ultimate Dev Environment?](https://myme.no/posts/2022-01-16-nixos-the-ultimate-dev-environment.html)

[What Nix Can Do](https://www.youtube.com/watch?v=6Le0IbPRzOE)

[1000 instances of nixpkgs](https://zimbatm.com/notes/1000-instances-of-nixpkgs). [Using nixpkgs.legacyPackages.${system} vs import](https://discourse.nixos.org/t/using-nixpkgs-legacypackages-system-vs-import/17462/6). [discourse](https://discourse.nixos.org/t/1000-instances-of-nixpkgs/17347)

> nixpkgs overlays are super useful. They are a mechanism that allows taking nixpkgs, and extending it with your own packages and overrides. In most cases, it’s more manageable than forking nixpkgs and managing your own long-running branch. NixOS also doesn’t provide a standard way to have other package sets so it makes sense to have them all in one. Those two reasons are what made them popular.

> We need at least one instance of nixpkgs (per system). The question is who is going to hold it.

> For this case to work, another requirement is to use the inputs “follows” feature, so they are both pinned to the same version of nixpkgs.

[nixos-anywhere](https://hachyderm.io/@domenkozar@fosstodon.org/110145895216438132)

[Packaging a Maven applicaiton with Nix](https://fzakaria.com/2020/07/20/packaging-a-maven-application-with-nix.html). [Nix in the Java ecosystem](https://av.tib.eu/media/50710)

> Fixed output derivations (FOD) are derivations that specify the hash of the output contents (Nix typically calculates the hash of the input). These derivations are allowed to perform network access in sandboxed mode.

[nix add-derivation](https://twitter.com/ericson2314_/status/1644816549105004552)

[DERIVATION OUTPUTS IN A CONTENT-ADDRESSED WORLD](https://www.tweag.io/blog/2021-02-17-derivation-outputs-and-output-paths/)

> Need to know whether a derivation has been built locally or in a binary cache? Just check whether its output path exists.

> This is really nice in a world where the output of the derivations are input-addressed, because there’s a direct mapping between a derivation and its output paths − the .drv file actually explicitly contains them − which means that given a derivation Nix can directly know what its output paths are.

> However this falls short with the addition of content-addressed derivations: if hello is content-addressed then I can’t introspect the derivation to know its output path anymore

[output hash](https://nixos.org/manual/nix/stable/language/advanced-attributes.html?highlight=outputHash#adv-attr-outputHash). [When should a fixed output path be used for a derivation in nix?](https://discourse.nixos.org/t/using-fixed-output-paths-for-a-derivation/6338). 

> It sometimes happens that the URL of the file changes, e.g., because servers are reorganised or no longer available. We then must update the call to fetchurl, e.g.,

> If a fetchurl derivation was treated like a normal derivation, the output paths of the derivation and all derivations depending on it would change.

> For fixed-output derivations, on the other hand, the name of the output path only depends on the outputHash* and name attributes

> The #1 reason we use fixed-output derivations is for network downloads. Since we cannot control the network, we disable it during builds to help with reproducibility.

> But what if we do need to download something? We make a compromise: if you’re a fixed-output derivation we enable network access for you, but in return tell me in advance the hash of what you’re going to download and give back as output. This way we retain reproducibility.

[Nix: what are fixed-output derivations and why use them?](https://bmcgee.ie/posts/2023/02/nix-what-are-fixed-output-derivations-and-why-use-them/)

> Irrespective of the build tool being used, when constructing a derivation the problem facing Nix developers is always the same: how do we capture the build dependencies in a reproducible fashion?

> So we have a Gradle-based application, and we want to package it with Nix. The derivation for that might look something like this:

> Well except for one problem: derivations don’t have network access.

> If you were to try and build this derivation you would have Gradle complaining that it can’t resolve any dependencies. We have to work around this limitation, and we do that with a fixed-output derivation.

> Whilst normal derivations are not allowed network access, fixed-output derivations are a compromise for situations like this. They are provided with network access but in return they must declare in advance a hash of their contents.

> Essentially what we have done here is to create an offline Maven repository.

[Restrict fixed-output derivations (2018)](https://github.com/NixOS/nix/issues/2270)

> For example, fetchcargo in Nixpkgs takes a Cargo.lock file as an input and produces an output containing all the dependencies specified in the Cargo.lock file. This is impure, but it works because fetchcargo is a fixed-output derivation. Such impurities are bad for reproducibility because the dependencies on external files are completely implicit: there is no way to tell from the derivation graph that the derivation depends on a bunch of crates fetched from the Internet.

> I don't like the idea where nix tries to solve all package managers in the world at all. There is already enough magic with lang2nix tools, and I don't see what is wrong with approach that we have for rust and go, where are we able to produce deterministic package depenency set. It is not nice and shiny, but reduces magic and gets the job done.

> Ok if I understand correctly, the problem is that fixed output derivations can be arbitrary complex as there are no boundaries from where information can be retrieved from internet. At the same time you lose dependency graph and it becomes time consuming to rebuild fixed output derivations.

> Yeah, I mean, I just don't see this as very realistic. I need a pijul fetcher among other things that simply do not will not ever belong in Nix.

[The Nix Hour #2 overriding derivations, fixed-output derivations, sharing closures](https://www.youtube.com/watch?v=x3EDiAKbnyI)

[Nix Flakes in Production: What, Why and How](https://www.youtube.com/watch?v=o1Y7rWrPEO8)

[Tips and Tricks for Nix Flakes](https://ipetkov.dev/blog/tips-and-tricks-for-nix-flakes/). [Dirty Nix flake quality-of-life hacks](https://siraben.dev/2022/02/13/nix-flake-hacks.html).

> After working with Nix flakes for a while you develop a sense for how to
> interact with them in more efficient or ergonomic ways. That said, a number
> of the interactions I'm about to describe were extremely non-obvious to me,
> especially as someone who had never peeked at their actual implementation.

> Having your flake pull in another flake as an input
> Having your flake pull in an input that is specified by another flake
> Forcing another flake to use an input specified in your flake
> Forcing another flake to use an input specified by yet a different flake

[flake outputs](https://zero-to-nix.com/concepts/flakes#outputs)

> Flake outputs are what a flake produces as part of its build. Each flake can have many different outputs simultaneously

[devenv - Using With Flakes](https://devenv.sh/guides/using-with-flakes/). [Single project with multiple shells](https://devenv.sh/guides/using-with-flakes/#single-project-with-multiple-shells)

> devenv can be integrated with Nix Flakes if you're more familiar with the Nix language and ecosystem.

[Is it possible to merge one flake’s devShell into another flake’s devShell?](https://discourse.nixos.org/t/is-it-possible-to-merge-one-flakes-devshell-into-another-flakes-devshell/18982)

> Unless you create a shell for cross compilation, you shouldn’t use buildInputs directly. Instead prefer packages.

> Also “combining” two shells should work using the inputsFrom argument.

[pkgs.lib.fixedPoints.composeExtensions wtf](https://stackoverflow.com/questions/76023823/how-to-prevent-a-nixpkgs-overlay-from-being-applied-more-than-once). [github](https://github.com/NixOS/nixpkgs/blob/master/lib/fixed-points.nix).

[Overlays in nested flakes](https://discourse.nixos.org/t/overlays-in-nested-flakes/17066)

[overlays](https://hachyderm.io/@DiazCarrete/110207965171306830)

[callPackage, a tool for the lazy](https://summer.nixos.org/blog/callpackage-a-tool-for-the-lazy/)

> callPackage adds more convenience by adding an attribute to the derivation it returns: the override function.

> Benefit: flexible dependency injection

> Each package's dependencies are now implicit at this level (they are still explicit in each of the package files), and callPackage "knows" how to resolve them. This relieves us from dealing with them manually, and precludes configuration errors that may only surface late into a lengthy build process.

[Good Enough](https://www.youtube.com/watch?v=asc1D5yPZhQ)

> Let's talk about software which disrupts the crystal: software which is hard to "nixify." Let's also talk about amazing user experiences that become possible by taking one step back from the edge.

[sub-flakes](https://hackmd.io/@nix-ux/BJwHCL9L9)

[flake-utils](https://github.com/numtide/flake-utils)

> a collection of pure Nix functions that don't depend on nixpkgs, and that are useful in the context of writing other Nix flakes

> flattenTree :: attrs -> attrs

> Nix flakes insists on having a flat attribute set of derivations in various places like the packages and checks attributes.

> This function traverses a tree of attributes (by respecting recurseIntoAttrs) and only returns their derivations, with a flattened key-space.

[recurseIntoAttrs](https://github.com/NixOS/nixpkgs/blob/ff24a05847080bf4edbbebae6c04eb5da4bb97d1/lib/attrsets.nix#L958). [Query all pnames in Nixpkgs with flakes](https://discourse.nixos.org/t/query-all-pnames-in-nixpkgs-with-flakes/22879/2)

> IIRC flake evaluation caching doesn’t work for nested package sets (as nixpkgs is) and thus is not disabled for anything that is in legacyPackages (normal packages has to be a flat attribute set).

> It’s legacyPackages to reflect the fact, that it’s not following the rules for packages, ie it’s not flat but a set of sets.

[what is legacyPackages?](https://github.com/NixOS/nixpkgs/blob/d85555f9ac2154b5e39cfda10a74e2b7d9cc81ad/flake.nix#L47)

> The "legacy" in `legacyPackages` doesn't imply that the packages exposed
> through this attribute are "legacy" packages. Instead, `legacyPackages`
> is used here as a substitute attribute name for `packages`. The problem
> with `packages` is that it makes operations like `nix flake show
> nixpkgs` unusably slow due to the sheer number of packages the Nix CLI
> needs to evaluate. But when the Nix CLI sees a `legacyPackages`
> attribute it displays `omitted` instead of evaluating all packages,
> which keeps `nix flake show` on Nixpkgs reasonably fast, though less
> information rich.

[--override-inputs](https://github.com/NixOS/nix/issues/4193). [Override flakes inputs transitively](https://discourse.nixos.org/t/override-flakes-inputs-transitively/16903). [manual](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-build.html).

[Propagate output with overlay between two linked flakes?](https://discourse.nixos.org/t/propagate-output-with-overlay-between-two-linked-flakes/16137)

```
$ nix repl
nix-repl> :lf .
```

[Why extending nixpkgs.legacyPackages behaves differently then extending flake packages?](https://discourse.nixos.org/t/why-extending-nixpkgs-legacypackages-behaves-differently-then-extending-flake-packages/24521). [makeExtensible](https://github.com/NixOS/nixpkgs/blob/9fc18a93a319ba2deea68a4d3bdd73b4dc65a8b1/lib/fixed-points.nix#L105). [Overlay/overriding improvement plan](https://github.com/NixOS/nixpkgs/issues/99100).

> my-pkgs = nixpkgs.legacyPackages.${system}.extend (overlay);

```
nix-repl> r = import <nixpkgs> {}
nix-repl> builtins.typeOf (r.extend (final : prev : prev))
"set"
```

> The amount of overlays that get evaluated with .extend is quadratic. Every new .extend access evaluates all previous overlays again.

[Extending NixOS configurations](https://determinate.systems/posts/extending-nixos-configurations). Interesting example of composition...

[recent news about Haskell-on-Nix](https://discourse.nixos.org/t/nix-haskell-development-2020/6170/28?u=danidiaz)

> People have seemed to get pretty comfortable with functions like haskellPackages.callCabal2nix, haskellPackage.callHackage, haskellPackages.developPackage, and haskellPackages.shellFor. You’re starting to really see a lot of use of these, which makes things pretty easy.

[The Nix, OpenGL and Ubuntu Integration Nightmare](https://lobste.rs/s/7h20zl/nix_opengl_ubuntu_integration_nightmare)

[Haskell project that uses Nix](https://twitter.com/sridca/status/1649484166495436800)

[Nix journey](https://twitter.com/mitchellh/status/1649503702456340483)

[Build a Jekyll blog with Nix using flakes](https://www.reddit.com/r/NixOS/comments/10a0m6o/build_a_jekyll_blog_github_pages_with_nix_using/)

[debugging effectively with break](https://discourse.nixos.org/t/how-to-use-builtins-break-effectively/23115)

>  nix develop --debugger --ignore-try 

[ruby-nix](https://github.com/sagittaros/ruby-nix)

[Nix why-depends](https://twitter.com/ProgrammerDude/status/1662744672811319297)

[cleanSource](https://github.com/NixOS/nixpkgs/blob/1c10051e58f643a199bfe8a1e634d12940f9522f/lib/sources.nix). [gitignore.nix](https://github.com/hercules-ci/gitignore.nix). [readTree](https://code.tvl.fyi/about/nix/readTree).  

[Filtering Source Trees with Nix and Nixpkgs](https://discourse.nixos.org/t/filtering-source-trees-with-nix-and-nixpkgs/19148). [clean the source](https://stonecode.ca/clean-the-source/). [reddit](https://www.reddit.com/r/NixOS/comments/nrhiof/clean_the_source_libcleansource/). [mastodon](https://hachyderm.io/@DiazCarrete/110798585198356457).

> Omitting cleanSource will not break your derivation, but it does make it much more difficult to get repeatable builds. In particular, if you are doing in-tree builds, symbolic links created by nix-build will change the source tree after every build. A simple change to the derivation eliminates much of the cruft in your source directory, and helps achieve repeatable builds.

> nix-repl> p = import <nixpkgs> {}
> nix-repl> cleaned = p.lib.cleanSource ./foldy2
> nix-repl> cleaner
> nix-repl> cleaned
> { _isLibCleanSourceWith = true; filter = «lambda @ /nix/store/spmy084a6l0phb574zdbb2zm6bb737b3-nixpkgs/nixpkgs/lib/sources.nix:105:16»; name = "source"; origSrc = /tmp/nixtest/foldy2; outPath = "/nix/store/pik4ddl1wm8kp3ir3zmld1jg4nbyfnwp-source"; }


[A path (e.g., ../foo/sources.tar) causes the referenced file to be copied to the store; its location in the store is put in the environment variable.](https://nixos.org/manual/nix/stable/language/derivations.html). [Relative path support for Nix flakes](https://discourse.nixos.org/t/relative-path-support-for-nix-flakes/18795). [ You know nix allows relative paths to be used,](https://nixos.org/guides/nix-pills/nix-store-paths.html#idm140737319582576). [When does a Nix path type make it into the Nix store when converted to a string and when not?](https://stackoverflow.com/questions/43850371/when-does-a-nix-path-type-make-it-into-the-nix-store-when-converted-to-a-string). [When is a path in a Nix expression copied into the Nix store?](https://discourse.nixos.org/t/when-is-a-path-in-a-nix-expression-copied-into-the-nix-store/27052).

> Now inspect the .drv to see where is ./myfile being stored

> Great, how did nix decide to use xv2iccirbrvklck36f1g7vldn5v58vck ? Keep looking at the nix comments.

> Note: doing nix-store --add myfile will store the file in the same store path.

> The copying of files into /nix/store happens at the time of nix-instantiate [is this correct?] the evaluation of nix expressions is still purely functional (no copying around happens at evaluation time), but instantiation ("building") is not.

[nix-instantiate](https://nixos.org/manual/nix/stable/command-ref/nix-instantiate.html). [What is the purpose of nix-instantiate? What is a store-derivation?](https://stackoverflow.com/questions/31490262/what-is-the-purpose-of-nix-instantiate-what-is-a-store-derivation). [nix diff](https://www.haskellforall.com/2017/11/compare-nix-derivations-using-nix-diff.html).

> nix-instantiate converts Nix source code to Nix derivations

> nix-store --realise converts Nix derivations to Nix build products

[type-path](https://nixos.org/manual/nix/stable/language/values.html#type-path)

> When an interpolated string evaluates to a path, the path is first copied into the Nix store and the resulting string is the store path of the newly created store object.

> nixtest$ nix repl
> nix-repl> "${./foo.txt}"
> "/nix/store/lz4553i89z3abxvsc9xpp6dx0gbinzyb-foo.txt"

[Haskell for all: How to use NixOS for lightweight integration tests](https://www.haskellforall.com/2020/11/how-to-use-nixos-for-lightweight.html). [QEMU vs. KVM: Exploring the Virtualization Giants](https://cloudzy.com/blog/qemu-vs-kvm/). [Difference between KVM and QEMU](https://serverfault.com/questions/208693/difference-between-kvm-and-qemu#_=_). 

[impure nix derivations](https://hackmd.io/@garbas/ByIFRQhSj). [A way to list all locally realised fixed output derivations](https://github.com/NixOS/nix/issues/6508).

> let pkgs = import <nixpkgs> {};
>  in
> pkgs.stdenv.mkDerivation {
>   name = "impure";
>   __impure = true; # marks this derivation as impure
>   buildCommand = "date > $out";
> }

> $ nix build --json -v --print-out-paths -f foo.nix

> $ nix realisation info --impure --json -f foo.nix
> this derivation will be built:
>   /nix/store/32pdpzaj793kg4q1paxc6bhzhnf93n8j-impure.drv
> error: cannot operate on an output of the unbuilt derivation 'sha256:ddffc26775f61118da8597d1f2f62c544ec92461b31b5b1075ed8689a7ee8292!out' 

For a pure derivation, this works:

> $ nix build --json -v --print-out-paths -f bar.nix
> [{"drvPath":"/nix/store/0n0g5z00dd0rnjrjfvc7pa5pd8smb1a3-impure.drv","outputs":{"out":"/nix/store/q5y3d3bzy9j0y2rh7gxh9r4492fihs2i-impure"},"startTime":0,"stopTime":0}]

And this:

> $ nix path-info --derivation /nix/store/q5y3d3bzy9j0y2rh7gxh9r4492fihs2i-impure
> /nix/store/0n0g5z00dd0rnjrjfvc7pa5pd8smb1a3-impure.drv

What! This does work! How to go in the opposite direction?

> $ nix-store --query --deriver /nix/store/pkiv6mw6cbivnj9cam44gb94q9lm6asq-impure
> /nix/store/cgyaqn1pzfhvrn6m758bnfl0bfs9ri47-impure.drv

[nixos and flakes for beginners](https://nixos-and-flakes.thiscute.world/)

> An operating system consists of various software packages, configuration files, and text/binary data, all of which represent the current state of the system. Declarative configuration can manage only the static portion of this state. Dynamic data, such as PostgreSQL, MySQL, or MongoDB data, cannot be effectively managed through declarative configuration(It is not feasible to delete all new PostgreSQL data that is not declared in the configuration during each deployment). Therefore, NixOS primarily focuses on managing a portion of the system state in a declarative manner. Dynamic data mentioned above, along with the contents in the user's home directory, remain unaffected by NixOS when rolling back to a previous generation.

[super colliding Nix stores](https://discourse.nixos.org/t/super-colliding-nix-stores/28462/11)

[Spot-Checking Build Determinism](https://nixos.org/manual/nix/stable/advanced-topics/diff-hook.html)

> error: derivation '/nix/store/cgl13lbj1w368r5z8gywipl1ifli7dhk-unstable.drv' may not be deterministic

[Dirty Nix flake quality-of-life hacks](https://siraben.dev/2022/02/13/nix-flake-hacks.html)

[trying to run the NixOS tests in WSL2](https://github.com/microsoft/WSL/issues/4193)

> error: a 'x86_64-linux' with features {kvm, nixos-test} is required to build '/nix/store/5zlxjs9xfb98yqhs1q4xsd15j81bcb2g-vm-test-run-unnamed.drv', but I am a 'x86_64-linux' with features {benchmark, big-parallel, ca-derivations, nixos-test, uid-range}

[Customizing packages in Nix](https://bobvanderlinden.me/customizing-packages-in-nix/)

[issues plaging Nix](https://lobste.rs/s/cojupc/many_issues_plaguing_nix)

[stop using nix-env](https://stop-using-nix-env.privatevoid.net/)

> It picks packages by attribute name rather than derivation name and it keeps track of the attribute path from which each package was installed, meaning name collisions when upgrading are eliminated.

[The Nix Hour](https://www.youtube.com/watch?v=5V1OFSa7VlQ&list=PLyzwHTVJlRc8yjlx4VR4LU5A5O44og9in)

[Nix does not guarantee reproducibility](https://github.com/NorfairKing/nix-does-not-guarantee-reproducibility). [tweet](https://twitter.com/kerckhove_ts/status/1691729905711456375).

[haskell-flake](https://discourse.haskell.org/t/haskell-flake-0-4-0-released-with-easy-overrides/7391)

> It replaces stack only, in practice. You still use cabal (the executable) in the dev shell―along with the .cabal file which defines the dependencies and other metadata) to build.

[Flake schemas: Making flake outputs extensible](https://determinate.systems/posts/flake-schemas). [hn](https://news.ycombinator.com/item?id=37338857).

[did maven.buildMavenPackage get better?](https://hachyderm.io/@pmidden@fosstodon.org/110989724631869303). [manual](https://nixos.org/manual/nixpkgs/unstable/#maven)

[Nix Flake Architecture in Practice](https://journal.platonic.systems/nix-flake-architecture-in-practice/)

[about nix flakes](https://lobste.rs/s/ytosdr/experimental_does_not_mean_unstable). [criticism](https://lobste.rs/s/wamkim/nix_flakes_is_experiment_did_too_much_at)

[NixCon 2023](https://media.ccc.de/b/conferences/nixcon/nixcon2023)

[microvm.nix](https://www.youtube.com/watch?v=iGteDsnlCoY)

[Nixify your haskell project: Introduction](https://discourse.haskell.org/t/nixify-your-haskell-project-introduction/7578)

[Haskell bindings for the new Nix C API](https://twitter.com/sandy_doo/status/1701219791183249661). [PR](https://github.com/NixOS/nix/pull/8699).

[An overview of Nix in practice](https://www.slice.zone/blog/nix-in-practice). [lobste.rs](https://lobste.rs/s/hhfiyd/overview_nix_practice)

[package naming conventions in Nix](https://discourse.nixos.org/t/how-to-tell-the-difference-between-wrapped-and-unwrapped-package/6823/5)

[notes about Nix flakes](https://jvns.ca/blog/2023/11/11/notes-on-nix-flakes/)

[Why you don't need flake-utils](https://ayats.org/blog/no-flake-utils/). [lobsters](https://lobste.rs/s/bx45ly/flaketools_simpler_less_bug_prone_flake).

[source filtering with file sets](https://www.tweag.io/blog/2023-11-28-file-sets/)

[Flakes aren't real and can't hurt you](https://lobste.rs/s/exlaeq/flakes_aren_t_real_cannot_hurt_you_guide)

[nix upgrade-nix](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-upgrade-nix)

[Using nixpkgs.legacyPackages.${system} vs import](https://discourse.nixos.org/t/using-nixpkgs-legacypackages-system-vs-import/17462). [more](https://discourse.nixos.org/t/using-nixpkgs-legacypackages-system-vs-import/17462/17). [Flake format](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-flake#flake-format)

> Note also that the flake registry by default sets nixpkgs to the unstable branch, and updates this automatically when you run nix commands after a time out of - I believe - a few hours. This is also why e.g. nix run nixpkgs#package will almost always download stuff by default (the latest nixpkgs unstable).

> In addition to the outputs of each input, each input in inputs also contains some metadata about the inputs. These are:

> outPath: The path in the Nix store of the flake's source tree. This way, the attribute set can be passed to import as if it was a path, as in the example above (import nixpkgs). [NOT RECOMMENDED, USE legacyPackages INSTEAD]

[Question regarding flake inputs: Why do they have to be a static set and can not be "calculated"](https://www.reddit.com/r/NixOS/comments/176ygv0/question_regarding_flake_inputs_why_do_they_have/)

[flake inputs](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-flake#flake-inputs). [indirect inputs (through the flake registry)](https://nixos.org/manual/nix/stable/command-ref/new-cli/nix3-flake#types)

> It is also possible to omit an input entirely and only list it as expected function argument to outputs. Thus,
> 
> outputs = { self, nixpkgs }: ...;
> without an inputs.nixpkgs attribute is equivalent to
> 
> 
> inputs.nixpkgs = {
>   type = "indirect";
>     id = "nixpkgs";
>     };
>

[how to debug flakes](https://discourse.nixos.org/t/debugging-a-flake/14898/2)

> nix-repl> :load-flake .

[Haskell section of the Nixpkgs manual](https://nixos.org/manual/nixpkgs/unstable/#haskell). [incremental builds](https://nixos.org/manual/nixpkgs/unstable/#haskell-incremental-builds)

> when you want to override the arguments passed to haskellPackages.mkDerivation. For this, the function overrideCabal from haskell.lib.compose is used

[derivations](https://nixos.org/manual/nix/stable/language/derivations.html)

> You can refer to each output of a derivation by selecting it as an attribute. The first element of outputs determines the default output and ends up at the top-level.

[Ephemeral Environments with Nix Shell](https://www.youtube.com/watch?v=0ulldVwZiKA)

[RPATH, or why lld doesn’t work on NixOS](https://matklad.github.io/2022/03/14/rpath-or-why-lld-doesnt-work-on-nixos.html). [HN](https://news.ycombinator.com/item?id=30688815).

> Curious observation: dynamic linking on NixOS is not entirely dynamic. Because executables expect to find shared libraries in specific locations marked with hashes of the libraries themselves, it’s not possible to just upgrade .so on disk for all the binaries to pick it up.

> `patchelf` solves a different problem: it fixes up an already built binary. Here, I am building the binary myself, so I’d rather make that just work without any extra build steps.

> Patchelf is indispensible for beating sense into third-party closed-source shared objects.

[How to know whether evaluation is (im)pure during runtime?](https://discourse.nixos.org/t/how-to-know-whether-evaluation-is-im-pure-during-runtime/20795). [How to tell what's making a flake impure?](https://discourse.nixos.org/t/how-to-tell-whats-making-a-flake-impure-inherit-macos-security/26105). [How to use builtins.currentSystem in flake output?](https://discourse.nixos.org/t/how-to-use-builtins-currentsystem-in-flake-output/10489). [Mastodon](https://hachyderm.io/@DiazCarrete/111948405408131247).

```
~$ env FOO=foo nix eval --expr 'builtins.getEnv "FOO"'
""
~$ env FOO=foo nix eval --impure --expr 'builtins.getEnv "FOO"'
"foo"
```

[How can we pass argument to flake.nix?](https://discourse.nixos.org/t/how-can-we-pass-argument-to-flake-nix/30833). [Override flakes inputs transitively ](https://discourse.nixos.org/t/override-flakes-inputs-transitively/16903). [Allow plain Nix expressions as flake inputs](https://github.com/NixOS/nix/issues/5663).

[Dirty Nix flake quality-of-life hacks](https://siraben.dev/2022/02/13/nix-flake-hacks.html)

[nix/readTree](https://code.tvl.fyi/about/nix/readTree)

[Managing dotfiles on macOS with Nix](https://lobste.rs/s/usq8dk/managing_dotfiles_on_macos_with_nix)

[Practical Nix flake anatomy: a guided tour of flake.nix](https://vtimofeenko.com/posts/practical-nix-flake-anatomy-a-guided-tour-of-flake.nix/)

[cabal2nix and system libraries](https://www.reddit.com/r/haskell/comments/1e3615y/cabal2nix_and_system_libraries_a_short_quirk/)

[Making a dev shell with nix flakes](https://fasterthanli.me/series/building-a-rust-service-with-nix/part-10)

[NixOS available WSL2?](https://x.com/tritlo/status/1816455336426975533). [repo](https://github.com/nix-community/NixOS-WSL).

[transitive models of ZFC](https://math.stackexchange.com/questions/4654388/difference-between-transitive-and-non-transitive-models)

[specialisations](https://www.reddit.com/r/NixOS/comments/1ec9xwm/specialisations_are_pretty_dope/)

[congruent configuration](https://github.com/cachix/devenv/issues/1362)

[An unordered list of hidden gems inside NixOS](https://kokada.dev/blog/an-unordered-list-of-hidden-gems-inside-nixos/)

[NixOS & Flakes Book. An unofficial book for beginners](https://nixos-and-flakes.thiscute.world/introduction/)

[NixOS-wsl](https://nix-community.github.io/NixOS-WSL/install.html). [repo](https://github.com/nix-community/NixOS-WSL). [How to configure NixOS-WSL with flakes](https://nix-community.github.io/NixOS-WSL/how-to/nix-flakes.html).

[My NixOS Dotfiles Explained](https://haseebmajid.dev/posts/2023-09-12-how-i-configure-nixos-as-part-of-my-development-workflow/)

[NixOS with Home Manager](https://nixos-and-flakes.thiscute.world/nixos-with-flakes/start-using-home-manager). [Home Manager Manual](https://nix-community.github.io/home-manager/index.xhtml)

> NixOS primarily focuses on managing the static portion of the system state in a declarative manner. Dynamic data, along with the contents in the user's home directory, remain unaffected by NixOS when rolling back to a previous generation.

> NixOS can only manage system-level configuration. To manage user-level configuration in the Home directory, we need to install Home Manager

> There are many software packages or configurations that can be set up using either NixOS Modules (configuration.nix) or Home Manager (home.nix), which brings about a choice dilemma: What is the difference between placing software packages or configuration files in NixOS Modules versus Home Manager, and how should one make a decision?

[Docker on NixOS](https://nixos.wiki/wiki/Docker)

[Dropping Home-Manager](https://ayats.org/blog/no-home-manager)

[nix develop doesn't remove the environment by default](https://nix.dev/manual/nix/2.22/command-ref/new-cli/nix3-develop#opt-ignore-environment)   

[lightweight Nix flake template for Haskell repositories](https://github.com/Gabriella439/haskell-flake)

[Nix diagram](https://x.com/GabriellaG439/status/1838126507568558182)

[[r/NixOS] Agenix + Passage Secrets management](https://www.reddit.com/r/NixOS/comments/1foipsn/agenix_passage_secrets_management/)

[Nix hashes in Nix](https://wastedintel.ca/2024/09/23/git-hashes-in-nix/)

[example-static-haskell-nix](https://github.com/cdepillabout/example-static-haskell-nix). [twitter](https://x.com/cdepillabout/status/1840357879863464188).

> an example repo of how to build a fully statically-linked x86-64 Linux #Haskell binary using #Nix

[NixOs and Flakes](https://nixos-and-flakes.thiscute.world/other-usage-of-flakes/inputs)

[Nix - Death by a thousand cuts](https://www.dgt.is/blog/2025-01-10-nix-death-by-a-thousand-cuts/)

[Towards a content-addressed model for Nix](https://www.tweag.io/blog/2020-09-10-nix-cas/)

> Most distributions, by default, don’t rebuild packages when their dependencies change, and have a (more-or-less automated) process to detect changes that require rebuilding reverse dependencies. For example, Debian tries to detect ABI changes automatically and Fedora has a more manual process. But Nix doesn’t.

[nix repl and flakes](https://hachyderm.io/@DiazCarrete/114229083591211399). [learn to use the Nix repl effectively](https://aldoborrero.com/posts/2022/12/02/learn-how-to-use-the-nix-repl-effectively/). 

[Should you have every flake follow nixpkgs?](https://www.reddit.com/r/NixOS/comments/1jbgmqw/should_you_have_every_flake_follow_nixpkgs/). [1000-instances-of-nixpkgs](https://zimbatm.com/notes/1000-instances-of-nixpkgs). [and technically doesn't help prevent incompatibilities from occurring, but I could be wrong about this as I am still a relative Nix newbie)](https://discourse.nixos.org/t/recommendations-for-use-of-flakes-input-follows/17413). [What is the purpose of input follows in a flake?](https://www.reddit.com/r/NixOS/comments/1bt8gfq/what_is_the_purpose_of_input_follows_in_a_flake/). [Automatic Nix flake follows](https://fzakaria.com/2024/07/31/automatic-nix-flake-follows.html)

> What pinning inputs.follows essentially does is to reuse the same instance of that pinned input, instead of managing a separate dependency for that flake input. This speeds up evaluation times 

> I depends on the flake, if the rust overlay for instance just exposes an overlay then you won’t need the follows since the overlay will be applied to your “main” nixpkgs input anyways, I don’t think flake-compat depends on nixpkgs at all, flake-utils claims to be pure nix and thus shouldn’t require nixpkgs either.

[installables docs](https://nix.dev/manual/nix/2.26/command-ref/new-cli/nix#installables). [document the "installable" concept](https://github.com/NixOS/nix/issues/11105)  

> If attrpath is omitted, Nix tries some default values; for most subcommands, the default is packages.system.default (e.g. packages.x86_64-linux.default), but some subcommands have other defaults. If attrpath is specified, attrpath is interpreted as relative to one or more prefixes; for most subcommands, these are packages.system, legacyPackages.*system* and the empty prefix. Thus, on x86_64-linux nix build nixpkgs#hello will try to build the attributes packages.x86_64-linux.hello, legacyPackages.x86_64-linux.hello and hello.

> If attrpath begins with . then no prefixes or defaults are attempted. This allows the form flakeref[#.attrpath], such as github:NixOS/nixpkgs#.lib.fakeSha256 to avoid a search of packages.*system*.lib.fakeSha256

[flake outputs](https://nixos-and-flakes.thiscute.world/other-usage-of-flakes/outputs#flake-outputs)

> Actually, we can also customize the location of the flake and the name of the NixOS configuration instead of using the defaults. This can be done by adding the --flake parameter to the nixos-rebuild command. Here's an example:

> sudo nixos-rebuild switch --flake /path/to/your/flake#your-hostname

[vscode in nixos](https://www.reddit.com/r/NixOS/comments/14p3q7t/comment/jqgh5x0/). [wiki](https://nixos.wiki/wiki/Visual_Studio_Code). [unfree software](https://nixos.wiki/wiki/Unfree_Software).

> With VS Code on Nix you’ve got two options. You can manage everything, including plugins and version declaratively (i.e. the Nix-iest way of doing it) or alternatively use the VSCode-FHS wrapper that essentially hides your filesystem from the application and makes it think it’s running on a traditional system, thereby allowing you to set plugins, version, etc. in the way you might be more accustomed to. There’s also a Flatpak version which may see slightly faster updates and similar performance to the -FHS wrapper.

[Module System and Custom Options](https://nixos-and-flakes.thiscute.world/other-usage-of-flakes/module-system). [Import list in `configuration.nix` vs `import` function](https://discourse.nixos.org/t/import-list-in-configuration-nix-vs-import-function/11372/6)

[Confused: configuration.nix vs module in flake](https://www.reddit.com/r/NixOS/comments/1fkt4rq/confused_configurationnix_vs_module_in_flake/)

> Also, to wrap it [configuration.nix], from the flake you call nixpkgs.lib.nixosSystem and import the module that way

[`nix store gc` equivalent to `–delete-older-than`?](https://discourse.nixos.org/t/nix-store-gc-equivalent-to-delete-older-than/31767). [nix profile wipe-history](https://nix.dev/manual/nix/2.25/command-ref/new-cli/nix3-profile-wipe-history)

> nix-collect-garbage --delete-old

[home.file, home-manager](https://discourse.nixos.org/t/deploy-files-into-home-directory-with-home-manager/24018/2). [docs](https://nix-community.github.io/home-manager/options.xhtml#opt-home.file). [reddit](https://www.reddit.com/r/NixOS/comments/1c3tgs2/comment/kzj529x/). 

[How to manage user configuration with flakes without home manager on nixos-21.05?](https://discourse.nixos.org/t/how-to-manage-user-configuration-with-flakes-without-home-manager-on-nixos-21-05/16102/11).

> trying to do a complex user-focused nixos without home manager essentially ends up being rewriting home manager, because you need to sort the problem of writing files from a nix build into $HOME and handling user services. Neither is trivial

[Home manager flake NixOS module](https://nix-community.github.io/home-manager/index.xhtml#sec-flakes-nixos-module). [Getting Started with Home Manager](https://nixos-and-flakes.thiscute.world/nixos-with-flakes/start-using-home-manager)

> According to the official Home Manager Manual, to install Home Manager as a module of NixOS, we first need to create /etc/nixos/home.nix. 

> There are many software packages or configurations that can be set up using either NixOS Modules (configuration.nix) or Home Manager (home.nix), which brings about a choice dilemma: What is the difference between placing software packages or configuration files in NixOS Modules versus Home Manager, and how should one make a decision?

[managing configurations with Git](https://nixos-and-flakes.thiscute.world/nixos-with-flakes/other-useful-tips#managing-the-configuration-with-git)

[runCommand](https://nixos-and-flakes.thiscute.world/development/intro#creating-a-development-environment-with-pkgs-runcommand). [trivial builders](https://ryantm.github.io/nixpkgs/builders/trivial-builders/). [why the need of makeWrapper](https://gist.github.com/CMCDragonkai/9b65cbb1989913555c203f4fa9c23374). [more](https://discourse.nixos.org/t/makewrapper-vs-buildinputs/21474). [more on inputs](https://gist.github.com/CMCDragonkai/45359ee894bc0c7f90d562c4841117b5). [nativeBuildInputs and cross-compiling (old)](https://github.com/NixOS/nixpkgs/issues/19370). [more](https://nixos.wiki/wiki/Development_environment_with_nix-shell). [how to package](https://unix.stackexchange.com/questions/717168/how-to-package-my-software-in-nix-or-write-my-own-package-derivation-for-nixpkgs).

> buildInputs simply make the listed packages available to the build environment. It is up to the individual build systems to ensure that runtime dependencies are available at runtime. The ld wrapper included in the standard environment does this automatically for ELF libraries but for programs, you may need to do it manually using a wrapper or by hardcoding the path into the executable using a patch.

> The comments in the code snippets on nativeBuildInputs and buildInputs above might seem pedantic --- who cares about build-time vs run-time when we're just making a dev environment, not a real package! However, the distinction becomes of practical importance if one wants a cross compilation development environment [...] nativeBuildInputs would be for the native platform, while buildInputs would be for the foreign platform

[the official docs for nativeBuildInputs](https://nixos.org/manual/nixpkgs/stable/#variables-specifying-dependencies)

> [nativeBuildInputs] This could be called depsBuildHost but nativeBuildInputs is used for historical continuity.

> [buildInputs] This would be called depsHostTarget but for historical continuity.

> buildInputs [...] are often programs and libraries used by the new derivation at run-time, but that isn’t always the case. For example, the machine code in a statically-linked library is only used at run-time, but the derivation containing the library is only needed at build-time.

[cross-compilation at nix.dev](https://nix.dev/tutorials/cross-compilation.html)

[Setting up tmux with nix home-manager](https://haseebmajid.dev/posts/2023-07-10-setting-up-tmux-with-nix-home-manager/). [programs.tmux.extraConfig](https://nix-community.github.io/home-manager/options.xhtml#opt-programs.tmux.extraConfig). [readFile](https://nix.dev/manual/nix/2.25/language/builtins.html#builtins-readFile) [In configuration.nix can I read a value from a file?](https://discourse.nixos.org/t/in-configuration-nix-can-i-read-a-value-from-a-file/4809/1)

[units of composition: recipes, overlays, and packages](https://archive.fosdem.org/2024/events/attachments/fosdem-2024-3107-units-of-composition-recipes-overlays-and-packages/slides/22506/flox_VEN2Zai.pdf). [video](https://archive.fosdem.org/2024/schedule/event/fosdem-2024-3107-units-of-composition-recipes-overlays-and-packages/).

[Package parameters and overrides with callPackage](https://nix.dev/tutorials/callpackage.html)

[home.sessionPath](https://nix-community.github.io/home-manager/options.xhtml#opt-home.sessionPath)

[home-manager flake in a standalone setup in non-NixOS systems](https://nix-community.github.io/home-manager/index.xhtml#sec-flakes-standalone)

[How to run non-nix executables on NixOS?](https://nix.dev/guides/faq#how-to-run-non-nix-executables)

[home-manager: Using the same home-manager config across multiple machines with different usernames](https://www.reddit.com/r/NixOS/comments/10tu984/using_the_same_homemanager_config_across_multiple/). [How to set up a configuration for multiple users/machines?](https://nix-community.github.io/home-manager/index.xhtml#_how_to_set_up_a_configuration_for_multiple_users_machines). [modularizing home.nix](https://discourse.nixos.org/t/is-this-a-good-way-to-modularize-home-manager-home-nix-for-home-work/5817)

> Optionally, use home-manager.extraSpecialArgs to pass arguments to home.nix

[home manager: dotfiles management](https://gvolpe.com/blog/home-manager-dotfiles-management/)

[home-manager.extraSpecialArgs](https://nix-community.github.io/home-manager/nixos-options.xhtml#nixos-opt-home-manager.extraSpecialArgs)

Example of how to substitute home-manager defined variables:

```
home.sessionPath = ["${config.home.homeDirectory}zzz"]
```

[home.username and home.homeDirectory in home.nix, mandatory for NixOS?](https://discord.com/channels/568306982717751326/570351771336310804/1356010317632635132) 

> only mandatory for standalone, as home manager's nixos module can grab those values from the nixos options set

> and as such, for the hm nixos module, you do not need to set programs.home-manager.enable in HM, as that only adds the CLI which is for managing standalone installations

[Appendix A. Home Manager Configuration Options](https://nix-community.github.io/home-manager/options.xhtml)

> Whereas option values can generally depend on other option values thanks to laziness, this does not apply to imports, which must be computed statically before anything else.

A possible example of importing something into home.nix?

```
{ config, pkgs, ... }:

{
 imports = [ ./foo.nix ];
  programs.home-manager.enable = true;
  }
```

[NixOS modules (Nixwiki)](https://nixos.wiki/wiki/NixOS_modules). [modules — NixOS quickstart](https://bits.raccoon.fun/nixos-quickstart/modules/modules.html). [Writing NixOS modules](https://nixos.org/manual/nixos/stable/index.html#sec-writing-modules).

[Making NixOS modules for fun and (hopefully) profit](https://xeiaso.net/talks/asg-2023-nixos/). [video](https://www.youtube.com/watch?v=SzyuLVzS5Fg). [](). [Basic NixOS Modules](https://www.youtube.com/watch?v=-Bfo3Byjwyg). [NixOS videos](https://www.youtube.com/watch?v=a67Sv4Mbxmc&list=PLko9chwSoP-15ZtZxu64k_CuTzXrFpxPE) [about modules](https://www.youtube.com/watch?v=vYc6IzKvAJQ&list=PLko9chwSoP-15ZtZxu64k_CuTzXrFpxPE&index=22). [module system](https://nix.dev/tutorials/module-system/index.html). [A basic module](https://nix.dev/tutorials/module-system/a-basic-module/index.html). [Declaring an IDE with evalModules](https://www.youtube.com/watch?v=WsU7sQvIh0U).

[Understanding NixOS Modules and Declaring Options](https://discourse.nixos.org/t/understanding-nixos-modules-and-declaring-options-blog-post/58932)

[`lib` could be a supported output in flakes](https://github.com/NixOS/nix/issues/4744)

[Difference between a module’s config property and directly defining](https://discourse.nixos.org/t/difference-between-a-modules-config-property-and-directly-defining-options/14972/2)

> As for the difference between putting definitions under config or not, it’s just because doing so is optional if you’re not also declaring options. Just makes config-only files (like a typical beginner’s configuration.nix) a little cleaner looking. Once you want to declare some new options though, you have to put your config definitions under config.

[nixosOptionsDoc](https://bmcgee.ie/posts/2023/03/til-how-to-generate-nixos-module-docs/)

[Handling Secrets in NixOS: An Overview (git-crypt, agenix, sops-nix, and when to use them)](https://discourse.nixos.org/t/handling-secrets-in-nixos-an-overview-git-crypt-agenix-sops-nix-and-when-to-use-them/35462)

> I’d be much more careful with this statement. Security without a threat model is somewhat vague, of course, but a lot of measures that NixOS as well as pretty much all services that deal with secrets provide depend on it being difficult to cross the user barrier.

> Most services will have their own users - not just humans - to prevent other (potentially exploited) services from being able to interfere with them. If you add secrets to your nix store, all systemd “hardening” becomes basically useless at protecting those secrets, and if user passwords are some of those secrets all other on-host security measures break down.

> sops is pretty explicit about public repos being a threat in the eyes of their threat model 246. I imagine similar things apply to agenix.

> A vulnerability in AES256_GCM could potentially leak the data key or the KMS master key used by a SOPS encrypted file. While no such vulnerability exists today, we recommend that users keep their encrypted files reasonably private.

[agenix threat model](https://github.com/ryantm/agenix/blob/main/README.md#threat-modelwarnings). [Harvest now, decrypt later](https://en.wikipedia.org/wiki/Harvest_now,_decrypt_later).

>  Additionally you should only encrypt secrets that you are able to make useless in the event that they are decrypted in the future and be ready to rotate them periodically as age is as of 19th June 2024 NOT Post-Quantum Safe and so in case the threat actor can access your encrypted keys e.g. via their use in a public repository then they can utilize the strategy of Harvest Now, Decrypt Later

[secrix](https://journal.platonic.systems/introducing-secrix/)

> Agenix is great at managing secrets until a system restart is needed or a wild power outage strikes—in which case, by default, you’ll need to redeploy to get your secrets back. 

[sops post](https://konradmalik.com/posts/2023/02/sops-nix-simple-secrets-management-for-nix/). [another](https://zohaib.me/managing-secrets-in-nixos-home-manager-with-sops/)

[nix-sops repo](https://github.com/Mic92/sops-nix)

[Sops-nix safe enough to commit id_rsa?](https://discourse.nixos.org/t/sops-nix-safe-enough-to-commit-id-rsa/34354/1). [threat model](https://github.com/getsops/sops#threat-model).

> It should be noted that you can carry the secrets outside your repository 94 if you are concerned about this, sops-nix has support for that.

> Upstream recommends keeping your secrets “reasonably private”, and I’d be a fool to suggest otherwise

> I think “publish on a public GitHub repo” is probably not “reasonably private”. While this wouldn’t result in your secrets immediately leaking, someone may in the future break the encryption used for it. Don’t panic if you’ve shared them already, but maybe consider pulling them offline and changing the secrets and keys involved.

> defaultSopsFile = "/etc/sops/secrets.yaml"; (outside the repo)

[private repositories for an extra layer of security - NixOS Secrets Management - Part 3/3](https://www.youtube.com/watch?v=HnmpYp1_aKo)

[nixos-anywhere guide](https://www.youtube.com/watch?v=4sypfTBuEbA&t=5s)

[Just, Nix Shell and Podman are a Killer Combo](https://www.reddit.com/r/NixOS/comments/xwmx6o/just_nix_shell_and_podman_are_a_killer_combo/)

[private keys in Nixos](https://hachyderm.io/@nobodyinperson@fosstodon.org/113698395612510425)

[Nix Remote Builds](https://docs.nixbuild.net/remote-builds/). [podcast](https://open.spotify.com/episode/3NJTpW6pnIrU408iEHt9jc).

[Build against an older libc, keep the newest in the runtime closure](https://github.com/NixOS/nixpkgs/issues/303405). [Libc version is different before and after nix-shell -p](https://discourse.nixos.org/t/libc-version-is-different-before-and-after-nix-shell-p/43946).

[stop using nix-env](https://stop-using-nix-env.privatevoid.net/)

[Development shells with Nix: four quick examples](https://michael.stapelberg.ch/posts/2025-07-27-dev-shells-with-nix-4-quick-examples/)

[Nixpkgs module system config modules graph](https://discourse.nixos.org/t/nixpkgs-module-system-config-modules-graph/67722).

[New AI Coding Teammate: Gemini CLI GitHub Actions](https://news.ycombinator.com/item?id=44822389)

[tarball-ttl](https://nix.dev/manual/nix/2.24/command-ref/conf-file.html#conf-tarball-ttl)

[Root downloads the same packages again](https://discourse.nixos.org/t/root-downloads-the-same-packages-again/33369/5). [How to pin nix registry nixpkgs to release channel](https://discourse.nixos.org/t/how-to-pin-nix-registry-nixpkgs-to-release-channel/14883). [unification](https://nix.dev/manual/nix/2.24/command-ref/new-cli/nix3-registry#unification).

> Note that this only happens because the nix “registry” isn’t pinned by default, so nix shell nixpkgs/release-23.05#... is checking the internet for the latest release-23.05 commit. If you pin your registry, it won’t have to download anything.

> The user registry ~/.config/nix/registry.json. This registry can be modified by commands such as nix registry pin.

> The to flake reference in a registry entry is unified with some flake reference R by taking to and applying the rev and ref attributes from R, if specified. For example:

> github:NixOS/nixpkgs unified with nixpkgs/nixos-20.09 produces github:NixOS/nixpkgs/nixos-20.09.

> github:NixOS/nixpkgs/master unified with nixpkgs/nixos-20.09 produces github:NixOS/nixpkgs/nixos-20.09.

> using the tag: nix run github:NixOS/nixpkgs/25.11#ripgrep fasdfadf

> Also, please don’t use release-23.05. Use nixos-23.05. The former has not undergone hydra caching and testing, while the latter has.

[You rarely want to use the tag. As it is static, it will not even receive security updates.](https://discourse.nixos.org/t/pinning-nixpkgs-in-documentation-examples/20749/5). [discord](https://discord.com/channels/568306982717751326/790886215532150815/1445170489986252902). [gh issue](https://github.com/NixOS/nixpkgs/issues/185168). [post](https://hachyderm.io/@DiazCarrete/115646598470982962)

[differences between (and perhaps use cases for) single-user and multi-user Nix installations](https://discourse.nixos.org/t/what-are-the-specific-differences-between-and-perhaps-use-cases-for-single-user-and-multi-user-nix-installations/25671) apparently multi-user is better

[nix flakes: flakes in subdirectories can access files in parent directories](https://github.com/NixOS/nix/issues/4414)

> This is actually intended behaviour. A flake in a subdirectory is allowed to access other directories in the same input tree. (For instance, I have NixOS configurations in subdirectory flakes that access modules like ../common/stuff.nix.)

> This means that the flake reference /path?dir=foo is not equivalent to /path/foo since the latter doesn't have access to /path.

[[r/NixOS] Nix or home-manager for packages?](https://www.reddit.com/r/NixOS/comments/1pfpcgl/nix_or_homemanager_for_packages/)

[Homeless Dotfiles With Nix Wrappers](https://www.youtube.com/watch?v=Zzvn9uYjQJY). 

[mkOutOfStoreSymlink](https://www.youtube.com/watch?v=Zzvn9uYjQJY&lc=Ugx9n1UEZ1X283JLBih4AaABAg.AOvF8mEsXGjAOvPvLlUYLt). [explanation, not sure if good idea](https://jeancharles.quillet.org/posts/2023-02-07-The-home-manager-function-that-changes-everything.html).

[The problem with LD lib path is that it might break child processes at random, as the LD path overwrites rrpath and therefore binaries might not find it's libs anymore](https://discord.com/channels/568306982717751326/790886215532150815/1447522487998087168)

[0062-content-addressed-paths.md](https://github.com/NixOS/rfcs/blob/master/rfcs/0062-content-addressed-paths.md)

> The idea behind the “content-addressed” model is that rather than deriving these output paths from the inputs of the build, we derive them from the output (the produced store path).

> Nix already supports a special-case of content-addressed derivations with the so-called “fixed-output” derivations. These are derivations that are content-addressed, but whose output hash has to be specified in advance, and are used in particular to fetch data from the internet (as the constraint that the hash has to be specified in advance means that we can relax the sandbox for these derivations).

> The main change required by the content-addressed model is that we can’t know the output paths of a derivation before building it.

> This means that the Nix evaluator doesn’t know the output paths of the dependencies it manipulates (it could know them if they are already built, but that would be a blatant purity hole), so these derivations can’t neither embed their own output path, nor explicitely refer to their dependencies by their output path.

> In a input-addressed-only world, the concrete path for a derivation output was a pure function of this output's id that could be computed at eval-time. However this won't be the case anymore once we allow CA derivations, so we now need a way to register this information in the store:

[Nix glossary](https://nix.dev/manual/nix/2.26/glossary)

Loading a flake from nix-repl:

```
nix-repl> foo = builtins.getFlake "flake:nixpkgs"
```

or 

```
nix-repl> :lf flake:nixpkgs
```

[About fetchers](https://ryantm.github.io/nixpkgs/builders/fetchers/)

> The fact that the hash belongs to the Nix derivation output and not the file itself can lead to confusion. 

> A common mistake is to update a fetcher’s URL, or a version parameter, without updating the hash.

> This will reuse the old contents. Remember to invalidate the hash argument, in this case by setting the hash attribute to an empty string.

> Use the resulting error message to determine the correct hash.

> blank sha for development: sha256-AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA=

[Fixed-output paths](https://nixos.org/guides/nix-pills/18-nix-store-paths.html#fixed-output-paths)

> fixed:out:

[Complete Store Path Calculation](https://nix.dev/manual/nix/2.32/protocols/store-path) 

> Regular users do not need to know this information --- store paths can be treated as black boxes computed from the properties of the store objects they refer to. But for those interested in exactly how Nix works, e.g. if they are reimplementing it, this information can be useful.

[nix store make-content-addressed](https://nix.dev/manual/nix/2.22/command-ref/new-cli/nix3-store-make-content-addressed). [What guarantees do signatures by binary caches give?](https://discourse.nixos.org/t/what-guarantees-do-signatures-by-binary-caches-give/34802/4).

> By contrast, in a content-addressed path, the hash part is computed from the contents of the path. This allows the contents of the path to be verified without any additional information such as signatures. 

[Nix derivation madness](https://news.ycombinator.com/item?id=45772347)

> derivers are simply not uniquely determined in the presence of fixed-output derivations, which is by design. That's even more true with CA derivations.

> The deriver field in Nix has always been a misfeature. It was intended to provide traceability back to the Nix expression used to create the derivation, but it doesn't actually do that (since that wasn't really possible in the pre-flakes world, without hermetic evaluation). So instead it just causes a lot of confusion when the deriver recorded in the binary cache doesn't match the local evaluation result, due to fixed-output derivations changing.


[What's in a Nix store path](https://fzakaria.com/2025/03/28/what-s-in-a-nix-store-path). [In Nix, why does hashDrv replace the inputDrvs with a recursive hashDrv of their contents](https://stackoverflow.com/questions/64054487/in-nix-why-does-hashdrv-replace-the-inputdrvs-with-a-recursive-hashdrv-of-their).

>  Learning Nix, one of the things you first learn are that the hashes that are part of the /nix/store are input-derived or “pessimistic” as I like to refer to them as.

`nix path-info --json .` vs `nix realisation info .` vs `nix derivation show .`

> But, the hashDrv given is better than one that just hashes the drv as-is, because the "modulo fixed output derivations part". By ignoring the rest fixed output derivations and just returning a hash based on the fixed output hash (and name) alone, we gain the ability to change how fixed output derivations produce the data they do without changing downstream hashes. This how in Nixpkgs today, we can for example do https://github.com/NixOS/nixpkgs/pull/82130 and it won't be a mass rebuild.

[Single Service VPN in NixOS](https://sashanoraa.gay/blog/nixos-vpn-service/)

[The flake registry](https://github.com/NixOS/flake-registry/)

[nix registry pin pain](https://discourse.nixos.org/t/my-painpoints-with-flakes/9750)

> Overwriting flake:nixpkgs with a local registry entry (eg. github:nixos/nixpkgs/nixos-20.09) seems to cause much less downloads and re-evaluations. And after using nix flake pin there haven’t been any downloads anymore, though then the local registry entry points to github:nixos/nixpkgs/$sha1, the information to which branch it pointed is lost. To “advance” the registry entry I have to actually know where it pointed to before and overwrite, and then pin again.

[Improved evaluation times with pre-resolved Nix store paths](https://discourse.nixos.org/t/improved-evaluation-times-with-pre-resolved-nix-store-paths/60196)

[caching evaluation results](https://www.tweag.io/blog/2020-06-25-eval-cache/)

> Naively, maybe we can keep a cache that records that attribute A of file X evaluates to derivation D (or whatever metadata we want to cache).


