# Papers

[Time clock and the ordering of events in a distributed system](http://amturing.acm.org/p558-lamport.pdf)

[Consensus on Transaction Commit](https://www.microsoft.com/en-us/research/publication/consensus-on-transaction-commit)

[An empirical study on the correctness of formally verified distributed systems](https://blog.acolyer.org/2017/05/29/an-empirical-study-on-the-correctness-of-formally-verified-distributed-systems/)

[Byzantizing Paxos by Refinement](https://lamport.azurewebsites.net/tla/byzsimple.pdf)

[Fast Byzantine Paxos](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=2394240BBB05A87245817B8BE819DFC0?doi=10.1.1.212.9626&rep=rep1&type=pdf)

[Impossibility of Distributed Consensus with One Faulty Process](http://www.podc.org/influential/2001-influential-paper/)

>  an asynchronous consensus algorithm cannot be guaranteed to be both safe and live. This is called the FLP Impossibility Result

[Blockchains from a Distributed Computing Perspective](http://cs.brown.edu/courses/csci2952-a/papers/perspective.pdf) [ht](https://news.ycombinator.com/item?id=16191506)

[Seeing is Believing: A Client-Centric Specification of Database Isolation](http://www.cs.utexas.edu/~ncrooks/2017-podc-seeing-tr.pdf)

[CASPaxos: Replicated State Machines without logs](https://arxiv.org/pdf/1802.07000.pdf)

[On Designing and Deploying Internet-Scale Services](https://www.usenix.org/legacy/event/lisa07/tech/full_papers/hamilton/hamilton.pdf)

[link collection](https://github.com/rShetty/awesome-distributed-systems)

[Composition: A Way to Make Proofs Harder](https://www.microsoft.com/en-us/research/publication/composition-way-make-proofs-harder/) [mentioned here](http://semantic-domain.blogspot.com.es/2018/04/are-functional-programs-easier-to.html)

[Paxos Made Live - An Engineering Perspective](https://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/papers/paper2-1.pdf). [Red Hat contributes etcd, the cornerstone of Kubernetes, to the Cloud Native Computing Foundation](https://www.redhat.com/en/blog/red-hat-contributes-etcd-cornerstone-kubernetes-cloud-native-computing-foundation). [HN](https://news.ycombinator.com/item?id=18683602).

[Building Consistent Transactions with Inconsistent Replication](https://web.eecs.umich.edu/~manosk/assets/papers/tapir.pdf).

[A generalised solution to distributed consensus](https://blog.acolyer.org/2019/03/08/a-generalised-solution-to-distributed-consensus/). [HN](https://news.ycombinator.com/item?id=19343398)

[Atul Adya’s PhD thesis](http://pmg.csail.mit.edu/papers/adya-phd.pdf). [Natacha Crooks](http://www.cs.cornell.edu/lorenzo/papers/Crooks17Seeing.pdf).

> Atul Adya’s PhD thesis gives a precise definition of the SQL standard isolation levels based on how reads and writes from different transactions may be interleaved. However these definitions are given from the point of view of the system. The recent work by Natacha Crooks et. al gives elegant and precise definitions from the point of view of the user.

[Interactive checks for coordination avoidance](https://blog.acolyer.org/2019/08/28/interactive-checks-for-coordination-avoidance/)

[scaling replicated state machines](https://twitter.com/heidiann360/status/1347961797882621953)

[why caches may be bad in distributed systems](https://twitter.com/MarcJBrooker/status/1431292083046862856). [hn](https://news.ycombinator.com/item?id=28344561).

>  real systems have metastable states, which surprises people. "Metastable" means that the system runs fine for a while, then something bad happens, the system goes into a bad state, and stays in the bad state after the bad stimulus is removed. Historically one of the first examples is the infamous Internet congestion collapse of 1986, which prompted the implementation of TCP congestion control.

# Posts

[Strong consistency models](https://aphyr.com/posts/313-strong-consistency-models)

> Because serializability allows arbitrary reordering of operations (so long as the order appears atomic), it is not particularly useful in real applications. Most databases which claim to provide serializability actually provide strong serializability, which has the same time bounds as linearizability. To complicate matters further, what most SQL databases term the SERIALIZABLE consistency level actually means something weaker, like repeatable read, cursor stability, or snapshot isolation.

> Consistency means linearizability, and in particular, a linearizable register.

[Serializability, linearizability, and locality](https://aphyr.com/posts/333-serializability-linearizability-and-locality)

[Difference between Linearizability and Serializability](http://stackoverflow.com/questions/4179587/difference-between-linearizability-and-serializability)

[Linearizability and Serializability in context of Software Transactional Memory](https://cs.stackexchange.com/questions/41698/linearizability-and-serializability-in-context-of-software-transactional-memory)

[Linearizability versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/)

> Serializability is the traditional “I,” or isolation, in ACID. If users’ transactions each preserve application correctness (“C,” or consistency, in ACID), a serializable execution also preserves correctness. Therefore, serializability is a mechanism for guaranteeing database correctness.1

> Granted, serializability is (more or less) the most general means of maintaining database correctness. In what’s becoming one of my favorite “underground” (i.e., relatively poorly-cited) references, H.T. Kung and Christos Papadimitriou dropped a paper in SIGMOD 1979 on “An Optimality Theory of Concurrency Control for Databases.” In it, they essentially show that, if all you have are transactions’ syntactic modifications to database state (e.g., read and write) and no information about application logic, serializability is, in some sense, “optimal”: in effect, a schedule that is not serializable might modify the database state in a way that produces inconsistency for some (arbitrary) notion of correctness that is not known to the database.

> Combining serializability and linearizability yields strict serializability: transaction behavior is equivalent to some serial execution, and the serial order corresponds to real time. For example, say I begin and commit transaction T1, which writes to item x, and you later begin and commit transaction T2, which reads from x. A database providing strict serializability for these transactions will place T1 before T2 in the serial ordering, and T2 will read T1’s write. A database providing serializability (but not strict serializability) could order T2 before T1.2

> As Herlihy and Wing note, “linearizability can be viewed as a special case of strict serializability where transactions are restricted to consist of a single operation applied to a single object.”

[Linearizability, serializability, transaction isolation and consistency models](https://dddpaul.github.io/blog/2016/03/17/linearizability-and-serializability/)

[Linearizability](https://en.wikipedia.org/wiki/Linearizability)

[Serializability](https://en.wikipedia.org/wiki/Serializability)

[Linearizability](http://muratbuffalo.blogspot.com/2021/10/linearizability.html). [tweet](https://twitter.com/muratdemirbas/status/1445935260018126850?t=ABFs3XCPYJkNbwc2I5KUhA&s=03).

[Please stop calling databases CP or AP](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html)

> Moreover, databases with snapshot isolation/MVCC are intentionally non-linearizable, because enforcing linearizability would reduce the level of concurrency that the database can offer. For example, **PostgreSQL’s SSI provides serializability but not linearizability**, and Oracle provides neither. Just because a database is branded “ACID” doesn’t mean it meets the CAP theorem’s definition of consistency. *Is this quote really correct?*

[Seriablizable but not linearizable](https://gist.github.com/pbailis/8279494)

[Distributed transactions](https://www.cs.rutgers.edu/~pxk/417/notes/content/transactions.html)

[How does two phase commit recover from a participant's failure?](https://www.quora.com/How-does-two-phase-commit-recover-from-a-participants-failure)

[How ACID is the two-phase commit protocol?](http://stackoverflow.com/questions/4639740/how-acid-is-the-two-phase-commit-protocol)

[Jepsen](https://aphyr.com/tags/jepsen)

[Notes on distributed systems for youngbloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) [some additional commentary](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/)

[Testing Distributed Systems for Linearizability](http://www.anishathalye.com/2017/06/04/testing-distributed-systems-for-linearizability/)

[Scalability Cheatsheet: The Road to Paxos](https://dzone.com/articles/scalability-cheatsheet-the-road-to-paxos)

[The Limits of the CAP Theorem](https://www.cockroachlabs.com/blog/limits-of-the-cap-theorem/) [HN](https://news.ycombinator.com/item?id=14646063)

> The only time that a CAP-Available system would be available when a CAP-Consistent one would not is when one of the datacenters can’t talk to the other replicas, but can talk to clients, and the load balancer keeps sending it traffic. 

> the 'A' in CAP is boring. It does not mean what you think it means. Lynch et al. probably chose the definition because it's one for which the 'theorem' is both true and easy to prove. This is not the impossibility result with which designers of distributed systems should be most concerned.

[The CAP Theorem - Foundation DB](http://www.odbms.org/wp-content/uploads/2013/11/cap-theorem.pdf)

[Clarifications On The CAP Theorem And Data-Related Errors](https://www.voltdb.com/blog/2010/10/21/clarifications-cap-theorem-data-related-errors/)

[Heisenbugs and Bohrbugs](https://www.cs.rutgers.edu/~rmartin/teaching/spring03/cs553/papers01/06.pdf)

[paxos vs. 2PC](https://stackoverflow.com/questions/27304887/paxos-vs-two-phase-commit)

> Paxos actually solves a *more genreal* problem than 3PC.

[Consensus on Transaction Commit](https://blog.acolyer.org/2016/01/13/consensus-on-transaction-commit/)

[Delivering Billions of Messages Exactly Once](https://segment.com/blog/exactly-once-delivery/) [HN](https://news.ycombinator.com/item?id=14664405)

> I don't want to ever see the phrase "Exactly Once" without several asterisks behind it. It might be exactly once from an "overall" point of view, but the client effectively needs infinitely durable infinite memory to perform the "distributed transaction" of acting on the message and responding to the server.

[how do you cut a monolith in half?](http://programmingisterrible.com/post/162346490883/how-do-you-cut-a-monolith-in-half) [HN](https://news.ycombinator.com/item?id=14668526)

[Exactly-once Semantics are Possible: Here’s How Kafka Does it](https://news.ycombinator.com/item?id=14670801) [reddit](https://pay.reddit.com/r/programming/comments/6kh65f/exactlyonce_semantics_is_possible_heres_how/) [nope](http://bravenewgeek.com/you-cannot-have-exactly-once-delivery-redux/)

> Providing API for building applications that have transactions and help with idempotent producing is really exciting. This will help lower a lot of pains associated with building stream processing systems. Doing it with very little performance overhead is amazing.

> Indeed. Idempotent operations is the mainstay of managing "at least once" message delivery. If you had a true "exactly once" system, idempotency would be unnecessary.

[Manage Kubernetes Clusters on AWS Using Kops](https://news.ycombinator.com/item?id=14715425)

[Docker & AWS](https://news.ycombinator.com/item?id=14853649)

> The problem with renting boxes is the hidden costs if you want to do it right. First of all, if you have anything mission critical, you need to run it in a high availability config, this is easy for stateless microservices, but when it comes to running your DB, you start renting three boxes instead of one or two and configuring them accordingly. And then you setup your Backup Infrastructure for disaster recovery, Glacier needs a replacement after all. No problem, just more disks(?) on a few more boxes(?) and bacula(?), better in a different Datacenter just to be on the safe side, it would be nasty if you whole rack gets fried and your data with it. Don't forget to backup your configuration, all of it. Loadbalancers, Server Environment Variables, Network (do you have an internal DNS?), Crontabs, some businesses need their audit logs stored etc...  On the infrastructure level there is lots and lots of stuff you can do and you won't ever really need AWS, you'll just spend significantly more time finding and administering the right solutions than just using the AWS Solutions where you'll find a treasure trove of great tutorials and can relatively cheaply pay for support.  If you then pay someone on top for 24/7 management/monitoring of your dedicated stack so that your team doesn't have to get up at 3 am because one of your VMs disk fills because some stray logfile is filling the disc, many of the savings you had by setting it up on a dedicated server go out of the window because the management partner needs to train their people to look into your infrastructure. AWS only Management Partners are just light-years cheaper because they can streamline their processes much better.  You could also hire your own team of admins...  Sure AWS is a beast with its own surprises, but overall the cost/benefit ratio is still very fair even if you factor in all the "surprises"(many of which your management partner will probably know about). Having layered support is really something beneficial aswell.  If something is wonky with RDS, you get to call your management partner if he didn't detect it before you, who if he can't tackle it himself can call AWS technicians. This gets you much much further than you would get elsewhere. The outside the world is paying for (for example) perconas consultants or someone similar if the problems grow over their team's head.  Sure, at some point in a companies growth, depending on how technical the operation is, there might be a time where an admin team and colocation/dedicated boxes make sense, where AWS technicians will scratch their heads etc., especially if you have some very very specific tasks you need to do.  But for most people this is far off if ever.

[Serializability, linearizability, and locality](https://aphyr.com/posts/333-serializability-linearizability-and-locality)

> Recall that strict serializability is essentially serializability plus linearizability’s real-time constraint: transactions cannot be arbitrarily re-ordered, but must appear to take place atomically at some time between their invocation and completion. When we add real-time constraints to sequential consistency, we get linearizability: a local property. Why can’t we add real-time constraints to serializability and obtain locality? Why don’t real-time multi-object transactions compose?

> We can view strict serializability as linearizability plus the multi-object transactions of serializability. But in another sense, linearizability is strict serializability with the constraint that transactions are constrained to act on a single object, because that restriction provides locality.

[Visualizing Linearizability](http://mwhittaker.github.io/2015/01/24/linearizability/)

[Linearizability: A Correctness Condition for Concurrent Objects (1990)](https://www.javagists.com/convenience-factory-methods-collections-java-9)

> Sequential consistency is equivalent to linearizability without condition L2. Serializability is analogous to sequential consistency with transactions, and strict serializability is analogous to linearizability with transactions. Sequential consistency, serializability, and strict serializability do not have the same locality and non-blocking properties as linearizability. Moreover, serializability and linearizability are for different domains. Serializability works well for databases because application developers should be able to easily express complex transactions. Linearizability is better for infrastructure in which the developer is willing to spend considerable effort to maximize concurrency.

[Consensus Protocols: Two-Phase Commit](http://the-paper-trail.org/blog/consensus-protocols-two-phase-commit/)

[Consensus Protocols: Three-Phase Commit](http://the-paper-trail.org/blog/consensus-protocols-three-phase-commit/)

[Consensus Protocols: Paxos](http://the-paper-trail.org/blog/consensus-protocols-paxos/)

> 3PC works very well when nodes may crash and come to a halt – leaving the protocol permanently when they encounter a fault. This is called the fail-stop fault model, and certainly describes a number of failures that we see every day. However, especially in networked systems, this isn’t the only way in which nodes crash. They may instead, upon encountering a fault, crash and then recover from the fault, to begin executing happily from the point that they left off (remember that, with stable storage that persists between crashes, there’s no reason that a restarted node couldn’t simply pick up the protocol from where it crashed). This is the fail-recover fault model, which is more general than fail-stop, and therefore a bit more tricky to deal with.

> Similarly, heavy network load can delay the delivery of a message for an arbitrary period. In a synchronous network model, there is a bound on the amount of time a remote host can take to process and respond to a message. In an asynchronous model, no such bound exists. The key problem that asynchronicity causes is that time outs can no longer be reliably used as a proxy for failure detection

> There are other ways that Paxos can go wrong. Acceptors need to keep a record of the highest proposal they have agreed to, and the value of any proposals they have accepted, in stable storage. If that storage should crash then the acceptor cannot take part in the protocol for fear of corrupting the execution (by effectively lying about the proposals it has already seen). This is a kind of Byzantine failure, where an acceptor deviates from the protocol.

> Rather than sacrifice correctness, which some variants (including the one I described) of 3PC do, Paxos sacrifices liveness, i.e. guaranteed termination, when the network is behaving asynchronously and terminates only when synchronicity returns.

[In distributed systems, what is a simple explanation of the Paxos algorithm?](https://www.quora.com/In-distributed-systems-what-is-a-simple-explanation-of-the-Paxos-algorithm)

> 3PC is fail-stop resilient, but not fail-recover resilient. Unfortunately real life requires fail-recover and hence we need a more general solution. This is where Paxos comes in.

> What happens if we mandate only one Leader at a time in Paxos, and also mandate that instead of majority, all nodes must vote? You are right – we get 2PC. 2PC is a specific case of Paxos.

[Byzantine faults, Paxos, and consensus](https://people.cs.umass.edu/~emery/classes/cmpsci691st/scribe/lecture17-byz.pdf)

> Paxos is in a sense sort of like RSA. RSA is expensive, so you use it as a wrapper to a cheaper protocol.
With Paxos you elect a leader to be in charge of a large-scale event. The coordinator is a single point of
failure, so you can use paxos to come up with a new coordinator. Most of the time you don’t run paxos, you
only run it when something bad happens to prevent any one thing to be a single point of failure.

[Version vector](https://en.wikipedia.org/wiki/Version_vector)

[Why is memory reclamation so important?](https://concurrencyfreaks.blogspot.com.es/2017/08/why-is-memory-reclamation-so-important.html) [HN](https://news.ycombinator.com/item?id=15269628)

[You Can’t Sacrifice Partition Tolerance](https://codahale.com/you-cant-sacrifice-partition-tolerance/)

[Fear and Loathing in lock-free programming](https://lobste.rs/s/3nutqy/fear_loathing_lock_free_programming)

[Google's Cloud Spanner: how does it stack up?](http://www.zdnet.com/article/google-spanner-and-how-it-compares-to-microsofts-cosmos-db/)

> Spanner was originally built by Google to handle workloads like AdWords and Google Play, that were, according to Google, previously running on massive, manually sharded MySQL implementations

[3PC. 2PC, Paxos](https://twitter.com/DiazCarrete/status/880181927420067841) [SO question](https://stackoverflow.com/questions/27304887/paxos-vs-two-phase-commit)

> So Paxos is a better, more general version of 2PC, and unlike 3PC, is has been proved correct?

[A Comparison of Advanced, Modern Cloud Databases](https://brandur.org/cloud-databases)

> Concurrent ACID: Whether the database supports ACID (atomicity, consistency, isolation, and durability) guarantees across multiple operations. ACID is a powerful tool for system correctness, and until recently has been a long sought but illusive chimera for distributed databases. I use the term “concurrent ACID” because technically Cosmos guarantees ACID, but only within the confines of a single operation.

> modern techniques can achieve CP while still keeping availability that’s incredibly good. Like five or more 9s of good. This result is so optimal that modern databases seem to be converging on it. Every database on the list above is CP with varying levels of A

> Time-based consistency. Sophisticated distributed systems like Spanner and CockroachDB tend to need a little more time to coordinate and verify the accuracy of the results that will be returned from any given node, and this makes them less suitable for low latency operations.

[Spanner, TrueTime and the CAP Theorem](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45855.pdf) [HN](https://news.ycombinator.com/item?id=15923507)

[Why you should pick strong consistency, whenever possible](https://cloudplatform.googleblog.com/2018/01/why-you-should-pick-strong-consistency-whenever-possible.html)

[Paxos derived](http://muratbuffalo.blogspot.com.es/2018/01/paxos-derived.html)

[distributed systems reading list](https://github.com/palvaro/CMPS232-Fall16/blob/master/readings.md)

[A History of Transaction Histories](https://ristret.com/s/f643zk/history_transaction_histories)

[Data Laced with History: Causal Trees & Operational CRDTs](http://archagon.net/blog/2018/03/24/data-laced-with-history/)

[another collection of links](https://github.com/rShetty/awesome-distributed-systems)

[Standing on Distributed Shoulders of Giants](https://queue.acm.org/detail.cfm?id=2953944)

[Tweets about distributed transactions](https://twitter.com/cmeik/status/986192004928417792)

[The Four Most Expensive Words in the English Language](https://blog.dshr.org/2018/06/the-four-most-expensive-words-in.html) [Proofs of Space](https://blog.dshr.org/2018/03/proofs-of-space.html)

[tweet about consensus](https://twitter.com/eikke/status/1009566187116793856)

[The Horrors of Upgrading Etcd Beneath Kubernetes](https://gravitational.com/blog/kubernetes-and-offline-etcd-upgrades?) [HN](https://news.ycombinator.com/item?id=17472761)

[Complex Event Flows in Distributed Systems](https://www.infoq.com/news/2018/07/complex-event-flows)

[An Illustrated Proof of the CAP Theorem](https://mwhittaker.github.io/blog/an_illustrated_proof_of_the_cap_theorem/) [hn](https://news.ycombinator.com/item?id=17528817)

[Two Generals and Time Machines](https://mwhittaker.github.io/blog/two_generals_and_time_machines/)

[Augmenting Agile with Formal Methods](https://lobste.rs/s/0j5s4m/augmenting_agile_with_formal_methods)

[1 like = 1 distributed systems paper](https://twitter.com/ifesdjeen/status/1024775959961128961)

[The many faces of consistency](http://muratbuffalo.blogspot.com/2018/08/the-many-faces-of-consistency.html?m=1)

[Diagnosing A Weak Memory Ordering Bug](https://robert.ocallahan.org/2018/08/for-first-time-in-my-life-i-tracked.html)

[Mind Your State for Your State of Mind](https://queue.acm.org/detail.cfm?id=3236388) [at another blog](http://muratbuffalo.blogspot.com/2018/08/mind-your-state-for-your-state-of-mind.html)

[Distributed Agreement on Random Order](https://deque.blog/2018/09/13/distributed-agreement-on-random-order-fun-with-lamport-timestamps/)

[Exploring Stretch Clusters for Red Hat OpenShift Dedicated](https://blog.openshift.com/exploring-stretch-clusters-for-red-hat-openshift-dedicated/)

> New Multi-AZ clusters can be deployed to AWS Regions that have at least three AZs. This allows for the control plane to be distributed with one node in each AZ (one master and one infra node in each AZ). In the event of an AZ outage, etcd quorum is not lost and the cluster can continue to operate normally.

[Partitioned consensus and its impact on Spanner’s latency](https://dbmsmusings.blogspot.com/2018/12/partitioned-consensus-and-its-impact-on.html). [HN](https://news.ycombinator.com/item?id=18682159).

[An Evaluation of the Advantages and Disadvantages of Deterministic Database Systems](http://www.vldb.org/pvldb/vol7/p821-ren.pdf).

[TLA is hard to learn](https://lorinhochstein.wordpress.com/2018/12/24/tla-is-hard-to-learn/)

[Introduction to TLA+ Model Checking in the Command Line](https://medium.com/@bellmar/introduction-to-tla-model-checking-in-the-command-line-c6871700a6a2). [HN](https://news.ycombinator.com/item?id=18937214).

[Time to Move on from Two Phase Commit](http://dbmsmusings.blogspot.com/2019/01/its-time-to-move-on-from-two-phase.html). [HN](https://news.ycombinator.com/item?id=18999520).

[Reliable Microservices Data Exchange With the Outbox Pattern](https://debezium.io/blog/2019/02/19/reliable-microservices-data-exchange-with-the-outbox-pattern/).

[session types](http://cs242.stanford.edu/f18/lectures/07-2-session-types.html) [hn](https://news.ycombinator.com/item?id=19296206)

[A Critical Look at Event-Driven Systems](https://www.infoq.com/news/2019/03/event-driven-systems)

[history of protocols distributed systems](https://www.infoq.com/presentations/history-protocols-distributed-systems)

[Toward Domain-Specific Solvers for Distributed Consistency](http://composition.al/blog/2019/03/31/toward-domain-specific-solvers-for-distributed-consistency-will-appear-at-snapl-2019/)

[Demystifying Database Systems: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels). [more on isolation levels](http://www.dbazine.com/db2/db2-disarticles/gulutzan6/). [Read committed Snapshot VS Snapshot Isolation Level](https://stackoverflow.com/questions/2741016/read-committed-snapshot-vs-snapshot-isolation-level). [follow up](https://dba.stackexchange.com/questions/205425/sql-difference-optimistic-reading-and-optimistic-writing). 

[What Write Skew Looks Like](https://www.cockroachlabs.com/blog/what-write-skew-looks-like/)

[Real Transactions are Serializable](https://www.cockroachlabs.com/blog/acid-rain/)

[Lamport about Practical TLA+](https://lamport.azurewebsites.net/tla/practical-tla.html?back-link=learning.html) [hn](https://lobste.rs/s/rvnotp/book_review_practical_tla)

[Building Robust Systems With ACID and Constraints](https://brandur.org/acid).

[A way to do atomic writes](https://news.ycombinator.com/item?id=20040779)

[Using Randomized Communication for Robust, Scalable Systems](https://www.infoq.com/presentations/randomized-communication-hashicorp-consul/)

[Panel: The Promises and Perils of Eschewing Distributed Coordination](https://www.infoq.com/presentations/panel-perils-distributed-coordination/)

[An explanation of the difference between Isolation levels vs. Consistency levels](https://dbmsmusings.blogspot.com/2019/08/an-explanation-of-difference-between.html) [HN](https://news.ycombinator.com/item?id=20779977)

[Distributed consensus reading list](https://github.com/heidi-ann/distributed-consensus-reading-list) great resource!

[partitions and stuff](https://twitter.com/HenryR/status/1202651199100469248)

[Gray Failure: The Achilles Heel of Cloud-Scale Systems](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/06/paper-1.pdf)

[Pulsar vs. Kafka](https://medium.com/@yuvarajl/why-nutanix-beam-went-ahead-with-apache-pulsar-instead-of-apache-kafka-1415f592dbbb). [blog](https://jack-vanlightly.com/). [blog](https://streaml.io/blog)

[Gandalf: An Intelligent, End-To-End Analytics Service for Safe Deployment in Cloud-Scale Infrastructure](https://twitter.com/copyconstruct/status/1225335185270423553)

[Atomic Replication Changes in etcd/Raft](https://dzone.com/articles/atomic-replication-changes-in-etcdraft)

[what papers to read](http://muratbuffalo.blogspot.com/2021/02/read-papers-not-too-much-mostly.html)

[Foundational distributed systems papers](https://twitter.com/muratdemirbas/status/1365730689535119360)

[a primer on memory consistency and cache coherence](https://news.ycombinator.com/item?id=26790827)

[PACELC theorem](https://en.wikipedia.org/wiki/PACELC_theorem)

[Patterns of Distributed Systems](https://martinfowler.com/articles/patterns-of-distributed-systems/)

[Distributed consensus made simple (for real this time!)](https://twitter.com/heidiann360/status/1443491633752850434)

[Consistency levels in Azure Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels)

- Strong
- Bounded staleness
- Session
- Consistent prefix
- Eventual

[the new temporal logic features in Alloy 6](https://twitter.com/trupill/status/1460620765473263617)

[Paxos made abstract](https://maheshba.bitbucket.io/blog/2021/11/15/Paxos.html). [tweet](https://twitter.com/maheshb/status/1460292887199977478?t=ap8_maEVG9pQmLfwXWmsHw&s=03)

[on the bug/ambiguity in Paxos Made Simple](https://brooker.co.za/blog/2021/11/16/paxos.html). [tweet](https://twitter.com/MarcJBrooker/status/1460665713836761098?t=nLR1miXkUwCn9PcGaT5MEg&s=03).

[the deadlock empire](https://news.ycombinator.com/item?id=29431308)

[Guaranteeing Consensus in Distributed Systems with CRDTs [PWL NYC]](https://twitter.com/papers_we_love/status/1468524523666526216)

[swarm consensus](https://news.ycombinator.com/item?id=29711381)

> This algorithm requires a lot of messages.

[retries are bad](https://twitter.com/MarcJBrooker/status/1489651911640825858)

[Testing Distributed Systems](https://news.ycombinator.com/item?id=30296770)

[common goroutine leaks](https://twitter.com/GolangTrends/status/1497548500220981252). [waiting groups in Golang](https://twitter.com/GolangTrends/status/1497367306502123527).

[Structured (Synchronous) Concurrency](https://fsantanna.github.io/structured-concurrency.html)

[Debugging Race Conditions in Production](https://lightrun.com/tutorials/debug-race-condition-production/)

[The Tower of Weakenings: Memory Models For Everyone](https://gankra.github.io/blah/tower-of-weakenings/). [rust](https://twitter.com/jonmsterling/status/1509485751909629969?t=VvmBvChOCzK5pdUkrW15yA&s=03)

[Distributed transaction patterns for microservices compared](https://twitter.com/gunnarmorling/status/1514163151905898500). [the dual write problem](https://developers.redhat.com/articles/2021/09/21/distributed-transaction-patterns-microservices-compared).

> The single indicator that you may have a dual write problem is the need to write to more than one system of record predictably. 

# Slides

[Distributed systems course](https://roxanageambasu.github.io/ds-class//assets/lectures/lecture17.pdf)

[Distributed Systems, Failures, and Consensus](https://www.cs.duke.edu/courses/fall07/cps212/consensus.pdf)

[another one](http://linux.macrofinances.com/index.php/coms-4995-distributed-systems/)

[CIS 505: Software Systems Lecture Note on Consensus](http://www.cis.upenn.edu/~lee/07cis505/Lec/lec-ch8a-consensus-v7.pdf)

[map of consistency models](https://jepsen.io/consistency) [tweet](https://twitter.com/jepsen_io/status/1013585943318626305)

[How to scale a distributed system](https://cdn.oreillystatic.com/en/assets/1/event/244/How%20to%20scale%20a%20distributed%20system%20Presentation.pdf)

> Symmetry breaking (with leader election as an example) 

> Small control plane, big data plane

- [Health Checks and Graceful Degradation in Distributed Systems](https://medium.com/@copyconstruct/health-checks-in-distributed-systems-aa8a0e8c1672) [Envoy Service Mesh Case Study: Mitigating Cascading Failure at Lyft](https://www.infoq.com/articles/envoy-service-mesh-cascading-failure)

> Rate limiting and circuit breaking based on static thresholds and limits can prove to be error-prone and brittle from both correctness and scalability standpoints.

[NewSQL databases fail to guarantee consistency and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html). [HN](https://news.ycombinator.com/item?id=18039489).

[Consensus Systems with Ethan Buchman](https://softwareengineeringdaily.com/2018/03/26/consensus-systems-with-ethan-buchman/)

[Help! I Accidentally Distributed My System!](https://www.infoq.com/presentations/distributed-systems-debug-manage).

[Why Logical Clocks are Easy](https://queue.acm.org/detail.cfm?id=2917756).

[Using TLA+ to Understand Xen Vchan](http://roscidus.com/blog/blog/2019/01/01/using-tla-plus-to-understand-xen-vchan/)

[Modern dining philosophers](http://lucteo.ro/2018/12/28/modern-dining-philosophers/)

[mapConcurrently-alike with concurrency limit, and ordered job start](https://github.com/simonmar/async/issues/83).

[go concurrency bugs](https://news.ycombinator.com/item?id=19280927)

[TLA+ material](https://twitter.com/owickstrom/status/1122140895564959744)

[transaction systems slides](http://dbis.cs.tu-dortmund.de/cms/de/lehre/ws1415/arch-dbms/slides/transaction-management.pdf)

# Courses

[Principles of Distributed Computing (lecture collection)](http://disco.ethz.ch/lectures/podc_allstars/)

[Another course](http://www0.cs.ucl.ac.uk/staff/B.Karp/gz03/f2014/lectures/)

[Distributed Systems W4995-1 Fall 2014 Roxana Geambasu](https://roxanageambasu.github.io/ds-class//schedule.html) [lecture 17](https://roxanageambasu.github.io/ds-class//assets/lectures/lecture17.pdf)

> 3PC trades safety for liveness, 2PC trades liveness for safety. Paxos is "largely live" and blocks only on exceptional circunstances 

[Notes on Theory of Distributed Systems CPSC 465/565: Fall 2017](http://cs-www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf)

[Languages and Abstractions for Distributed Programming CMPS290S, Fall 2018](http://composition.al/CMPS290S-2018-09/2018/11/11/welcome-to-the-languages-and-abstractions-for-distributed-programming-blog.html).

[distsys class](https://github.com/aphyr/distsys-class)

[Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation)

[ceph evolution](https://blog.acolyer.org/2019/11/06/ceph-evolution/)

[formal foundations of serverless computing](https://blog.acolyer.org/2019/11/18/formal-foundations-of-serverless-computing/)

[the huge costs of coordination in our systems](https://twitter.com/PatHelland/status/1365722790888804355)

[CSE138, Spring 2021](https://twitter.com/lindsey/status/1402763622745477121)

# Books

[Replication theory and practice](https://www.goodreads.com/book/show/8296096-replication)

- [Consistency Models for Replicated Data](http://disi.unitn.it/~montreso/ds/papers/replication.pdf)

- [Replication techniques for availability](https://pdfs.semanticscholar.org/d5b6/87ed91cf1043cbbf1442959283e354f7e966.pdf)

- [Modular Approach to Replication for Availability](https://www.researchgate.net/publication/221029795_Modular_Approach_to_Replication_for_Availability)

- [Stumbling over Consensus Research: Misunderstandings and Issues](https://www.semanticscholar.org/paper/Stumbling-over-Consensus-Research-Misunderstanding-Aguilera/bcbf8095e24ab1574da8691f6aed1b461dcd0da6)

- [Replicating for Performance: Case Studies](http://www.globule.org/publi/RPCS_lncs2010.pdf)

- [A History of the Virtual Synchrony Replication Model](https://www.cs.cornell.edu/ken/history.pdf)

- [From Viewstamped Replication to Byzantine Fault Tolerance](http://www.pmg.csail.mit.edu/papers/vr-to-bft.pdf)

- [Implementing Trustworthy Services Using Replicated State Machines](https://www.cs.cornell.edu/fbs/publications/TrustSurvey.pdf)

- [State Machine Replication with Byzantine Faults](https://www.zurich.ibm.com/~cca/papers/byzrepl.pdf)

- [Selected Results from the Latest Decade of Quorum Systems Research](https://kelehers.me/others/replicationTheoryPractice.pdf)

- [From Object Replication to Database Replication](http://compsciclub.ru/media/slides/replication_2010_spring/2010_05_22_replication_2010_spring.pdf)

- [Database Replication: A Tutoria](https://pdfs.semanticscholar.org/c15c/1921f07cd6647d3db24babcbaff451674e16.pdf)

- [Practical Database Replication](https://repositorium.sdum.uminho.pt/bitstream/1822/12268/1/Tese.pdf)

- [An introduction to distributed systems](https://github.com/aphyr/distsys-class/blob/master/README.markdown)

- [when I started designing languages](https://news.ycombinator.com/item?id=19428433)

- [Emily Short - Five Strategies For Collaborating With A Machine [PROCJAM 2016]](https://twitter.com/MatthewGuz/status/1112392893501722624)

- [Distributed systems theory for the distributed systems engineer](https://www.the-paper-trail.org/post/2014-08-09-distributed-systems-theory-for-the-distributed-systems-engineer/)

- [An Overview of Distributed Systems and the Consensus Problem](https://probablyexactlywrong.com/distsys)

- [queues are bad](https://twitter.com/rbranson/status/1131989746643742721)

- [learning to build distributed systems](https://news.ycombinator.com/item?id=20249946)

- [composition in distributed systems](https://blog.sigplan.org/2019/12/23/composition-in-distributed-systems/)

# Videos

[Our concurrent past, our distributed future](https://aphyr.com/posts/313-strong-consistency-models)

[Distributed Systems vs Compositionality—Roland Kuhn](https://www.youtube.com/watch?v=LcUIIRqXwTY)

[Consistency without consensus in production systems](https://www.youtube.com/watch?v=em9zLzM8O7c) [https://www.youtube.com/watch?v=lsKaNDj4TrE](https://www.youtube.com/watch?v=lsKaNDj4TrE) [Martin Kleppmann - Conflict Resolution for Eventual Consistency](https://www.youtube.com/watch?v=8_DfwEpHE88) [GOTO 2015 • Coordination-Free Computations](https://www.youtube.com/watch?v=AF8fpDzfUOc) [GOTO 2014 • How the Bitcoin Protocol Actually Works](https://www.youtube.com/watch?v=GiU4b7ldKMs)

[Distributed Systems Theory for Practical Engineers](https://www.infoq.com/presentations/distributed-systems-theory)

[Applied Distributed Research in Apache Cassandra](https://www.infoq.com/presentations/distributed-research-cassandra)

[Four Distributed Systems Architectural Patterns by Tim Berglund](https://www.youtube.com/watch?v=tpspO9K28PM)

[What Came First: The Ordering of Events in Systems](https://www.infoq.com/presentations/events-riak-go)

[Four Distributed Systems Architectural Patterns by Tim Berglund](https://www.youtube.com/watch?v=tpspO9K28PM)

> [17:00] If you are a service, like Slack, which is composed of a series of organizations which are not as big... 

[Distributed Systems in One Lesson by Tim Berglund](https://www.youtube.com/watch?v=Y6Ev8GIlbxc)

[Think Twice before Dropping ACID](https://www.infoq.com/presentations/acid-cap)

[The Practice and Theory of TLA+](https://www.youtube.com/watch?v=15uy9Ga-14I) [more](https://www.youtube.com/watch?v=p54W-XOIEF8) [more](https://www.youtube.com/watch?v=-4Yp3j_jk8Q)

[Consensus: Why Can't We All Just Agree?](https://www.infoq.com/presentations/future-distributed-consensus)

[The Future of Distributed Databases Is Relational](https://www.infoq.com/presentations/future-distributed-database-relational)

[Streaming SQL to Unify Batch & Stream Processing w/ Apache Flink](https://www.infoq.com/presentations/sql-streaming-apache-flink)

[Cluster Consensus: When Aeron Met Raft](https://www.infoq.com/presentations/aeron-raft-consensus)

[CRDTs and Distributed Consensus](https://www.dataengineeringpodcast.com/crdts-with-christopher-meiklejohn-episode-14/)

[How to Build Observable Distributed Systems](https://www.infoq.com/presentations/observable-distributed-ststems)

[Jepsen 7: Anna Concurrenina by Kyle Kingsbury](https://www.youtube.com/watch?v=eSaFVX4izsQ)

[JavaZone talk: Transactions and Concurrency Control Patterns](https://www.reddit.com/r/programming/comments/9ghkmx/javazone_talk_transactions_and_concurrency/)

[cool linearizability diagram](https://twitter.com/Dev14e/status/1050795733819875328)

[Help! I Accidentally Distributed My System!](https://www.infoq.com/presentations/distributed-systems-debug-manage).

[A Raft implementation in Haskell](https://news.ycombinator.com/item?id=18475736).

[Everything about distributed systems is terrible | Code Mesh LDN 18](https://www.youtube.com/watch?v=tfnldxWlOhM).

[Apache Zookeeper As A Building Block For Distributed Systems](https://www.dataengineeringpodcast.com/apache-zookeeper-with-patrick-hunt-episode-59/).

[Think local](https://vimeo.com/304106598).

[VIDEO: Consensus algorithms, Paxos and Raft](https://www.youtube.com/watch?v=fcFqFfsAlSQ).

[Apache Zookeeper As A Building Block For Distributed Systems with Patrick Hunt - Episode 59](https://www.dataengineeringpodcast.com/apache-zookeeper-with-patrick-hunt-episode-59/).

[High reliability infrastructure migrations](https://www.youtube.com/watch?v=obB2IvCv-K0)

[Time, Clocks and Ordering of Events in a Dist. System by Dan Rubenstein [PWL NYC]](https://www.youtube.com/watch?v=hK6m6WBk-d8)

[Decoding Distributed Systems](https://www.infoq.com/presentations/distributed-systems-components-designs)

[Building A "Simple" Distributed System - Formal Verification](https://jack-vanlightly.com/blog/2019/1/27/building-a-simple-distributed-system-formal-verification).

[What happens if the server dies after db commit but before saving event to kafka?](https://github.com/kbastani/event-sourcing-microservices-example/issues/28).

[Paxos tweet](https://twitter.com/cmeik/status/1093652495136636933).

[Serializability vs “Strict” Serializability: The Dirty Secret of Database Isolation Levels](https://fauna.com/blog/serializability-vs-strict-serializability-the-dirty-secret-of-database-isolation-levels).  [HN](https://news.ycombinator.com/item?id=19219722).

[Impossibility of Distributed Consensus with One Faulty Process](https://twitter.com/paperswelovenyc/status/1102898822890614784).

[towards language support for distributed systems](https://www.infoq.com/presentations/research-languages-crdt-serverless-functions).

[Designing Distributed Systems with TLA+](https://www.infoq.com/presentations/tla-plus)

[Lecture 14: Optimistic Concurrency Control and Snapshot Isolation](https://www.youtube.com/watch?v=eosTGyXOAM0)

[Patterns for Decoupling in Distributed Systems: Summary Event](http://verraes.net/2019/05/patterns-for-decoupling-distsys-summary-event/)

[Distributed Systems Engineering with Apache Kafka](https://www.buzzsprout.com/186154/1355206-distributed-systems-engineering-with-apache-kafka-ft-jason-gustafson)

[Correctness Anomalies Under Serializable Isolation](http://dbmsmusings.blogspot.com/2019/06/correctness-anomalies-under.html)

[data condition vs. data race](https://news.ycombinator.com/item?id=20495483)

[Transactional Outbox pattern - A piece of the eventual consistency puzzle.](https://www.reddit.com/r/programming/comments/cgsc4k/transactional_outbox_pattern_a_piece_of_the/)

[Those Who Forget the Past Are Doomed to Repeat It](https://www.enterprisedb.com/blog/those-who-forget-past-are-doomed-repeat-it)

[Strange Loop 2019:  "Correctness proofs of distributed systems with Isabelle" by Martin Kleppmann](https://twitter.com/strangeloop_stl/status/1172972515767083014)

[Distributed consensus revised](https://pwlconf.org/2019/heidi-howard/)

> Distributed consensus, the ability to reach agreement in the face of failures and asynchrony, is a fundamental and powerful primitive for constructing reliable distributed systems from unreliable components. For over two decades, the Paxos algorithm has been synonymous with distributed consensus. Paxos is widely deployed in production systems, yet it is poorly understood and it proves to be heavyweight, unscalable and unreliable in practice.

[simulation](https://twitter.com/ryanworl/status/1177273802818031617)

[flexible paxos](https://news.ycombinator.com/item?id=21486002) [tweet](https://twitter.com/heidiann360/status/1192909682735755264)

[mergeable replicated datatypes](https://blog.acolyer.org/2019/11/25/mergeable-replicated-data-types-part-i/)

[Designing Distributed Cache - Part I](https://www.reddit.com/r/programming/comments/e32ofe/designing_distributed_cache_part_i/)

[Correctness proofs of distributed systems with Isabelle](https://www.youtube.com/watch?v=NfdP6wwjsGk)

[Consistency in Non-Transactional Distributed Storage Systems](https://twitter.com/therealdatabass/status/1203384229532450817)

[CS 144: Introduction to Computer Networking, Fall 2019](https://news.ycombinator.com/item?id=21794270)

[My Distributed Systems Seminar's reading list for Spring 2020](https://muratbuffalo.blogspot.com/2019/12/my-distributed-systems-seminars-reading.html)

[failure detectors](https://twitter.com/paperswelovenyc/status/1221478022404091905)

[Best of 2019 in Tech Talks](https://medium.com/@copyconstruct/best-of-2019-in-tech-talks-bac697c3ee13)

[Jepsen: Etcd 3.4.3](https://news.ycombinator.com/item?id=22191717)

[A walkthrough tutorial of TLA+ and its tools: analyzing a blocking queue](https://news.ycombinator.com/item?id=22496287)

[PigPaxos: Devouring the communication bottlenecks in distributed consensus](https://muratbuffalo.blogspot.com/2020/03/pigpaxos-devouring-communication_18.html)

[AVOID REUSABILITY ACROSS PROCESS BOUNDARIES](https://www.ufried.com/blog/reusability_fallacy_3/)

[distributed id generation](https://www.reddit.com/r/programming/comments/fnksrf/scalability_concepts_distributed_id_generation/)

[Friday afternoon distributed systems thread: quorums and latency](https://twitter.com/MarcJBrooker/status/1248721614096568320)

[Paxos vs. Raft](https://news.ycombinator.com/item?id=22994420)

[debugging distributed systems](https://dl.acm.org/doi/pdf/10.1145/2927299.2940294)

[Retries in distributed systems: good and bad parts](https://dev.to/shubheksha/retries-in-distributed-systems-good-and-bad-parts-1ajl)

["A fault-tolerance shim for serverless computing"](https://twitter.com/MarcJBrooker/status/1259905223901863937)

[CRDTs: The Hard Parts [video]](https://news.ycombinator.com/item?id=23802208)

[eventual consistency isn't for streaming](https://news.ycombinator.com/item?id=23832149)

[How to Build a Highly Available System Using Consensus](https://news.ycombinator.com/item?id=24736068)

> One of many timeless works from Butler Lampson. The patterns are still widely in use to this day. The trade offs between lease times and availability are so clearly put, reading this could save a lot of hard earned lessons.

[a review of consensus protocols](https://news.ycombinator.com/item?id=24768971)

[How you could have come up with Paxos yourself](https://news.ycombinator.com/item?id=24906225)

[Helios](https://twitter.com/adriancolyer/status/1320769664893489156)

> Helios is Microsoft's high speed stream ingestion and indexing system, but it's more than just that - it's also a reference architecture for their next-generation big data systems

[Notes on Paxos](https://matklad.github.io//2020/11/01/notes-on-paxos.html)

[Advanced Join Patterns for the Actor Model Based on CEP Techniques](https://news.ycombinator.com/item?id=25014513)

[Structured Concurrency](https://news.ycombinator.com/item?id=25032133)

> That's the easy part and typically not entirely what you want. 

https://vorpus.org/blog/notes-on-structured-concurrency-or-go-statement-considered-harmful/

https://news.ycombinator.com/item?id=25061901

[Fairness in multi-tenant systems](https://aws.amazon.com/builders-library/fairness-in-multi-tenant-systems/)

[Fast Flexible Paxos](https://twitter.com/heidiann360/status/1328367733424197634)

[S3 strong consistency](https://news.ycombinator.com/item?id=25271791)

> I had to work around the issue by storing a high-water mark in the config ID, and then poll an external system to find the expected high water mark before I knew I could safely read and update.

[distributed systems reading list](https://news.ycombinator.com/item?id=25327077)

[a list of distributed transaction protocols](https://twitter.com/MarcJBrooker/status/1348700272860696577)

[scalability comes from avoiding coordination](https://twitter.com/MarcJBrooker/status/1352697289807040512)

[1. No shared memory. 2. No shared clock.](https://news.ycombinator.com/item?id=26089683)

[Anna: A KVS for Any Scale](https://twitter.com/MarcJBrooker/status/1359561487149240323)

[Data laced with history](https://news.ycombinator.com/item?id=26127570)

[too much concurrency & lock trashing](https://twitter.com/reubenbond/status/1363154953657720835)

[Paxos & Raft](https://twitter.com/MarcJBrooker/status/1364626856062820352)

[We found and fixed a rare race condition in our session handling](https://news.ycombinator.com/item?id=26506920)

[how to test a databse - simulation testing](https://twitter.com/asatarin/status/1364428055523913730). [testing distributed systems](https://asatarin.github.io/testing-distributed-systems/)

[	Internal Consistency in Streaming Systems ](https://news.ycombinator.com/item?id=26851803)

[Tail Latency Might Matter More Than You Think](https://brooker.co.za/blog/2021/04/19/latency.html)

[Metastable Failures in Distributed Systems](https://twitter.com/MarcJBrooker/status/1396876735354912773)

[Pipelining in TypedProtocols](https://coot.me/posts/typed-protocol-pipelining.html)

[Lamport Clock](https://martinfowler.com/articles/patterns-of-distributed-systems/lamport-clock.html)

[Getting To Know Logical Clocks By Implementing Them](https://brunocalza.me/getting-to-know-logical-clocks-by-implementing-them/)

[Scalable but Wasteful or Why Fast Replication Protocols are Actually Slow](https://twitter.com/AlekseyCharapko/status/1414417037187862528)

[The Fundamental Mechanism of Scaling](https://news.ycombinator.com/item?id=27865038)

[State Machine Replication, and Why You Should Care](https://signalsandthreads.com/state-machine-replication-and-why-you-should-care/)

[Distributed Systems Shibboleths](https://lobste.rs/s/p3uayt/distributed_systems_shibboleths)

> Your system might implement at-least-once delivery with idempotent processing, but it does not implement exactly-once which is demonstrated to be impossible in the Two Generals problem. These words matter because building idempotency has to be something you thread through your whole distributed system, all the way down to the system that is mutating the source of truth state and all the way up to your clients. It takes effort to build in idempotency, and can be difficult to add as an afterthought.

> Distributed leases are possible because the participating nodes agree ahead of time how much time they are allowed to assume they hold a lease without coordinating. This introduces unavailability under partitions (preserving CP by choosing to fail under a partition).

[Databases = Frameworks for Distributed Systems](https://news.ycombinator.com/item?id=31459745)

[distributed stuff](https://twitter.com/nodirt_/status/1530297313473617920)

["Formal Methods Only Solve Half My Problems"](https://twitter.com/MarcJBrooker/status/1532376318456655872?t=-uqj83fgJkznW9s9pKhT2Q&s=03)

[High Watermark — Distributed Design Patterns](https://distributedsystemsmadeeasy.medium.com/high-watermark-distributed-design-patterns-c1f3330d8129)

[Adventures in Building Reliable Distributed Systems with Liquid Haskell](https://www.reddit.com/r/haskell/comments/w4bjjn/adventures_in_building_reliable_distributed/)

[Strict-serializability, but at what cost, for what purpose?](https://muratbuffalo.blogspot.com/2022/08/strict-serializability-but-at-what-cost.html)

[Watermarks in Stream Processing Systems: Semantics and Comparative Analysis of Apache Flink and Google Cloud Dataflow](https://twitter.com/gunnarmorling/status/1599344380728393729)

[Distributed Transactional Systems Cannot Be Fast](https://twitter.com/penberg/status/1604011981782093852)

[Transactions in distributed systems](https://medium.com/nerd-for-tech/transactions-in-distributed-systems-b5ceea869d7d)

[Concurrency Deep Dive: Code Strategies for High Traffic Applications](https://nathanpeck.com/concurrency-deep-dive-strategies-for-high-traffic-applications/)

[Modeling Database Tables in Alloy](https://bytes.zone/posts/modeling-database-tables-in-alloy/). [modelling Git internals](https://lobste.rs/s/hulawt/modeling_git_internals_alloy_part_1_blobs).

[Outwards from the Middle of the Maze](https://www.youtube.com/watch?v=cJRuEr0MiM4). [tweet](https://twitter.com/asatarin/status/1611531598679396353).

[Great perspective on observability overhead](https://twitter.com/felixge/status/1643024606897250310)

[falsify for Haskell](https://twitter.com/EdskoDeVries/status/1643664485515657235)

[who invented vector clocks?](https://news.ycombinator.com/item?id=35506236)

[The Inner Workings of Distributed Databases](https://questdb.io/blog/inner-workings-distributed-databases/)

[An Introduction to TLA+ and Its Use in Parties](https://www.innoq.com/en/articles/2023/04/an-introduction-to-tla/)

[Open and Closed, Omission and Collapse](https://brooker.co.za/blog/2023/05/10/open-closed.html)

[Backfilling an Amazon DynamoDB Time to Live (TTL) attribute with Amazon EMR](https://aws.amazon.com/es/blogs/database/backfilling-an-amazon-dynamodb-time-to-live-ttl-attribute-with-amazon-emr/)

[What Kind of Asynchronous is Right For You?](https://www.reactivesystems.eu/2023/06/15/what-kind-of-asynchronous-is-right-for-you.html)

[Time is not a synchronization primitive](https://lobste.rs/s/b0e2nt/time_is_not_synchronization_primitive)

[Tips for concurrent programming](http://catern.com/concur.html)

[retries and backoff](https://fediscience.org/@marcbrooker/110645316730835757)

[Nanosecond timestamp collisions are common](https://www.evanjones.ca/nanosecond-collisions.html)

[the CAP theorem](https://apple.github.io/foundationdb/cap-theorem.html). [tweet](https://twitter.com/debasishg/status/1700542360621547718)

[   50 years later, is two-phase locking the best we can do? ](https://news.ycombinator.com/item?id=37706893)

[TLA+ for postmortem analysis](https://twitter.com/tianyin_xu/status/1708247209634914576)

[There is No Now—Problems with simultaneity in distributed systems](https://queue.acm.org/detail.cfm?id=2745385)

[Hints for Distributed Systems Design](https://muratbuffalo.blogspot.com/2023/10/hints-for-distributed-systems-design.html)

[State-Machine Replication (SMR) and Atomic Commit](https://ilyasergey.net/CS6213/week-02-consensus.html)

[modeling CRDTs in Alloy - introduction and the importance of idempotence](https://bytes.zone/posts/modeling-crdts-in-alloy-introduction-and-the-importance-of-idempotence/)

[advisory locking](https://twitter.com/yet_anotherDev/status/1711235976238964804?t=1v5rOjI179eIJhVFnEMsqA&s=03)

[Avoiding fallback in distributed systems (AWS builders library)](https://aws.amazon.com/builders-library/avoiding-fallback-in-distributed-systems/?nc1=h_ls)

[Unlocking Idempotency with Retroactive Tombstones](https://www.warpstream.com/blog/unlocking-idempotency-with-retroactive-tombstones)

[Shedlock](https://twitter.com/maciejwalkowiak/status/1728854453229695217)

[Catalog of Patterns of Distributed Systems](https://martinfowler.com/articles/patterns-of-distributed-systems/)

[It’s About Time!](https://brooker.co.za/blog/2023/11/27/about-time.html)

[Spanner under the hood: Understanding strict serializability and external consistency](https://cloud.google.com/blog/products/databases/strict-serializability-and-external-consistency-in-spanner)

[Thinking above the code](https://twitter.com/DominikTornow/status/1736106419211120862)

[exactly once—not possible, but you can hack it with idempotence](https://twitter.com/paul_snively/status/1737911146387046448)

[A CAP tradeoff in the wild](https://decomposition.al/blog/2023/12/31/a-cap-tradeoff-in-the-wild/)

> K8s caching layers on top of etcd end up undermining the correctness guarantees it provides in the first place

[Does Your Test Suite Account for Weak Transaction Isolation?](https://news.ycombinator.com/item?id=38867841).

[distributed systems papers](https://twitter.com/eatonphil/status/1747364101758529744)

[while speaking about frontends](https://timkellogg.me/blog/2024/01/17/htmx)

> I’ve spent a fair amount of time working with distributed systems. It’s just regular programming, just that everything is harder. Exceptions don’t bubble up, errors can be indistinguishable from latency, systems don’t compose, error handling doesn’t have a single best approach, even retries are harder than they should be.

[a primer on write skew](https://twitter.com/justinjaffray/status/979037185084096514)

[Some people say serializability is from the database-y research side of things and linearizability is from the distsys-y research side of things.](https://twitter.com/eatonphil/status/1754215016008389022)

[A distributed systems reading list | Hacker News](https://news.ycombinator.com/item?id=39303160)

[An intuition for distributed consensus in OLTP systems](https://notes.eatonphil.com/2024-02-08-an-intuition-for-distributed-consensus-in-oltp-systems.html)

[You Might Not Need a CRDT: Document Sync in the Wild by Paul Butler](https://www.youtube.com/watch?v=0d73MdQkJOk)

[fetch-and-add-based queues](https://news.ycombinator.com/item?id=40058253)

[Fault Tolerance via Idempotence (2013)](https://x.com/DominikTornow/status/1812978230959481083)

> To handle idempotence of arbitrary actions correctly end to end, every upstream component has to cooperate

[Exactly-Once Processing vs. Exactly-Once Delivery](https://ssudan16.medium.com/exactly-once-processing-in-kafka-explained-66ecc41a8548). [more](‘Exactly Once’ processing with Spark Structured Streaming). [polemic](https://www.reddit.com/r/programming/comments/6kh65f/comment/djnjywk/). [so question](https://stackoverflow.com/questions/58894281/difference-between-idempotence-and-exactly-once-in-kafka-stream). [Exactly Once = At least once + Idempotence](https://news.ycombinator.com/item?id=34986995). [more](https://news.ycombinator.com/item?id=15602841). [in Spring Cloud Stream](https://spring.io/blog/2023/10/16/apache-kafkas-exactly-once-semantics-in-spring-cloud-stream-kafka). [more](https://www.felpfe.com/2023/10/03/exactly-once-processing-guarantees-with-kafka-streams/). [pulsar](https://streamnative.io/blog/exactly-once-semantics-transactions-pulsar). [Do you really need exactly-once delivery?](https://streamingdata.substack.com/p/do-you-really-need-exactly-once-delivery).

[CAP is eventually boring](https://x.com/HenryR/status/1816509962173993428). [tweet](https://x.com/MarcJBrooker/status/1816503977577721913). [Let’s Consign CAP to the Cabinet of Curiosities](https://brooker.co.za/blog/2024/07/25/cap-again.html). [rethinking eventual consistency](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/sigtt611-bernstein.pdf). [Availability and availability](https://brooker.co.za/blog/2018/02/25/availability-liveness.html) 

> Where CAP goes off the rails is the second box: if a quorum of replicas is available to the client, they can still get both strong consistency, and uncompromised availability.

> It’s well known that the term Availability in the CAP theorem (as formally defined by Gilbert and Lynch) means something different from the term availability that’s commonly used by the designers, builders and operators of distributed systems

> It also doesn’t mean that there aren’t interesting trade-offs to be considered. Interesting ones include trade-offs between on-disk durability and write latency, between read latency and write latency, between consistency and latency, between latency and throughput, between consistency and throughput2, between isolation and throughput, and many others.

[Apache Iceberg consistency model](https://x.com/eatonphil/status/1821145093409017858)

[Understanding Delta Lake's consistency model + TLA+ proof](https://jack-vanlightly.com/analyses/2024/4/29/understanding-delta-lakes-consistency-model)

[thinking above the code](https://x.com/DominikTornow/status/1824536730860655090)

[Leader Election With S3 Conditional Writes](https://www.morling.dev/blog/leader-election-with-s3-conditional-writes/)

[prefix consistency](https://x.com/vanlightly/status/1826954250083033525)

[ implemented SERIALIZABLE transactions with optimistic concurrency control](https://x.com/eatonphil/status/1826359437243941320)

[Linearizability! Refinement! Prophecy!](https://surfingcomplexity.blog/2024/09/22/linearizability-refinement-prophecy/). [Consistency](https://surfingcomplexity.blog/2023/12/29/the-inherent-weirdness-of-system-behavior/).

> When we move from sequential programs to concurrent ones, we need to extend our concept of what “correct” means to account for the fact that operations from different threads can overlap in time. Linearizability is the strongest consistency model for single-object systems, which means that it’s the one that aligns closest to our intuitions. Other models are weaker and, hence, will permit anomalies that violate human intuition about how systems should behave.

> What I love about consistency models is that they aren’t treated as correctness models. Instead, they’re weirdness models

[Snapshot Isolation vs Serializability](https://brooker.co.za/blog/2024/12/17/occ-and-isolation.html)

[Versioning versus Coordination](https://brooker.co.za/blog/2025/02/04/versioning.html)

[The Synchrony Budget](https://www.morling.dev/blog/the-synchrony-budget/)

[Decomposing Transactional Systems](https://transactional.blog/blog/2025-decomposing-transactional-systems)

[Decomposing Aurora DSQL](https://brooker.co.za/blog/2025/04/17/decomposing.html).

[Consensus algorithms at scale: Part 1 - Introduction](https://planetscale.com/blog/consensus-algorithms-at-scale-part-1)

[What even is distributed systems](https://notes.eatonphil.com/2025-08-09-what-even-is-distributed-systems.html)

[using dbs for queues yay or nay](https://x.com/MarcJBrooker/status/1970280783500976168)

[why strong consistency?](https://brooker.co.za/blog/2025/11/18/consistency.html)

[on idempotency keys](https://www.morling.dev/blog/on-idempotency-keys/). [tweet](https://x.com/kellabyte/status/1993823493746577823).



