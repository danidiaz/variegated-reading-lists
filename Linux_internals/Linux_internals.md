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


