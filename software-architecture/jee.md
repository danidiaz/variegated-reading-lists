[Java 9 on Java EE 8 Using Eclipse and Open Liberty](https://dzone.com/articles/java-9-on-java-ee-8-using-eclipse-and-open-liberty)

[JAVA EE 8 ON JAVA 9 - FROM INSTALL TO DEPLOYMENT WITH OPENLIBERTY SERVER](http://adambien.blog/roller/abien/entry/java_ee_8_on_java)

[Build your own open source Eclipse MicroProfile](https://jaxenter.com/open-source-microprofile-145749.html)

[Graceful Shutdown Spring Boot Applications](https://dzone.com/articles/graceful-shutdown-spring-boot-applications)

[How to bootstrap JPA programmatically without the persistence.xml configuration file](https://vladmihalcea.com/how-to-bootstrap-jpa-programmatically-without-the-persistence-xml-configuration-file/)

[Difference Between BeanFactory and ApplicationContext in Spring](https://dzone.com/articles/difference-between-beanfactory-and-applicationcont)

[Build your own open source Eclipse MicroProfile](https://jaxenter.com/open-source-microprofile-145749.html)

[The magic of Spring Data](https://dzone.com/articles/magic-of-spring-data)

[Understanding Jakarta EE: “Modularity is key to faster release cycles”](https://jaxenter.com/understanding-jakarta-ee-series-rahman-147683.html)

[Spring Boot – Best Practices](https://www.e4developer.com/2018/08/06/spring-boot-best-practices/)

[10 Spring Boot Security Best Practices](https://snyk.io/blog/spring-boot-security-best-practices/)

[Deep Dive into JUnit 5 Extension Model](https://www.infoq.com/articles/deep-dive-junit5-extensions)

[Ten Things You Can Do With GraalVM](https://www.youtube.com/watch?v=tEaEAq0L9Pk)

[Java Performance Puzzlers](https://www.youtube.com/watch?v=wgQBz2Ldhvk)

[Exploring Java 9: The Key Parts](https://www.youtube.com/watch?v=Yacu1yUktjY)

[Build a MySQL Spring Boot App Running on WildFly on an Azure VM](https://www.infoq.com/articles/azure-wildfly-spring-boot-app)

[BORING ENTERPRISE JAVA](http://eldermoraes.com/2018/08/31/boring-enterprise-java-airhacks-fm-podcast/)

[JWT and Scalability, JSON-B Configuration, Bulk Data and JAX-RS, EclipseLink, Hibernate and Schema Validation, designing distributed storage applications, Payara Dockerfile explanation](http://adambien.blog/roller/abien/entry/from_tokens_over_storage_systems) [twitter](https://twitter.com/AdamBien/status/1037721019606294529)

[Consumer Driven Contract with Spring Boot](https://medium.com/@caysever/consumer-driven-contract-with-spring-boot-65ab504b529e)

[JDBC in Java, Hibernate, and ORMs: The Ultimate Resource](https://www.databasestar.com/jdbc-in-java/)

[Helidon](https://jaxenter.com/helidon-microservices-interview-kornilov-149734.html)

[Building an offline app from scratch and with web standards only.](https://twitter.com/AdamBien/status/1043783135488606208).

[sts 4](https://spring.io/blog/2018/09/25/spring-tools-4-ga-released)

[kubernetes para desarrolladores java](workshop-04-Kubernetes-para-desarrolladores-Java)

[airhacks](https://twitter.com/AdamBien/status/1046625240359620608)

[A NOTE ON DATA TRANSFER OBJECTS (DTO)S](http://adambien.blog/roller/abien/entry/a_note_on_dtos).

[frameworks for Java application development.

[Mastering Spring framework 5, Part 2: Spring WebFlux](https://www.javaworld.com/article/3288219/spring-framework/mastering-spring-framework-5-part-2-spring-webflux.html).

[Oracle Code One 2018](https://developer.oracle.com/codeone).

[Live-Coding Web Apps (PWAs)—Without Frameworks](https://www.youtube.com/watch?v=SUpnzspMFkI).

[Guide to "Reactive" for Spring MVC Developers](https://www.infoq.com/presentations/spring-reactive-webflux).

[HOW TO STRUCTURE JAKARTA EE APPLICATIONS FOR PRODUCTIVITY WITHOUT BLOAT](http://adambien.blog/roller/abien/entry/how_to_structure_jakarta_ee).

[Designing the infrastructure persistence layer](https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design).

[Can you have multiple transactions within one Hibernate Session?](https://stackoverflow.com/questions/25893476/can-you-have-multiple-transactions-within-one-hibernate-session).

> A hibernate session is more or less a database connection and a cache for database objects. 

> A Session is an inexpensive, non-threadsafe object that should be used once and then discarded for: a single request, a conversation or a single unit of work. 

[How do I get the connection inside of a Spring transaction?](https://stackoverflow.com/questions/11779469/how-do-i-get-the-connection-inside-of-a-spring-transaction).

> The transaction manager is completely orthogonal to data sources. Some transaction managers interact directly with data sources, some interact through an intermediate layer (eg, Hibernate), and some interact through services provided by the container (eg, JTA).

[Class HibernateTransactionManager](https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/orm/hibernate5/HibernateTransactionManager.html#setSessionFactory-org.hibernate.SessionFactory-).

> PlatformTransactionManager implementation for a single Hibernate SessionFactory. Binds a Hibernate Session from the specified factory to the thread, potentially allowing for one thread-bound Session per factory. SessionFactory.getCurrentSession() is required for Hibernate access code that needs to support this transaction handling mechanism, with the SessionFactory being configured with SpringSessionContext.

> Note: To be able to register a DataSource's Connection for plain JDBC code, this instance needs to be aware of the DataSource (setDataSource(javax.sql.DataSource)). The given DataSource should obviously match the one used by the given SessionFactory.

> This transaction manager is appropriate for applications that use a single Hibernate SessionFactory for transactional data access, but it also supports direct DataSource access within a transaction (i.e. plain JDBC code working with the same DataSource). This allows for mixing services which access Hibernate and services which use plain JDBC (without being aware of Hibernate)! Application code needs to stick to the same simple Connection lookup pattern as with DataSourceTransactionManager (i.e. DataSourceUtils.getConnection(javax.sql.DataSource) or going through a TransactionAwareDataSourceProxy).


[Interface Session](http://docs.jboss.org/jbossas/javadoc/7.1.2.Final/org/hibernate/Session.html).

> The main runtime interface between a Java application and Hibernate. This is the central API class abstracting the notion of a persistence service.

> The lifecycle of a Session is bounded by the beginning and end of a logical transaction. (Long transactions might span several database transactions.)

> It is not intended that implementors be threadsafe. Instead each thread/transaction should obtain its own instance from a SessionFactory.

[Class DataSourceUtils](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/jdbc/datasource/DataSourceUtils.html#doGetConnection-javax.sql.DataSource-).

> Is aware of a corresponding Connection bound to the current thread, for example when using DataSourceTransactionManager. Will bind a Connection to the thread if transaction synchronization is active (e.g. if in a JTA transaction).

[Hibernate commit() and flush()](https://stackoverflow.com/questions/14581865/hibernate-commit-and-flush).

> flush() will synchronize your database with the current state of object/objects held in the memory but it does not commit the transaction. So, if you get any exception after flush() is called, then the transaction will be rolled back. You can synchronize your database with small chunks of data using flush() instead of committing a large data at once using commit() and face the risk of getting an Out Of Memory Exception.

> commit() will make data stored in the database permanent. There is no way you can rollback your transaction once the commit() succeeds.

> One common case for explicitly flushing is when you create a new persistent entity and you want it to have an artificial primary key generated and assigned to it, so that you can use it later on in the same transaction. In that case calling flush would result in your entity being given an id.

> Commit(); Commit will make the database commit.When you have a persisted object and you change a value on it, it becomes dirty and hibernate needs to flush these changes to your persistence layer.So You should commit but it also ends the unit of work.transaction.commit()

> It is usually not recommended to call flush explicitly unless it is necessary. Hibernate usually auto calls Flush at the end of the transaction and we should let it do it's work. Now, there are some cases where you might need to explicitly call flush where a second task depends upon the result of the first Persistence task, both being inside the same transaction.

[Hibernate sessions and transaction management guidelines](https://developer.atlassian.com/server/confluence/hibernate-sessions-and-transaction-management-guidelines/).

> Hibernate sessions are not thread-safe. Not only does this mean you shouldn’t pass a Hibernate session into a new thread, it also means that because objects you load from a session can be called from (and call back to) their owning session, you must not share Hibernate-managed objects between threads. Once again, try to only pass object IDs, and load the object freshly from the new thread’s own session.

> Spring’s transaction management places the Hibernate session in a ThreadLocal variable, accessed via the sessionFactory. All Confluence DAOs use that ThreadLocal. This means that when you create a new thread you no longer have access to the Hibernate session for that thread (a good thing, as above), and you are no longer part of your current transaction.

[MicroProfile, the microservice programming model made for Istio](https://www.eclipse.org/community/eclipse_newsletter/2018/september/MicroProfile_istio.php).

[Spring Boot in a Container](https://spring.io/blog/2018/11/08/spring-boot-in-a-container).

[From Jakarta EE over MicroProfile to Serverless: Interactive Onstage Hacking](https://www.youtube.com/watch?v=eBcpvmLjpZM).

[Full Stack Reactive Java con @ProjectReactor!](https://speakerdeck.com/mkheck/full-stack-reactive-java-con-project-reactor-y-spring-boot-2). [tweet](https://twitter.com/mkheck/status/1068811689666232320).

[2019 predictions](http://adambien.blog/roller/abien/entry/2019_predictions).

[Jakarta EE MicroProfile WebStandards, On Stage Hacking noslides by Adam Bien](https://www.youtube.com/watch?v=_a8FVESHjlQ)

[JSON-P: REMOVING A SLOT FROM A JSONOBJECT WITH JSONPATCH](http://adambien.blog/roller/abien/entry/json_p_removing_a_slot).

[Pagination and Sorting With Spring Data JPA](https://dzone.com/articles/pagination-and-sorting-with-spring-data-jpa)

[tweet](https://twitter.com/lukaseder/status/1100323374960701440)

> So. The correct way to fix someone else's Spring Boot setup is to just try random annotations until it works, right?

[EXCEPTION HTTP STATUS MAPPING WITHOUT MAPPERS](http://adambien.blog/roller/abien/entry/exception_http_status_mapping_without)

[i18n in Java 11, Spring Boot, and JavaScript](https://developer.okta.com/blog/2019/02/25/java-i18n-internationalization-localization)

[searching in a distributed world](https://www.infoq.com/presentations/redis-enterprise-spring)

[OPTIMIZING FOR HUMANS, NOT MACHINES](http://adambien.blog/roller/abien/entry/optimizing_for_humans_not_machines)

[jee](https://piotrminkowski.wordpress.com/2019/03/11/a-magic-around-spring-boot-externalized-configuration/)

[ the Spring Framework Early Days, Languages Post-Java, & Rethinking CI/CD](https://www.infoq.com/podcasts/johnson-spring-framework)

[how fast is spring?](https://www.infoq.com/presentations/spring-framework-slow)

[java in the 21 century](https://jaxenter.com/java-in-the-21st-century-156544.html)

[webmvc.fn](https://twitter.com/SpringTipsLive/status/1113351225104314368)

[Spring tips - dinamic views](https://twitter.com/SpringTipsLive/status/1126184279099228160)

[MULTIPLE CACHE CONFIGURATIONS WITH CAFFEINE AND SPRING BOOT](https://techblog.bozho.net/multiple-cache-configurations-with-caffeine-and-spring-boot/)

> Caching is key for performance of nearly every application. Distributed caching is sometimes needed, but not always. In many cases a local cache would work just fine and there’s no need for the overhead and complexity of the distributed cache.

[Using ConfigMaps to configure MicroProfile / Java EE 8 applications](https://twitter.com/AdamBien/status/1128161192629944320)

[A Quick Guide to Spring Boot Login Options](https://developer.okta.com/blog/2019/05/15/spring-boot-login-options)

[Reactive Transactions with Spring](https://spring.io/blog/2019/05/16/reactive-transactions-with-spring)

[@ComponentScan on a @Service class in #Spring actually works and contributes to the application context](https://twitter.com/rotnroll666/status/1129042374989160449)

[Basic Concepts: @Bean and @Configuration](https://docs-stage.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-java-basic-concepts)

[Build a Spring Boot App With Flyway and Postgres](https://dzone.com/articles/build-a-spring-boot-app-with-flyway-and-postgres)

[Spring boot tips](https://twitter.com/spring_io/status/1135474016368701440). [video](https://www.youtube.com/watch?v=azTAKKCtNXE).

[Event Driven Microservices with Axon and Spring Boot](https://twitter.com/spring_io/status/1135502736890454017)

[the proxy fairy and the magic of Spring](https://www.youtube.com/watch?v=HbbvyZh3IZo)

[spring boot internals](https://twitter.com/madhurabhave23/status/1149003060657582081)

[I DON'T YOUR DEPENDENCY INJECTION](http://adambien.blog/roller/abien/entry/i_don_t_your_dependency)

[correspondences](https://twitter.com/_JamesWard/status/1151250878218850305)

[bootiful podcast hateoas](https://twitter.com/BootifulPodcast/status/1154649344361893889)

[Installing Jenkins, creating S2I build, setting up a CD pipeline, building, deploying and testing a Java EE / Jakarta EE / MicroProfile service (twice) and configuring the readiness probe ...in 7 minutes](http://adambien.blog/roller/abien/entry/building_microservices_on_openshift_with)

[Spring Cloud Data Flow](https://www.youtube.com/watch?v=ecNfohOuzMI)

[Things that should not appear in Java code in 2019](https://twitter.com/_JamesWard/status/1158419711153098753)

> (about no getters) Most libraries (Jackson, Spring, etc) have supported direct field access for a while.

[What's new in Spring Framework 5.x](https://github.com/spring-projects/spring-framework/wiki/What's-New-in-Spring-Framework-5.x#testing)

[CODE SHRINKING TECHNIQUES WITH JAKARTA EE AND MICROPROFILE--DEVOXX](http://adambien.blog/roller/abien/entry/code_shrinking_techniques_with_jakarta)

[live refactoring session](https://www.youtube.com/watch?v=Zfgc7qJEZZ0)

[polyglot microservice example using #helidon and #graalVM](https://twitter.com/langer_tomas/status/1160899987561226241)

[web frameworks](https://twitter.com/danieldietrich/status/1171424384679985155)

[From Spring Boot apps to functional Kotlin](https://www.reddit.com/r/programming/comments/d3mmo9/from_spring_boot_apps_to_functional_kotlin/)

[From Spring Boot apps to functional Kotlin](https://www.youtube.com/watch?v=f6a78mCrSeE)

[Modernize and optimize Spring Boot applications](https://developer.ibm.com/articles/modernize-and-optimize-spring-boot-applications/)

[dynamic CDS archives](https://twitter.com/nipafx/status/1173481641404243968)

[Understanding Low Latency JVM GCs - Jean-Philippe BEMPEL](https://www.reddit.com/r/java/comments/d28wtw/understanding_low_latency_jvm_gcs_jeanphilippe/)

[The Lean, Mean... OpenJDK?](https://www.reddit.com/r/java/comments/d3ept6/the_lean_mean_openjdk/)

[JAKARTA EE 8: LINKS AND RESOURCES](http://adambien.blog/roller/abien/entry/jakarta_ee_8_useful_links)

[JAVA EE IS DEAD](http://adambien.blog/roller/abien/entry/java_ee_is_dead_completely)

[The definite guide to Java agents](https://vimeo.com/362325091)

[Writing controllers](https://dzone.com/articles/14-tips-for-writing-spring-mvc-controller)

[CODE SHRINKING WITH QUARKUS AND PANACHE ORM](http://adambien.blog/roller/abien/entry/code_shrinking_with_quarkus_and)

[Live-Coding Web Apps (PWAs)—Without Frameworks](https://www.youtube.com/watch?v=SUpnzspMFkI)

[henandoah – ultra-low Pause Time Garbage Collector](https://www.youtube.com/watch?v=nEs_i_Vc24Y)

[How Quarkus brings imperative and reactive programming together](https://developers.redhat.com/blog/2019/11/18/how-quarkus-brings-imperative-and-reactive-programming-together/)

[How to Get Productive with Spring Boot](https://www.infoq.com/presentations/spring-boot-di-devtools-autocompletion/)

[Quarkus and CORS](https://www.youtube.com/watch?v=MD-GdTDVKJM&feature=youtu.be)

[My view is that a vast majority of applications are fine as monoliths](https://twitter.com/reza_rahman/status/1235923816116817920)

[Well secured and documented REST API with Eclipse Microprofile and Quarkus](https://kostenko.org/blog/2020/02/jwt-openapi-microprofile-quarkus.html)

[Configuring a Main Class in Spring Boot](https://dzone.com/articles/configuring-a-main-class-in-spring-boot)

[Back to Shared Deployments](https://twitter.com/AdamBien/status/1239220326195699718)

[Autoconfigurations In-Depth](https://twitter.com/nicolas_frankel/status/1242728634030448640)

[Part III: Read Entities - Jakarta EE CRUD API Tutorial](https://www.youtube.com/watch?v=iT7G7yvE1Zw)

[Full-Duplex Scalable Client-Server Communication with WebSockets and Spring Boot (Part I)](https://twitter.com/DZoneInc/status/1256259750502727680)

[Best Performance Practices for Hibernate 5 and Spring Boot 2](https://dzone.com/articles/50-best-performance-practices-for-hibernate-5-amp)

[create a simple  @SpringData #JPA application using  @intellijidea](https://twitter.com/JPABuddy/status/1414550810571198466)

[Java REST API Framework Comparison - PWX 2021](https://speakerdeck.com/mraible/java-rest-api-framework-comparison-pwx-2021)

[using DTOs for #JPA entities with @GetMapStruct requires synchronizing default values and #validation settings for all fields.](https://twitter.com/JPABuddy/status/1491339638715592705)

[java Swagger custom validation](https://www.baeldung.com/java-swagger-custom-validation). [generated validation annotations](https://guntherrotsch.github.io/blog_2020/openapi-bean-validation.html).

[custom validation with Swagger codegen](https://www.baeldung.com/java-swagger-custom-validation)

[OpenAPI generator to spring-boot with custom java validations](https://bartko-mat.medium.com/openapi-generator-to-spring-boot-with-custom-java-validations-623381df9215)

[comparing dates with times](https://news.ycombinator.com/item?id=30315984)

[Serialize Debezium events with Apache Avro and OpenShift Service Registry](https://twitter.com/CertDepot/status/1493211745279692804)

[multiple datasources in Spring Boot](https://twitter.com/baeldung/status/1496832283621404676?t=eX65BSEZGvCKIqlE-bISAw&s=03)

[With @springboot 3, we'll be able to rewrite queries in @SpringData repositories!](https://twitter.com/JPABuddy/status/1528685565423628288?t=OrvenTpTHB_gfwk0Va6sRA&s=03)

[One-Stop Guide to Mapping with MapStruct](https://reflectoring.io/java-mapping-with-mapstruct/)

[Object Mapping advanced features & QoL with Java](https://www.reddit.com/r/programming/comments/xj8w29/object_mapping_advanced_features_qol_with_java/)

[A nice way to convert an id to a domain object in #SpringBoot using #SpringData and the DomainClassConverter](https://twitter.com/therealdanvega/status/1575498674960224257)

[jee debugger tasks](https://twitter.com/GeoffreyDeSmet/status/1577262981427392514)

[ORM, 20 years later](https://www.youtube.com/watch?v=pc6QIwx0EL0)

[Migrating to Spring Boot 3](https://twitter.com/jkuipers/status/1587208557639892996)

[A Hipster History of CORS](https://www.youtube.com/watch?v=0YJ-yhoJh2I)

[Spring + Kotlin](https://twitter.com/kotlin/status/1588506350463721474)

[Spring framework 6.0.0 reference PDF](https://twitter.com/maciejwalkowiak/status/1589544162650882048)

> 1427 pages 🤯

[ttcli](https://twitter.com/wimdeblauwe/status/1589520033822408704)

> command line tool to run on top of a fresh Spring Boot app to quickly setup Thymeleaf with live reload, webjars, and Bootstrap or Tailwind CSS as CSS framework

[types of generators in Hibernate](https://twitter.com/1ovthafew/status/1599371472677400576)

> Until Hibernate 6.2, each kind of thing was handled by completely separate machinery. And there were separate extension points for programs using Hibernate, with completely different APIs: IdentifierGenerator, UserVersionType, and AnnotationValueGeneration.

[Hibernate pooled and pooled-lo identifier generators](https://twitter.com/vlad_mihalcea/status/1458785093607174151)

[ResponseEntity best practices](https://twitter.com/therealdanvega/status/1599814600463355906)

[choosing Java](https://news.ycombinator.com/item?id=34064310)

[Implementing an OAuth 2 authorization server with Spring Security - the new way!](https://twitter.com/spring_io/status/1605500208456032258). [Getting modules right with Domain-driven Design](https://twitter.com/spring_io/status/1605500799983009792).

[Beginner’s Guide to the JPA AttributeConverter](https://vladmihalcea.com/jpa-attributeconverter/)

[jakarta.annotation.PostConstruct](https://stackoverflow.com/a/73852298/1364288). [Spring bean creation lifecycle : Why having multiple interaction points?](https://stackoverflow.com/questions/65091869/spring-bean-creation-lifecycle-why-having-multiple-interaction-points). [this linked one is possibly bad advice, see the critical comments](https://levelup.gitconnected.com/stop-using-postconstruct-in-your-java-applications-2a66fb202cb8)

> Spring uses jakarta.annotation.PostConstruct. As a contributor in spring-cloud-kubernetes, I have used it and included it in that project numerous times. As a matter of fact we favor dropping InitializingBean.

[Executing Code on Spring Boot Application Startup](https://reflectoring.io/spring-boot-execute-on-startup/)

> The @PostConstruct method is called right after the bean has been created by Spring, so we cannot order it freely with the @order annotation, as it may depend on other Spring beans that are @Autowired into our bean.

[Spring Boot - The Missing Guide: 2](https://twitter.com/sivalabs/status/1622819084462325760)

[JobRunr, the Java Scheduler Library, Released Version 6.0](https://www.infoq.com/news/2023/02/jobrunr-scheduler-java/)

[Journeys in Java, Level 7: Externalize Microservice Configuration](https://foojay.io/today/journeys-in-java-level-7-externalize-microservice-configuration/)

[Spring Boot and Flyway - clear database between integration tests](https://twitter.com/maciejwalkowiak/status/1627592317774311424)

[modules use case](https://twitter.com/rotnroll666/status/1630922218803720194)

[Spring Boot the Ripper – Part I](https://www.youtube.com/watch?v=6i17IBBa-I0)

[How to Best Use Java Records as DTOs in Spring Boot 3](https://foojay.io/today/how-to-best-use-java-records-as-dtos-in-spring-boot-3/)

[For even less glue code](https://twitter.com/odrotbohm/status/1637145519536390146)

[doubts about Mapstruct](https://twitter.com/maciejwalkowiak/status/1638853501726998532). [MapStruct in Spring application - is "spring" component model the right approach?](https://github.com/mapstruct/mapstruct/discussions/3208). [mappers as converters](https://mapstruct.org/documentation/spring-extensions/reference/html/#mapperAsConverter). [a hater](https://twitter.com/simas_ch/status/1643874199260282881)

> I don’t see the harm: you’re depending on a component, you’re using a framework that manages components. Your mappers won’t typically need DI or AOP, but there definitely are use cases for that (I have them).
Why resort to factory methods if you can use DI?

[Virtual Threads Arrive in JDK 21, Ushering a New Era of Concurrency](https://news.ycombinator.com/item?id=35535906)

[Comparison of Java HTTP Clients](https://reflectoring.io/comparison-of-java-http-clients/)

[A pattern implemented as part of @springmodulith ‘s Event Publication Registry](https://twitter.com/odrotbohm/status/1648378551131947008)


loom (2020) [1](https://webtide.com/do-looms-claims-stack-up-part-1/) [2](https://webtide.com/do-looms-claims-stack-up-part-2/)

> Loom aims to remove the dilemma between wasting money on hardware due to under-utilisation vs spending more money on development, maintenance and operations with async.

> As to 1 million threads, the assumption is that if you have 1 million threads they won’t be serving 1M concurrent single-threaded transactions (unless you have the requirements and therefore resources to do that), but rather, you’d have something like 100K concurrent transactions, each served by one “deep stack thread” plus, say, 9 more “shallow” threads doing subtasks like outgoing microservice calls.

[@JobRunr - perhaps the best implementation of job scheduler. ](https://twitter.com/maciejwalkowiak/status/1664295458099871745)

[Working with jOOQ and Flyway using Testcontainers](https://testcontainers.com/guides/working-with-jooq-flyway-using-testcontainers/)

[HTTP Interface Clients in #SpringBoot ](https://twitter.com/therealdanvega/status/1668297196658106369)

[jpa dynamic entity graphs](https://twitter.com/JPABuddy/status/1674692647741521920)

[fast back](https://twitter.com/sitnikcode/status/1679549264454623233)

[spring, Thymeleaf and htmx](https://www.linkedin.com/events/springboot-thymeleaf-andhtmx7085889711675764736/comments/)

[automapping in .NET](https://twitter.com/pdevito3/status/1680277396275036162)

[Using XPath in 2023](https://denizaksimsek.com/2023/xpath/)

[Hibernate's metamodel generator](https://twitter.com/1ovthafew/status/1682324169998888960)

[This is the Beginning of the End of the N+1 Problem: Introducing Single Query Loading.](https://spring.io/blog/2023/08/31/this-is-the-beginning-of-the-end-of-the-n-1-problem-introducing-single-query)

> Starting with Spring Data JDBC 3.2.0-M2, Spring Data JDBC supports Single Query Loading. Single Query Loading loads arbitrary aggregates with a single select statement.

[MVC Controllers are Dinosaurs - Embrace API Endpoints](https://ardalis.com/mvc-controllers-are-dinosaurs-embrace-api-endpoints/#sq_hcvqfhumxh)

[Pattern Matching for Switch and Record Patterns in Java 21](https://emilie-robichaud.medium.com/pattern-matching-for-switch-and-record-patterns-in-java-21-979d034b3c5)

[Easy OAuth with the Durable Spring Authorization Server](https://www.youtube.com/watch?v=wq7oU2UCsbo). [code](https://github.com/coffee-software-show/the-durable-spring-authorization-server).

[Dynamically Changing log4j or logback log levels in Java](https://prefab.cloud/blog/dynamically-changing-java-log-level/)

[Why spring data JDBC?](https://docs.spring.io/spring-data/jdbc/docs/current/reference/html/#jdbc.why)

[scoped values](https://openjdk.org/jeps/446). [tweet](https://twitter.com/msimoni/status/1705990149648101670).

[The Second Best Way to Fetch a Spring Data JPA DTO Projection](https://blog.jooq.org/the-second-best-way-to-fetch-a-spring-data-jpa-dto-projection/). [tweet](https://twitter.com/maciejwalkowiak/status/1707109360390840346).

[Do you really need Hibernate](https://www.youtube.com/watch?v=ykoUBctblno). [Better database access with SQL-centric APIs ](https://www.youtube.com/watch?v=2dvCuWxNTV4&t=1s)

[aot with profile-guided optimizations](https://twitter.com/fniephaus/status/1708019895286313082)

[@PostConstruct](https://quarkus.io/guides/cdi)

> It’s a good practice to keep the logic in the callbacks "without side effects"

[Entity Framework Core 8](https://www.youtube.com/watch?v=_8iH5QnkIJo&list=PLdo4fOcmZ0oULyHSPBx-tQzePOYlhvrAU&index=9). [Quartz.NET 3.8.0](https://github.com/quartznet/quartznet/releases/tag/v3.8.0). [A Complete Guide to all ASP.NET Builtin Middlewares - Part 3](https://adnanrafiq.com/blog/a-complete-guide-to-all-asp-dot-net-builtin-middlewares-part3/).

[spring modulith](https://twitter.com/starbuxman/status/1728199106836013188)

[Do you really need Hibernate by Simon Martinelli @ Spring I/O 2023](https://www.youtube.com/watch?v=ykoUBctblno)

[resilience4j](https://resilience4j.readme.io/)

> Resilience4j is a lightweight fault tolerance library inspired by Netflix Hystrix, but designed for functional programming.

> Resilience4j provides higher-order functions (decorators) to enhance any functional interface, lambda expression or method reference with a Circuit Breaker, Rate Limiter, Retry or Bulkhead.

[THE “SPRING WAY” OF DOING THINGS: 9 WAYS TO IMPROVE YOUR SPRING BOOT SKILLS](https://digma.ai/blog/the-spring-way-of-doing-things-9-ways-to-improve-your-spring-boot-skills/)

> Another way to utilize Spring Boot to its full potential is to try as much as possible to externalize your configuration instead of hard coding them. Externalizing your configuration will make your application more flexible and easier to manage.

[Spring Tips: DataSources](https://www.youtube.com/watch?v=rt_cUtb8LnQ)

[Common Spring Developer Mistakes](https://www.youtube.com/watch?v=nd5JzDIEI6A)

[basic Java tips](https://twitter.com/maciejwalkowiak/status/1752960760064462888)

[Spring Application Events subsystem](https://www.youtube.com/watch?v=5YdjBWSGtbE)

[Spring MVC Http Interfaces](https://www.youtube.com/watch?v=aR580OCEp7w)

[LaunchDarkly Java Testing and Local Development Hints](https://rieckpil.de/launchdarkly-java-testing-and-local-development-hints/)

[Spring Boot failure analyzer](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto.application.failure-analyzer)

[Distributed Job Scheduling with Jobrunr](https://www.youtube.com/watch?v=e9POHS0BjEg)

[Notes on debugging HotSpot's JIT compilation](https://news.ycombinator.com/item?id=39813626)

[Automate the process of upgrading your #Java & #SpringBoot applications with OpenRewrite](https://www.youtube.com/watch?v=e4R6AZHpAD8)

[epbf & java?](https://x.com/richardstartin/status/1768397634534768839)

[dynamic projections with Spring Data JPA](https://maciejwalkowiak.com/blog/spring-data-jpa-dynamic-projections/) [tweet](https://twitter.com/maciejwalkowiak/status/1779948952269279396)

[how open rewrite happened](https://open.spotify.com/episode/0kR28LMf6P9xB9vwokfnYU)

[modern Java practices](https://github.com/binkley/modern-java-practices)

[Modern Testing Tools for Java Developers](https://speakerdeck.com/eliasnogueira/modern-testing-tools-for-java-developers)

[Spring Tips: Beans, Beans: What's in a Spring bean?](https://www.youtube.com/watch?v=Z5hxolai4Tk)

[http webserver utilities](https://hachyderm.io/@java_discussions@mastodon.social/112411328057966270)

[Distributed Scheduling with JobRunr and Spring Boot](https://www.youtube.com/watch?v=jxNTpfVft-M). [Distributed Scheduling with Spring Boot: the challenges & pitfalls of implementing a background job](https://x.com/spring_io/status/1799063492860977371). [Getting Started with JobRunr: Powerful Background Job Processing Library](https://foojay.io/today/getting-started-with-jobrunr-a-powerful-task-scheduler-in-ja/).

[Spring core container revisited](https://www.youtube.com/watch?v=GzX3C0sTFbw). 

[Creating Future-Proof Spring Applications with Event Sourcing](https://www.youtube.com/watch?v=xr6Gq3Cn4UQ).

[Migrating from (Spring Data) JPA to Spring Data JDBC](https://www.youtube.com/watch?v=WYa9n0F4CRM).




