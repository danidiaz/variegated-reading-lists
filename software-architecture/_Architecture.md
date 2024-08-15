[Vertical decomposition. Creating cohesive services](http://hecodes.com/2018/07/vertical-decomposition-creating-cohesive-services/)

> One of the biggest misconceptions about services is that a service is an independent deployable unit, i.e., service equals process. With this view, we are defining services according to how components are physically deployed. In our example, since it’s clear that the backend admin runs in its own process/container, we consider it to be a service.

> But this definition of a service is wrong. Rather you need to define your services in terms of business capabilities. The deployment aspect of the system doesn’t have to be correlated to how the system has been divided into logical services. For example, a single service might run in different components/processes, and a single component might contain parts of multiple services. Once you start thinking of services in terms of business capabilities rather than deployment units, a whole world of options open.

> What are the Admin UI, Admin Backend and Website UI, Website Backend components? They basically act as containers of services. They are maintained by their own teams and their sole purpose is to coordinate between services. These components are business-logic agnostic.

[Avoiding Microservice Megadisasters](https://www.youtube.com/watch?v=gfh-VCTwMw8) unsure about the approach to search and data duplication

[Microservices and Rules Engines – a blast from the past](https://www.youtube.com/watch?v=Fuac__g928E)

> "search engine, not search service"
> "allows each microservice to put a component into it, and the search engine will run that set of rules"
> "what we are talking about here is not the whole microservice, but the search component of that service"
> "that way, the search engine doesn't need in and of itself access to all of that data directly"

[Don't build a distributed monolith](https://www.microservices.com/talks/dont-build-a-distributed-monolith/)

> "Don't couple systems with binary dependencies"

> Alas this seems to go against the "thinking of services in terms of business capabilities rather than deployment units" principle. If the deployment is intertwined, is seems that there will be binary dependencies.

[The Art of the node.js Rescue](https://peterlyons.com/problog/2018/07/the-art-of-the-node-js-rescue)

[The entity service antipattern](http://www.michaelnygard.com/blog/2017/12/the-entity-service-antipattern/)

[Five pieces of advice for new technical leads](http://engineering.rallyhealth.com/technical-lead/leadership/new-leader/advice/new-role/tech-lead/2018/07/05/five-pieces-of-advice-for-new-technical-leads.html)

[The System Design Primer](https://github.com/donnemartin/system-design-primer) [hn](https://news.ycombinator.com/item?id=17522362)

> in general, re-organizing the architecture of a system is usually possible - if and only if - the underlying data model is sane.

> What is the convention for addressing assets and entities? Is it consistent and useful for informing both security or data routing?

> What is the security policy for any specific entity in your system? How can it be modified? How long does it take to propagate that change? How centralized is the authentication?

> If a piece of "data" is found, how complex is it to find the origin of this data?

> What is the policy/system for enforcing subsystems have a very narrow capability to mutate information?

[More than concentric layers](https://herbertograca.com/2018/07/07/more-than-concentric-layers/) [The Software Architecture Chronicles](https://herbertograca.com/2017/07/03/the-software-architecture-chronicles/)

[Managing the Complexity of Microservices Deployments](https://www.infoq.com/presentations/microservices-pcf-spring-boot-edge)

[Designing Microservice Architectures the Right Way](https://www.infoq.com/news/2018/07/bryzek-microservice-architecture) [slides](https://www.slideshare.net/mbryzek/design-microservice-architectures-the-right-way)

[To Test A System, You Need A Good Design](https://medium.com/@fagnerbrack/how-to-mock-the-network-with-nock-and-javascript-to-test-parts-of-a-system-you-need-a-good-design-9432c9c05a30) [Shunt pattern](http://wiki.c2.com/?ShuntPattern) [Two-level test suites?](https://twitter.com/DiazCarrete/status/1006863912761987072)

> For a test environment, you can inject an “In-Memory Data Source.” For production, you can use the “HTTP Server Data Source.”

[How Contract Tests Improve the Quality of Your Distributed Systems](https://www.infoq.com/articles/contract-testing-spring-cloud-contract)

[SOLID Architecture in Slices not Layers](https://vimeo.com/190925521)

> For too long we've lived under the tyranny of n-tier architectures. Building systems with complicated abstractions, needless indirection and more mocks in our tests than a comedy special. But there is a better way - thinking in terms of architectures of vertical slices instead horizontal layers. Once we embrace slices over layers, we open ourselves to a new, simpler architecture, changing how we build, organize and deploy systems.

[Scaling without cross-functional teams](https://vimeo.com/190925319)

[Growing Object-Oriented Software, Guided by Tests Without Mocks](https://enterprisecraftsmanship.com/2016/07/05/growing-object-oriented-software-guided-by-tests-without-mocks/) [Unit testing anti-patterns: Structural Inspection](https://enterprisecraftsmanship.com/2016/07/21/unit-testing-anti-patterns-structural-inspection/)

[Test automation without a headache: Five key patterns](https://vimeo.com/154289460)

[What’s your release process like?](https://lobste.rs/s/mc85ko/what_s_your_release_process_like)

[ndepend and code analysis](https://www.blinkingcaret.com/2018/08/22/software-development-emergent-system-ndepend/)

[Lessons from Building Static Analysis Tools at Google](https://cacm.acm.org/magazines/2018/4/226371-lessons-from-building-static-analysis-tools-at-google/fulltext)

[Writing Documentation When You Aren't a Technical Writer ](https://blog.stoplight.io/writing-documentation-when-you-arent-a-technical-writer-part-one-ef08a09870d1?gi=870678b3f858) [hn](https://news.ycombinator.com/item?id=17829751). [Semantic linefeeds](http://rhodesmill.org/brandon/2012/one-sentence-per-line/). [guidelines](https://news.ycombinator.com/item?id=17834084).

> automated the checks as much as possible with linters [2].

[Age of Invisible Disasters](https://news.ycombinator.com/item?id=17844712)

[Conforming container antipattern](http://blog.ploeh.dk/2014/05/19/conforming-container/)


[microfrontends](https://www.youtube.com/watch?v=rCxj-ONZmxs)

[Break Up With Your Frontend Monolith - Elisabeth Engel](https://www.youtube.com/watch?v=7MHsPfoonqs)

[Compositional UIs - the Microservices Last Mile - Jimmy Bogard](https://www.youtube.com/watch?v=gjtFGx0yX5M)

[Explicitly Yours](http://kislayverma.blogspot.com/2018/08/explicitly-yours.html)

[jdepend](http://mcs.une.edu.au/doc/jdepend/docs/JDepend.html)

> Before using JDepend, it is important to understand that "good" design quality metrics are not necessarily indicative of good designs. Likewise, "bad" design quality metrics are not necessarily indicative of bad designs. The design quality metrics produced by JDepend should not be used as yard sticks by which all designs are measured.

[Reconstructing thalia.de with self-contained systems](https://www.youtube.com/watch?v=r3v8e62abH8)

[Optimizing for iteration speed](https://erikbern.com/2017/07/06/optimizing-for-iteration-speed.html)

> one of the most scary thing in software engineering is “inventory” of code that builds up without going into production. It represents deployment risk, but also risk of building something users don’t want. Not to mention lost user value from not shipping parts of the feature earlier (user value should be thought of as feature value integrated over time, not as the feature value at the end state).

[Thinking Architecturally](https://www.youtube.com/watch?v=EfKT1dgsLFA)

[Unit test your Java architecture](https://www.archunit.org/) [tweet](https://twitter.com/gunnarmorling/status/1039055538699612161)

> If your primary motivation for building microservices is to enforce modular architectures, think twice. Modularity is solved within the JVM (JPMS, OSGi, JBoss Modules; even multimodule builds get you far), don't pay the price of distributed computing + remote calls just for this.

[Majestic Modular Monolith!](https://www.youtube.com/watch?v=oBiH003x9bY)

[SonarJS](https://www.youtube.com/watch?v=z930dsujSgw)

[Apache Kafka als Backend für Webanwendungen?](https://www.heise.de/developer/artikel/Apache-Kafka-als-Backend-fuer-Webanwendungen-4153355.html)

[How Events Are Reshaping Modern Systems by Jonas Bonér](https://www.youtube.com/watch?v=3V3pHm2Cpks)

[Serverless](https://www.youtube.com/watch?v=PgZ2dxnj734)

[Complex Event Flows in Distributed Systems](https://www.infoq.com/presentations/event-flow-distributed-systems)

[Designing Events-first Microservices](https://www.infoq.com/presentations/microservices-events-first-design). [Journey to Event Driven – Part 1](https://www.confluent.io/blog/journey-to-event-driven-part-1-why-event-first-thinking-changes-everything)

[Microservices in a Post-Kubernetes Era](https://www.infoq.com/articles/microservices-post-kubernetes)

> In the post-Kubernetes era, using libraries to implement operational networking concerns (such as Hystrix circuit breaking) has been completely overtaken by service mesh technology.

[the testing renaissance](https://blog.twitter.com/engineering/en_us/topics/insights/2017/the-testing-renaissance.html). [tweets](https://twitter.com/copyconstruct/status/950533079851982848) about [testing](https://twitter.com/Hillelogram/status/1046602709028286464).

[HANDS-ON INTRO TO KUBERNETES & OPENSHIFT](http://gist-reveal.it/bit.ly/nodejs-on-k8s?theme=9181e48c0dd8e6b45d692a11d5a72bd5#/HANDS-ON).

[Tell Don't Ask](https://www.martinfowler.com/bliki/TellDontAsk.html). [more](https://www.javacodegeeks.com/2018/11/extension-telldontask.html). [How Interfaces Are Refactoring Our Code](https://www.amihaiemil.com/2017/08/12/how-interfaces-are-refactoring-our-code.html). [The art of embugging](https://media.pragprog.com/articles/jan_03_enbug.pdf). [GetterEradicator](https://www.martinfowler.com/bliki/GetterEradicator.html).

[AWS Solution Architect Associate exam](https://loige.co/aws-solution-architect-associate-exam-notes-tips/).

[Hybrid Networking Reference Architectures](https://blogs.msdn.microsoft.com/azurecat/2018/11/20/hybrid-networking-reference-architectures/).

[Docs as Code – Architekturdokumentation leicht gemacht](https://jaxenter.de/docs-as-code-2-77404).

[No More Silos: How to Integrate Your Databases with Apache Kafka and CDC](https://www.confluent.io/blog/no-more-silos-how-to-integrate-your-databases-with-apache-kafka-and-cdc).

[Streaming Data Clears the Path for Legacy Systems Modernization](https://www.linkedin.com/pulse/streaming-data-clears-path-legacy-systems-jagdish-mirani/).

[Integrating legacy and CQRS](https://community.risingstack.com/integrating-legacy-and-cqrs-2/).

[Streaming MySQL tables in real-time to Kafka](https://engineeringblog.yelp.com/2016/08/streaming-mysql-tables-in-real-time-to-kafka.html).

[Streaming databases in realtime with MySQL, Debezium, and Kafka](https://wecode.wepay.com/posts/streaming-databases-in-realtime-with-mysql-debezium-kafka). Mención en: [¡Larga vida al legacy!](https://youtu.be/uR3TTzX7C9Y?t=1714).

> no ser el dueño del modelo de datos debería ser algo temporal

> parece que el "sistema secundario" es solo de lectura en un principio

> el siguiente pase, de alguna manera, tienes que ser capaz de modificar el sistema antiguo... arquitecturasa más complejas con bidireccionalidad. no uses bus de eventos. expon servicios en el sistema nuevo, haz que el sistema legado los accede. no uses bus de eventos (?)

> sin eventos obligo al software legado a saber a dónde me he llevado ese trocito que le he quitado.

> [para sincronizar] podemos usar eventos, triggers... 

[GETTING STARTED WITH DDD WHEN SURROUNDED BY LEGACY SYSTEMS - Eric Evans](http://domainlanguage.com/wp-content/uploads/2016/04/GettingStartedWithDDDWhenSurroundedByLegacySystemsV1.pdf). [bubble context](https://www.thoughtworks.com/radar/techniques/autonomous-bubble-pattern). [strategy 1 - bubble context](http://dddcommunity.org/library/evans_2011_2/2). [strategic design](http://dddcommunity.org/strategic-design/). [bounded context](https://martinfowler.com/bliki/BoundedContext.html).

[Listen to Yourself: A Design Pattern for Event-Driven Microservices](https://medium.com/@odedia/listen-to-yourself-design-pattern-for-event-driven-microservices-16f97e3ed066).

> For example, you cannot guarantee that a commit to Cassandra and a message delivery to Kafka would be done atomically or not done at all.

> Let’s take a common use case: Updating a local NoSQL database and also notifying a legacy system of record about the activity.

> However, there is still a concrete problem: How do you guarantee atomic execution of both the NoSQL writes and the publishing of the event to the message broker?

> Note: Potential duplicate messages are always a possibility with a message broker so you should design your message handling to be idempotent regardless of the solution you choose.

> All your events and database writes must be idempotent to avoid duplicate records.

> The client isn’t guaranteed to read their own writes immediately.

> The transaction log tailing pattern can achieve similar results to those described here. Your transactions will be atomic without resorting to two phase commit. The transaction log tailing pattern has the added benefit of guranteeing your database is committed before returning a response to the client.

[Pattern: Transaction log tailing](https://microservices.io/patterns/data/transaction-log-tailing.html).

>  each step of a saga must atomically update the database and publish messages/events. It is not viable to use a distributed transaction that spans the database and the message broker.

[How to solve two generals issue between event store and persistence layer?](https://stackoverflow.com/questions/50702676/how-to-solve-two-generals-issue-between-event-store-and-persistence-layer).

[Event-Driven Data Management for Microservices](https://dzone.com/articles/event-driven-data-management-for-microservices-1).

> One way to achieve atomicity is for the application to publish events using a multi-step process involving only local transactions. The trick is to have an EVENT table, which functions as a message queue, in the database that stores the state of the business entities. 

[Domain events: simple and reliable solution](https://enterprisecraftsmanship.com/2017/10/03/domain-events-simple-and-reliable-solution/).

> In an event-driven architecture there is also the problem of atomically updating the database and publishing an event.

> [my thoughs] are the options: 1 - "listen to yourself" pattern and 2 - "keeping an internal events table"? Also 3 - "log trailing"?

[Paypal talk](https://twitter.com/deanwampler/status/1070468311991775232). [slides](https://www.slideshare.net/r39132/big-data-fast-data-paypal). [Streaming Data Microservices](https://deanwampler.github.io/polyglotprogramming/papers/KafkaMicroservices-AkkaStreams-KafkaStreams.pdf). [Oracle Golden Gate](https://www.oracle.com/middleware/technologies/goldengate.html).

> from the slides:
66: XA transactions: ensure consistency, give up availability
67: Event Sourcing: give up read-your-writes consistency (Is this the "listen to yourself" pattern?)
68: Change Data Capture: read-your-writes + eventual consistency across systems

> OLAP engines like Apache Druid, LinkedIn's Pinot

>  "Use Change Data Capture, rather than XA Transactions or Event Sourcing, for replicating data between data systems where consistency is required, etc., such as financial services... Also use schemas"

> logs, not queues!

> Unlike queues, consumers don't delete entries; Kafka manages their lifecycles

> N Consumers, who start reading where they want

> Akka Streams, Kafka Streams - libraries for “data-centric microservices”. Smaller scale, but great flexibility

[Kubernetes: Your Next Application Server](https://developers.redhat.com/blog/2018/12/07/kubernetes-application-server/). [video](https://www.youtube.com/watch?v=K6gM4wFEmwA).

[How to extract change data events from MySQL to Kafka using Debezium](https://vladmihalcea.com/how-to-extract-change-data-events-from-mysql-to-kafka-using-debezium/).

[about architectures](https://twitter.com/mononcqc/status/1070373406917517313).

[Openshift secrets management](https://www.youtube.com/watch?v=LPFs-2b2z9U&feature=youtu.be&list=PLaR6Rq6Z4IqctmZiEgyO64ymwcfC77Nmv)

[one step forward, two steps back](https://news.ycombinator.com/item?id=18689544).

[Introduction to the Kubernetes Operator Framework](https://developers.redhat.com/blog/2018/12/18/introduction-to-the-kubernetes-operator-framework/)

[Keynote: Maturing Kubernetes Operators - Rob Szumski](https://www.youtube.com/watch?v=kld1Fi8RrRQ).

[DEATH OF LOGGING, HEXAGONAL ARCHITECTURES, TECHNOLOGY AND ARCHITECTURES](http://adambien.blog/roller/abien/entry/death_of_logging_hexagonal_architectures).

[Kubernetes The Database](https://www.youtube.com/watch?v=eja7b3tahMg&index=292&list=PLj6h78yzYM2PZf9eA7bhWnIh_mK1vyOfU&t=0s).

[Introduction to Cloud Storage for Developers](https://dev.to/jeremylikness/introduction-to-cloud-storage-for-developers-2hig).

[building a CI / CD bot with Kubernetes](https://www.reddit.com/r/programming/comments/a4li0l/building_a_cicd_bot_with_slack_and_kubernetes/)

[docker secrets](https://www.reddit.com/r/devops/comments/a3wfgq/why_cant_i_wrap_my_head_around_docker/)

> managing env vars in production comes down to doing one of two things: using an environment file that is securely stored and securely retrieved, or retrieving each key from a secure secrets management service like Vault, Keywhiz or Cyberarc. The former is easier, as it requires less infrastructure, but requires greater care. The latter requires more infrastructure but handles things like role based access for each key more easily

[Istio Multicluster on OpenShift](https://blog.openshift.com/istio-multicluster-on-openshift)

[Kafka for long-term storage](https://www.quora.com/Is-Apache-Kafka-robust-enough-to-be-used-as-the-only-persistent-storage). [so](https://stackoverflow.com/questions/46925924/use-kafka-topics-to-store-data-for-many-years). [hn](https://news.ycombinator.com/item?id=15185652). [How Pinterest runs Kafka at scale](https://medium.com/pinterest-engineering/how-pinterest-runs-kafka-at-scale-ff9c6f735be). [Streaming Hundreds of Terabytes of Pins from MySQL to S3/Hadoop Continuously](https://www.confluent.io/kafka-summit-sf18/pinterests-story-of-streaming-hundreds-of-terabytes). [Is Kafta a database?](https://www.youtube.com/watch?v=v2RJQELoM6Y). [experimentation with event-based systems](https://www.youtube.com/watch?v=_RgUxUTuxH4). [The Magical Rebalance Protocol of Apache Kafka](https://www.youtube.com/watch?v=MmLezWRI3Ys). [The Death and Rebirth of the Event-Driven Architecture](https://www.youtube.com/watch?v=gsUZ6RYmL1s). [ETL Is Dead, Long Live Streams](https://www.youtube.com/watch?v=I32hmY4diFY). [event-based architectures with Kafka and Atom](https://www.softwaretalks.io/v/4979/goto-2018-o-event-based-architecture-and-implementations-with-kafka-and-atom-o-eberhard-wolff). [Complex Event Flows in Distributed Systems](https://www.infoq.com/presentations/event-flow-systems). [Restoring Confidence in Microservices: Tracing That's More Than Traces](https://www.infoq.com/presentations/microservices-distributed-tracing).

> This is an important requirement for processes that calculate real-time results but need to periodically recalculate results (say when their processing logic changes).

> Something to keep in mind as well is that cluster restarts (especially after unclean shutdowns) might take a very long time, as all logs would need to be checked at broker startup. Apart from that I can't think of large reasons not to do this, though I agree that dumping data to S3/HDFS/similar should be the preferred solution

> we use Kafka to transport data to our data warehouse, including critical events like impressions, clicks, close-ups, and repins. We also use Kafka to transport visibility metrics for our internal services

[Language-oriented software engineering](http://parametri.city/blog/2018-12-23-language-oriented-software-engineering/index.html). [tweet](https://twitter.com/themattchan/status/1076977773195931648).

[Using ETL Staging Tables](https://www.timmitchell.net/post/2017/06/14/etl-staging-tables/)


[The future of Kubernetes is Virtual Machines](http://tech.paulcz.net/blog/future-of-kubernetes-is-virtual-machines/) [hn](https://news.ycombinator.com/item?id=18765670)

[Developing applications on OpenShift in an easier way](https://blog.openshift.com/developing-applications-on-openshift-in-an-easier-way/)

[Mastering Spring framework 5, Part 2: Spring WebFlux](https://www.javaworld.com/article/3288219/spring-framework/mastering-spring-framework-5-part-2-spring-webflux.html)

[Day Two Kubernetes: Tools for Operability](https://www.infoq.com/presentations/kubernetes-tools).

[kubernetes guideposts 2019](https://blog.openshift.com/kubernetes-guideposts-for-2019/) [Simple Multi-tenancy with Django Running on OpenShift](https://itnext.io/simple-multi-tenancy-with-django-running-on-openshift-b5859a94dd52)

[KUBERNETES FAILURE STORIES](https://srcco.de/posts/kubernetes-failure-stories.html). [hn](https://news.ycombinator.com/item?id=18953647).

[Cloud native Java EE on OpenShift](https://twitter.com/AdamBien/status/1087610788183969793) Adam Bien.

[making the most of Kubernetes clusters](https://www.infoq.com/presentations/chick-fil-a-k8-clusters)

[Scaling a Distributed Stream Processor in a Containerized Environment](https://www.infoq.com/articles/distributed-stream-processor-container)

[Kubinception](https://www.ovh.com/fr/blog/kubinception-using-kubernetes-to-run-kubernetes/).

[kubernetes vs. docker](https://dzone.com/articles/kubernetes-vs-docker)

[rethinking legacy and monolithic systems](https://www.infoq.com/presentations/monolith-legacy-rethinking)

["how do I propagate state across asynchronous, reactive execution pipelines?"](https://twitter.com/SpringTipsLive/status/1090515218025705472). [video](https://www.youtube.com/watch?v=5tlZddM5Jo0). [Spring Tips: Testing Reactive Code](https://www.youtube.com/watch?v=RPmTXiw-dHA). [RxJava vs Reactor](https://www.nurkiewicz.com/2019/02/rxjava-vs-reactor.html). [Reactive Spring: Eine Einführung in die reaktive Programmierung](https://jaxenter.de/reactive-spring-76966). [Point-to-Point Messaging Architecture - The Reactive Endgame](https://www.infoq.com/presentations/messaging-architecture-future). [building reactive pipelines](https://speakerdeck.com/mkheck/building-reactive-pipelines) [tweet](https://twitter.com/mkheck/status/1099332530791243777). [reactive DDD](https://www.infoq.com/presentations/reactive-ddd). [How (not) to use Reactive Streams in Java 9+](https://www.reddit.com/r/programming/comments/ax895o/how_not_to_use_reactive_streams_in_java_9/). [Assembly time Subscription time Execution time)](https://spring.io/blog/2019/03/06/flight-of-the-flux-1-assembly-vs-subscription) [404](https://www.baeldung.com/spring-webflux-404). [construyendo pipelines reactivos](https://twitter.com/mkheck/status/1107376655096520704) [slides](https://speakerdeck.com/mkheck/construyendo-pipelines-reactivos). [Spring Tips: Reactive MySQL with Jasync SQL and R2DBC](https://spring.io/blog/2019/03/20/spring-tips-reactive-mysql-support-with-jasync-sql-and-r2dbc). [reactive streams operators](https://www.infoq.com/news/2019/03/microprofile-reactive-stream-1.0). [RxJava by example](https://twitter.com/argntprgrmr/status/1114146417164062720). [reactive jdbc tweet](https://twitter.com/vlad_mihalcea/status/1114609048178106371). [5 reasons to use RxJava in your projects](https://jaxenter.com/5-reasons-use-rxjava-148982.html). [reactive programming - lessons learned](https://www.youtube.com/watch?v=5TJiTSWktLU). [reactive transactions](https://twitter.com/SpringTipsLive/status/1130898402731024386). [reactive-revolution course materials](https://twitter.com/starbuxman/status/1131067765983522817). [marble diagrams](https://twitter.com/atomicobject/status/1135638282669305861). [reactive streams and Kotlin flows](https://medium.com/@elizarov/reactive-streams-and-kotlin-flows-bfd12772cda4). [Event Driven with Spring](https://www.youtube.com/watch?v=xjJuZCrqWnA). [How to build Reactive Server in 50 minutes](https://www.youtube.com/watch?v=IzwOvMJ8lrQ). [moving from imperative to reactive](https://www.youtube.com/watch?v=vSHNBgY7MGA). [reactive programming - lessons learned](https://www.youtube.com/watch?v=5TJiTSWktLU). [more](https://www.youtube.com/watch?v=g_JyHJ20Iog). [slides](https://nurkiewicz.github.io/talks/2018/reactive-lessons/#/). [Five Things About RxJS and Reactive Programming](https://channel9.msdn.com/Shows/5-Things/Five-Things-About-RxJS-and-Reactive-Programming?WT.mc_id=channel9-twitter-cda). [Going full reactive with Spring Webflux and the new CosmosDB API v3](https://dev.to/azure/going-full-reactive-with-spring-webflux-and-the-new-cosmosdb-api-v3-1n2a). [reactive streams basic concepts](https://twitter.com/thjanssen123/status/1150467791918698496). [Streaming data as one additional use case for #reactive programming](https://twitter.com/odrotbohm/status/1172426045900783616). [building reactive pipelines](https://twitter.com/mkheck/status/1173718834005413888). [the value of reactive systems](https://www.infoq.com/presentations/template-reactive-system/). [reactor](https://twitter.com/InfoQ/status/1221466834660184065). [Do's and Don'ts: Avoiding First-Time Reactive Programmer Mines](https://www.infoq.com/presentations/reactive-mines/).


[Learn Openshift operator framework](https://learn.openshift.com/operatorframework/)

[certified](https://news.ycombinator.com/item?id=19062042)

> In big companies, 95% of apps are still old school: firewall -- load balancer -- 5 front ends -- 3 back ends -- two database servers. 

["everybody wants to get rid of ELK for logging quite soon"](https://twitter.com/x0rg/status/1092021673803632640).

[airhacks tv 59](http://adambien.blog/roller/abien/entry/2019_predictions_java_ee_authentication) docker vs. openshift [effective web standards](http://effectiveweb.training/)

[metrics for the masses](https://www.infoq.com/presentations/metrics-apache-geode-micrometer)

[Service Catalog and Kubernetes](https://www.infoq.com/articles/service-catalog-kubernetes)

> Kubernetes declarative object configuration model is one of the most interesting features of the orchestrator

[12 ways to get smarter about Kubernetes](https://enterprisersproject.com/article/2019/2/kubernetes-12-ways-get-smarter).

[Microservices in a Post-Kubernetes Era](https://www.infoq.com/articles/microservices-post-kubernetes).

[How Kubernetes can break: networking](https://twitter.com/b0rk/status/1108164989012135936)

[Automating stateful applications with Kubernetes operators](https://speakerdeck.com/jankleinert/automating-stateful-applications-using-kubernetes-operators) [Reaching for the Stars with Ansible Operator](https://blog.openshift.com/reaching-for-the-stars-with-ansible-operator/)

[Why are we templating YAML?](https://news.ycombinator.com/item?id=19108787).

[An Incremental Architecture Approach to Building Systems](https://www.infoq.com/news/2019/01/rearchitecture-system-success).


Various links about persistence and DDD:

https://tech.transferwise.com/hibernate-and-domain-model-design/
https://stackoverflow.com/questions/10099636/are-persistence-annotations-in-domain-objects-a-bad-practice
https://stackoverflow.com/questions/14737652/entity-objects-vs-value-objects-hibernate-and-spring
https://stackoverflow.com/questions/31400432/ddd-domain-entities-vo-and-jpa
https://stackoverflow.com/questions/2597219/is-it-a-good-idea-to-migrate-business-logic-code-into-our-domain-model
https://stackoverflow.com/questions/821276/why-should-i-isolate-my-domain-entities-from-my-presentation-layer
https://softwareengineering.stackexchange.com/questions/350067/is-it-good-practice-to-use-entity-objects-as-data-transfer-objects
https://softwareengineering.stackexchange.com/questions/378866/understanding-ddd-when-using-an-orm-such-as-hibernate
https://softwareengineering.stackexchange.com/questions/171457/what-is-the-point-of-using-dto-data-transfer-objects
https://softwareengineering.stackexchange.com/questions/140826/do-orms-enable-the-creation-of-rich-domain-models
https://blog.pragmatists.com/refactoring-from-anemic-model-to-ddd-880d3dd3d45f
https://enterprisecraftsmanship.com/2016/04/05/having-the-domain-model-separate-from-the-persistence-model/

[Custom Implementations for Spring Data Repositories](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#repositories.custom-implementations).

[Three-Part Architecture of the Next Generation Data Center Inside NetApp](https://blog.netapp.com/three-part-architecture-of-the-next-generation-data-center-inside-netapp/).

[Conquering the Challenges of Data Preparation for Predictive Maintenance](https://www.infoq.com/articles/challenges-of-data-preparation-for-predictive-maintenance)

[Java 9: Bessere Domänenmodelle mit Java-9-Modulen](https://jaxenter.de/domaenenmodelle-java-9-77030).

Links about the strangler pattern https://news.ycombinator.com/item?id=19122973 strangler pattern https://news.ycombinator.com/item?id=19125333 https://paulhammant.com/2013/07/14/legacy-application-strangulation-case-studies/ https://www.michielrook.nl/2016/11/strangler-pattern-practice/ https://trunkbaseddevelopment.com/strangulation/ https://www.leadingagile.com/2018/10/the-urge-to-stranglethe-strangler-pattern/ https://www.martinfowler.com/bliki/StranglerApplication.html https://twitter.com/martinfowler/status/357142664665251841 https://blog.overops.com/strangler-pattern-how-to-keep-sane-with-legacy-monolith-applications/ https://blogs.sap.com/2017/09/25/strangler-applications-monolith-to-microservices/

Links about DTO mappers https://auth0.com/blog/automatically-mapping-dto-to-entity-on-spring-boot-apis/ https://www.baeldung.com/entity-to-and-from-dto-for-a-java-spring-application http://modelmapper.org/ https://medium.com/@hackmajoris/a-generic-dtos-mapping-in-java-11d649b8a486 https://stackoverflow.com/questions/2828403/dto-and-mapper-generation-from-domain-objects https://stackoverflow.com/questions/14523601/bo-dto-mapper-in-java https://stackoverflow.com/questions/15117403/dto-pattern-best-way-to-copy-properties-between-two-objects https://stackoverflow.com/questions/1432764/any-tool-for-java-object-to-object-mapping https://stackoverflow.com/questions/678217/best-practices-for-mapping-dto-to-domain-object https://codereview.stackexchange.com/questions/64731/mapping-interface-between-pojos-and-dtos https://softwareengineering.stackexchange.com/questions/171457/what-is-the-point-of-using-dto-data-transfer-objects https://www.jhipster.tech/using-dtos/ http://appsdeveloperblog.com/java-objects-mapping-with-modelmapper/ http://www.adam-bien.com/roller/abien/entry/creating_dtos_without_mapping_with The Ping class is a JPA entity and JSON-B DTO at the same time: http://www.adam-bien.com/roller/abien/entry/creating_dtos_without_mapping_with DTOs are also motivated by their typesafe nature. Lacking typesafety, JSON-P JsonObjects are not used as DTOs. https://www.credera.com/blog/technology-solutions/mapping-domain-data-transfer-objects-in-spring-boot-with-mapstruct/ https://rmannibucau.wordpress.com/2014/04/07/dto-to-domain-converter-with-java-8-and-cdi/ https://vladmihalcea.com/the-best-way-to-map-a-projection-query-to-a-dto-with-jpa-and-hibernate/ https://github.com/porscheinformatik/anti-mapper [jpa hashCode euquals dilemma](https://stackoverflow.com/questions/5031614/the-jpa-hashcode-equals-dilemma/26826084?stw=2#26826084)

[What's new in Spring Data](https://www.infoq.com/presentations/spring-data-kotlin)

[Running your own DBaaS based on your preferred DBs, Kubernetes operators and containerized storage](https://blog.openebs.io/running-your-own-dbaas-based-on-your-preferred-dbs-kubernetes-operators-and-containerized-storage-3cc36ba115b8).

[Microservices in a Post-Kubernetes Era](https://www.infoq.com/articles/microservices-post-kubernetes)

> In the post-#Kubernetes era, using libraries to implement operational networking concerns (such as Hystrix circuit breaking) has been completely overtaken by service mesh technology.

[Netflix Titus, Its Feisty Team, and Daemons](https://www.infoq.com/presentations/netflix-titus-2018).

[Scaling a Distributed Stream Processor in a Containerized Environment](https://www.infoq.com/articles/distributed-stream-processor-container)

[Odo](https://twitter.com/jorgemoralespou/status/1098919559187320838).

[Is Shared Database in Microservices actually anti-pattern?](https://hackernoon.com/is-shared-database-in-microservices-actually-anti-pattern-8cc2536adfe4). [hn](https://news.ycombinator.com/item?id=19239247)

[The Whys and Hows of Database Streaming](https://www.infoq.com/presentations/wepay-database-streaming)

[The Changing Face of ETL: Event-Driven Architectures for Data Engineers](https://speakerdeck.com/rmoff/the-changing-face-of-etl-event-driven-architectures-for-data-engineers)

[Your migrations are bad, and you should feel bad](https://djrobstep.com/talks/your-migrations-are-bad-and-you-should-feel-bad). [hn](https://news.ycombinator.com/item?id=19286885).

[An introduction to distributed systems](https://github.com/aphyr/distsys-class/blob/master/README.markdown)

[Paying Technical Debt at Scale - Migrations @Stripe](https://www.youtube.com/watch?v=OFjvJmS_uDo).

Transaction scripts https://dzone.com/articles/transaction-script-pattern https://stackoverflow.com/questions/16139941/transaction-script-is-antipattern https://gunnarpeipman.com/architecture-design-patterns/transaction-script-pattern/ https://learnbycode.wordpress.com/2015/04/12/the-business-logic-layer-transaction-script-pattern/ http://www.servicedesignpatterns.com/webserviceimplementationstyles/transactionscript http://lorenzo-dee.blogspot.com/2014/06/quantifying-domain-model-vs-transaction-script.html http://grahamberrisford.com/AM%202%20Methods%20support/06DesignPatternPairs/Domain%20Driven%20Design%20v.%20Transaction%20script.htm

[Automating applications with @kubernetesio operators](https://twitter.com/jorgemoralespou/status/1107135127035928577)

[Code in the database vs. code in the application](https://softwareengineering.stackexchange.com/questions/108867/how-do-you-decide-between-putting-the-code-in-the-database-or-putting-the-code-i). [2](https://dba.stackexchange.com/questions/2450/what-are-the-arguments-against-or-for-putting-application-logic-in-the-database). [3](https://stackoverflow.com/questions/3378686/putting-database-logic-in-the-application-instead-of-trigger-stored-procedures). [4](https://stackoverflow.com/questions/1486342/where-to-put-the-sql-logic/1486627#1486627). [5](https://stackoverflow.com/questions/119540/business-logic-database-or-application-layer/123106). [6](https://stackoverflow.com/questions/1473624/business-logic-in-database-versus-code/1473670#1473670). [7 by Lukas Eder](https://www.vertabelo.com/blog/notes-from-the-lab/business-logic-in-the-database-yes-or-no-it-depends). [tweet](https://twitter.com/lukaseder/status/1107268462919979008). [8](https://softwareengineering.stackexchange.com/questions/194446/how-much-business-logic-should-the-database-implement). [reddit](https://www.reddit.com/r/programming/comments/41pks0/business_logic_in_the_database_yes_or_no_it/). [9](https://enterprisecraftsmanship.com/2015/11/11/is-sql-a-good-place-for-business-logic/). [10](https://asktom.oracle.com/pls/apex/f?p=100:11:0::::P11_QUESTION_ID:2143974700346554115). [11](https://www.red-gate.com/simple-talk/sql/database-administration/ten-common-database-design-mistakes/). [mf](https://martinfowler.com/articles/dblogic.html).

> The big myth perpetrated by architects who don’t really understand relational database architecture (me included early in my career) is that the more tables there are, the more complex the design will be. 

[feature flags at Twitter](https://twitter.com/DiazCarrete/status/815574080325881856)

[Kubernetes commandments](https://www.youtube.com/watch?v=mKCwpuod7RQ)

[Kafka running on OpenShift4 using Ceph Block Storage](https://medium.com/@karansingh010/https-medium-com-karansingh010-look-mumma-kafka-running-on-openshift4-using-ceph-block-storage-afcc61195894)

[What's next for Kubernetes](https://enterprisersproject.com/article/2019/3/kubernetes-hybrid-cloud-whats-next).

[12 Factors for Cloud Native and Openshift](https://medium.com/@rlackdejr89/12-factors-for-cloud-native-with-openshift-b95e849b55ea).

[Openshift on Azure](https://www.youtube.com/watch?v=w_qpbptv594)

[domain probes](https://martinfowler.com/articles/domain-oriented-observability.html) [hn](https://news.ycombinator.com/item?id=19555452)

[data preparation for predictive machine learning](https://www.infoq.com/articles/challenges-of-data-preparation-for-predictive-maintenance)

[spring high performance batch processing](https://www.infoq.com/presentations/batch-performance-spring-4-1)

[Installing Openshift 4 from start to finish](https://blog.openshift.com/installing-openshift-4-from-start-to-finish/). [Multiple stages within a Kubernetes cluster](https://jaxenter.com/multiple-stages-within-kubernetes-cluster-157036.html).

[Migrating a Retail Monolith to Microservices: Sebastian Gauder at MicroXchg Berlin](https://www.infoq.com/news/2019/04/monolith-microservices-migration). [slides](https://speakerdeck.com/rattakresch/microxchg-2019-a-competitive-food-retail-architecture-with-microservice).

[microservices gone wrong](https://www.youtube.com/watch?v=DlEXHqtj2dA)

[Idempotency - challenges and solutions over HTTP](https://www.ably.io/concepts/idempotency)

[reflections on moving to Kubernetes](https://twitter.com/copyconstruct/status/1118914725050368000). [advanced kubernetes](https://twitter.com/DZone/status/1119133535195914240). [when to use kubernetes](https://twitter.com/danveloper/status/1119208594707185664).

[Bringing up an OpenShift playground in AWS](https://blog.dbi-services.com/bringing-up-an-openshift-playground-in-aws/)

[Should that be a microservice?](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind) [hn](https://news.ycombinator.com/item?id=19708997).

[deploy != release](https://twitter.com/copyconstruct/status/1071510828971520000). [Testing in Production, the safe way](https://medium.com/@copyconstruct/testing-in-production-the-safe-way-18ca102d0ef1). [Deploy != Release (Part 1)](https://blog.turbinelabs.io/deploy-not-equal-release-part-one-4724bc1e726b). [Deploy != Release (Part 2)](https://blog.turbinelabs.io/deploy-not-equal-release-part-two-acbfe402a91c). [Istio Observability with Go, gRPC, and Protocol Buffers-based Microservices](https://itnext.io/istio-observability-with-go-grpc-and-protocol-buffers-based-microservices-d09e34c1255a). [works in staging](https://twitter.com/copyconstruct/status/974530841190608897). [Using Blue-Green Deployment to Reduce Downtime and Risk
](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html). [NoStaging](https://www.youtube.com/watch?v=lD3ZuvLFiDo). [How to Deploy Software with Envoy](https://blog.turbinelabs.io/incremental-blue-green-deploys-fde90b0ebdab). [Reactive REST API Using Spring Boot and RxJava](https://dzone.com/articles/reactive-rest-api-using-spring-boot-and-rxjava-1). 


[Mature Microservices and How to Operate Them](https://www.infoq.com/presentations/microservices-financial-times).

[Reconciling Kubernetes and PCI DSS for a Modern and Compliant Payment System](https://www.infoq.com/news/2019/04/kubernetes-pci-dss-compliance).

[become a better software architect](https://github.com/justinamiller/SoftwareArchitect)



[Eoin Woods on Democratising Software Architecture at ICSA 2019](https://www.infoq.com/news/2019/04/ICSA-2019-Software-Architecture)

> Software architecture is still needed because stakeholders are still around, we need to decide on design tradeoffs and we have several cross cutting concerns in software. In practice, what happens nowadays is having more empowered cross-functional teams and using more lightweight descriptions for architecture than in the past. Difficult to understand and evolve architecture diagrams are now replaced by lightweight C4 and Architecture Decision Records diagrams. Code static and runtime analyses combined with informal documentation in the form of Wiki or powerpoint documents can substitute complex static documents. Tools like sonarqube for static code analysis or jaeger, zipkin, ELK, prometheus/grafana and NewRelic for distributed monitoring and tracing services in production can give an accurate and real time view of code and its architecture.


[Architecture decision record](https://github.com/joelparkerhenderson/architecture_decision_record)

[Drinking from the stream](https://twitter.com/mkheck/status/1121912122903027712). [slides](https://speakerdeck.com/mkheck/bebiendo-del-stream-como-usar-las-plataformas-de-mensajeria-para-escalamiento-y-rendimiento).

[Streaming IoT Data and MQTT Messages to Apache Kafka](https://dzone.com/articles/streaming-iot-data-and-mqtt-messages-to-apache-kaf).

[distributed tracing](https://jaxenter.com/distributed-tracing-serverless-thompson-158312.html)

[DDD Ports and Adapters with Onion architecture, what goes where?](https://stackoverflow.com/questions/52321971/ddd-ports-and-adapters-with-onion-architecture-what-goes-where)

> What is left inside a Hexagon is a logic to gather external data, call a decision maker and process result. 

[Layers, Onions, Ports, Adapters: it's all the same](https://blog.ploeh.dk/2013/12/03/layers-onions-ports-adapters-its-all-the-same/)

> I've put the UI components (the orange boxes) and the Data Access components (the blue boxes) in the same laye

[DDD, Hexagonal, Onion, Clean, CQRS, … How I put it all together](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)

> the typical application flow goes from the code in the user interface, through the application core to the infrastructure code, back to the application core and finally deliver a response to the user interface.

> while the CLI console and the web server are used to tell our application to do something, the database engine is told by our application to do something

> The adapters that tell our application to do something are called Primary or Driving Adapters while the ones that are told by our application to do something are called Secondary or Driven Adapters.

[Cockburn on Hexagonal Architecture](https://web.archive.org/web/20180822100852/http://alistair.cockburn.us/Hexagonal+architecture)

> The ports and adapters pattern is deliberately written pretending that all ports are fundamentally similar. That pretense is useful at the architectural level. In implementation, ports and adapters show up in two flavors, which I’ll call ‘’primary’’ and ‘’secondary’’, for soon-to-be-obvious reasons. They could be also called ‘’driving’’ adapters and ‘’driven’’ adapters.

[good description of ports and adapters](https://softwarecampament.wordpress.com/portsadapters/)

> Asymmetry: Configurable Dependency implementation is different for each side. In the driver side, the application doesn’t know about which adapter is driving it. But in the driven side, the application must know which driven adapter it must talk to.

[Isn't this just a layered architecture with a different name and drawn differently?](https://stackoverflow.com/a/29583641/1364288). [Onion vs. N-Layered Architecture](https://stackoverflow.com/questions/28021807/onion-vs-n-layered-architecture?rq=1). [hexagonal architecture with spring data](https://stackoverflow.com/questions/46509252/hexagonal-architecture-with-spring-data?rq=1). [video](https://www.youtube.com/watch?v=_Js-GEqB-8I).

[The Evolution of Comcast’s Architecture Guild](https://www.infoq.com/articles/architecture-guild-800-friends)

[Application Integration for Microservices Architectures: A Service Mesh Is Not an ESB](https://www.infoq.com/articles/application-integration-service-mesh)

[Craftconf architecture talk](https://twitter.com/martinfowler/status/1128661759701680128)

[Real-time Data Processing using Redis Streams and Apache Spark Structured Streaming](https://www.infoq.com/articles/data-processing-redis-spark-streaming)

[majestic modular monoliths](https://jaxenter.com/majestic-modular-monoliths-158593.html)

[How Netflix Thinks of DevOps](https://www.youtube.com/watch?v=UTKIT6STSVM)

[How to Move Beyond a Monolithic Data Lake to a Distributed Data Mesh](https://martinfowler.com/articles/data-monolith-to-mesh.html). [tweet](https://twitter.com/martinfowler/status/1130462303378432000)

[cloud native apps](https://twitter.com/kennybastani/status/1130276404820529153)

[clean code, direct style](https://twitter.com/dan_abramov/status/1130951861123657730)

> code with few possible control flow combinations, direct style (can always trace what connects to what), doesn’t violate grep test, comments explain why.

[FRP can help increase code cohesion](https://medium.com/@cdsmithus/building-and-debugging-frp-with-codeworld-and-reflex-a912083e66c1)

[Lessons Learned Replacing a DI Framework in a Legacy Codebase](https://twitter.com/_thunk_/status/1131905316461961217)

[DI composition root](https://labs.tadigital.com/index.php/2018/12/14/dependency-injection-implementing-using-composition-root/). [What is a composition root in the context of Dependency Injection](https://stackoverflow.com/questions/6277771/what-is-a-composition-root-in-the-context-of-dependency-injection). [more](https://softwareengineering.stackexchange.com/questions/359064/how-to-reuse-parts-of-dependency-injection-composition-root/359070). [more](https://softwareengineering.stackexchange.com/questions/343493/dependecy-injection-and-composition-root). [more](https://visualstudiomagazine.com/articles/2014/06/01/how-to-refactor-for-dependency-injection.aspx). [more](https://medium.com/@cfryerdev/dependency-injection-composition-root-418a1bb19130). [more](https://freecontent.manning.com/dependency-injection-in-net-2nd-edition-understanding-the-composition-root/). [Clean Composition Roots with Pure Dependency Injection (DI)](https://www.dotnetcurry.com/patterns-practices/1285/clean-composition-roots-dependency-injection). [Are We Just Moving the Coupling?](https://jeremybytes.blogspot.com/2013/03/dependency-injection-composition-root.html)

[Microservices, Apache Kafka, and domain-driven design](https://www.confluent.io/blog/microservices-apache-kafka-domain-driven-design)

[91 global variables in Excel that were protected by one spin lock. No one could unravel the hairball](https://twitter.com/schrockn/status/1131965852662657024)

[A Service Mesh Is Not an ESB](https://www.infoq.com/articles/application-integration-service-mesh/)

> A service mesh is only meant to be used as infrastructure for communicating between services, and developers should notbe building any business logic inside the service mesh.

[Restoring Confidence in Microservices: Tracing That's More Than Traces](https://www.youtube.com/watch?v=Wg_C4O0IhkI)

[The Potential for Using a Service Mesh for Event-Driven Messaging](https://www.infoq.com/articles/service-mesh-event-driven-messaging/)

[Cloud Functions](https://www.reddit.com/r/haskell/comments/bvfj2e/brave_new_world_tales_of_purescript_and_haskell/)

[Aggregating REST and Real-Time Data Sources](https://dzone.com/articles/aggregating-rest-and-real-time-data-sources)

[Maintainable ETLs](https://multithreaded.stitchfix.com/blog/2019/05/21/maintainable-etls/). [hn](https://news.ycombinator.com/item?id=20058267)

[USE THE MOST PRODUCTIVE STACK YOU CAN GET](http://adambien.blog/roller/abien/entry/use_the_most_productive_stack). [JAVA'S JOB LISTINGS, JWT, KAFKA, SERVERLESS, STREAMING, JARS IN WARS, THREADS, CODE COVERAGE--63RD AIRHACKS.TV](http://adambien.blog/roller/abien/entry/java_s_job_listings_jwt)

[microfrontends](https://news.ycombinator.com/item?id=20148308)

[cloud transactions](https://www.infoq.com/articles/cloud-transactions-dahan/)

[the state of Java relational persistence](https://www.youtube.com/watch?v=WSjj-IhBiSY). [slides](https://speakerdeck.com/maciejwalkowiak/the-state-of-java-relational-persistence). [Spring Data JPA from 0-100 in 60 Minutes](https://www.youtube.com/watch?v=kJst_Tsl9cw)

[TRANSACTIONS, J2EE, JAVA EE, JAKARTA EE, MICROPROFILE AND QUARKUS](http://adambien.blog/roller/abien/entry/transactions_j2ee_java_ee_jakarta)

[temporal modelling](http://videos.ncrafts.io/video/339925511)

[regarding bad internal technology](http://www.smashcompany.com/business/why-are-large-companies-so-difficult-to-rescue-regarding-bad-internal-technology). [HN](https://news.ycombinator.com/item?id=20260114).

[Fast key-value stores: An idea whose time has come and gone](https://ai.google/research/pubs/pub48030). [hn](https://news.ycombinator.com/item?id=20262235)

[Getting value out of your monad](https://www.youtube.com/watch?v=F9bznonKc64)

[some best (?) practices](https://twitter.com/dan_abramov/status/1144896647505297413)

[the Challenges of Operationalizing Microservices](https://www.infoq.com/presentations/challenges-operationalizing-microservices/)

[Mistakes we made adopting event sourcing](http://natpryce.com/articles/000819.html)

> And if you store events with both an event_timestamp and effective_timestamp, you get bi-temporal state for free too.
Invaluable when handing a time series of financial events subject to adjustments and corrections. For instance, backdate interest adjustments due to misbooked payments, recalculate a derivatives trade if reported market data was initially incorrect, calculate adjustments to your business end of month P&L after correcting errors from two months ago.

[as time goes by - technical challenges of bi-temporal Event Sourcing](https://vimeo.com/275529977). [same talk](https://www.youtube.com/watch?v=xzekp1RuZbM). [event sourcing with bi-temporal data](https://groups.google.com/forum/#!topic/dddcqrs/3gPU6rSZf8M)

[The evolution of the Shopify codebase](https://www.youtube.com/watch?v=ISYKx8sa53g)

[forging a functional enterprise](https://www.youtube.com/watch?v=n5S3hScE6dU)

[Feature Flags and Test-Driven Design: Some Practical Tips](https://www.grahamlea.com/2019/05/feature-flags-tdd-practical-tips/)

[Design Techniques for Building #Streaming Data, Cloud-Native Applications](https://twitter.com/lightbend/status/1146861251915632640)

[lots of lambdas](https://twitter.com/_msw_/status/1150276665651544064). [tweet](https://twitter.com/copyconstruct/status/1150652648397213697).

[How to get along with HATEOAS](https://www.youtube.com/watch?v=nMHJT2yn4pc)

[Von Service-orientierten Architekturen (SOA) zu DDD und Microservices](https://www.youtube.com/watch?v=2lEz4An4quQ)

[When we try to force a service decomposition that isn't really there, we freeze today's technical design into an organizational design](https://twitter.com/keithmadams/status/1150852201293598722)

[Updating Materialized Views and Caches Using Kafka](https://zcox.wordpress.com/2017/01/16/updating-materialized-views-and-caches-using-kafka/)

[the good parts of aws](https://news.ycombinator.com/item?id=20545561)

[Event-sourcing at Nordstrom: Part 2](https://medium.com/tech-at-nordstrom/event-sourcing-at-nordstrom-part-2-f64c416d1885)

[apache kafka tutorials](https://www.confluent.io/blog/announcing-apache-kafka-tutorials)

[TEMPORAL MODELLING](http://videos.ncrafts.io/video/339925511)

[envers vs. debezium](https://twitter.com/dr_pompeii/status/1164196878034116610)

[Software Architecture Guide](https://news.ycombinator.com/item?id=20786448)

[How To Keep the Layers of your Spring App Separate using Integration Tests
](https://www.youtube.com/watch?v=YyE8fyYJsbE&index=1&list=PLjXUjSTUHs0SBkPlUEnkXcDqQKlyUOyAS&t=105s)

[MySQL CDC with Apache Kafka and Debezium](https://blog.clairvoyantsoft.com/mysql-cdc-with-apache-kafka-and-debezium-3d45c00762e4)

[Message transformations for change data capture](https://twitter.com/gunnarmorling/status/1166728691025625088)

[Modern applications at AWS](https://www.allthingsdistributed.com/2019/08/modern-applications-at-aws.html)

[Dependency Management and Versioning With a Maven Multi-Module Project](https://dzone.com/articles/maven-multi-module-project-with-versioning)

[From PHP to transactions - airhacks](http://adambien.blog/roller/abien/entry/from_php_to_transactions_airhacks)

[perhaps not a good idea](https://twitter.com/jbogard/status/1173089706525057024)

[what microservices are](https://twitter.com/gunnarmorling/status/1173280755985899522)

[performance matters](https://www.reddit.com/r/programming/comments/d4k5x5/performance_matters_by_emery_berger_strange_loop/)

[Package by feature or by layer](https://www.reddit.com/r/java/comments/d38xrc/most_developers_package_by_layer_have_you_tried/)

[hexagonal architecture in practice](https://www.youtube.com/watch?v=sOaS83Ir8Ck) [more](https://www.youtube.com/watch?v=lJT0aZbrWUo) [more](https://www.youtube.com/watch?v=xNWFy8t2m_Y)

[intimidated by the sheer breadth of #DDD](https://twitter.com/odrotbohm/status/1176160920357285891)

[DDDTrouble](https://twitter.com/deanwampler/status/1177977002734899201)

["Building audit logs with change data capture and stream processing"](https://twitter.com/gunnarmorling/status/1179062410134638594)

[you can't have a rollback button](https://twitter.com/theBrc007/status/1180178601599213573). [Rolling Forward and other Deployment Myths](http://swreflections.blogspot.com/2011/10/rolling-forward-and-other-deployment.html)

[Debezium resources](https://debezium.io/documentation/online-resources/)

[software archeology](https://twitter.com/SusanPotter/status/1180803724068954112)

[CDC, @debezium Streaming and  @apachekafka an http://airhacks.fm episode](https://twitter.com/AdamBien/status/1183374066268459008)

[How many storage devices does a workload require?](http://smalldatum.blogspot.com/2019/10/how-many-storage-devices-does-workload.html)

[Battle of the circuit breakers](https://twitter.com/nicolas_frankel/status/1187670506809548801)

[Streaming Database Changes with Debezium by Gunnar Morling](https://www.youtube.com/watch?v=IOZ2Um6e430) [slides](https://speakerdeck.com/gunnarmorling/practical-change-data-streaming-use-cases-with-apache-kafka-and-debezium?slide=53)

[CQRS](https://www.sderosiaux.com/articles/2019/08/29/cqrs-why-and-all-the-things-to-consider/)

[Kafka Streams: Topology and Optimizations](https://www.sderosiaux.com/articles/2019/08/07/kafka-streams-topology-and-optimizations/)

[Build your own X](https://github.com/danistefanovic/build-your-own-x)

[How to sleep at night having a cloud service: common Architecture Do's](https://danielsada.tech/blog/cloud-services-dos/)

["Stop Mapping Stuff in Your Middleware"](https://twitter.com/lukaseder/status/1194531255163015170) Logic in the database vs. logic in the application

[The dark side of events](https://www.youtube.com/watch?v=ev5k51AxZbI). [Finding your service boundaries](https://www.youtube.com/watch?v=jdliXz70NtM). [Monolith Decomposition Patterns](https://www.youtube.com/watch?v=64w1zbpHGTg). [the usefulness of pre-allocating ids at the beginning](https://youtu.be/jdliXz70NtM?t=905). [Event-Driven Microservices, the Sense, the Non-sense and a Way Forward](https://www.youtube.com/watch?v=jrbWIS7BH70&feature=youtu.be&list=PLEx5khR4g7PKT9RvuVyQxJLO8CZUJzNMy)

[Kafka stream workshop](https://github.com/antonmry/kafka-streams-workshop) and [slides](https://docs.google.com/presentation/d/1VSkZihLUd2HhVufmF05WfO6NlE3nCG3XXbHTRgyGXjw/edit#slide=id.p).

[The Configuration Complexity Curse – Don’t Be a YAML Engineer](https://www.reddit.com/r/programming/comments/dwt9gj/the_configuration_complexity_curse_dont_be_a_yaml/)

[Step Away From The Database - A step-by-step example of how to introduce Hazelcast into an existing database backed application.](https://github.com/hazelcast/hazelcast-code-samples/tree/master/hazelcast-integration/spring-data-jpa-hazelcast-migration)

[auto-formatting @java source code as part of the build process is a blessing](https://twitter.com/gunnarmorling/status/1199006301008871424)

[Have you built applications following #DDDesign principles, using #JPA for persistence?](https://twitter.com/gunnarmorling/status/1199633652524748801)

[To Domain Driven Design](https://twitter.com/jessitron/status/1201669788285706240)

[Vertical Slices](https://deviq.com/vertical-slices/). [Out with the Onion, in with Vertical Slices](https://medium.com/@jacobcunningham/out-with-the-onion-in-with-vertical-slices-c3edfdafe118). [The Importance of Vertically Slicing Architecture](https://www.youtube.com/watch?v=1bOkyfvoWaw). [Vertical Slice Architecture](https://www.youtube.com/watch?v=SUiWfhAhgQw). [APLICA VERTICAL SLICE](http://xurxodev.com/vertical-scile/). [Why vertical slice architecture is better](https://headspring.com/2019/11/05/why-vertical-slice-architecture-is-better/). [Our architecture is a mess! Are you sure?](https://www.youtube.com/watch?v=ZDpPmK5VQLA)

[Ensuring rollback safety during deployments](https://aws.amazon.com/builders-library/ensuring-rollback-safety-during-deployments/?did=ba_card&trk=ba_card). [Dealing with safely rolling forward *and* rolling back stateful services isn't something people talk about much, if at all. It's the sort of thing that gets hand-waved away.](https://twitter.com/copyconstruct/status/1205806624817872899)

[Java Cloud Native Starter or Kubernetes, OpenShift, istio, Postgres, Clouds, Backend for Frontend, vue.js and MicroProfile](http://adambien.blog/roller/abien/entry/java_cloud_native_starter_with)

[To DTO or not to DTO](https://twitter.com/vlad_mihalcea/status/1207887006883340288)

[Azure for AWS specialists](https://docs.microsoft.com/en-us/azure/architecture/aws-professional/)

[Our setup of Prometheus and Grafana (as of the end of 2019)](https://utcc.utoronto.ca/~cks/space/blog/sysadmin/PrometheusGrafanaSetup-2019)

[A Thought Experiment: Using the ECS Pattern Outside of Game Engines](https://news.ycombinator.com/item?id=21892126). [cache-friendliness](https://news.ycombinator.com/item?id=21674818)

[CSRF, XSS, JWT, REACTIVE DATABASES, TX AND WEBSOCKETS, JSON-B, OPENSHIFT](http://adambien.blog/roller/abien/entry/csrf_xss_jwt_reactive_databases)

[Practical Change Data Streaming Use Cases with Apache Kafka & Debezium](https://www.infoq.com/presentations/data-streaming-kafka-debezium/)

[Qualities of a Highly Effective Architect](https://www.youtube.com/watch?v=vTq5mBe7s7c)

[Plumbing At Scale](https://engineering.grab.com/plumbing-at-scale)

[END-TO-END ARGUMENTS IN SYSTEM DESIGN](http://web.mit.edu/Saltzer/www/publications/endtoend/endtoend.pdf)

[How I write backends](https://github.com/fpereiro/backendlore). [hn](https://news.ycombinator.com/item?id=22106482)

[The Many Faces of Modularity](https://www.youtube.com/watch?v=SfW9w-FogeE&feature=emb_logo)

[3 database architectures](https://news.ycombinator.com/item?id=22151409)

[Modular Monolithic Architecture](https://www.infoq.com/news/2020/01/monolith-architectural-drivers/)

[Monoliths are the future](https://news.ycombinator.com/item?id=22193383)

[2020 Predictions](http://adambien.blog/roller/abien/entry/2020_predictions)

[The Let It Crash Philosophy Outside Erlang](http://stratus3d.com/blog/2020/01/20/applying-the-let-it-crash-philosophy-outside-erlang/)

[Scaling to 100k Users](https://alexpareto.com/scalability/systems/2020/02/03/scaling-100k.html). [complexity](https://lobste.rs/s/ggdy4h/fractals_complexity)

[Data Modernization for Spring-based Microservices](https://www.infoq.com/presentations/spring-microservices-scalability/)

[Why did disabling hyperthreading make my server slower?](https://serverfault.com/questions/1005612/why-did-disabling-hyperthreading-make-my-server-slower)

[Modularity does not have to be fancy. It could be as simple as using DDD and intelligent package naming](https://twitter.com/reza_rahman/status/1236035575913869315)

[Testing Microservices: an Overview of 12 Useful Techniques - Part 1](https://www.infoq.com/articles/twelve-testing-techniques-microservices-intro/)

[Data-oriented architecture](https://news.ycombinator.com/item?id=22519974)

[git-flow](https://nvie.com/posts/a-successful-git-branching-model/) vs [GitHub flow](https://guides.github.com/introduction/flow/)

> This is not the class of software that I had in mind when I wrote the blog post 10 years ago. If your team is doing continuous delivery of software, I would suggest to adopt a much simpler workflow (like GitHub flow) instead of trying to shoehorn git-flow into your team.

> If, however, you are building software that is explicitly versioned, or if you need to support multiple versions of your software in the wild, then git-flow may still be as good of a fit to your team as it has been to people in the last 10 years. In that case, please read on.

> Branching is a core concept in Git, and the entire GitHub flow is based upon it. There's only one rule: anything in the master branch is always deployable.

[Ready for changes with Hexagonal Architecture | Netflix Tech Blog](https://www.reddit.com/r/programming/comments/fgkllr/ready_for_changes_with_hexagonal_architecture/)

[Re-architecting 2-tier to 3-tier](https://www.youtube.com/watch?v=AQJYLGg1JCk&feature=emb_logo)

[Builders, fluent builders](https://twitter.com/ploeh/status/1238093241523802115)

[Your database as an API](https://lobste.rs/s/nbyzgm/your_database_as_api)

[becoming an architect](https://www.youtube.com/watch?v=v_nhv6aY1Kg)

GOTO 19 [ "Good Enough" Architecture ](https://www.youtube.com/watch?v=PzEox3szeRc). [ Monolith Decomposition Patterns • Sam Newman](https://www.youtube.com/watch?v=9I9GdSQ1bbM) [ Building Resilient Frontend Architecture • Monica Lent](https://www.youtube.com/watch?v=TqfbAXCCVwE)

[Systems design for Advanced Beginners](https://robertheaton.com/2020/04/06/systems-design-for-advanced-beginners/)

[ humble guide to database schema design ](https://news.ycombinator.com/item?id=22806142)

["API-first"](https://twitter.com/stilkov/status/1250355396864176132)

[Beyond the Distributed Monolith](https://www.infoq.com/presentations/bbc-distributed-monolith-microservices/)

[Should services always return DTOs, or can they also return domain models?](https://stackoverflow.com/questions/21554977/should-services-always-return-dtos-or-can-they-also-return-domain-models). [Service layer returns DTO to controller but need it to return model for other services](https://softwareengineering.stackexchange.com/questions/400953/service-layer-returns-dto-to-controller-but-need-it-to-return-model-for-other-se). [Pass DTO to service layer](https://stackoverflow.com/questions/20092440/pass-dto-to-service-layer). [Map DTOs and Models within the Service Layer due to a missing Business Layer](https://codereview.stackexchange.com/questions/180528/map-dtos-and-models-within-the-service-layer-due-to-a-missing-business-layer). [Entity To DTO Conversion for a Spring REST API](https://www.baeldung.com/entity-to-and-from-dto-for-a-java-spring-application). [LocalDTO (2004)](https://martinfowler.com/bliki/LocalDTO.html)

> Not only you could pass DTO objects to Service Layer, but you should pass DTO objects instead of Business Entities to Service Layer.

> Your service should receive DTOs, map them to business entities and send them to the repository. It should also retrieve business entities from the repository, map them to DTOs and return the DTOs as reponses. So your business entities never get out from the business layer, only the DTOs do.

> Some people argue for them as part of a Service Layer API because they ensure that service layer clients aren't dependent upon an underlying Domain Model. While that may be handy, I don't think it's worth the cost of all of that data mapping. As my contributor Randy Stafford says in P of EAA "Don't underestimate the cost of [using DTOs].... It's significant, and it's painful - perhaps second only to the cost and pain of object-relational mapping".

> Let's now look at a service level operation – which will obviously work with the Entity (not the DTO)

>  @GetMapping
>     @ResponseBody
>     public List<PostDto> getPosts(...) {
>         //...
>         List<Post> posts = postService.getPostsList(page, size, sortDir, sort);
>         return posts.stream()
>           .map(this::convertToDto)
>           .collect(Collectors.toList());
>     }

[service layer (old)](https://martinfowler.com/eaaCatalog/serviceLayer.html)

> Enterprise applications typically require different kinds of interfaces to the data they store and the logic they implement: data loaders, user interfaces, integration gateways, and others. Despite their different purposes, these interfaces often need common interactions with the application to access and manipulate its data and invoke its business logic. The interactions may be complex, involv-ing transactions across multiple resources and the coordination of several responses to an action. Encoding the logic of the interactions separately in each interface causes a lot of duplication.

[Presentation Model (old)](https://martinfowler.com/eaaDev/PresentationModel.html)

[ON DTOS (old)] much conflicting information!

> DTOs are only created when their structure significantly differs from the that of the entity. In all other cases the entity itself is used. The cases when you don’t want to show some fields (especially when exposing via web services to 3rd parties) exist, but are not that common. This can sometimes be handled via the serialization mechanism – mark them as @JsonIgnore or @XmlTransient for example

> Don’t use the mappers/entity-to-dto constructors in controllers, use them in the service layer. The reason DTOs are used in the first place is that entities may be ORM-bound, and they may not valid outside a session (i.e. outside the service layer).

[performance of Java mapping frameworks](https://www.baeldung.com/java-performance-mapping-frameworks)

> Creating large Java applications composed of multiple layers require using multiple models such as persistence model, domain model or so-called DTOs. Using multiple models for different application layers will require us to provide a way of mapping between beans.

> Dozer is a mapping framework that uses recursion to copy data from one object to another.  The framework is able not only to copy properties between the beans, but it can also automatically convert between different types.

sooo subsetting and type conversions are an important part of mapping frameworks?

[to DTO or not to DTO](http://guntherpopp.blogspot.com/2010/09/to-dto-or-not-to-dto.html)

[DTO : Hipster Ou Dépassé ?](https://www.infoq.com/fr/articles/dto-hipster-ou-depasse/)

[One of the most common uses of the #DTO pattern is decoupling the presentation layer from #JPA entities.](https://twitter.com/JPABuddy/status/1435187332177661955). [New Post: The DTO Pattern (Data Transfer Object)](https://twitter.com/baeldung/status/1434214807817932810).

[The magic behind the Dependency Injection of Quarkus](https://twitter.com/AdamBien/status/1253339691270586372)

[Java & SQL - stronger together](https://twitter.com/MarkusWinand/status/1255574331083685889) overview of the lasagna 

[Domain Events Versus Change Data Capture](https://dzone.com/articles/domain-events-versus-change-data-capture)

[From Batch to Streaming to Both](https://www.infoq.com/presentations/skyscanner-streaming/). [Internet of Tomatoes: Building a Scalable Cloud Architecture](https://www.infoq.com/presentations/iot-framework-farmers-sensors/).

[newbie architect](https://news.ycombinator.com/item?id=23152092)

[Software Architecture for Agile Enterprises](https://twitter.com/stilkov/status/1263088258151579648)

[One thing I never liked about ORMs and OGMs: Let the application define the database scheme, indexes or constraints.](https://twitter.com/rotnroll666/status/1266670279394308096)

[Haskell arch](https://twitter.com/mattoflambda/status/1275469469360336896)

[Domain event](https://martinfowler.com/eaaDev/DomainEvent.html)

[Event-Driven Architectures for Spring Developers](https://www.infoq.com/presentations/event-driven-arch-spring/)

[Adoption of Cloud Native Architecture, Part 2: Stabilization Gaps and Anti-Patterns](https://www.infoq.com/articles/cloud-native-architecture-adoption-part2/)

[Things I Wish I’d Known About CSS](https://news.ycombinator.com/item?id=23868355)

[Dividing front end from back end is an antipattern](https://news.ycombinator.com/item?id=23938421) (?)

[Domain-Oriented Microservice Architecture](https://news.ycombinator.com/item?id=23937005)

[For any event-based system, the message structures it exposes to external consumers are its public interface. Evolve their schemas with the same care and attention to backwards compatibility as your synchronous APIs.](https://twitter.com/gunnarmorling/status/1288072124222103553). [cdc breaks encapsulation](https://riccomini.name/kafka-change-data-capture-breaks-database-encapsulation)

[How to design a REST API that can “prompt” the client about long-running operations?](https://softwareengineering.stackexchange.com/questions/414355/how-to-design-a-rest-api-that-can-prompt-the-client-about-long-running-operati)

[Building dashboards for operational visibility](https://aws.amazon.com/builders-library/building-dashboards-for-operational-visibility/)

[Inside the Hidden World of Legacy IT Systems](https://news.ycombinator.com/item?id=24311298).

> I've tackled legacy systems my entire career, and there is a certain art to untying the knot of dependencies, procedures, and expectations.

> It’s painful to see the people who know all the hotkeys and key sequences on an old green terminal suddenly thrust into a world of mouse hunting and clicking. It makes you wonder if new things are really better.

[HLint evolution](https://www.youtube.com/watch?v=lDXyqzcM580)

[Under Deconstruction: The State of Shopify’s Monolith](https://news.ycombinator.com/item?id=24505467)

[To Microservices and Back Again](https://www.infoq.com/presentations/microservices-monolith-antipatterns/) very good.

[Design Microservice Architectures the Right Way (2018)](https://www.youtube.com/watch?v=j6ow-UemzBc)

[Event Sourcing You are doing it wrong (2018)](https://www.youtube.com/watch?v=GzrZworHpIk) See the papers mentioned at the end: [the dark side of event sourcing](https://www.researchgate.net/publication/315637858_The_dark_side_of_event_sourcing_Managing_data_conversion). [versioning in an event sourced system](https://leanpub.com/esversioning/read). 

[Moving BBC Online to the cloud](https://www.bbc.co.uk/blogs/internet/entries/8673fe2a-e876-45fc-9a5f-203c049c9f9c)

[Go in Production – Lessons Learned](https://news.ycombinator.com/item?id=25012115)

[Asynchronous Task Scheduling at Dropbox](https://news.ycombinator.com/item?id=25061901)

If you have the opportunity, please do not build it like this. Referring to the architectural diagram, it is going to be much more efficient for the "Frontend" to persist the task data into a durable data store, like they show, but then the Frontend should simply directly call the "Store Consumer" with the task data in an RPC payload. There is no reason in the main execution path why the store consumers should ever need to read from the database, because almost all tasks can cut-through immediately and be retired. Reading from the database should only need to happen due to restarts and retries of tasks that fail to cut through.

[Terrible Source code](https://news.ycombinator.com/item?id=25186348)

> One of the best, and first, things we did when starting our machine learning platform was to design it using a plugin architecture. There's a lot of scar tissue and horrible experience through our previous ML products we built for enterprise.
Namely, it was extremely hard to onboard new developers to work on the product. They had to understand the whole thing in order to contribute.

[Not Just Events: Developing Asynchronous Microservices](https://www.youtube.com/watch?v=kyNL7yCvQQc). [Creating event-driven microservices: the why, how and what](https://www.youtube.com/watch?v=ksRCq0BJef8).

[Haskell app architecture.](https://twitter.com/taylorfausak/status/1334147384037826561)

[Stored Procedures as a Back End](https://news.ycombinator.com/item?id=25290339)

[sagas - Azure reference architectures](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga). [sagas for consistency](https://www.youtube.com/watch?v=YPbGW3Fnmbc). [2](https://www.youtube.com/watch?v=cpdL73GsM5c). [Not Just Events: Developing Asynchronous Microservices](https://www.youtube.com/watch?v=kyNL7yCvQQc). [Battle-tested event-driven patterns for your Microservices archit](https://www.youtube.com/watch?v=jSpwRnyYwII&feature=emb_logo). [Opportunities and Pitfalls of Event-driven Utopia
](https://www.youtube.com/watch?v=jjYAZ0DPLNM)

[Clean Architecture Boundaries with Spring Boot and ArchUnit](https://reflectoring.io/java-components-clean-boundaries/)

[Clean Architecture with Spring by Tom Hombergs](https://www.youtube.com/watch?v=cPH5AiqLQTo)

[If All You Have Is a Database, Everything Looks Like a Nail](https://pathelland.substack.com/p/if-all-you-have-is-a-database-everything). [HN](https://news.ycombinator.com/item?id=25330223).

> Soon, there was an established trend that increased the entropy and intertwining of applications and tables.  It became common to have transactional updates across tables for different apps.

> Sometimes people stage read-only copies of tables. These are asynchronously updated from the authoritative owning application. Other applications then “own” the read-only copy in their application set of tables.  

> is only good advice if the tables are application specific data and you don't do microservices in that stupid braindead way that makes it so that everything from the admin panel to data visualization are their own "applications" with their own databases and doing things that would be even the simplest of queries becomes a project in writing what are effectively bad performance joins via random http APIs. IE have a data model and understand where the most painless boundaries are, don't throw up dozens of DBs for the hell of it.

> Look into the patterns of CQRS, event sourcing, flow based programming and materialized views. GraphQL is an interface layer, but you still have to solve for the layer below. API composition only works when the network boundary and services are performance compatible to federate queries. The patterns above can be used to work around the performance concern at a cost of system complexity.

> Don't forget the part where the queries are impossible to test, because you can't spin up real instances of all 15 APIs in a test environment, so all the HTTP calls are mocked and the responses are meaningless!

> A lot of posters here seem to have been deeply burned from microservices designed along the wrong lines. I mean, sure, it happens. You're going to make mistakes just like you can misjudge how to separate concerns in a set of classes. It shouldn't be an issue to fix it. Maybe some teams focus on pure separation before they have a solid design? Maybe its just a culture of feeling like service boundaries can never change?

> There’s a model of software based around shipping events around, and subscriptions between systems. The purposes of separation are at least a couple important, perhaps you know. Each has a DB, often embedded, that is suitable and materialized from the subscriptions and its own; mutated predictably.

[Software Design for Flexibility](https://news.ycombinator.com/item?id=25322938) book.

[Engineers who participated in originally building a system are often magnitudes faster in fixing bugs and building features that engineers that joined later](https://twitter.com/TomHombergs/status/1336040866272571392).

[logs](https://news.ycombinator.com/item?id=25346851)

> But in practice, the accumulation of cold data on a local disk is where this starts to hurt, particularly if that has to serve read traffic which starts from the beginning of time (i.e your queries don't start with a timestamp range).

> KSQL transforms does help reduce the depth of the traversal, by building flatter versions of the data set, but you need to repartition the same data on every lookup key you want - so if you had a video game log trace, you'd need multiple materializations for (user) , (user,game), (game) etc.

> 1) Write a event recording a _desire_ to checkout. 2) Build a view of checkout decisions, which compares requests against inventory levels and produces checkout _results_. This is a stateful stream/stream join. 3) Read out the checkout decision to respond to the user, or send them an email, or whatever.

> CDC is great and all, too, but there are architectures where ^ makes more sense than sticking a database in front.

> Admittedly working up highly available, stateful stream-stream joins which aren't challenging to operate in production is... hard, but getting better.

[Unpopular opinion: SQL is better than GraphQL](https://twitter.com/rakyll/status/1336528841481674752?s=03). [some good aspects](https://twitter.com/djnemec/status/1336552934629404673). [better for trees and DAGs](https://twitter.com/joakimlundborg/status/1250911822888218625). [level limitation](https://twitter.com/PierB/status/1250919455338659840). [what about using views?](https://twitter.com/simonw/status/1250804038955761664). [another (older) comparative](https://twitter.com/kellabyte/status/1059956838744158213)

> GraphQL is better when what you are requesting is best expressed as a tree (or a "graph", though only the DAG variety). This is not always the case, but it very often is when building API:s for production use.

> Of course, you *can* express tree structures in table form, but it is not very convenient for clients to consume. In particular if your client is rendering nested component views, what you want is very often something hierarchical.

> performance is more predictable, exactly because the language is more restricted. You can't just join in all the things,  or select billions of rows by accident. The schema dictates what is allowed.

> you can't request a tree structure (eg: a menu with submenus) with an unknown number of levels.

> You don't have to expose your entire schema, instead expose carefully designed SQL views (so you can refactor your tables without breaking your API)

[Lessons Learned from Reviewing 150 Infrastructures](https://www.infoq.com/presentations/150-infrastructures/)

[sharing transactions and persistence contexts across module boundaries -- yea or nay?](https://twitter.com/gunnarmorling/status/1342921546801811459)

[Data architecture vs backend architecture](https://erikbern.com/2019/01/10/data-architecture-vs-backend-architecture.html)

[are queues overkill?](https://twitter.com/rbranson/status/1344382319977590785)

[Bit little guide to message queues](https://news.ycombinator.com/item?id=25591492).

[How we rebuilt the Walmart Autocomplete Backend](https://medium.com/walmartglobaltech/how-we-rebuilt-the-walmart-autocomplete-backend-10efe71d624a)

[good checklist](https://ozataman.medium.com/choosing-haskell-isnt-a-stand-in-for-good-software-design-7d893882f963)

[React created roadblocks in our enterprise app](https://news.ycombinator.com/item?id=25874105). [original link](https://medium.com/better-programming/i-almost-got-fired-for-choosing-react-in-our-enterprise-app-846ea840841c). [Using react in enterprise contexts](https://www.digitalprimates.net/blog/using-react-in-enterprise-contexts-codeitlive/). The "seams" link in that last one is interesting as well.

[Software engineering topics I changed my mind on](https://news.ycombinator.com/item?id=25887373)

[Architecture.md](https://news.ycombinator.com/item?id=26048784). [ADR](https://news.ycombinator.com/item?id=26053498).

[reworking of GHC's errors](https://twitter.com/TechnoEmpress/status/1359130608354668544) nice architectural choice to avoid cyclic dependencies

[The complexity that lives in the GUI](https://news.ycombinator.com/item?id=26131178)

[Why microservices: part 5](https://twitter.com/crichardson/status/1361734093159940098)

[	The Database Inside Your Codebase ](https://news.ycombinator.com/item?id=26160186)

[You probably don’t need a micro-frontend](https://blog.scottlogic.com/2021/02/17/probably-dont-need-microfrontends.html)

[Developing microservices with aggregates](https://www.youtube.com/watch?v=7kX3fs0pWwc)

[Modules, monoliths, and microservices](https://tailscale.com/blog/modules-monoliths-and-microservices/). [hn](https://news.ycombinator.com/item?id=26247052).

[	Why isn't Godot an ECS-based game engine? ](https://news.ycombinator.com/item?id=26284982). [lobsters](https://lobste.rs/s/hzqlgc/why_isn_t_godot_ecs_based_game_engine).

[testing quarkus](https://twitter.com/InfoQ/status/1365771195724029952)

[bbc and serverless](https://twitter.com/danielbryantuk/status/1365327390608621571)

[Capturing Every Change From Shopify’s Sharded Monolith](https://twitter.com/gunnarmorling/status/1370781283207548929)

[Backpressure in Reactive Systems](https://blog.frankel.ch/backpressure-reactive-systems/)

[necessarily microservices but something akin to serverless functions running on a managed platform](https://twitter.com/copyconstruct/status/1371597566593232896?s=03)

[In praise of --dry-run](https://news.ycombinator.com/item?id=27265386)

[Software Architecture Design for Busy Developers](https://massimo-nazaria.github.io/blog/2019/09/05/software-architecture-design-for-busy-developers.html)
 
[kafka](https://twitter.com/themoah/status/1398930689857363973)
  
[The pedantic checklist for changing your data model in a web application](https://rtpg.co/2021/06/07/changes-checklist.html)

[database migrations and continuous delivery](https://spring.io/blog/2021/06/10/a-bootiful-podcast-redgate-technical-lead-for-the-flyway-team-mikiel-agutu-on-database-migrations-and-continuous-delivery)
 
 [	Zero-downtime schema migrations in Postgres using views ](https://news.ycombinator.com/item?id=27531934)
 
 [	Notes on streaming large API responses ](https://news.ycombinator.com/item?id=27632949)
 
 [don't forget structure and then try to remember it](https://twitter.com/lukaseder/status/1410322348029497355)
 
 [Microservices and Cross-Cutting Concerns](https://www.baeldung.com/cs/microservices-cross-cutting-concerns)
 
 [Qualities of a Highly Effective Architect](https://www.youtube.com/watch?v=QeKheNfO3Yg)
 
 [events, not webhooks](https://news.ycombinator.com/item?id=27823109)
 
 [The Database Ruins All Good Ideas](https://lobste.rs/s/nsrhor/database_ruins_all_good_ideas)
 
 [Thinking in Events: From Databases to Distributed Collaboration Software](https://news.ycombinator.com/item?id=27824509)
 
 [On the Evilness of Feature Branching](https://lobste.rs/s/y0kaen/on_evilness_feature_branching_tale_two)
 
 [Changes tend to be made higher up in the stack, ultimately the UI, because that has a lower risk of breaking something else. This gets very messy very fast.](https://news.ycombinator.com/item?id=28128729)
 
 [How much business logic should be allowed to exist in the controller layer?](https://softwareengineering.stackexchange.com/questions/26438/how-much-business-logic-should-be-allowed-to-exist-in-the-controller-layer). [How accurate is “Business logic should be in a service, not in a model”?](https://softwareengineering.stackexchange.com/questions/218011/how-accurate-is-business-logic-should-be-in-a-service-not-in-a-model?rq=1). [Why put the business logic in the model?](https://softwareengineering.stackexchange.com/questions/176639/why-put-the-business-logic-in-the-model-what-happens-when-i-have-multiple-types).
 
 [requirements](https://pm.stackexchange.com/a/7856/35217)
 
 > Soliciting requirements is a iterative process, starting at an abstract level and diving down as you iterate. It is a data pull from the stakeholders; so it is about asking a ton of questions, several different ways, and becoming more tactical as you go along.
 
[Solving the double (quintuple) declaration Problem in GraphQL Applications](https://news.ycombinator.com/item?id=28180472)
 
[Domain services (2012)](https://softwareengineering.stackexchange.com/a/176646/76774). [Services in Domain-Driven Design (DDD)](http://gorodinski.com/blog/2012/04/14/services-in-domain-driven-design-ddd/).
 
> application services which act as a facade. Application services are simple classes which have methods corresponding to use cases in your domain 
 
> When a significant process or transformation in the domain is not a natural responsibility of an ENTITY or VALUE OBJECT, add an operation to the model as standalone interface declared as a SERVICE. Define the interface in terms of the language of the model and make sure the operation name is part of the UBIQUITOUS LANGUAGE. Make the SERVICE stateless.
 
[Retry long-running message processing in case of processing node failure](https://softwareengineering.stackexchange.com/questions/431131/retry-long-running-message-processing-in-case-of-processing-node-failure).
 
[Are Repositories implementations part of my domain? Should repositories have SQL queries?](https://stackoverflow.com/questions/24679777/are-repositories-implementations-part-of-my-domain-should-repositories-have-sql)
 
[DDD repositories in application or domain service](https://softwareengineering.stackexchange.com/questions/330428/ddd-repositories-in-application-or-domain-service)
  
[DDD: is it correct for a root aggregate to hold a reference to another root aggregate?](https://softwareengineering.stackexchange.com/questions/328571/ddd-is-it-correct-for-a-root-aggregate-to-hold-a-reference-to-another-root-aggr)

> A commonly accepted good practice is to refer to an AR by storing its ID, not a full reference.

> Nothing outside the AGGREGATE boundary can hold a reference to anything inside, except to the root ENTITY. The root ENTITY can hand references to the internal ENTITIES to other objects, but those objects can use them only transiently, and they may not hold on to the reference. The root may hand a copy of a VALUE OBJECT to another object, and it doesn't matter what happens to it, because it's just a VALUE and no longer will have any association with the AGGREGATE.

> Root ENTITIES have global identity. ENTITIES inside the boundary have local identity, unique only within the AGGREGATE.

[DDD, Aggregate Root and entities in library application scenario](https://softwareengineering.stackexchange.com/questions/408389/ddd-aggregate-root-and-entities-in-library-application-scenario)

> Should I pass here the references to these objects (book and user) instead of ids?


[How is a delete of an aggregate root handled in DDD?](https://stackoverflow.com/questions/8578943/how-is-a-delete-of-an-aggregate-root-handled-in-ddd). [DDD: Aggregates and Deletes](https://stackoverflow.com/questions/54301335/ddd-aggregates-and-deletes). [Don’t Delete – Just Don’t](https://udidahan.com/2009/09/01/dont-delete-just-dont/). [DDD to remove an order item](https://github.com/dotnet-architecture/eShopOnContainers/issues/835). [DDD: Is an aggregate root responsible for deleting its child entities from their repository?](https://softwareengineering.stackexchange.com/questions/370185/ddd-is-an-aggregate-root-responsible-for-deleting-its-child-entities-from-their). [Define one repository per aggregate](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design#define-one-repository-per-aggregate).

> I doubt there is such a thing as "Delete" in your ubiquitous language. Most likely people will call it "archive", "taking out of order", "remove", "out of stock"

> Of course, since then GDPR has become a thing. So you may want to include Forget Me as a domain concept.

> Custom repositories are useful for the reasons cited earlier, and that is the approach for the ordering microservice in eShopOnContainers. However, it isn't an essential pattern to implement in a DDD design or even in general .NET development.

>  I'm really not a fan of repositories, mainly because they hide the important details of the underlying persistence mechanism. It's why I go for MediatR for commands, too. I can use the full power of the persistence layer, and push all that domain behavior into my aggregate roots. I don't usually want to mock my repositories – I still need to have that integration test with the real thing. Going CQRS meant that we didn't really have a need for repositories any more. 

[Specification pattern: C# implementation](https://enterprisecraftsmanship.com/posts/specification-pattern-c-implementation/). [tweet](https://twitter.com/ploeh/status/1429533996652933122).

[Is domain driven design an anti-SQL pattern?](https://softwareengineering.stackexchange.com/questions/389981/is-domain-driven-design-an-anti-sql-pattern). [Read Models vs Write Models](https://cascadefaliure.vocumsineratio.com/2019/04/read-models-vs-write-models.html).

> These days, you are likely to see reads (queries) handled differently than writes (commands). In a system with a complicated query, the query itself is unlikely to pass through the domain model (which is primarily responsible for maintaining the consistency of writes).

> we'll design a data model optimized around the reads, and a query of that data model will usually take a code path that does not include the domain model

[What is the CQRS pattern?](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs). [HN](https://news.ycombinator.com/item?id=13339972).

[Event Sourcing: Lessons on failure](https://cascadefaliure.vocumsineratio.com/2018/10/event-sourcing-lessons-on-failure-part.html)

[Designing the Ledgers API with Optimistic Locking](https://www.moderntreasury.com/journal/designing-ledgers-with-optimistic-locking)

[Patterns of Legacy Displacement](https://martinfowler.com/articles/patterns-legacy-displacement/)

[Hexagonal architecture in Rust #1](https://lobste.rs/s/5xfrel/hexagonal_architecture_rust_1)

[Enterprise Software Projects killed the Software Developer](https://news.ycombinator.com/item?id=28355502)

[Design Patterns, Empathy, and Reading Complex Code](https://understandlegacycode.com/blog/legacy-of-socrates-6th-edition/)

[all data relationships become many-to-many over time](https://news.ycombinator.com/item?id=28491331)

[Indirection adds cognitive load. Abstraction reduces it.](https://twitter.com/jbrains/status/1437036779295674373)

[annotation-free Spring](https://blog.frankel.ch/annotation-free-spring/)

[usually there are many error cases and 1 happy case so the bulk of time and code is dedicated to the errors](https://news.ycombinator.com/item?id=28555806)

[Keep IDs internal with REST](https://twitter.com/ploeh/status/1439838561734365185?s=03)

[Practical Frontend Architecture](https://news.ycombinator.com/item?id=28590879)

[Git Flow is a bad idea](https://www.youtube.com/watch?v=_w6TwnLCFwA)

[Data, objects, and how we're railroaded into poor design](https://www.tedinski.com/2018/01/23/data-objects-and-being-railroaded-into-misdesign.html)

[Database-driven realtime architectures](https://ably.com/blog/database-driven-realtime-architectures-serverless-editable-chat-app-part-2)

[API Design Principles and Process at Slack](https://twitter.com/InfoQ/status/1447549246509568001)

[frameworks yay or nay](https://news.ycombinator.com/item?id=28920095)

[The "return a command" trick](https://www.haskellforall.com/2021/10/the-return-command-trick.html). [always be composing](https://www.youtube.com/watch?v=3oQTSP4FngY).

[Spring for Architects](https://www.youtube.com/watch?v=e3kgfcO0af4)

[exploratory refactoring](https://victorrentea.ro/blog/exploratory-refactoring/) 

[Why and how to use service injection in Node.js](https://news.ycombinator.com/item?id=29047685)

[Reducing complexity by integrating through the database](https://news.ycombinator.com/item?id=29093896)

[Azure Architecture Center](https://docs.microsoft.com/en-us/azure/architecture/). [CQRS](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs). [Geode](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs). 

[Anti-Patterns to Avoid in Lambda Based Apps](https://blog.basimhennawi.com/5-anti-patterns-to-avoid-in-lambda-based-apps). [hn](https://news.ycombinator.com/item?id=29092390)

[The strong and weak forces of architecture](https://martinfowler.com/articles/strong-weak-arch.html) . [hn](https://news.ycombinator.com/item?id=29180428)

> In our context the lines separating what should be domain-specific boundaries are blurry. 

[micro-commits](https://twitter.com/ploeh/status/1461969368703717378)

[the outbox pattern to the next level & use it for implementing Sagas](https://twitter.com/InfoQ/status/1464677410155241474)

[Engineering Fundamentals Checklist](https://microsoft.github.io/code-with-engineering-playbook/ENG-FUNDAMENTALS-CHECKLIST/). [style guides](https://news.ycombinator.com/item?id=29361004).

[Thinking Architecturally](https://www.youtube.com/watch?v=0qIS92vs33w)

[keep changelog](https://news.ycombinator.com/item?id=29438221)

[You Can't Buy Integration](https://martinfowler.com/articles/cant-buy-integration.html). [hn](https://news.ycombinator.com/item?id=29478375).

[Don't start with microservices – monoliths are your friend](https://news.ycombinator.com/item?id=29576352)

[Scaling productivity on microservices at Lyft](https://eng.lyft.com/scaling-productivity-on-microservices-at-lyft-part-1-a2f5d9a77813). [tweet](https://twitter.com/copyconstruct/status/1478552675293696000).

> “fullstack in a box” doesn’t scale
>  fast, local, native dev environments are indispensable (h/t Tilt)
> staging overrides with Envoy

[Spring drama](https://news.ycombinator.com/item?id=29971182)

[Examining the covidtests.gov architecture](https://adhoc.team/2022/01/18/covidtests-usps-aws-managed-services/).

[getting your data models wrong leads to awful user outcomes](https://twitter.com/JorgeO/status/1483213537254117384)

[UK COVID-19 dashboard built using Postgres and Citus for millions of users](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/uk-covid-19-dashboard-built-using-postgres-and-citus-for/ba-p/3036276)

[DTOs yet again](https://victorrentea.ro/blog/control-your-data-structures/). [And yet again](https://twitter.com/AdamBien/status/1613125106171084801).

[Azure Application Insights](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview).

[Composition over configuration](https://johno.com/composition-over-configuration)

[There's No Reason to Write OpenAPI By Hand](https://apisyouwonthate.com/blog/theres-no-reason-to-write-openapi-by-hand)

[API Design: Don’t expose your JPA entities in your REST API](https://www.youtube.com/watch?v=1O3FyRxDvLY). [post](https://thorben-janssen.com/dont-expose-entities-in-api/). [another post](https://thorben-janssen.com/dont-expose-entities-in-api/).

[I noticed that almost identical UI elements often evolve in completely opposite directions](https://twitter.com/shumovichy/status/1492452330486353923)

[Architecture Advice Process](https://twitter.com/ThomasBetts/status/1493588507394142216)

[Logging at Twitter](https://news.ycombinator.com/item?id=30393683)

[The different types of events in event-driven systems](https://news.ycombinator.com/item?id=30396873)

[Startup tooling: our product management, sales, and marketing stack](https://news.ycombinator.com/item?id=30394218)

[What does Snowflake offer you that you can’t get from Postgres or even an analytics engine like Elasticsearch?](https://news.ycombinator.com/item?id=30394218)

> Pages, Numbers, Keynote and iCloud for collab. 0€ No maintenance.

[System design #architecture for hotel booking apps (Like Airbnb, OYO)](https://twitter.com/VKazulkin/status/1497825991774855168)

[breaking problems into concepts, not into steps](https://twitter.com/dabeaz/status/1498034981825925127). [video](https://www.youtube.com/watch?v=t-IUY6QrJyU).

[What does a 1972 paper have to do with the Single Responsibility Principle?](https://news.ycombinator.com/item?id=30529854)

> it is almost always incorrect to begin the decomposition of a system into modules on the basis of a flowchart

[Why “API-first” might not be a good idea](https://www.youtube.com/watch?v=fNLQiurGQhE). [slides](https://www.innoq.com/de/talks/2022/03/why-api-first-might-not-be-a-good-idea/).

[Typische Architekturfehler](https://www.youtube.com/watch?v=Sr4cfp8KYCU)

[migrations](https://twitter.com/GergelyOrosz/status/1502216949425651712)

[FWA](https://news.ycombinator.com/item?id=30634496)

> After working for the past ~3 years with a microservice oriented architecture, I can only imagine the horrors of having to work on a project built with lambdas

[How to Design Better APIs](https://news.ycombinator.com/item?id=30647784)

> Microsoft's REST API design guidelines are both thorough and there's very little I'd object to.

[Storing UTC is not a silver bullet (2019)](https://news.ycombinator.com/item?id=30659164)

> If you've worked on a distributed team that had members in the UK/EU and the
> USA then you've run into this before when scheduling meetings.  A 10am PDT
> America/Los_Angeles meeting is different from a 6pm BST Europe/London meeting
> which is different from a 5pm GMT meeting and those will jump around by an
> hour depending on time changes. If the bulk of your team is in Seattle then
> you probably want to pick the US timezone for the meeting and not GMT or
> London. If you have a manager in London, though, who sets up the meeting time
> in their local timezone then Seattle employees will notice tomorrow that the
> meeting is a hour later in Seattle than it normally is.

[The hardest thing about engineering is requirements](https://news.ycombinator.com/item?id=30631571)

[Seven Ways to Fail at Microservices](https://www.infoq.com/articles/microservices-seven-fail/)

[Microservices: Why Are We Doing This?](https://news.ycombinator.com/item?id=30758723)

[In defense of simple architectures](http://danluu.com/simple-architectures/). [tweet](https://twitter.com/garybernhardt/status/1512113012781555712).

[If you expose your class names as configuration, it’s easy for refactoring to create breaking changes. ](https://twitter.com/richardstartin/status/1514359414517551113)

[DDD](https://news.ycombinator.com/item?id=31162623)

> the worst I ran into is the DB layer and the unit-of-work pattern. That is, loading an entity from the database, then implementing the domain logic at a high level (in-memory), and then you have to figure out how to translate this into DB updates AND make the whole thing concurrency-safe.

> My own solution was to keep no entity state in memory and translate everything into DB updates immediately. Use DB transactions where needed. You'll need another layer of code to abstract those higher-level DB operations so your domain code isn't littered with DB accesses, but apart from the extra lines-of-code the whole thing becomes very clean IMHO. Problem is, you won't find this solution described anywhere, and you are completely on your own.

> There's a relevant term called "DDD Trilemma" (I like it because it's easy to find back articles on it). It states that you can't have both a pure, complete and performant domain.

[What is a Collection of Aggregates Referred to in Domain Driven Design?](https://softwareengineering.stackexchange.com/questions/306871/what-is-a-collection-of-aggregates-referred-to-in-domain-driven-design)

[DDD: Aggregate Roots](https://stackoverflow.com/questions/2558469/ddd-aggregate-roots)

[DDD: Is an aggregate root responsible for deleting its child entities from their repository?](https://softwareengineering.stackexchange.com/questions/370185/ddd-is-an-aggregate-root-responsible-for-deleting-its-child-entities-from-their). [Don’t Delete – Just Don’t (2009)](https://udidahan.com/2009/09/01/dont-delete-just-dont/). [How is a delete of an aggregate root handled in DDD?](https://stackoverflow.com/questions/8578943/how-is-a-delete-of-an-aggregate-root-handled-in-ddd)

[Where to put Created date and Created by in DDD?](https://stackoverflow.com/questions/12940954/where-to-put-created-date-and-created-by-in-ddd). [DDD: Where should I set modified date and modified by? Repository or application service?](https://stackoverflow.com/questions/37877448/ddd-where-should-i-set-modified-date-and-modified-by-repository-or-application). [Domain model purity and the current time](https://enterprisecraftsmanship.com/posts/domain-model-purity-current-time/).

[Thoughts about Layered Architecture - Mapping efficiently with SQL](https://twitter.com/javahippie/status/1522176560165527553)

[Why billing systems are a nightmare for engineers](https://news.ycombinator.com/item?id=31424450)

[Nginx Modern Reference Architectures](https://news.ycombinator.com/item?id=31436726)

[Flags Are a Code Smell (2014)](https://news.ycombinator.com/item?id=31462229). [The Clean Code Talks -- Inheritance, Polymorphism, & Testing](https://www.youtube.com/watch?v=4F72VULWFvc).

[Locality of Behaviour (LoB) in the context of htmx](https://htmx.org/essays/locality-of-behaviour/)

[don't look for things](https://www.youtube.com/watch?v=RlfLCWKxHJ0).

[Jackson structured programming](https://twitter.com/GabriellaG439/status/1534703908781584384)

> "There are certain close analogies between the methods used for structuring data and the methods for structuring a program which processes that data." (Tony Hoare, Notes on Data Structuring, 1972)

> "if your recursion isn't structural you want a different structure"

[Improving Distributed Caching Performance and Efficiency at Pinterest](https://medium.com/pinterest-engineering/improving-distributed-caching-performance-and-efficiency-at-pinterest-92484b5fe39b).

[#CQRS is not a general purpose style of architecture.](https://twitter.com/tpierrain/status/1546039271676678144)

[How to design better APIs -- 15 language-agnostic, actionable tips on #REST API design](https://twitter.com/gunnarmorling/status/1550014399884283909)

[Dependency validation of a Haskell application](https://thma.github.io/posts/2022-08-07-dependency-validation-of-haskell-applications.html)

> Automating CleanArchitecture dependency validation

[growing Internet services with feature boundaries, data autonomy, cell-based architectures, service dependencies, graceful degradation, unique identifiers, idempotency, SLOs and quotas, and observability](https://twitter.com/rakyll/status/1562504263951011841)

[One Serverless Principle to Rule Them All: Idempotency](https://news.ycombinator.com/item?id=32690073)

[logs vs. tracing](https://lobste.rs/s/schsks/structured_leveled_logging_go_s_standard#c_4oolft). [more](https://dev.to/aspecto/logging-vs-tracing-why-logs-aren-t-enough-to-debug-your-microservices-4jgi). [more](https://epsagon.com/observability/distributed-tracing-vs-logging/). 

> all projects I have been part of have moved to using OpenTelemetry to output traces/spans. We have it configured to output to the console in local development, and in other environments send to an OpenTelemetry collector

> A distributed trace is defined as a collection of spans. A span is the smallest unit in a trace and represents a piece of the workflow in a distributed landscape. It can be an HTTP request, call to a database, or execution of a message from a queue. 

[Building a Framework on top of Spring Boot](https://www.youtube.com/watch?v=1qT__SBWOhA&t=2s)

[9 Puzzles to Convince You You Don't Understand Dependence](https://www.pathsensitive.com/2022/09/bet-you-cant-solve-these-9-dependency.html)

[Undoing the harm of layers](https://nrkbeta.no/2017/04/29/undoing-the-harm-of-layers/). [tweet](https://twitter.com/bjartnes/status/1576826289398300672). [tweet](https://twitter.com/david_whitney/status/1576614587935268865).

[Getting modules right with Domain-driven Design](https://twitter.com/spring_io/status/1576900677305077760). [slides](https://speakerdeck.com/mploed/getting-modules-right-with-domain-driven-design).

[spring dependency injection guide](https://twitter.com/therealdanvega/status/1577110880936161280)

[The Contract-Powered Data Platform](https://buz.dev/blog/the-contract-powered-data-platform)

[Architecting in health tech](https://aws.amazon.com/es/blogs/architecture/lets-architect-architecting-in-health-tech/)

[Haskell Cake How to bake reusable components](https://twitter.com/jjcarett2/status/1579459583554498560)

[Frameworks, yay or nay?](https://berk.es/2022/09/06/frameworks-harm-maintenance/). [hn](https://news.ycombinator.com/item?id=33185383)

> 1. Every sufficiently complex framework-free application contains an ad hoc, informally-specified, bug-ridden, slow implementation of half of a framework.

[Observability with Spring Boot 3](https://spring.io/blog/2022/10/12/observability-with-spring-boot-3). [Tweet](https://twitter.com/MGrzejszczak/status/1580309749215637505?t=EQi2jJXMrZkKAuakmL2J1Q&s=03). [bulding observability](https://www.youtube.com/watch?v=UJA4PGKny2k). [tweet](https://twitter.com/mat4nier/status/1580333644039991298?t=FMWA5LSBsx0yuJW3LWszuQ&s=03)

[Real-World Engineering Challenges #6: Migrations](https://newsletter.pragmaticengineer.com/p/real-world-engineering-challenges). [HN](https://news.ycombinator.com/item?id=33232580).

[Using Record Types to Build Better Domain Models](https://www.youtube.com/watch?v=DyJ4_a84Hrs) 

[Application deployment and testing strategies](https://cloud.google.com/architecture/application-deployment-and-testing-strategies).

[Package by domain/business concert rather than technicalities](https://twitter.com/gunnarmorling/status/1588812750611890176)

[Preemptive Pluralization is (Probably) Not Evil](https://www.swyx.io/preemptive-pluralization)

[Always use closed, open) intervals](https://lobste.rs/s/8i19nz/always_use_closed_open_intervals)

[Vertical Slicing Architectures](https://www.youtube.com/watch?v=H7HWOlANX78). [Horizontal or Vertical Slicing for Agile?](https://www.youtube.com/watch?v=jQg27pFGmWA).

[How event-driven architecture solves modern web app problems](https://twitter.com/gunnarmorling/status/1601980378557911045).

[Structuring Clojure Applications](https://news.ycombinator.com/item?id=34052268)

[Always throw custom exceptions](https://news.ycombinator.com/item?id=34052363)

[Strangling The Monolith: Applied Patterns & Practices From The Trenches](https://www.youtube.com/watch?v=cGcrReJ6FbY). [Refactoring Is Not Just Clickbait](https://www.youtube.com/watch?v=piUesxuZkIQ)

[PostgREST](https://news.ycombinator.com/item?id=34172205)

[modules, not microservices](http://blogs.newardassociates.com/blog/2023/you-want-modules-not-microservices.html) [hn](https://news.ycombinator.com/item?id=34230641)

[Domain modelling in object-oriented and functional programming](https://www.youtube.com/watch?v=yan1YOXvAUM)

[Splitting a monolith into microservices with their own data stores means giving up on foreign keys for ensuring referential integrity.](https://twitter.com/gunnarmorling/status/1611796616104534018)

[Architecture diagrams should be code](https://brianmckenna.org/blog/architecture_code). [lobsters](https://lobste.rs/s/i40mos/architecture_diagrams_should_be_code)

[Overengineering in Onion/Hexagonal Architectures](https://victorrentea.ro/blog/overengineering-in-onion-hexagonal-architectures/)

[local reasoning](https://twitter.com/nipafx/status/1613444693424996352). [thread](https://mail.openjdk.org/pipermail/amber-dev/2022-November/007580.html)

[awesome-infrastructure-questions](https://github.com/dyrector-io/awesome-infrastructure-questions)

[separate view logic and app logi layers](https://twitter.com/ryanflorence/status/1618661815843721216)

[Vertical Slice Architecture, not Layers!](https://www.youtube.com/watch?v=L2Wnq0ChAIA) 

[What is a DDD Aggregate?](https://www.youtube.com/watch?v=zlFqjD2LKlE). [The DDD Starter Modelling Process](https://www.youtube.com/watch?v=qeir72soorI)

[If you have separate packages for dto, model, service, repository, controller, etc you're doing it wrong](https://twitter.com/maciejwalkowiak/status/1622621528385851395). [package-private](https://twitter.com/maciejwalkowiak/status/1622625667836792839).  

[Demystifying Dependence](https://www.youtube.com/watch?v=WA3yRvcCq0U)

[databases in Haskell](https://www.reddit.com/r/haskell/comments/10y8ryt/comment/j7x9nbr/)

[DAOs should usually not start their own transactions](https://twitter.com/gunnarmorling/status/1625095115936088065)

[ArchUnit for Java & guardian for Haskell](https://www.archunit.org/motivation)

[Local-First Web Development](https://localfirstweb.dev/)

[bias, bias, bias](https://twitter.com/gwenshap/status/1625335409017487361)

[If your services are interfaces, implementations end with Impl, and both are public, you're doing it wrong.](https://twitter.com/maciejwalkowiak/status/1631350354246770689). [Message listeners beans play the same role as web controllers](https://twitter.com/maciejwalkowiak/status/1631250938047463426).

[Don't let Event-Driven Architecture buzzwords fool you](https://news.ycombinator.com/item?id=34994439)

[structuring a PR—Go](https://twitter.com/felixge/status/1634270662767329280)

[steel threads](https://news.ycombinator.com/item?id=35090989)

[single methods interfaces in go](https://eli.thegreenplace.net/2023/the-power-of-single-method-interfaces-in-go/)

[an irrational fear of getting layering wrong](https://mastodon.social/@odrotbohm@chaos.social/110057304333359782)

[Your Code Might Not Need State](https://news.ycombinator.com/item?id=35336632)

[The lost art of software design](https://www.youtube.com/watch?v=UzFpFQgeEyc)

[DDD is Overrrated](https://news.ycombinator.com/item?id=26312652). [database illiterate?](https://twitter.com/VaughnVernon/status/1641605323801894913)

[MIT system design course](https://twitter.com/eatonphil/status/1644051606768349184)

[A thinking and recording tool: Decision Records](https://martinfowler.com/articles/scaling-architecture-conversationally.html#adr)

[System design and the cost of architectural complexity (2013)](https://news.ycombinator.com/item?id=35470905)

[engineering elegance squarespace](https://www.youtube.com/watch?v=0u1CnLoewfQ)

[graphQL oops](https://betterprogramming.pub/graphql-from-excitement-to-deception-f81f7c95b7cf) interesting bits about code-first and api-first

[How to Structure Modern Enterprise Java Projects](https://blog.sebastian-daschner.com/entries/structure-modern-enterprise-java-projects). [video](https://www.youtube.com/watch?v=oJ5xCo2vzRA).

[putting proto defined service and RPC boundaries in place even if I'm linking everything into a single binary](https://twitter.com/rakyll/status/1646002715846406145)

[How to Name your Types](https://www.youtube.com/watch?v=qA65QjWCl60)

[In defense of simple architectures](https://lobste.rs/s/oyroj4/defense_simple_architectures)

[simplify](https://twitter.com/VicVijayakumar/status/1652004299075928071). [simplify](https://twitter.com/Carnage4Life/status/1651746258091147264).

[Scaling up the Prime Video audio/video monitoring service and reducing costs](https://news.ycombinator.com/item?id=35811741)

[uuids, ulids, and idempotency at shopify](https://twitter.com/hnasr/status/1657569218609684480)

> When you make a purchase, Shopify guarantees idempotency by having the client uniquely tagging the request using UUID. If you accidentally replay the request and they check if the request exist or not and no-op. 

[repositories & actually switching databases](https://twitter.com/davidfowl/status/1657418789288579073)

[very large javascript applications](https://twitter.com/cramforce/status/1658775915353047042)

[design for copypaste](https://twitter.com/dan_abramov/status/1659348147150245889)

[start with vertical slice](https://twitter.com/BajoranEngineer/status/1659603296217096194)

[yet again hexagonal](https://twitter.com/TotherAlistair/status/1659603989938204672)

[dependency composition](https://martinfowler.com/articles/dependency-composition.html)

[background jobs, in-server?](https://twitter.com/kentcdodds/status/1664367910465466369). [Java JobRunr](https://twitter.com/maciejwalkowiak/status/1664295458099871745)

[Building a b2b SaaS product is 95% forms and background jobs so get really fucking good at those](https://twitter.com/_swanson/status/1664797358301798400)

[Anything can be a message queue if you use it wrongly enough](https://xeiaso.net/blog/anything-message-queue)

[Monitoring is a Pain](https://lobste.rs/s/qiy7if/monitoring_is_pain)

> Let each team own their own Prometheus. 

[AWS multitenancy architectures](https://aws.amazon.com/es/blogs/architecture/lets-architect-multi-tenant-saas-architectures/)

[defining an initial model is comparatively easy](https://twitter.com/gunnarmorling/status/1669746063698276363)

[global state](https://twitter.com/housecor/status/1671545401206353920)

[extension/plugin architectures](https://twitter.com/steveruizok/status/1672926467393564673)

[Amazon Builders' Library](https://twitter.com/g_bonfiglio/status/1673650452846505985)

[Asynchronous Request-Reply pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/async-request-reply)

[how not to write a pipeline](https://cohost.org/tef/post/1764930-how-not-to-write-a). [hn](https://news.ycombinator.com/item?id=36501548).

[Everything that uses configuration files should report where they're located](https://news.ycombinator.com/item?id=36465886)

[threads arch](https://twitter.com/alangrow/status/1677132403553488896)

[one component per file is wrong](https://twitter.com/BHolmesDev/status/1679125597446979589)

[Stick to boring architecture for as long as possible](https://addyosmani.com/blog/boring-architecture/). [tweet](https://twitter.com/addyosmani/status/1682144663149608960).

[An “Order”, “Product” and “Payment” are different things](https://nickjanetakis.com/blog/what-i-learned-about-payment-systems-while-working-at-a-pizza-place)

[don't be clever](https://news.ycombinator.com/item?id=36984695)

[The Physics of Readability](https://loup-vaillant.fr/articles/physics-of-readability)

[Structural Software Design](https://jenkov.com/tutorials/software-design/structural-software-design.html). [video](https://www.youtube.com/watch?v=bj9DoZsu7Ls&list=PLL8woMHwr36HWMaOTIiWNf_fYYkZCHPxo&index=6).

[How architecture diagrams enable better conversations](https://www.unravelled.dev/how-architecture-diagrams-enable-better-conversations/)

[Remix future flags](https://twitter.com/kentcdodds/status/1697219018036596936). [Future Proofing Your Remix App](https://remix.run/blog/future-flags). [API development strategy](https://remix.run/docs/en/main/pages/api-development-strategy).

[architecture tips](https://www.youtube.com/watch?v=wQYRl--58zM)

[Managing Asynchronous Workflows with a REST API](https://aws.amazon.com/es/blogs/architecture/managing-asynchronous-workflows-with-a-rest-api/)

> We implemented this pattern using Amazon API Gateway, Amazon DynamoDB, and AWS Step Functions

> The server creates a new item to represent the report and returns the resource’s URI to the client. In this example, we built a storage-first API using the direct integration between API Gateway and DynamoDB to create the record without writing any code of our own. In addition to the report fields sent by the client, the resource gains a “completed” field to indicate whether the report has been successfully generated.

> Finally, the Lambda function updates the DynamoDB table, marking the report as complete and supplying the S3 URL that the report can be retrieved from.

[How Boundary Control Entity, UML and Components Happened--airhacks.fm podcast](https://adambien.blog/roller/abien/entry/how_boundary_control_entity_uml)

[Dependency Injection, The Best Pattern](https://www.youtube.com/watch?v=J1f5b4vcxCQ). [twitter](https://twitter.com/davidfowl/status/1703296478717038955).

[Principles for building and scaling feature flag systems](https://docs.getunleash.io/topics/feature-flags/feature-flag-best-practices). [hn](https://news.ycombinator.com/item?id=37611136).

[Package by Layer vs Package by Feature](https://www.youtube.com/watch?v=B1d95I7-zsw). [tweet](https://twitter.com/therealdanvega/status/1704867889004564622).

[Database-per-user is the holy grail for multi-tenant SaaS](https://twitter.com/PavelTcholakov/status/1708067192120484213)

[D style](https://news.ycombinator.com/item?id=37748543)

[Top 5 techniques for building the worst microservice system ever](https://www.youtube.com/watch?v=88_LUw1Wwe4)

[Compliance & Regulatory Standards Are NOT Incompatible With Modern Development Best Practices](https://twitter.com/mipsytipsy/status/1709335980333990271)

[separation of concerns](https://twitter.com/jaffathecake/status/1717886846632329317)

[modularity](https://hachyderm.io/@jasongorman@mastodon.cloud/111311911352630518)

[start with a walking skeleton](https://hachyderm.io/@nat@ruby.social/111348115134601487)

[the quest for modularity](https://newcome.wordpress.com/2022/11/28/the-quest-for-modularity/). [hn](https://news.ycombinator.com/item?id=38155926).

[Oh my poor business logic](https://news.ycombinator.com/item?id=38159363)

[don't to this with log files](https://twitter.com/gunnarmorling/status/1727586416413077924). [reddit](https://www.reddit.com/r/dataengineering/comments/180q34j/best_way_to_repartition_json_data_in_s3_bucket/).

[data-oriented development is a lie](https://news.ycombinator.com/item?id=38345843). [lobste.rs](https://lobste.rs/s/xw1qcm/data_driven_development_is_lie)

[Two Tier Architectures are Anachronistic](https://www.tele-task.de/lecture/video/10304/)

[“Change Data Capture Breaks Encapsulation”. Does it, though?](https://www.decodable.co/blog/change-data-capture-breaks-encapsulation-does-it-though)

> The contract of the outbox events is kept separated from the internal data model, allowing you to expose the data in exactly the way you want to expose it. 

> But you may also decide to adjust the types of exposed fields, only expose a subset of all your data attributes—giving you the opportunity to omit any sensitive or implementation-specific attributes—and much more. Having a separate contract allows you to evolve it independently from your internal model, too. Say, you rename a column in one of your tables; it’s a conscious decision then to also rename it in the schema of your outbox events (potentially requiring a new major version of the same), or keep it as is.

> From a procedural perspective, it’s important that the team owning and publishing a data contract can apply changes to the contract without having to synchronize with any event consumers, who perhaps may not even be known to the upstream team. At the same time, any changes to the contract should not break existing consumers—after a schema change they should be able to continue to process a change event stream based on the previous schema known to them. 

> This means data contracts for change event streams should be evolved in a forward compatible way, which allows for the addition of new fields and the removal of optional fields, whereas existing non-optional fields may not be removed.

[Interceptors Are Functions Too](https://gist.github.com/quad/13e9f8b6e88dec1729e30b270ebf22df)

[YAGNI exceptions](https://lukeplant.me.uk/blog/posts/yagni-exceptions/). [You might as well timestamp it](https://changelog.com/posts/you-might-as-well-timestamp-it). [Rule #4: DON'T return arrays as top level responses](https://github.com/stickfigure/blog/wiki/How-to-(and-how-not-to)-design-REST-APIs#rule-4-dont-return-arrays-as-top-level-responses)

[Interceptors are functions, too](https://lobste.rs/s/qlvcpm/interceptors_are_functions_too)

[the choice to move their idempotent UUID4 requests to ULID](https://twitter.com/hnasr/status/1729062666621055366)

[Should you split that file?](https://www.pathsensitive.com/2023/12/should-you-split-that-file.html). [hn](https://news.ycombinator.com/item?id=38489485).

[Stop building databases](https://sqlsync.dev/posts/stop-building-databases/) [hn](https://news.ycombinator.com/item?id=38489307)

[FUNARCH 2023](https://www.functional-architecture.org/events/funarch-2023/)

[What is a cell-based architecture?](https://docs.aws.amazon.com/wellarchitected/latest/reducing-scope-of-impact-with-cell-based-architecture/what-is-a-cell-based-architecture.html)

[Unnecessary layers](https://dzone.com/articles/simplify-java-reducing-unnecessary-layers-and-inte)

[Multi-tenant data isolation with PostgreSQL Row Level Security](https://aws.amazon.com/es/blogs/database/multi-tenant-data-isolation-with-postgresql-row-level-security/). [in Haskell](https://www.reddit.com/r/haskell/comments/18s3901/approaching_multi_tenancy_in_haskell/).

[updated data stack](https://news.ycombinator.com/item?id=38813634)

[architecture antipatterns](https://architecture-antipatterns.tech/)

[package by feature, yet again](https://twitter.com/ryanflorence/status/1749906558069395710). [vertical split](https://twitter.com/TkDodo/status/1749717832642736184). [more](https://twitter.com/TkDodo/status/1749737745587503272). 

[Domain Driven Design and Relational Databases](https://docs.spring.io/spring-data/relational/reference/jdbc/domain-driven-design.html)

[Lessons Learned From Payments Startups](https://pgrs.net/2024/01/26/lessons-learned-from-payemnts-startups/)

[cell architectures](https://twitter.com/gwenshap/status/1752897127863533869). [post](https://www.infoq.com/news/2024/01/doordash-service-mesh/).

[modularity is not about reuse](https://hachyderm.io/@jasongorman@mastodon.cloud/111311911352630518)

[AWS re:Invent 2023 - Application architecture as code (GBL301) - English version](https://www.youtube.com/watch?v=vasvpFRPx9c&list=PLsuboX68NN3DL-sYP16NRyaLFRvSexa_s&index=3)

[Context Control in Go Best practices for handling context plumbing.](https://zenhorace.dev/blog/context-control-go/)

[Go queue on postgres](https://github.com/dataddo/pgq). [   River: A fast, robust job queue for Go and Postgres ](https://news.ycombinator.com/item?id=38349716). [tweet](https://twitter.com/samokhvalov/status/1726699397579493382).

- Every queue is the single postgres table.

- You maintain the table on your own. You can extend it as you need.

[the issue with repositories](https://twitter.com/chrislpenner/status/1755652305058492856)

[(Almost) Every infrastructure decision I endorse or regret after 4 years running infrastructure at a startup](https://lobste.rs/s/pgahrv/almost_every_infrastructure_decision_i). [HN](https://news.ycombinator.com/item?id=39313623)

[Modular Monolith: Is This the Trend in Software Architecture?](https://arxiv.org/abs/2401.11867)

[Give me /events, not webhooks](https://news.ycombinator.com/item?id=27823109)

["Anatomy of a Spring Boot App with Clean Architecture"](https://twitter.com/sergialmar/status/1760594547661279508)

[Why are non-DRY specs more maintainable?](https://lobste.rs/s/mu2c6n/why_are_non_dry_specs_more_maintainable)

[Managing change with Rollout Flags](https://tech.scrive.com/2024-03-19-managing-change-with-rollout-flags/)

[Uncovering the Seams in Mainframes for Incremental Modernisation](https://martinfowler.com/articles/uncovering-mainframe-seams.html).

[Implementing Stripe-like Idempotency Keys in Postgres](https://brandur.org/idempotency-keys)

[All you need is Wide Events](https://lobste.rs/s/4a7sxq/all_you_need_is_wide_events_not_metrics)

[Event Modeling from Beginner to Expert](https://www.youtube.com/watch?v=Pin_B-AbdXE)

[The data model behind Notion's flexibility](https://news.ycombinator.com/item?id=39805744)

[Why I prefer trunk-based development](https://trishagee.com/2023/05/29/why-i-prefer-trunk-based-development/)

[The High-Risk Refactoring](https://news.ycombinator.com/item?id=39735570)

[A Taxonomy Of Data Change Events](https://twitter.com/gunnarmorling/status/1768185698064978033)

[You Don't Need a Dedicated Cache Service – PostgreSQL as a Cache](https://news.ycombinator.com/item?id=39619204)

[Inheriting a C++ codebase](https://news.ycombinator.com/item?id=39549486)

[API design is difficult](https://twitter.com/satnam6502/status/1762166553095852155)

[claim-check pattern](https://twitter.com/dunithd/status/1776240114726846691)

[first steps towards feature flags](https://twitter.com/housecor/status/1781019085062488366)

[code vs. architecture](https://twitter.com/rickasaurus/status/1781872569819230422)

[Always rest?](https://twitter.com/housecor/status/1782764241071546765)

[applications vs. library programming](https://lobste.rs/s/shksoq/good_essays_on_application_vs_library)

[The problem with invariants is that they change over time](https://surfingcomplexity.blog/2024/03/26/the-problem-with-invariants-is-that-they-change-over-time/). [hn](https://news.ycombinator.com/item?id=40112282).

[Design patterns for extracting from REST APIs](https://blog.sequin.io/design-patterns-for-extracting-from-rest-apis/)

[consumer-driven contracts](https://martinfowler.com/articles/consumerDrivenContracts.html). [mastodon](https://hachyderm.io/@odrotbohm@chaos.social/112350905696144423).

[event architectures: orchestration vs. choreography](https://news.ycombinator.com/item?id=40497602)

[Before you try to do something, make sure you can do nothing](https://devblogs.microsoft.com/oldnewthing/20230725-00/?p=108482). [ls](https://lobste.rs/s/ssg6q3/before_you_try_do_something_make_sure_you). 

[Architecturally evident Spring applications with jMolecules](https://www.youtube.com/watch?v=-I7KiV_6f-s)

[not a fan of the hexagon](https://x.com/sivalabs/status/1803756156331982954)

[Why do message queue-based architectures seem less popular now?](https://news.ycombinator.com/item?id=40723302)

[overcomplicated?](https://x.com/sivalabs/status/1804007181752164753). [tweet](https://x.com/1ovthafew/status/1805287714826170721). [Overengineering in Onion/Hexagonal Architectures](https://victorrentea.ro/blog/overengineering-in-onion-hexagonal-architectures/).

[Stop your (business rules) engines](https://lobste.rs/s/isc1qn/stop_your_business_rules_engines)

[return the resource upon PATCH](https://x.com/WarrenInTheBuff/status/1806820934109597775)

[Qualities of a Highly Effective Architect](https://www.youtube.com/watch?v=QeKheNfO3Yg)

[the tomato architecture](https://www.sivalabs.in/tomato-architecture-pragmatic-approach-to-software-design/)

[How to organize large Rust codebases](https://kerkour.com/rust-how-to-organize-large-workspaces)

[vent-driven = Loosely coupled? Not so fast!](https://www.enterpriseintegrationpatterns.com/ramblings/eventdriven_coupling.html). [tweet](https://x.com/ghohpe/status/1814993924974621163)

[Do not pass DTOs to UI components](https://darios.blog/posts/do-not-pass-dtos-to-ui-components)

[Control Flow—The Other Half of Integration Patterns](https://www.enterpriseintegrationpatterns.com/ramblings/queues_control_flow.html)

[DTOs yet again](https://x.com/VaughnVernon/status/1819004089771975164)

[append-only code?](https://x.com/smarr/status/1821857748570546314)

[Queues invert control flow but require flow control](https://x.com/ghohpe/status/1821155314105757779)

[Are You Done Yet? Mastering Long-Running Processes in Modern Architectures](https://www.infoq.com/articles/mastering-long-running-processes/)

[The Perils of Future-Coding](https://lobste.rs/s/gomjcb/perils_future_coding)

[How event-driven architecture solves modern web app problems](https://stackoverflow.blog/2020/03/16/how-event-driven-architecture-solves-modern-web-app-problems/).

[Truth First, or Why You Should Mostly Implement Database First Designs](https://blog.jooq.org/truth-first-or-why-you-should-mostly-implement-database-first-designs/)

[Event-Driven Architectures: Anti-Patterns](https://www.panos.tech/event-driven-2/). [Queues invert control flow but require flow control ](https://news.ycombinator.com/item?id=41195805). [Best practices for delayed actions in event-driven architecture](https://softwareengineering.stackexchange.com/questions/445645/best-practices-for-delayed-actions-in-event-driven-architecture). [Idempotency and ordering in event-driven systems](https://www.cockroachlabs.com/blog/idempotency-and-ordering-in-event-driven-systems/).

[The gains from fixing something are much smaller than the possible losses from breaking something](https://x.com/d_feldman/status/1823424913929068955)

[Using only a Domain Model to persist restaurant table configurations](https://blog.ploeh.dk/2024/08/12/using-only-a-domain-model-to-persist-restaurant-table-configurations/). [tweet](https://x.com/ploeh/status/1822982482452508788).

>  the goal is to being able to design Domain Models unconstrained by serialization concerns, but also being able to format external data unconstrained by Reflection-based serializers

[Modular Monolith: A Primer](https://www.kamilgrzybek.com/blog/posts/modular-monolith-primer)


