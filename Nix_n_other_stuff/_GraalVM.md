[React Server Side Rendering with GraalVM for Clojure](https://news.ycombinator.com/item?id=20381423). [tweet](https://twitter.com/grashalm_/status/1148195194900271104)

> Note that you aren't tied to Java 8, which is quite old by now, but can also run GraalJS with OpenJDK 11, 12, 13, and enjoy the recent performance improvements to the GC (using ZGC or Shenandoah) and startup time (using Application CDS):

> Graal-dev here,

> We are working with a very high priority on JDK 11 support. We should be able to ship it in a few months from now.

> - So is graal polyglot already compatible with newer JDKs and it's just native image generation that's blocking the upgrade?

> Not just. We also need to upgrade the JVMCI version we use in order to support libgraal (Graal compiler as native-image in HotSpot). Also, modules make everything a little bit more complicated as well

https://github.com/graalvm/graal-js-jdk11-maven-demo

[Introducción a GraalVM - codemotion](https://www.youtube.com/watch?v=wzAIDNbC6X8)

[Substrate VM – A framework that allows AOT compilation of Java applications](https://news.ycombinator.com/item?id=16070262)

> Truffle is basically a toolkit for building language runtimes. It provides a framework for creating AST interpreters. Generally AST interpreters are easy to work with and reason about, but slow. Truffle addresses the speed issue by using Graal's API to perform partial evaluation on the interpreter. So, you get very fast runtimes without having to build a custom VM. But, it also exposes some compiler details by way of an annotation-based DSL if you want to take advantage of it. This includes control for PIC sizes, loop exploding, and explicit branch profiling amongst others.

> This is awesome! Substrate VM not being open source was a major reason I wasn't more excited about Truffle/Graal. Without Substrate VM, startup times for Truffle-based interpreters are terrible 

> Now anyone outside of Oracle can write cool JIT compilers using Truffle, and have them start quickly! I think it can also be used to compile normal Java programs to native executables.

http://lafo.ssw.uni-linz.ac.at/papers/2017_PLDI_GraalTutorial.pdf

[Do Graal native images run faster than the Java bytecode ordinarily produced](https://github.com/oracle/graal/issues/1069)

> FAIK currently executables produced by native-image have lower peak performance than the original Java code running under GraalVM JIT. OTOH native-image starts faster and can have much lower memory overhead for simple applications.

> Devirtualization, escape analysis, inlining

[GraalVM docs](https://www.graalvm.org/docs/)

> GraalVM is an ecosystem and shared runtime offering performance advantages not only to JVM-based languages such as Java, Scala, Groovy, and Kotlin, but also to other programming languages such as JavaScript, Ruby, Python, and R. Additionally, it enables the execution of native code on the JVM via an LLVM front-end. GraalVM 19.1.0 is based on JDK version 8u212.

[SubstrateVM limitations](https://github.com/oracle/graal/blob/master/substratevm/LIMITATIONS.md)  

> Substrate VM is a framework that allows ahead-of-time (AOT) compilation of Java applications under closed-world assumption into executable images or shared objects (ELF-64 or 64-bit Mach-O). 
 
https://aboullaite.me/understanding-jit-compiler-just-in-time-compiler/
https://en.wikipedia.org/wiki/Just-in-time_compilation
https://javapapers.com/core-java/jvm-server-vs-client-mode/
https://stackoverflow.com/questions/198577/real-differences-between-java-server-and-java-client

[Understanding How Graal Works - a Java JIT Compiler Written in Java](https://chrisseaton.com/truffleruby/jokerconf17/)

https://www.oracle.com/technetwork/java/jvmls2015-wimmer-2637907.pdf

[self-hosting](https://en.wikipedia.org/wiki/Self-hosting_(compilers))

[SimpleLnaguage](https://github.com/graalvm/simplelanguage). [truffle-material](https://gist.github.com/smarr/d1f8f2101b5cc8e14e12). [Introduction to SimpleLanguage](https://www.graalvm.org/docs/graalvm-as-a-platform/implement-language/).

[Performance tuning Twitter services with GraalVM and Machine Learning](https://www.youtube.com/watch?v=3lukwqAkz90)

> Many services work below optimality

[Baeldung - Deep Dive Into the New Java JIT Compiler – Graal](https://www.baeldung.com/graal-java-jit-compiler).

[Java JIT compiler inlining](https://dzone.com/articles/jit-inlining). [Method Inlining in the JVM](https://www.baeldung.com/jvm-method-inlining). [Java JIT compiler inlining](https://techblug.wordpress.com/2013/08/19/java-jit-compiler-inlining/). [JVM JIT loop unrolling](http://fasihkhatib.com/2018/05/20/JVM-JIT-Loop-Unrolling/). [What are some of the most useful JVM JIT optimizations and how to use them?](https://blog.overops.com/java-on-steroids-5-super-useful-jit-optimization-techniques/).

> As you know the Java Virtual Machine (JVM) optimizes the java bytecode at runtime using a just-in-time-compiler (JIT). However the exact behavior of the JIT is hard to predict and documentation is scarce. You probably know that the JIT will try to inline frequently called methods in order to avoid the overhead of method invocation. But you may not realize that the heuristic it uses depends on both how often a method is invoked and also on how big it is. Methods that are too big can not be inlined without bloating the call sites.

> Confirm this: the JIT can "take guesses" and backtrack if they turn to have lower performance

> Theoretically, javac could do something similar [loop unrolling] when translating Java to bytecode, but the JIT compiler has better knowledge of the actual CPU that the code will be running on and knows how to fine tune the code in a much more efficient way.

[Understanding JIT Compilation and Optimizations](https://docs.oracle.com/cd/E13150_01/jrockit_jvm/jrockit/geninfo/diagnos/underst_jit.html)

[A close look at Java's JIT: Don't Waste Your Time on Local Optimizations](https://www.beyondjava.net/a-close-look-at-javas-jit-dont-waste-your-time-on-local-optimizations)

> If there is no method call, but the program spends a lot of time in a method, the method is compiled. After that the program is stopped, the variables are transferred to the machine code version of the method and the machine code version is started. This is a difficult operation called On Stack Replacement. Usually, the JIT tries to optimize everything else before starting OSR.

[Øredev 2011 - JVM JIT for Dummies (What the JVM Does With Your Bytecode When You're Not Looking)](https://www.slideshare.net/CharlesNutter/redev-2011-jvm-jit-for-dummies-what-the-jvm-does-with-your-bytecode-when-youre-not-looking). [video](https://www.youtube.com/watch?v=FnDHp3Qya6s)

> -XX:+UnlockDiagnosticVMOptions

> -XX:+PrintCompilation

> -XX:+PrintAssembly

> -XX:+PrintInlining

> -XX:+LogCompilation

> CALL operation in the assembly indicate that something failed to inline

[Optimization by Java Compiler](https://stackoverflow.com/questions/5981460/optimization-by-java-compiler) 

> javac will only do a very little optimization, if any.

> The point is that the JIT compiler does most of the optimization - and it works best if it has a lot of information, some of which may be lost if javac performed optimization too. If javac performed some sort of loop unrolling, it would be harder for the JIT to do that itself in a general way - and it has more information about which optimizations will actually work, as it knows the target platform.)

[Loop Transformations in the Ahead-of-Time Optimization of Java Bytecode (paper)](https://warwick.ac.uk/fac/sci/dcs/people/research/csrcbc/research/publications/cc2006.pdf). [vectorization in hotspot VM](https://cr.openjdk.java.net/~vlivanov/talks/2017_Vectorization_in_HotSpot_JVM.pdf)

[New tricks of the GraalVM](https://pdfs.semanticscholar.org/0966/90689e7b97453b6c0d97ff40e34de9432ef3.pdf)

> Snippets Finally we arrive at the concept that really makes having a separate JIT compiler written in a high level language possible - snippets. Snippets can be seen as the glue that ties the compiler and the JVM together.

[What a difference a JVM makes?](http://psy-lob-saw.blogspot.com/2018/01/what-difference-jvm-makes.html)

> You don't need a JVM and the binary can be as small as a few megabytes. The SubstrateVM uses Graal todo this compilation. In some configurations, the SubstrateVM can also compile Graal into itself so that it can compile code at runtime as well, just-in-time. So Graal is ahead-of-time compiling itself.

https://chrisseaton.com/truffleruby/jokerconf17/
https://www.reddit.com/r/java/comments/8zbqfo/getting_to_know_graal_and_graalvm/
https://www.beyondjava.net/graal-towards-the-holy-grail-of-polyglot-programming
https://www.graalvm.org/docs/reference-manual/aot-compilation/

> GraalVM Native Image allows you to ahead-of-time compile Java code to a standalone executable, called a native image. This executable includes the application, the libraries, the JDK and does not run on the Java VM, but includes necessary components like memory management and thread scheduling from a different virtual machine, called “Substrate VM”. Substrate VM is the name for the runtime components (like the deoptimizer, garbage collector, thread scheduling etc.). The resulting program has faster startup time and lower runtime memory overhead compared to a Java VM.

https://gist.github.com/smarr/d1f8f2101b5cc8e14e12
One Compiler: Deoptimization to Optimized Code (work on SubstrateVM, AOT compilation of Truffle code)http://doi.org/10.1145/3033019.3033025

Key Papers
- The Truffle paper: “Self-Optimizing AST Interpreters” http://lafo.ssw.uni-linz.ac.at/papers/2012_DLS_SelfOptimizingASTInterpreters.pdf
- How to represent Objects Efficiently: “An Object Storage Model for the Truffle Language Implementation Framework” http://chrisseaton.com/rubytruffle/pppj14-om/pppj14-om.pdf
- The Truffle+Graal paper: "One VM to Rule Them All" http://lafo.ssw.uni-linz.ac.at/papers/2013_Onward_OneVMToRuleThemAll.pdf
- The Partical Evaluation paper: "Practical partial evaluation for high-performance dynamic language runtimes" https://chrisseaton.com/rubytruffle/pldi17-truffle/pldi17-truffle.pdf

https://github.com/oracle/graal/issues/1069

> AFAIK currently executables produced by native-image have lower peak performance than the original Java code running under GraalVM JIT. OTOH native-image starts faster and can have much lower memory overhead for simple applications.

https://github.com/oracle/graal/tree/master/substratevm
https://medium.com/de-bijenkorf-techblog/speed-up-application-launch-time-with-graalvm-3d629131adb1
https://news.ycombinator.com/item?id=16070262
https://github.com/oracle/graal/tree/master/substratevm
https://medium.com/de-bijenkorf-techblog/speed-up-application-launch-time-with-graalvm-3d629131adb1
https://news.ycombinator.com/item?id=16070262
https://medium.com/graalvm/understanding-class-initialization-in-graalvm-native-image-generation-d765b7e4d6ed

> tl;dr: Classes reachable for a GraalVM native image are initialized at image build time. Objects allocated by class initializers are in the image heap that is part of the executable. The new option --delay-class-initialization-to-runtime= delays initialization of listed classes to image run time.

https://hackernoon.com/why-the-java-community-should-embrace-graalvm-abd3ea9121b5
https://www.oracle.com/technetwork/java/jvmls2015-wimmer-2637907.pdf
https://nirvdrum.com/2017/02/15/truffleruby-on-the-substrate-vm.html
https://www.codacy.com/blog/scala-faster-and-slimmer-with-graalvm/
http://lafo.ssw.uni-linz.ac.at/papers/2017_PLDI_GraalTutorial.pdf
https://www.complang.tuwien.ac.at/lehre/ubvo/substrate.pdf substrate vm

> an embeddable VM with fast startup and low footprint for, and written in, a subset of Java optimized to execute Truffle languages ahead-of-time compiled using Graal integrating with native development tools.

https://developers.redhat.com/blog/2018/07/30/natively-compile-java-code-for-better-startup-time/
https://stackoverflow.com/questions/tagged/graalvm
https://e.printstacktrace.blog/ratpack-graalvm-how-to-start/
[Java for Serverless: Ahead-of-Time compilation with Micronaut and GraalVM](https://www.exoscale.com/syslog/java-serverless-micronaut-graalvm/)
https://www.infoq.com/presentations/graal-jit-c2/

https://benchmarksgame-team.pages.debian.net/benchmarksgame/fastest/java-substratevm.html

[Graal How to use the new JVM JIT compiler in real life (C. Thalinger)](https://www.youtube.com/watch?v=Rvb-kvuPzqI)

[Down the rabbit hole](https://www.youtube.com/watch?v=HBKVdJph_oQ)

https://medium.com/graalvm/graalvms-javascript-engine-on-jdk11-with-high-performance-3e79f968a819

> Written in Java to lower the entry barrier – Graal compiling and optimizing itself is also a good optimization opportunity

https://stackoverflow.com/questions/2719469/why-is-the-jvm-stack-based-and-the-dalvik-vm-register-based
https://stackoverflow.com/questions/3315938/is-it-possible-to-view-bytecode-of-class-file
https://stackoverflow.com/questions/30928786/how-do-i-check-assembly-output-of-java-code

[Shenandoah and Concurrent GCs](https://www.reddit.com/r/java/comments/cbh2yk/aleksey_shipil%C3%ABv_on_shenandoah_and_concurrent_gcs/)

[revirivueltas](https://twitter.com/jerolba/status/1149572836417101824)

[building a DSL with GraalVM](https://www.youtube.com/watch?v=G4c4BoXZN1o)

> gu install native-image

```
bash-4.2# gu list
ComponentId              Version             Component name      Origin
--------------------------------------------------------------------------------
graalvm                  19.1.1              GraalVM Core
native-image             19.1.1              Native Image        github.com
```

[GraalVM on Goldman Sachs](https://www.youtube.com/watch?v=hPjDWzPiaCs). [tweet](https://twitter.com/grashalm_/status/1152542007535067138)

[Thomas Wuerthinger on GraalVM and Optimizing Java with Ahead-of-Time Compilation](https://www.infoq.com/podcasts/graalvm-optimizing-java/)

[one vm to rule them all?](https://www.youtube.com/watch?v=hPjDWzPiaCs)

[graalvm for Java developers 2019](https://www.youtube.com/watch?v=GinNxS3OSi0)

[Graal: How to use the new JVM JIT compiler in real life video 2019](https://news.ycombinator.com/item?id=16346648)

> The JVMCI code that Graal depends on was added to Java 9 and is inbuilt. However, all Graal and Graal-downstream projects use a custom built Java 8 release. This is also the plan for the "foreseeable future" 

[Clojure Interop with R and Python on GraalVM](https://www.reddit.com/r/Clojure/comments/787338/clojure_interop_with_r_and_python_on_graalvm/)

[clojureD 2019: "Native Clojure with GraalVM" by Jan Stępień](https://www.reddit.com/r/Clojure/comments/bmwvi2/clojured_2019_native_clojure_with_graalvm_by_jan/)

https://clojureverse.org/t/why-is-graalvm-so-fast/2079 https://discourse.purescript.org/t/you-should-check-out-graalvm/814 [GraalVM: Run Programs Faster Anywhere](https://news.ycombinator.com/item?id=16859559) https://www.reddit.com/r/haskell/comments/8dr3xw/could_haskell_benefit_from_graalvm/ https://stackoverflow.com/questions/53712580/does-graalvm-jvm-support-java-11 https://stackoverflow.com/questions/48252830/does-java-9-include-graal https://markmail.org/message/42jds3ktwib6jn6r?q=net%2Ejava%2Eopenjdk [	Substrate VM – A framework that allows AOT compilation of Java applications](https://news.ycombinator.com/item?id=16070262). https://assets.ctfassets.net/oxjq45e8ilak/3VZgJf2jLWaQQGKaeSsecc/a015330e94f964d96df0b366321ec068/Dmitry_Chuyko_AOT.pdf https://www.reddit.com/r/java/comments/73c9vb/has_anyone_of_you_used_aot_compilation_on_java9/ 

> Truffle is basically a toolkit for building language runtimes. It provides a framework for creating AST interpreters. Generally AST interpreters are easy to work with and reason about, but slow. Truffle addresses the speed issue by using Graal's API to perform partial evaluation on the interpreter. So, you get very fast runtimes without having to build a custom VM. But, it also exposes some compiler details by way of an annotation-based DSL if you want to take advantage of it. This includes control for PIC sizes, loop exploding, and explicit branch profiling amongst others.

> As a language toolkit, Truffle also gives you an instrumentation framework so you get things like a debugger and profiler for minimal effort. It provides a polyglot system so you can call into other Truffle languages. Since they all inherit from the same base Node class, the compiler can even inline nodes across language boundaries. Truffle takes advantage of that itself by shipping functionality, such as its own native function interface, as its own Truffle language.

> With Substrate VM you get way faster startup for your Truffle language and potentially overall less dynamic footprint.
Graal VM is based on HotSpot, which is sort of "bloated" for the specific use case that Truffle has.

> What's the difference between substrate vm and jaotc? https://mjg123.github.io/2017/10/02/JVM-startup.html

> Substrate VM is more mature? jaotc was response to closed Substrate VM?

> `jaotc` integrates with the HotSpot VM, while Substrate VM provides its own runtime (GC etc.) and intentionally supports only a subset of the JVM features. FWIW, both use Graal as a compiler.

[Graal: Not just a new JIT for the JVM](https://qconlondon.com/system/files/presentation-slides/qcon-london.pdf)

[todo list compiled with Graal for fast startup](https://twitter.com/alvinalexander/status/1158251066221199361)

[Polyglot exception](https://twitter.com/grashalm_/status/1159455488301502464)

GraalVM updater https://www.graalvm.org/docs/reference-manual/graal-updater/ https://medium.com/graalvm/graalvm-19-2-new-tools-b78a70f54b06

https://www.reddit.com/r/Kotlin/comments/bnl8qk/q_is_the_aotc_in_graalvm_native_image_comparable/

GraalVM updater https://www.graalvm.org/docs/reference-manual/graal-updater/ https://medium.com/graalvm/graalvm-19-2-new-tools-b78a70f54b06

[Q: Is the AOTC in GraalVM Native Image comparable to / able to replace Kotlin Native?](https://www.reddit.com/r/Kotlin/comments/bnl8qk/q_is_the_aotc_in_graalvm_native_image_comparable/)

[Baeldung - Deep Dive Into the New Java JIT Compiler – Graal - Very good!](https://www.baeldung.com/graal-java-jit-compiler)
[Graal: How to use the new JVM JIT compiler in real life](https://www.youtube.com/watch?v=yhtrRhNUHvQ)
https://openjdk.java.net/projects/graal/
https://news.ycombinator.com/item?id=16346773
https://github.com/oracle/truffleruby/issues/556#issuecomment-335118818
https://github.com/graalvm/truffleruby/blob/master/doc/user/using-graalvm.md
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/jdk.internal.jvmci.compiler/javadoc/index.html
https://www.infoq.com/articles/Graal-Java-JIT-Compiler/

> This goal has been achieved as evidenced by the inclusion of the Graal compiler in JDK 9 as the basis for jaotc and in JDK 10 as an experimental tier 4 just-in-time compiler. To use the latter, simply add these VM options to the java command line:

> There are several key advantages of writing a compiler in Java. First of all, safety, meaning no crashes but exceptions instead and no real memory leaks. Furthermore, we’ll have a good IDE support and we’ll be able to use debuggers or profilers or other convenient tools. Also, the compiler can be independent of the HotSpot and it would be able to produce a faster JIT-compiled version of itself.

> What this means is that we can run a simple program in three different ways: with the regular tiered compilers, with the JVMCI version of Graal on Java 10 or with the GraalVM itself.

> The JVMCI code that Graal depends on was added to Java 9 and is inbuilt. However, all Graal and Graal-downstream projects use a custom built Java 8 release. This is also the plan for the "foreseeable future" (https://github.com/oracle/truffleruby/issues/556#issuecommen...)

> Additionally, "mx" : the build system that Graal uses is fairly funky - and everyone including Chris (the engineer that made this video) is trying to get the team to move on

> That's not a perfect solution I'm afraid. We recommend using GraalVM and won't support anything else at the moment (beyond attempting to be helpful).

> GraalVM is sticking with a custom Java 8 build that includes JVMCI, for the foreseeable future. I'm not responsible for that and there are many projects which need to co-ordinate beyond TruffleRuby to upgrade - that's why it's not trivial to do.

> The GraalVM is the way we package up everything and distribute it for end-users. If you want to use a standard JDK you need to build everything from scratch.

> Graal is used for many more things than dynamically compiling Java. Besides others it's used for SubstrateVM (closed world AOT compilation) and Truffle languages like TruffleRuby, Graal.JS, FastR, Sulong(llvm integration) and our newest member Graal.Python.

> Graal comes out of Oracle Labs. The build tool mx is short for Maxine, the spiritual predecessor of the Graal project. If you don't know mx it's quite intimidating and ugly. It's Python written by Java developers. But it does it's job coping with our not so standard building and testing requirements. No we don't run mx on Graal.Python yet, but we are working on it for full build tool metacircularity ;).

[JEP 295: Ahead-of-Time Compilation](https://openjdk.java.net/jeps/295)

> AOT compilation is done by a new tool, jaotc [...] It uses Graal as the code-generating backend.

[Understanding How Graal Works - a Java JIT Compiler Written in Java 2017](https://chrisseaton.com/truffleruby/jokerconf17/)

> things to never do again: write a vm in C++

[introduction to simple language](https://www.graalvm.org/docs/graalvm-as-a-platform/implement-language/)

[jvmci](http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/jdk.internal.jvmci.compiler/javadoc/index.html)

[Java Code Examples for jdk.vm.ci.runtime.JVMCI](https://www.programcreek.com/java-api-examples/?api=jdk.vm.ci.runtime.JVMCI)

[JVMCI examples for Java Day Tokyo 2017](https://github.com/YaSuenag/jdt-2017-examples) Very good, re-watch this!

> very interesting, talks about (explicit) bootstrapping

> perhaps give an example of the JVMCI being compiled itself

> it takes 10 seconds for comiling xxxx methods...

> sooo the jvci can slow down startup times

> CompileGraalWithC1Only "we just compile with C1 and that's usually fine"

> sometimes (long running programs) explicit bootstrap (despite slow startup) can be better than C1

> either upfront or on demand during runtime

> if Graal compiles a methods, it uses heap memory to do that

[JMVCI javadocs?](http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/jdk.internal.jvmci.compiler/javadoc/index.html)

> Package that defines the interface between a Java application that wants to install code and the runtime.

http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/runtime/JVMCI.html

https://neomatrix369.wordpress.com/tag/jit/
https://csl.name/post/python-jit/ not Graal
https://github.com/spencertipping/jit-tutorial not Graal
http://blog.reverberate.org/2012/12/hello-jit-world-joy-of-simple-jits.html not Graal
https://jaxenter.com/jep-draft-java-jit-compiler-158398.html

[Compiler Interface and Experimentations](https://medium.com/@nigamnaman/compiler-interface-and-experimentations-f511e34b2b6b)

> Metropolis was created to explore Java-on-Java technologies and indeed the results of which came along with Java-9 with an introduction to the Java-Level JVM Compiler Interface (JVMCI) which targeted AOT compilation for improving the start-up time of both small and large Java applications by compiling classes to native code prior to launching the virtual machine.

> As explained by Doug in an OpenJDK thread, one can use the following code block to verify this on their system:

[Determining if JVMCI is enabled and whether it is being used by the	JVM](http://mail.openjdk.java.net/pipermail/graal-dev/2016-June/004434.html)

[test code for JVMCI?](https://github.com/sourcemirror/jdk-9-hotspot/blob/master/test/compiler/jvmci/code/TestAssembler.java)

https://www.dynatrace.com/news/blog/new-ways-introducing-compiled-code-java-9/ <- useful
https://medium.com/@nigamnaman/compiler-interface-and-experimentations-f511e34b2b6b <- useful
https://github.com/jruby/jruby-graal/blob/master/src/main/java/org/jruby/jvmci/JRubyJVMCI.java <- useful
https://github.com/oracle/graal/issues/306

```
-Djvmci.Compiler=graal
```

> I have been working on a wrapper for Graal that can plug into JVMCI but allow us to tweak compilation specific to JRuby's workloads. The code for this is at https://github.com/jruby/jruby-graal.

> Originally, the code simply wrapped and delegated all the Graal JVMCI endpoints, and this worked correctly to decorate Graal's high tier with a special pass for JRuby.


https://github.com/graalvm/graal-jvmci-8/tree/master/jvmci <- good javadocs
https://github.com/oracle/graal/tree/master/compiler/src/org.graalvm.compiler.nodes/src/org/graalvm/compiler/nodes/java
https://github.com/oracle/graal/tree/master/compiler/src/org.graalvm.compiler.nodes/src/org/graalvm/compiler/nodes
https://github.com/oracle/graal/blob/master/compiler/src/org.graalvm.compiler.nodes/src/org/graalvm/compiler/nodes/StructuredGraph.java
https://github.com/graalvm/graal-jvmci-8/blob/master/jvmci/jdk.vm.ci.runtime/src/jdk/vm/ci/runtime/JVMCIRuntime.java
https://github.com/graalvm/graal-jvmci-8/blob/master/jvmci/jdk.vm.ci.runtime/src/jdk/vm/ci/runtime/JVMCIBackend.java
https://github.com/graalvm/graal-jvmci-8/blob/master/jvmci/jdk.vm.ci.code/src/jdk/vm/ci/code/TargetDescription.java code cache
https://github.com/graalvm/graal-jvmci-8/blob/master/jvmci/jdk.vm.ci.runtime/src/jdk/vm/ci/runtime/JVMCICompiler.java
https://github.com/graalvm/graal-jvmci-8/tree/master/jvmci

http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/compiler/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/common/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/code/stack/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/code/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/runtime/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/service/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/hotspot/package-tree.html
http://lafo.ssw.uni-linz.ac.at/javadoc/graalvm/all/jdk/internal/jvmci/code/TargetDescription.html

[Does Java 9 include Graal?](https://stackoverflow.com/questions/48252830/does-java-9-include-graal)
https://stackoverflow.com/questions/49505629/jdk-vm-ci-common-jvmcierror-no-jvmci-compiler-selected-with-java9-but-not-in-ja?noredirect=1&lq=1 

[GraalVM: the holy graal of polyglot JVM?](https://www.reddit.com/r/programming/comments/d0p52f/graalvm_the_holy_graal_of_polyglot_jvm/)

[29 GraalVM related talks at @OracleCodeOne and  @oracleopenworld](https://twitter.com/grashalm_/status/1171166305069752321). [article](https://blogs.oracle.com/graalvm/graalvm-at-oracle-code-one-and-oracle-openworld)

[Quarkus and GraalVM: Booting Hibernate at Supersonic Speed, Subatomic Size](https://www.infoq.com/presentations/quarkus-graalvm-sao-paulo-2019/)

[Graal: How to Use the New JVM JIT Compiler in Real Life](https://www.infoq.com/presentations/graal-jvm-jit/)

[Maximizing Performance with GraalVM](https://www.infoq.com/presentations/graalvm-performance/)

[interesting commentary towards the end on annotations & SubstrateVM](https://www.youtube.com/watch?v=f6a78mCrSeE)

[I don't get the difference substratevm - graal](https://news.ycombinator.com/item?id=16074410). [more](https://www.reddit.com/r/java/comments/73c9vb/has_anyone_of_you_used_aot_compilation_on_java9/)

> In every application I've tried, AOT actually decreases startup performance because of the time it takes to load the shared library. Class Data Sharing (CDS or AppCDS) might be a better choice 1

[Optimizing Java: Practical Techniques for Improving JVM Application Performance](https://www.goodreads.com/book/show/27015350-optimizing-java)

[Graal JIC C2](https://www.infoq.com/presentations/graal-jit-c2/)

[slides](https://qconlondon.com/system/files/presentation-slides/qcon-london.pdf)

> Graal isn’t just a JIT
> Many parts of a compiler are the same whether you do the
> compilation ahead of time or just in time
> You can do ahead of time compilation using jaotc

[check the JEP](https://stackoverflow.com/questions/48252830/does-java-9-include-graal)

> AOT compilation is done by a new tool, jaotc:

> jaotc --output libHelloWorld.so HelloWorld.class
> jaotc --output libjava.base.so --module java.base
> It uses Graal as the code-generating backend.

[slides - implementing ruby - interesting rationale for truffle](https://chrisseaton.com/truffleruby/ecoop14/ecoop14-ruby-truffle.pdf)

[investigate "bootstrapping"](https://github.com/oracle/graal/issues/1140)

[native IMAGE limitations](https://github.com/oracle/graal/blob/master/substratevm/LIMITATIONS.md). [some other info](https://technology.amis.nl/2018/08/21/java-programs-as-native-executables-graalvm-is-the-answer/)

[master your java applications on K8s](https://www.doag.org/formes/pubfiles/11148325/2019-NN-Andy_Moncsek-Master_your_Java_applications_in_Kubernetes-Praesentation.pdf)

> Cons: worse performance of long-running applications

> GraalVM allows you to compile your programs ahead-of-time into a native executable. The resulting program does not run on the Java HotSpot VM, but uses necessary components like memory management, thread scheduling from a different implementation of a virtual machine, called Substrate VM. Substrate VM is written in Java and compiled into the native executable. The resulting program has faster startup time and lower runtime memory overhead compared to a Java VM.

> Don’t overlook Serverless!! § GraalVM and other projects focusing low footprint & fast startup

> The application life cycle has changed § no longer dominated by uptime § startup is now critical to your application

[The GraalVM frenzy](https://medium.com/@jponge/the-graalvm-frenzy-f54257f5932c)

> requires more iterations than C2 to reach peak performance, un-tiered compilation (e.g., Graal without C1) is slower until Graal kicks-in.

> Today they can be combined, so that code is compiled with C1 first and then C2 later if they are still being executed a lot and it looks worth spending the extra time. This is called tiered compilation.

[what I learned writing my own JIT language](https://news.ycombinator.com/item?id=17408942)

[Graal(VM) – Versuch eines Überblicks](http://itblog.huber-net.de/2019/07/graalvm-versuch-eines-ueberblicks/)

> Es gibt bei jaotc jede Menge Einschränkungen, die den Einsatz in der Praxis wirkungsvoll verhindert haben – zumindest in der Breite. Immerhin gab es bei Java 10 einige Bemühungen, um diverse gravierende Einschränkungen wie “funktioniert nur unter Linux-x64” aufzuheben. GraalVM geht heute aber noch einen großen Schritt weiter mit “native-image”.

> libgraal ist der Versuch, den Graal-JIT-Compiler mittels GraalVM-native-image (dazu später mehr) in eine Bibliothek zu überführen, die das Performance-Problem des Compile-Vorgangs des Graal-JIT-Compilers in der JVM lösen soll. Da schon alles in nativem Code vorliegt, muss sich der JIT-Compiler nur noch um den Anwendungscode kümmern und nicht mehr um sich selbst. Im Prinzip wird dadurch Graal zu einem – was das Laufzeitverhalten angeht – sehr ähnlichen JIT-Compiler wie der klassische C1 und C2 in der HotSpot-JVM. Langsame JIT-Compilierung während der JVM-Warm-Up-Phase wird dadurch verhindert.

[How do I run a class compiled with jaotc?](https://stackoverflow.com/questions/45298045/how-do-i-run-a-class-compiled-with-jaotc/45298588) Aha! Es esta la principal diferencia con native-image?

[libgraal: GraalVM compiler as a precompiled GraalVM native image](https://medium.com/graalvm/libgraal-graalvm-compiler-as-a-precompiled-graalvm-native-image-26e354bee5c). [HN](https://news.ycombinator.com/item?id=20448766) "but still no windows support of position-independent code". 

> This has several advantages, libgraal improves startup times and completely avoids interfering with the heap usage and profiling of the application code. That is, the compiler now “codes like Java, runs like C++”. More specifically in the context of HotSpot, libgraal executes like C2 while preserving most of the advantages of a managed runtime. Libgraal significantly contributes to improving the compilation speed and performance on shorter and medium length workloads in GraalVM 19.1 release. Keep reading to learn more.

> The primary benefit of libgraal is that compilations are fast from the start. This is because the compiler is running compiled from the get-go, by-passing the HotSpot interpreter altogether. Furthermore, it’s compiled by itself. By contrast, jargraal is compiled by C1. The result is that the compiled code of the compiler is more optimized with libgraal than with jargraal.

> They're still keeping performance optimizations out of CE (free) version. Unheard of for a language runtime and quite crappy

[Oracle GraalVM Enterprise Edition 19 Guide - Compiler Options - good info!](https://docs.oracle.com/en/graalvm/enterprise/19/guide/overview/compiler.html)

> There are two operating modes of the GraalVM compiler when used as a HotSpot JIT compiler:

> libgraal: the GraalVM compiler is compiled ahead of time into a native shared library. In this operating mode, the shared library is loaded by the HotSpot VM. The compiler uses memory separate from the HotSpot heap and it runs fast from the start since it does not need to warm-up. This is the default and recommended mode of operation.

> jargraal: the GraalVM compiler goes through the same warm-up phase that the rest of Java application does. That is, it is first interpreted before its hot methods are compiled. This mode is selected with the -XX:-UseJVMCINativeLibrary command line option. This will delay the time to reach peak performance as the compiler itself needs to be compiled before it produces code quickly. This mode allows you to debug the GraalVM compiler with a Java debugger.

[Run JVM-based Languages with GraalVM Enterprise](https://docs.oracle.com/en/graalvm/enterprise/19/guide/reference/jvm-languages.html)

> The compiler depends on a JVM that supports a compatible version of the JVM Compiler Interface (JVMCI). GraalVM Enterprise includes a version of the HotSpot JVM that supports JVMCI. JVMCI is a privileged low-level interface to the JVM. It can read metadata from the VM such as method bytecode and install machine code into the VM . GraalVM Enterprise includes the Truffle Language Implementation framework. For improved performance of Truffle Abstract Syntax Trees (AST), they are compiled to machine code by the GraalVM compiler. When such a Truffle AST is hot (i.e., called many times), it is scheduled for compilation by the compiler. The pipeline for such a compilation is:

> Truffle Framework code and data (AST) is partially evaluated to produce a compilation graph.
> The compilation graph is optimized by the GraalVM compiler to produce machine code.
> The JVMCI API is used to install this machine code in the VM’s code cache.
> The AST will automatically redirect execution to the installed machine code once it is available. [NOTE: look more into this]

> If an uncaught exception is thrown by the compiler, the compilation is simply discarded and execution continues. However, the compiler can instead produce diagnostic data (such as compiler immediate representation graphs) that can be submitted along with a bug report. This is enabled with -Dgraal.CompilationFailureAction=Diagnose. The default location of the diagnostics output is in graal_dumps/ under the current working directory of the process but can be changed with the -Dgraal.DumpPath option. During VM shutdown, the location of the archive containing the diagnostic data is printed to the console.

[Running JVM-based Apps](https://www.graalvm.org/docs/reference-manual/languages/jvm/) good resource about options

> Difference between running the GraalVM compiler in a Native Image vs on the JVM
When running the GraalVM compiler on the JVM, it goes through the same warmup phase that the rest of Java application does. That is, it is first interpreted before its hot methods are compiled. This can translate into slightly longer times until the application reaches peak performance when compared to the native compilers in the JVM such as C1 and C2.

> To address the issue of taking longer to reach to peak performance, libgraal was introduced – a shared library, produced using Native Image framework to ahead-of-time compile the compiler itself. That means the GraalVM compiler is deployed as a native shared library. In this mode, the compiler uses memory separate from the HotSpot heap and it runs compiled from the start. That is, it has execution properties similar to other native HotSpot compilers such as C1 and C2. Currently, this is the default mode of operation in both GraalVM Community and Enterprise images. It can be disabled with -XX:-UseJVMCINativeLibrary.

[Under the hood of GraalVM JIT optimizations](https://medium.com/graalvm/under-the-hood-of-graalvm-jit-optimizations-d6e931394797) very good

[really small java apps](https://news.ycombinator.com/item?id=21450079)

> GraalVM native-image is not a listed option, but I regularly use it to produce binaries that are competitive with (often better than) Go in terms of size and (start time) perf.
> A Clojure tool that parses, traverses and processes JSON (caro, see below) worked out to 3.2MB. I'm sure C and Rust can do better, but it's not bad compared to a JVM, and it's an order of magnitude better than the best option in the article. It's also small enough that while comparisons like "that's three floppies!" are interesting historical perspective, you can't reasonably complain about having a 3 MB binary in ~/.local/bin.

[Everything you need to know about GraalVM](https://twitter.com/thomaswue/status/1192794746470711302) 3h!

[A race of two compilers: GraalVM JIT versus HotSpot JIT C2](https://www.youtube.com/watch?v=pnVdUCfgwKo&feature=emb_logo) [slides](https://twitter.com/ionutbalosin/status/1192910873905508353)

[The sea of nodes and the HotSpot JIT](https://www.youtube.com/watch?v=98lt45Aj8mo)

Not directly related to Graal, but cool stuff:

Devoxx Ukraine 2019: The Sea of Nodes and the HotSpot JIT https://www.youtube.com/watch?v=98lt45Aj8mo&feature=youtu.be
https://www.youtube.com/watch?v=-vizTDSz8NU A JVM Does That?
JIT and AOT in the JVM https://www.youtube.com/watch?v=gx8DVVFPkcQ
Understanding the Tricks Behind the JIT https://www.youtube.com/watch?v=oH4_unx8eJQ
https://www.youtube.com/watch?v=-vizTDSz8NU A JVM does that?

[Quarkus http://1.0.0.Final](https://twitter.com/myfear/status/1199003816676470784)

[Compiling Native Projects via the GraalVM LLVM Toolchain](https://medium.com/graalvm/graalvm-llvm-toolchain-f606f995bf)

[mixed interactive debugging](https://twitter.com/graalvm/status/1205561788324028417)

[lambdas](https://twitter.com/headius/status/1207846145210355712)

[2019 year in review](https://medium.com/graalvm/graalvm-in-2019-year-in-review-9ae272816e47)

## native-image

[Profile-guided Optimizations](https://www.graalvm.org/docs/reference-manual/aot-compilation/)

> GraalVM also supports monitoring and generating heap dumps of the Native Image processes.

> Warning: This functionality is available in the Enterprise Edition of GraalVM.

> For additional performance gain and higher throughput in GraalVM ahead-of-time (AOT) mode, make use of profile-guided optimizations (PGO). With PGO, you can collect the profiling data in advance and then feed it to the GraalVM native-image utility, which will use this information to optimize the performance of the resulting binary.

> Warning: Profile-guided optimizations (PGO) is a GraalVM Enterprise feature.

> To achieve such aggressive ahead-of-time optimizations, we run an aggressive static analysis that requires a closed-world assumption. We need to know all classes and all bytecodes that are reachable at run time. Therefore, it is not possible to load new classes that have not been available during ahead-of-time-compilation.

[about inlining](https://miuv.blog/2018/02/25/jit-optimizations-method-inlining/). [Java on Steroids: 5 Super Useful JIT Optimization Techniques](https://blog.overops.com/java-on-steroids-5-super-useful-jit-optimization-techniques/). [compiler inlining messages](https://wiki.openjdk.java.net/display/HotSpot/Server+Compiler+Inlining+Messages). [the meaning of non-entrant](https://stackoverflow.com/questions/2930838/java-printcompilation-output-whats-the-meaning-of-made-not-entrant-and-made). [baeldung](https://www.baeldung.com/jvm-method-inlining)

[hot code is faster code - addressing JVM warmup](https://es.slideshare.net/MarkPrice7/hot-code-is-faster-code-addressing-jvm-warmup-110231712)

[GraalVM: Run Programs Faster Everywhere - 2019](https://www.youtube.com/watch?v=6hd7UFlsIsg)

[Can GraalVM combine ahead of time compilation with adaptive optimization?](https://stackoverflow.com/questions/55957553/can-graalvm-combine-ahead-of-time-compilation-with-adaptive-optimization)

> AOT libraries can be compiled in two modes controlled by --compile-for-tiered flag:

> Non-tiered AOT compiled code behaves similarly to statically compiled C++ code, in that no profiling information is collected and no JIT recompilations will happen.

> Tiered AOT compiled code does collect profiling information. The profiling done is the same as the simple profiling done by C1 methods compiled at Tier 2. If AOT methods hit the AOT invocation thresholds then these methods are recompiled by C1 at Tier 3 first in order to gather full profiling information. This is required for C2 JIT recompilations in order to produce optimal code and reach peak application performance.

[Graal IR: An Extensible Declarative Intermediate Representation](https://pdfs.semanticscholar.org/6688/214dab5456c75c99f8171846242e09d4f5e3.pdf)

[GraalVM: the holy graal of polyglot JVM?](https://www.transposit.com/blog/2019.01.02-graalvm-holy/)

[Learn about the trade-offs between GraalVM's JIT mode and its AOT mode](https://twitter.com/thomaswue/status/1175152815129468936). [GraalVM-Native Images: The Best Startup Solution for Your Applications](https://www.youtube.com/watch?v=z0jedLjcWjI)

[...custom JVMCI implementation...](https://twitter.com/kmett/status/1177775208591048705). [reddit](https://www.reddit.com/r/programming/comments/da1ruc/closures_crafting_interpreters/)

[Graal native compilations are expensive](https://twitter.com/rotnroll666/status/1177603313115770880)

[Native Clojure with Graal](https://www.youtube.com/watch?v=kjZP_wBQJ2U)

[Graal criticism](https://twitter.com/danieldietrich/status/1179692365180743681)

[Lots of GraalVM internship positions available all over the world](https://twitter.com/grashalm_/status/1182259810747764736)

[JEP 295: Ahead-of-Time Compilation](https://openjdk.java.net/jeps/295)

> The logical compilation mode for java.base is tiered AOT since JIT recompilation of java.base methods is desired to reach peak performance. Only in certain scenarios does a non-tiered AOT compilation make sense. This includes applications which require predictable behavior, when footprint is more important than peak performance, or for systems where dynamic code generation is not allowed. In these cases, AOT compilation needs be done on the entire application and is thus experimental in JDK 9.

[Tika](https://jaxenter.com/apache-tika-data-driven-analytics-heart-modern-applications-163377.html)

The lower memory footprint is achieved due to a number of reasons. One of them is to do with the fact that reading the configuration files, particularly in XML format, results in loading a lot of class instances required to parse the configuration. Yet another reason is that Substrate VM does not need to aggressively optimize the way the traditional Java VM does it so there is no need to keep the extra meta-data in memory.

[tweet](https://twitter.com/headius/status/1187032596162777089)

> Graal native images will work well for the very smallest, self-contained apps, but the build time is rather long and the lack of dynamic code loading limits use cases. For local development tasks, inability to rapidly iterate code and load libraries is a showstopper.

[Java JIT vs Java AOT vs Go for small, short-lived processes](http://macias.info/entry/201912201300_graal_aot.md) [notes about memory usage](https://twitter.com/nicolas_frankel/status/1209392586051538945). [more](https://news.ycombinator.com/item?id=21871645)

> The optimization capabilities of a JIT compiler makes the executable running faster than in any other implementation.

[Quarkus & Graal VM 2020](https://www.youtube.com/watch?v=sCb26d44UBk&feature=youtu.be)

## Truffle

Investigate partial evaluation and exact relationship with JVCI.

[This Tuffle language exposes GPUs to the polyglot GraalVM. The goal is to](https://github.com/NVIDIA/grcuda)

[Safe and sandboxed execution of native code](https://medium.com/graalvm/safe-and-sandboxed-execution-of-native-code-f6096b35c360)

[Will the JVM ever inline an object's instance variables and methods?](https://stackoverflow.com/questions/6215138/will-the-jvm-ever-inline-an-objects-instance-variables-and-methods) [Is this up-to-date](http://www.ssw.uni-linz.ac.at/Research/Papers/Wimmer08PhD/Wimmer08PhD.pdf)?

[Futamura projections](https://twitter.com/DiazCarrete/status/1173661122001588224)

[publications](https://github.com/oracle/graal/blob/master/docs/Publications.md)

[Partial Evaluation and Automatic Program Generation](https://www.goodreads.com/book/show/3267877-partial-evaluation-and-automatic-program-generation)

> • Truffle Optimizer: this includes the partial evaluation, and is implemented on top of the API that the Graal compiler [45] provides. [partial evaluation depends on GRAAL!]

[Self-Specialising Interpreters and Partial	Evaluation (2016)](https://chrisseaton.com/truffleruby/metass16/metass.pdf)

> The main overhead in our interpreter comes from dynamic dispatch between nodes.
However, the targets of those dynamic dispatches are constant except when
rewriting occurs.  We count the number of invocations of a tree and reset the
counter in the event of a node replacement. When the number of invocations on a
stable tree exceeds a threshold, we speculate that the tree has reached its
final state. We then start a special compilation for a specific tree where we
assume every node in the tree remains unmodified. This way, the virtual
dispatch between the execute nodes can be converted to a direct call, because
the receiver is a constant.  These direct calls are all inlined, forming one
combined unit of compilation for a whole tree.  Because every node of the tree
is assumed constant, many values in the tree can also be treated as constants.
This helps the compiler produce efficient code for nodes that have constant
parameters. Examples include the actual value of a constant node, the index of
a local variable access (see Section 4.2), and the target of a direct call.
This special compilation of the interpreter by assuming the nodes in the tree
to be constants is an application of partial evaluation to generate compiled
code from an interpreter definition [21].

[One VM to Rule Them All by Thomas Wuerthinger](https://www.youtube.com/watch?v=mMmOntDWSgw). [One VM to Rule Them All? Lessons Learned with GraalVM](https://www.youtube.com/watch?v=hPjDWzPiaCs)

[Tracing vs. Partial Evaluation Comparing Meta-Compilation Approaches for Self-Optimizing Interpreters](https://stefan-marr.de/papers/oopsla-marr-ducasse-meta-tracing-vs-partial-evaluation/)

[Best practice: Use Java exceptions for inter-node control flow](https://chrisseaton.com/truffleruby/metass16/metass.pdf)

[To investigate performance issues, we recommend the Ideal Graph Visualizer (here and after “IGV”)](https://www.graalvm.org/docs/graalvm-as-a-platform/implement-language/#dump-graphs)

[Practical Partial Evaluation for High-Performance Dynamic Language Runtimes](https://chrisseaton.com/rubytruffle/pldi17-truffle/pldi17-truffle.pdf). [One VM to Rule Them All paper](http://lafo.ssw.uni-linz.ac.at/papers/2013_Onward_OneVMToRuleThemAll.pdf)

> Our approach significantly reduces the implementation effort for a dynamic
language by decoupling the language semantics and the optimization system.
However, this comes at the cost of longer warmup times compared to a runtime
system specialized for a single language. Our measurements show that warmup
times are an order of magnitude longer than in a specialized runtime.

> Graal compiles Java bytecode to optimized machine code, and can serve as a replacement for the Java HotSpot server compiler. **We extended it with a frontend that performs PE**, and added intrinsic methods that support our core primitives.

[Applying Futamura Projections to Compose Languages and Tools in GraalVM (Invited Talk)](https://popl19.sigplan.org/details/pepm-2019-papers/2/Applying-Futamura-Projections-to-Compose-Languages-and-Tools-in-GraalVM-Invited-Talk)

[Benchmarking Partial Evaluation in Truffle](http://ssw.jku.at/General/Staff/Latifi/vmm18/presentation.pdf)

> Speed up partial evaluation: by implementing second Futamura projection

https://github.com/graalvm/simplelanguage https://chrisseaton.com/truffleruby/metass16/metass.pdf
https://github.com/oracle/graal/tree/master/truffle/docs
https://github.com/oracle/graal/tree/master/truffle#using-truffle
https://github.com/oracle/graal/blob/master/truffle/docs/LanguageTutorial.md
https://github.com/oracle/graal/blob/master/truffle/docs/TruffleLibraries.md
https://github.com/oracle/graal/blob/master/truffle/docs/InteropMigration.md

For an excellent, in-depth presentation on how to implement your language with Truffle, please have a look at a three hour walkthrough presented at a recent Conference on Programming Language Design and Implementation PLDI 2016.

[crafting interpreters](http://craftinginterpreters.com/closures.html)

[Why is 2 * (i * i) faster than 2 * i * i](https://stackoverflow.com/questions/53452713/why-is-2-i-i-faster-than-2-i-i-in-java)

["Language-Independent Development Environment Support for Dynamic Runtimes"(https://twitter.com/grashalm_/status/1177514061963022337)

[Haskell & Truffle](https://www.reddit.com/r/haskell/comments/8dr3xw/could_haskell_benefit_from_graalvm/)

https://github.com/ekmett/core

[How does PE take place for a Truffle interpreter AOT-compiled with native-image?](https://stackoverflow.com/questions/58361484/how-does-pe-take-place-for-a-truffle-interpreter-aot-compiled-with-native-image/58367455#58367455)

[Origins of IGV](https://twitter.com/thomaswue/status/1187704665498177536)

[Deep dive into using GraalVM for Java and JavaScript developers](https://www.youtube.com/watch?v=a-XEZobXspo)

[@ExplodeLoop](https://twitter.com/grashalm_/status/1199636566009884674)

[Why use truffle](https://twitter.com/grashalm_/status/1212763944043139072)

## JVM flags and properties

    -XX:+UnlockExperimentalVMOptions 
    -XX:+EnableJVMCI 
    -XX:+UseJVMCICompiler 
    -XX:-TieredCompilation 
    -XX:+PrintCompilation 
    -XX:CompileOnly=Demo::workload 
    
    -XX:+PrintCompilation -XX:+UnlockDiagnosticVMOptions -XX:+PrintInlining
    
    -XX:+LogCompilation
    -XX:LogFile=foo.log t
    
    -Djvmci.Compiler=graal
    GraalCompileOnly
    CompileGraalWithC1Only "we just compile with C1 and that's usually fine" relationship with libgraal

    AOTLibrary
    
    --tool:chromeinspector
    Run a java program in JIT mode with a -Dgraal.PGOInstrument
    
    --language:python to make sure Python is available as a language for the image;
    
    -XX:FreqInlineSize=10
    
    -XX:+UnlockExperimentalVMOptions -XX:+EnableJVMCI -XX:+JVMCIPrintProperties
    
    GraalVM supports debugging of guest language applications and provides a built-in implementation of the Chrome DevTools Protocol. This allows you to attach compatible debuggers such as Chrome Developer Tools to GraalVM.

[HotSpot Graal compiler factory](https://github.com/oracle/graal/blob/master/compiler/src/org.graalvm.compiler.hotspot/src/org/graalvm/compiler/hotspot/HotSpotGraalCompilerFactory.java)

[For Metropolis with libgraal, CompileGraalWithC1Only doesn't make sense to me](https://bugs.openjdk.java.net/browse/JDK-8218926)

[TruffleRuby and deoptimization](https://news.ycombinator.com/item?id=22841847)

# Other

[Build Great Native CLI Apps in Java with Graalvm and Picocli](https://twitter.com/InfoQ/status/1236259549310529536)

[Interview on GraalVM](https://twitter.com/maxandersen/status/1254334393029623814)

[graalvm tips and tips for quarkus](https://twitter.com/_JamesWard/status/1258399220903673860)

[Spring Tips: Spring and GraalVM (pt. 2)](https://www.youtube.com/watch?v=aTNLtU5YYtg)

[Truffle Tutorial: Adding 1 and 1 Together](https://norswap.com/truffle-tutorial/)

[Java frameworks for the cloud: Establishing the bounds for rapid startups](https://blogs.oracle.com/javamagazine/java-frameworks-for-the-cloud-establishing-the-bounds-for-rapid-startups)

[Announcing GraalVM 20.2.0](https://medium.com/graalvm/announcing-graalvm-20-2-0-674e7f6dae27)

[How the HotSpot and Graal JVMs execute Java Code](https://twitter.com/InfoQ/status/1313113258639974400)

[Java on Truffle – Going Fully Metacircular](https://news.ycombinator.com/item?id=25838364)

[Cadenza Building Fast Functional Languages Fast](https://www.reddit.com/r/haskell/comments/l95mb6/edward_kmett_cadenza_building_fast_functional/)
