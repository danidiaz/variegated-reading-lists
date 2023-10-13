# FRP

## papers

[Functional reactive animation](http://conal.net/papers/icfp97/)

[Push-pull functional reactive programming](http://conal.net/papers/push-pull-frp/)

[Functional Reactive Programming, Continued](http://haskell.cs.yale.edu/wp-content/uploads/2011/02/workshop-02.pdf)

[Efficient and Compositional Higher-Order Streams](http://sgate.emt.bme.hu/documents/patai/publications/PataiWFLP2010.pdf)

[Signals, not generators!](http://www.ioc.ee/~wolfgang/research/tfp-2009-paper.pdf)

[Practical Principled FRP](http://www.cse.chalmers.se/~atze/papers/prprfrp.pdf)

[Towards a Common Categorical Semantics for Linear-Time Temporal Logic and Functional Reactive Programming](http://www.ioc.ee/~wolfgang/research/mfps-2012-paper.pdf)

[LTL types FRP](http://ect.bell-labs.com/who/ajeffrey/papers/plpv12.pdf)

[Synchronous Functional Programming: The Lucid Synchrone Experiment](http://www.di.ens.fr/~pouzet/bib/chap_lucid_synchrone_english_iste08.pdf)

[Causal commutative arrows](http://haskell.cs.yale.edu/wp-content/uploads/2012/06/FromJFP.pdf)

[Causal Commutative Arrows and Their Optimization](http://haskell.cs.yale.edu/?post_type=publication&p=72)

[Causal commutative arrows, revisited](https://www.cl.cam.ac.uk/~jdy22/papers/causal-commutative-arrows-revisited.pdf)

[Functional Reactive Programming, Refactored](http://www.cs.nott.ac.uk/~psxip1/papers/2016-HaskellSymposium-Perez-Barenz-Nilsson-FRPRefactored-short.pdf)

> There's a few of approaches to dealing with this that work together. Many of us hope to package them up into nicer abstractions now that we've started recognizing them. There are two very important ones to know. The first is to push dynamicity into the leaves of your data structure. Instead of rendering a Dynamic [a], you can work with a Dynamic [Dynamic a]. This let's you model changes to the leaves of the list separately from changes to the spine of the list. The nuclear weapon of this approach is traverseDMapWithKeyWithAdjust and the MonadAdjust class in general. It's quite rough in the currently unreleased Reflex 0.5 (which is what should be used since 0.4 is very old and doesn't have any lessons from industrial use incorporated).

> The second major technique is to use patches instead of naive update Events. There is a variant of Dynamic called Incremental whose update value is a type that represents changes to the value the Incremental holds. You can write your own patch types and specify the value type they act on. Combined with the previous technique this lets you incrementally update the spine of a data structure instead of all at once. You can specify arbitrary changes which is less user friendly but more powerful.

[Fault tolerant functional reactive programming](https://dl.acm.org/citation.cfm?id=3236791)

[Fault Tolerant Functional Reactive Programming (Functional Pearl)](https://dl.acm.org/citation.cfm?id=3236791)

[A Fitch-style Modal Calculus for Reactive Programming Without Space Leaks](https://arxiv.org/pdf/1903.05879.pdf)

[Rhine: FRP with Type-Level Clocks](https://www.manuelbaerenz.de/files/Rhine.pdf)

[Modal FRP For All](https://github.com/pa-ba/Rattus/raw/master/docs/paper.pdf) related to [Rattus](https://www.reddit.com/r/haskell/comments/hr1jbn/ann_rattus_01_an_embedded_frp_language_with_modal/).

[Reactive Probabilistic Programming](https://news.ycombinator.com/item?id=23901374)

## posts

[FRP - Dynamic event switching in reactive-banana-0.7](http://apfelmus.nfshost.com/blog/2012/09/03-frp-dynamic-event-switching-0-7.html)

[FRP — API redesign for reactive-banana 1.0](http://apfelmus.nfshost.com/blog/2015/08/29-frp-banana-api-redesign.html)

[FRP for free](https://www.reddit.com/r/haskell/comments/40x4wf/frp_for_free/)

[A Farewell to FRP](http://elm-lang.org/blog/farewell-to-frp)

[How to implement a game loop in reactive banana?](http://stackoverflow.com/questions/12685430/how-to-implement-a-game-loop-in-reactive-banana)

[Time delays in reactive banana](http://stackoverflow.com/questions/19668940/reactive-banana-time-delays)

[The future of Netwire](https://groups.google.com/forum/#!topic/haskell-cafe/7loPik5Vix0)

[Beliefs and the Unimpossibility of Functional Reactive Programming](https://lukepalmer.wordpress.com/2010/01/17/beliefs-and-the-unimpossibility-of-frp/)

[What's the status of current Functional Reactive Programming implementations?](http://stackoverflow.com/questions/13341937/whats-the-status-of-current-functional-reactive-programming-implementations)

[My thoughts after spending 5 month writing an frp library](https://www.reddit.com/r/haskell/comments/4zugyb/my_thoughts_after_spending_5_month_writing_an_frp/)

[Intro to machines and arrows](https://blog.jle.im/entries/series/+intro-to-machines-and-arrows.html)

[All about auto](https://blog.jle.im/entries/series/+all-about-auto.html) [Reddit](https://www.reddit.com/r/haskell/comments/6mrcbj/encoding_objects_school_of_haskell/dk3wtmn/)

[auto](http://hackage.haskell.org/package/auto) and [wires](http://hackage.haskell.org/package/wires)

[Haskell with Reactive Banana and GTK3](http://paulspontifications.blogspot.com.es/2018/02/haskell-with-reactive-banana-and-gtk3.html?m=1)

[Does functional reactive programming in haskell scale well in GUI programs?](https://www.reddit.com/r/haskell/comments/8mmzfc/does_functional_reactive_programming_in_haskell/)

[An introduction to reflex](https://qfpl.io/posts/reflex/basics/introduction/) [more](https://qfpl.io/projects/reflex/)

[skateboard](https://lolc.at/haskellboard)

[What is the current status of functional reactive programming (FRP) in Haskell?](https://www.reddit.com/r/haskell/comments/9zvqn3/what_is_the_current_status_of_functional_reactive/).

[Let's reinvent FRP](http://vindum.io/blog/lets-reinvent-frp/).

[How can I best learn functional reactive programming?](https://www.reddit.com/r/haskell/comments/ajxq3a/how_can_i_best_learn_functional_reactive/).

[frp and state machines](https://www.reddit.com/r/haskell/comments/bew8be/the_monads_of_haskell/el9bw3l?utm_source=share&utm_medium=web2x)

[Your Easy Guide to Functional Reactive Programming](https://medium.com/@lettier/functional-reactive-programming-a0c7b08f6b67)

[iOS](https://twitter.com/TacticalGrace/status/1137447609830912000)

[FRP in CodeWorld](https://medium.com/@cdsmithus/functional-reactive-programming-with-reflex-and-codeworld-85495360f1b7). [reddit](https://www.reddit.com/r/haskell/comments/c7ov4g/functional_reactive_programming_with_reflex_and/eshmn0k/). [Building and Debugging FRP with CodeWorld and Reflex](https://medium.com/@cdsmithus/building-and-debugging-frp-with-codeworld-and-reflex-a912083e66c1)

> Instead of the state being the big deal, and components interact via shared state, the dependency graph becomes the big deal, and components interact by being passed their dependencies as arguments, and producing their results. That's made workable by correctly modeling the nature of these dependencies and results, and keeping state local .

[reflex-vty: A library for building functional reactive terminal applications](https://www.reddit.com/r/haskell/comments/clrg1s/reflexvty_a_library_for_building_functional/)

[FRP implementation details in Rust](https://github.com/Pauan/rust-dominator/issues/16)

[FRP in Haskell Weekly](https://haskellweekly.news/episode/23.html). [reddit](https://www.reddit.com/r/haskell/comments/dpf9za/functional_reactive_programming_haskell_weekly/)

[the roots of frp](https://futureofcoding.org/essays/dctp) nice diagrams [hn objections](https://news.ycombinator.com/item?id=21430745)

[An IDE implemented using reflex](https://mpickering.github.io/posts/2020-03-16-ghcide-reflex.html)

[reflex html - the basics](https://mmhaskell.com/blog/2020/3/2/reflex-html-basics)

[The Misunderstood Roots of FRP](https://futureofcoding.org/essays/dctp.html). [Explicitly Comprehensible Functional Reactive Programming](https://futureofcoding.org/papers/comprehensible-frp/).

[An efficient normalisation procedure for linear temporal logic](https://twitter.com/Jose_A_Alonso/status/1259048078029578242)

[Rattus 0.1: An embedded FRP language with modal types](https://www.reddit.com/r/haskell/comments/hr1jbn/ann_rattus_01_an_embedded_frp_language_with_modal/). 

[What are different flavors of functional reactive programming?](https://www.reddit.com/r/haskell/comments/jbpbsa/what_are_different_flavors_of_functional_reactive/)

[clash](https://www.reddit.com/r/haskell/comments/lt3gtx/linear_types_for_circuit_design_in_haskellclash/gp5offn/)

> you describe sequential circuits as functions operating over infinite streams, where memory/state is 'inferred' when you prepend an element in front of a stream: by doing that you move the present to the future, thus requiring memory.

[Any book recommended for reactive functional programming in haskell?](https://www.reddit.com/r/haskell/comments/s9uylb/any_book_recommended_for_reactive_functional/)

## slides

[basic propositional linear logic](http://www.pst.informatik.uni-muenchen.de/lehre/WS0304/tl/Vorlesung/46-1.pdf)

[Temporal logic and functional reactive programming](http://de.slideshare.net/SergeiWinitzki/temporal-logic-and-functional-reactive-programming)

## books

[Functional Reactive Programming](https://www.manning.com/books/functional-reactive-programming)


## videos

[Functional Reactive Programming in Java](https://realm.io/news/droidcon-gomez-functional-reactive-programming/)

[A Sensible Intro to FRP](https://www.reddit.com/r/haskell/comments/4uz7cw/a_sensible_intro_to_frp_video/)

[Making Reactive Programs Function](https://pay.reddit.com/r/haskell/comments/5683bp/making_reactive_programs_function/) [part2](https://www.youtube.com/watch?v=qMK7pdcb1TE)

[FRP, refactored](https://www.youtube.com/watch?v=FmwOd4z9LdM)

[CCA revisited](https://www.youtube.com/watch?v=bnFHYsL4QNc)

[Doug Beardsley: Real World Reflex](https://www.youtube.com/watch?v=dNBUDAU9sv4)

[Do-It-Yourself Functional Reactive Programming](https://www.youtube.com/watch?v=Rm7rwWL6lIY)

> Sampling is pull

[Purely Functional User Interfaces that Scale](https://www.youtube.com/watch?v=jVeGoqyq5Fs).

[Principled Testing of Functional Reactive Systems](https://skillsmatter.com/skillscasts/14174-principled-testing-of-functional-reactive-systems)

[what is FRP?](https://www.reddit.com/r/haskell/comments/dyzoyi/what_is_functional_reactive_programming_scale_by/)

[bearriver](https://twitter.com/IvanPerezKeera/status/1218592110196273152)

[Synthesis of Functional Reactive Programs via a Reduction of Asynchronous Inputs to Lists](https://www.youtube.com/watch?v=KdKaHuZBJ6s)

[A Fresh Look at Linear Temporal Logic](https://www.youtube.com/watch?v=iZI4wLxemeY)

## software

[reactive-banana](http://hackage.haskell.org/package/reactive-banana)

[reflex-process](https://www.reddit.com/r/haskell/comments/epldda/reflexprocess_a_reflexfrp_interface_for_running/)

[reflex-ghci](https://www.reddit.com/r/haskell/comments/eqc698/ann_reflexghci_a_ghcidlike_program_for/)

[dunai](https://www.reddit.com/r/haskell/comments/eu0vs2/ann_dunai_06_classic_and_arrowized_frp_stream_and/)

[alpaca-netcode: Rollback/replay NetCode for realtime, deterministic, multiplayer games](https://www.reddit.com/r/haskell/comments/mivfng/introducing_alpacanetcode_rollbackreplay_netcode/)

## quotes

> From what I can read here and there, Netwire and reactive-banana have different purposes and goals. Netwire specialises in modelising framed signals, such as a game server, because what a game server typically does is sending its state to client in periodic frames. Reactive-banana would be the better choice for creating a GUI because a GUI is a purely event-driven model and is not tolerant to time leak.

> netwire: Useful library, but needs maintenance and has high 
  maintenance cost due to its design.  I'll likely replace it by a new 
  abstraction at some point, using a different package name. 
  Currently I recommend using one of the following libraries for FRP: 
  
> reactive-banana: My former favourite when it comes to push/pull 
  FRP.  Well designed, clean semantics, reasonably efficient. 

> reflex: My current favourite when it comes to push/pull FRP. 
  Well designed, clean semantics, reasonably efficient. 

> Yampa: AFRP for games, simulations and other real-time 
  applications (for when a high and predictable framerate is more 
  important than pushed events, same target domain as Netwire). 

> Evan Czaplicki's talk (https://www.youtube.com/watch?v=Agu6jipKfYw) linked in frp-zoo is great! After watching it I would say that varying is definitely in his Arrowized FRP category. The main type in varying is an instance of Arrow. Signals are not connected to the world, and when a signal is not being run - it's cold.
Unlike Netwire, varying doesn't have implicit time or inhibition. A Netwire 'wire' written in varying would be something like
Monad m => Var m t (Event b)
where t is time and b is the value. Event allows inhibition explicitly.
Unlike Auto, varying is small and more focused on tweening and allowing you to build data structures that change in a smooth manner over time (or another domain). Auto has a lot of extra functionality like serialization, etc. I purposefully made the varying API tiny in an effort to make learning it really easy.
They're all capable of expressing one another in their own terms though, so they're all worth a visit.

> Auto is at least as much "FRP" as elerea. Purists to Elliot's approach, notably including Auto's author, will tell you neither one is FRP at all. Five years ago I'd probably be agreeing with them, but IMO at this point that ship has sailed.

[Arrowized FRP in Scala](https://twitter.com/IvanPerezKeera/status/1144392188022931456)

[Building a reactive calculator in Haskell (1/5)](https://keera.co.uk/2020/05/28/building-a-reactive-calculator-in-haskell-1-5/) [Reactive Web Apps in Haskell (all posts + live demo)](https://www.reddit.com/r/haskell/comments/hapak2/reactive_web_apps_in_haskell_all_posts_live_demo/)

[Rattus 0.1: An embedded FRP language with modal types](https://www.reddit.com/r/haskell/comments/hr1jbn/ann_rattus_01_an_embedded_frp_language_with_modal/)

[Explicitly Comprehensible Functional Reactive Programming](https://futureofcoding.org/papers/comprehensible-frp/comprehensible-frp.pdf). [zulip](https://funprog.zulipchat.com/#narrow/stream/201385-Haskell/topic/Reflex.20FRP.20.3E.20Elm).

> One thing I encountered while playing with Specular (basically Reflex port to PS) is that you can code yourself into a corner if you don't push Dynamic s low enough, ending up not being able to avoid unnecessary updates

[Towards Principled Reactive UI](https://news.ycombinator.com/item?id=24599560)

[Reflex.Host.Headless](https://funprog.zulipchat.com/#narrow/stream/201385-Haskell/topic/FRP.20build.20system/near/245209079)

[reactive-banana 1.2.2.0](https://discourse.haskell.org/t/reactive-banana-1-2-2-0/3249/4)

> anything loosely involving a possibly-dynamic collection of locally-stateful “entities” that relate to one another, whose implementation might otherwise involve spooky callbacks or other non-compositional abstractions 

[An Overview of Functional Reactive Programming](https://es.cs.uni-kl.de/publications/datarsg/Kock21.pdf)

[Seven GUIs in reflex-vty, Part 1: The Counter](https://twitter.com/HaskellDiscu/status/1561360146793922560)

[The Essence of Reactivity](https://dl.acm.org/doi/pdf/10.1145/3609026.3609727)

[Asynchronous Reactive Programming with Modal Types in Haskell](https://bahr.io/pubs/files/asyncrattus-paper.pdf)

[RHINE-BAYES: A LIBRARY FOR ONLINE REACTIVE BAYESIAN INFERENCE](https://www.tweag.io/blog/2023-10-12-rhine-bayes/#online-reactive-bayesian-machine-learning-in-haskell)


