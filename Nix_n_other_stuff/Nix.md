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

[NixOS in production](https://lobste.rs/s/bbbjfz/nixos_production)

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


