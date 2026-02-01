[Anatomy of a Program in Memory](https://manybutfinite.com/post/anatomy-of-a-program-in-memory/). [hn](https://news.ycombinator.com/item?id=452005). [more hn](https://news.ycombinator.com/item?id=16955523).

[Awesome LD_PRELOAD](https://github.com/gaul/awesome-ld-preload/blob/master/README.md)

[Branch Prediction - Fundamentals Every Programmer Need Not Know](http://www.mycpu.org/branch-prediction-basics/)

[Watching for software inefficiencies with Valgrind](https://kristerw.blogspot.com/2020/02/watching-for-software-inefficiencies.html)

[Lecture 12	How Linux Works II : I/O, Memory Management, Booting, Loadable Kernel Modules](https://www.cis.upenn.edu/~cis191/lectures.html)

> In Linux, network devices aren't represented as device files; network interfaces exist in their own namespace and export a different set of operations.

[FOSDEM20 events](https://fosdem.org/2020/schedule/events/) [Go debuggind with GDB](https://www.youtube.com/watch?v=2kjmLQY8RJk) [The GDB Text User Interface](https://fosdem.org/2020/schedule/event/debugging_gdb_tui/) [Postmodern strace](https://fosdem.org/2020/schedule/event/debugging_strace_modern/). [Debugging apps running in Kubernetes
](https://fosdem.org/2020/schedule/event/debugging_kubernetes/)

[tcmalloc](https://twitter.com/dvyukov/status/1227874576434110471)

[RAM and bus timing](https://www.reddit.com/r/programming/comments/f4mstp/ram_and_bus_timing_ben_eater/)

[Firecracker paper from AWS - isolation](https://twitter.com/copyconstruct/status/1229982588732751872). [paper](https://www.amazon.science/publications/firecracker-lightweight-virtualization-for-serverless-applications). [Firecracker – Lightweight Virtualization for Serverless Computing](https://aws.amazon.com/blogs/aws/firecracker-lightweight-virtualization-for-serverless-computing/). [main page](https://firecracker-microvm.github.io/)

[virtualization concepts](https://twitter.com/b0rk/status/1229768879569805313)

[Loading NumPy arrays from disk: mmap() vs. Zarr/HDF5](https://news.ycombinator.com/item?id=22423632)

[Cost of a thread in C++ under Linux](https://lemire.me/blog/2020/01/30/cost-of-a-thread-in-c-under-linux/)

[When Bloom filters don't bloom](https://blog.cloudflare.com/when-bloom-filters-dont-bloom/) [hn](https://news.ycombinator.com/item?id=22463979)

[Two new ways to read a file quickly](https://news.ycombinator.com/item?id=22506184)

[Bus errors, core dumps, and binaries on NFS (2018)](https://news.ycombinator.com/item?id=22509943)

[Want fast C++? Know your hardware!](https://www.youtube.com/watch?v=BP6NxVxDQIs)

[cache associativity. Here's my attempt to explain: The cache stores data in cache sets, which can each hold a number of cache lines (typically 64 byte chunks). It's best to think of cache sets like buckets in a hash table](https://twitter.com/typeswitch/status/1236776268143755266)

[Memory efficient search trees help with cache amplification](https://twitter.com/MarkCallaghanDB/status/1237401294484078595)

[Linux kernel teaching](https://news.ycombinator.com/item?id=22564665)

[Writing a memory allocator for fast serialization (2017)](https://lobste.rs/s/peaoze)

[Linux Kernel Development and Writing a Simple Kernel Module (2018)](https://news.ycombinator.com/item?id=22579640)

[Optimizing Interrupt Handling Performance for Memory Failures in Large Scale Data Centers](https://research.fb.com/publications/optimizing-interrupt-handling-performance-for-memory-failures-in-large-scale-data-centers/)

[Compiled tips 'n tricks guide for PIC microcontrollers (2009) [pdf]](https://news.ycombinator.com/item?id=22648563)

[A Comparison of Software and Hardware Techniques for x86 Virtualization](https://www.vmware.com/pdf/asplos235_adams.pdf) obsolete with newer hardware, but of historical interest

[Understanding the bin, sbin, usr/bin, usr/sbin split (2010)](https://news.ycombinator.com/item?id=22614731)

[Why the EAX register of x86 is called like that](https://news.ycombinator.com/item?id=22645910)

[A “living” Linux process with no memory](https://news.ycombinator.com/item?id=22693805)

[Understanding CPU Microarchitecture to Increase Performance](https://www.infoq.com/presentations/microarchitecture-modern-cpu/)

[how are uniz pipes implemented](https://toroid.org/unix-pipe-implementation)

[jvm inside out](https://blog.adamfurmanek.pl/2020/01/04/jvm-inside-out-part-2/)

[learn ePBF tracing](http://www.brendangregg.com/blog/2019-01-01/learn-ebpf-tracing.html). [more on epvf](https://docs.google.com/presentation/d/1AcB4x7JCWET0ysDr0gsX-EIdQSTyBtmi6OAW7bE0jm0/edit#slide=id.g704abb5039_2_106). [hn](https://news.ycombinator.com/item?id=22953730).

[Optimising for Concurrency: Comparing the BEAM and JVM virtual machines](https://news.ycombinator.com/item?id=23168119)

[Hoare’s Rebuttal and Bubble Sort’s Comeback](https://blog.reverberate.org/2020/05/29/hoares-rebuttal-bubble-sorts-comeback.html)

[Linux kernel map](https://makelinux.github.io/kernel/map/)

[virtualization papers](https://twitter.com/MarcJBrooker/status/1270081815139635200)

[The Subtle Semantics of epoll_wait](https://jfischoff.github.io/blog/when-threadwaitread-doesnt.html)

[cache-oblivious algorithms](https://news.ycombinator.com/item?id=23662434) [cache-line associativity](https://stackoverflow.com/questions/15617871/how-would-you-generically-detect-cache-line-associativity-from-user-mode-code)

> I tried cache-oblivious algorithms for some numerical code, but found them underwhelming. The cache-oblivious model does not consider the effects of prefetching and cache line associativity. Both can make a huge difference.

[dynamic linking](https://blog.stephenmarz.com/2020/06/22/dynamic-linking/)

[bg](http://www.brendangregg.com/overview.html)

[malloc geirger counter](https://news.ycombinator.com/item?id=24303832j)

[initcalls](https://www.collabora.com/news-and-blog/blog/2020/09/25/initcalls-part-2-digging-into-implementation/)

[mmap vs system calls](https://lobste.rs/s/h5dfjo/why_mmap_is_faster_than_system_calls)

[How debuggers work](https://www.moritz.systems/blog/how-debuggers-work-getting-and-setting-x86-registers-part-1/)

[What's in a Linux Executable?](https://news.ycombinator.com/item?id=24926925)

[File Descriptor Transfer over Unix Domain Sockets](https://news.ycombinator.com/item?id=24964966)

[C is not a low-level language](https://queue.acm.org/detail.cfm?id=3212479)

[Why mmap is faster than system calls – by Alexandra (Sasha) Fedorova](https://news.ycombinator.com/item?id=25701959)

[Tracking a segfault](https://news.ycombinator.com/item?id=25818126)

[	But how, exactly, do databases use mmap? ](https://news.ycombinator.com/item?id=25881911)

[Recreating An Old "Dirty Gamedev Trick"](http://kylehalladay.com/blog/2019/12/04/Recreating-A-Dirty-Gamedev-Hack.html)

[what's the last problem you solved using strace?](https://twitter.com/b0rk/status/1378014888405168132). [post](https://lobste.rs/s/d9ucpe/what_problems_do_people_solve_with_strace)

[A Primer on Memory Consistency and Cache Coherence, Second Edition](https://www.morganclaypool.com/doi/10.2200/S00962ED2V01Y201910CAC049)

[	Dropping cache didn’t drop cache ](https://blog.twitter.com/engineering/en_us/topics/open-source/2021/dropping-cache-didnt-drop-cache.html) [hn](https://news.ycombinator.com/item?id=27086209)

[Hardware memory models](https://twitter.com/_rsc/status/1409930048480727043)

[How to add eBPF observability to your product ](https://news.ycombinator.com/item?id=27722947)

[Computing Performance on the Horizon](https://news.ycombinator.com/item?id=27738312)

[Linux block devices: hints for debugging and new developments](https://news.ycombinator.com/item?id=28400579)

[How PCI-Express works (2020)](https://news.ycombinator.com/item?id=28490021)

[The speed of time](https://www.brendangregg.com/blog/2021-09-26/the-speed-of-time.html)

[Debugging a hang: Chasing the wait chain inside a process](https://devblogs.microsoft.com/oldnewthing/20141024-00/?p=43773)

[Debugging memory corruption: who the hell writes “2” into my stack? (2016)](https://news.ycombinator.com/item?id=29215725)

[You can't copy code with memcpy](https://news.ycombinator.com/item?id=29729931)

[Executable and Linkable Format 101 Part 3: Relocations](https://www.intezer.com/blog/malware-analysis/executable-and-linkable-format-101-part-3-relocations/). [Haskell](https://github.com/zw3rk/mobile-core-log/blob/master/LOG.md). [CS 140: Operating Systems (Winter 2013)](https://web.stanford.edu/~ouster/cgi-bin/cs140-winter13/lecture.php?topic=vm). [CS 537 Notes, Section #15: Base and Bounds, Segmentation](http://pages.cs.wisc.edu/~bart/537/lecturenotes/s15.html).

[Bootloader basics](https://lobste.rs/s/vfxz9s/bootloader_basics)

[MIT 6.S081 – Operating System Engineering](https://news.ycombinator.com/item?id=30094376)

[Landing a new syscall, part 1: What is futex?](https://news.ycombinator.com/item?id=30271902)

[Restartable Sequences in Glibc 2.35](https://news.ycombinator.com/item?id=30285032)

[Anatomy of a Terminal Emulator](https://poor.dev/blog/terminal-anatomy/)

[Analysis and introspection options in linkers](https://maskray.me/blog/2022-02-27-analysis-and-introspection-options-in-linkers)

[Debugging with GDB](https://felix-knorr.net/blog/using_gdb_directly.html)

[Pointer Tagging for x86 Systems](https://news.ycombinator.com/item?id=30865423)

[Indirect branch tracking in Linux for Intel CPUs ](https://news.ycombinator.com/item?id=30868032)

[Magic-trace – High-resolution traces of what a process is doing](https://news.ycombinator.com/item?id=31121319)

[The Lost Art of C Structure Packing](https://news.ycombinator.com/item?id=31182449)

[Alignment](https://en.wikipedia.org/wiki/Data_structure_alignment)

> Padding is only inserted when a structure member is followed by a member with a larger alignment requirement or at the end of the structure. 

[Alignment and endianness](https://developer.arm.com/documentation/102376/0100/Alignment-and-endianness)

> An access is described as aligned if the address is a multiple of the element size.

[What Programmers Should Know About Memory Allocation](https://www.youtube.com/watch?v=gYfd25Bdmws)

[debugging a JVM crash](https://twitter.com/BrianJStafford/status/1523789921764356096)

[gcc profiler internals](https://trofi.github.io/posts/243-gcc-profiler-internals.html)

[Logging C Functions](https://news.ycombinator.com/item?id=31443198)

[What happens when you press a key in your terminal?](https://news.ycombinator.com/item?id=32175100)

[How much memory my program uses or the tale of working set size](https://biriukov.dev/docs/page-cache/7-how-much-memory-my-program-uses-or-the-tale-of-working-set-size/#how-much-memory-my-program-uses-or-the-tale-of-working-set-size)

[I don't understand terminals, shells and SSH](https://news.ycombinator.com/item?id=34382976)

[Investigating Filter Communication Ports](https://windows-internals.com/investigating-filter-communication-ports/)

[Huge pages](https://lobste.rs/s/hwf01p/huge_pages_are_good_idea)

[Reverse engineering the MacBook clamshell mode](https://alinpanaitiu.com/blog/turn-off-macbook-display-clamshell/)

[bad news with transparent hugepages](https://news.ycombinator.com/item?id=34607604)

[A complete guide to Linux process scheduling](https://trepo.tuni.fi/bitstream/handle/10024/96864/GRADU-1428493916.pdf)

[Linux Debuginfo Formats - DWARF, ELF, dwo, dwp - What are They All?](https://www.youtube.com/watch?v=l3h7F9za_pc)

[ sometimes just stracing code to make sure I can explain all syscalls](https://twitter.com/pkhuong/status/1637081793730867200)

[misattribute the reduction](https://twitter.com/kmett/status/1642072709923508224)

[libc](https://twitter.com/eatonphil/status/1644657305181454337)

[Searchable Linux Syscall Table for x86 and x86_64](https://news.ycombinator.com/item?id=35574259)

[Unwinding the stack the hard way](https://lesenechal.fr/en/linux/unwinding-the-stack-the-hard-way)

[How Does an Intel Processor Boot? (2018)](https://news.ycombinator.com/item?id=35598636)

[The use of mmap for databases, can lead to TLB shootdowns](https://twitter.com/PeterVeentjer/status/1655060775726198786)

[linux fault injection tools](https://twitter.com/eatonphil/status/1657192644114632705)

[memory initialization, a visual guide](https://samwho.dev/memory-allocation/)

[Direct Syscalls vs Indirect Syscalls](https://redops.at/en/blog/direct-syscalls-vs-indirect-syscalls)

[linux kernel modules](https://sysprog21.github.io/lkmpg/)

[behind Hello world on Linux](https://jvns.ca/blog/2023/08/03/behind--hello-world/)

[Using LD_PRELOAD to cheat, inject features and investigate programs](https://news.ycombinator.com/item?id=37439125)

[How does Linux start a process](https://news.ycombinator.com/item?id=37521240)

[Intercepting and modifying Linux system calls with ptrace](https://notes.eatonphil.com/2023-10-01-intercepting-and-modifying-linux-system-calls-with-ptrace.html)

[Faster hash maps, binary trees etc. through data layout modification](https://johnnysswlab.com/faster-hash-maps-binary-trees-etc-through-data-layout-modification/)

[Faster & Fewer Page Faults](https://www.youtube.com/watch?v=TEHRMzZ01nE). [tweet](https://twitter.com/debasishg/status/1710308840732807334). [Maple tree](https://www.youtube.com/watch?v=XwukyRAL7WQ).

[Not knowing the /proc file system](https://news.ycombinator.com/item?id=38009372). [A tale of /dev/fd](http://phala.isatty.net/~amber/hacks/devfd). [and dup](https://utcc.utoronto.ca/~cks/space/blog/unix/DevFdAndDup)

[backtraces with strace](https://shane.ai/posts/backtraces-with-strace/)

[storing data in pointers](https://lobste.rs/s/5417dx/storing_data_pointers)

[How are zlib, gzip and zip related?](https://news.ycombinator.com/item?id=38432127)

[bootloader debugging story](https://michael.stapelberg.ch/posts/2024-02-11-minimal-linux-bootloader-debugging-story/)

[Anatomy of a system call, part 1](https://lwn.net/Articles/604287/)

[Linux crisis tools](https://www.brendangregg.com/blog/2024-03-24/linux-crisis-tools.html)

["Unstripping" binaries: Restoring debugging information in GDB](https://news.ycombinator.com/item?id=41481682)

[ keisku/gmon: An eBPF tool monitoring a goroutine](https://github.com/keisku/gmon)

[ECS 150: Operating Systems and System Programming](https://lupteach.gitlab.io/courses/ucd-ecs150/online/)

[Exploring the mild oddity that Unix pipes are buffered](https://utcc.utoronto.ca/~cks/space/blog/unix/BufferedPipes)

[0+0 > 0: C++ thread-local storage performance](https://news.ycombinator.com/item?id=43077675)

[Debugging an Undebuggable App](https://news.ycombinator.com/item?id=43081713). [How setup a React project with Vite, Typescript and Tailwind](https://www.reddit.com/r/reactjs/comments/1irl9pc/how_setup_a_react_project_with_vite_typescript/).

[Giving up the dylib dream](https://lobste.rs/s/ybbhxp/giving_up_dylib_dream)

[vdso](https://man7.org/linux/man-pages/man7/vdso.7.html). [How does ld load itself?](https://stackoverflow.com/questions/53786527/how-does-ld-load-itself). [How to run programs with ld-linux.so?](https://unix.stackexchange.com/questions/467999/how-to-run-programs-with-ld-linux-so). [What is the .interp section in an ELF and how do custom loaders work?](https://stackoverflow.com/questions/70648681/what-is-the-interp-section-in-an-elf-and-how-do-custom-loaders-work)

[sonames](https://tldp.org/HOWTO/Program-Library-HOWTO/shared-libraries.html)

> Every shared library has a special name called the ``soname''. The soname has the prefix ``lib'', the name of the library, the phrase ``.so'', followed by a period and a version number that is incremented whenever the interface changes (as a special exception, the lowest-level C libraries don't start with ``lib''). A fully-qualified soname includes as a prefix the directory it's in; on a working system a fully-qualified soname is simply a symbolic link to the shared library's ``real name''.

> Every shared library also has a ``real name'', which is the filename containing the actual library code. The real name adds to the soname a period, a minor number, another period, and the release number. The last period and release number are optional. The minor number and release number support configuration control by letting you know exactly what version(s) of the library are installed. Note that these numbers might not be the same as the numbers used to describe the library in documentation, although that does make things easier.

[Understanding Linux readelf "program interpreter"](https://stackoverflow.com/questions/72933760/understanding-linux-readelf-program-interpreter-how-is-this-set-at-compile-t). [overwrite default /lib64/ld-linux-x86-64.so.2 to call executables](https://superuser.com/questions/1144758/overwrite-default-lib64-ld-linux-x86-64-so-2-to-call-executables) 

[glibc backward compat](https://www.linuxquestions.org/questions/linux-general-1/glibc-backward-compatibility-4175445005/)

[How programs get run: ELF binaries](https://lwn.net/Articles/631631/). [Debug with gdb an application running with different libc (ld-linux.so)](https://stackoverflow.com/questions/66376921/debug-with-gdb-an-application-running-with-different-libc-ld-linux-so). [How to deal with `/lib64/ld-linux-x86-64.so.2` missing on NixOS?](https://discourse.nixos.org/t/how-to-deal-with-lib64-ld-linux-x86-64-so-2-missing-on-nixos/11401). [overwrite default /lib64/ld-linux-x86-64.so.2 to call executables](https://superuser.com/questions/1144758/overwrite-default-lib64-ld-linux-x86-64-so-2-to-call-executables)

[linear address spaces](https://news.ycombinator.com/item?id=46442282)

[Linux 7.0 Aims To Replace More Caching Code With Sheaves For "Hopefully" Improved Performance](https://www.phoronix.com/news/Linux-7.0-Replace-Slabs-Sheaves)





