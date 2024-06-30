- [Customizing My Postgres Shell](https://www.citusdata.com/blog/2017/07/16/customizing-my-postgres-shell-using-psqlrc/)

- [Why favor PostgreSQL over MariaDB/MySQL?](https://news.ycombinator.com/item?id=15171917)

- [Better Database Migrations in Postgres](http://www.craigkerstiens.com/2017/09/10/better-postgres-migrations/)

- [Six ways to paginate in Postgres](http://allyouneedisbackend.com/blog/2017/09/24/the-sql-i-love-part-1-scanning-large-table/)

- [Mastering PostgreSQL in Application Developement](https://news.ycombinator.com/item?id=15634953)

- [What it means to be a postgresql extension](https://news.ycombinator.com/item?id=15633136)

- [PostgreSQL anti-patterns: read-modify-write cycles](https://blog.2ndquadrant.com/postgresql-anti-patterns-read-modify-write-cycles/)

- [Isolation levels](https://www.postgresql.org/docs/9.1/static/transaction-iso.html)

> Applications using this level must be prepared to retry transactions due to serialization failures.

> The Serializable isolation level provides the strictest transaction isolation. This level emulates serial transaction execution, as if transactions had been executed one after another, serially, rather than concurrently. However, like the Repeatable Read level, applications using this level must be prepared to retry transactions due to serialization failures. In fact, this isolation level works exactly the same as Repeatable Read except that it monitors for conditions which could make execution of a concurrent set of serializable transactions behave in a manner inconsistent with all possible serial (one at a time) executions of those transactions. This monitoring does not introduce any blocking beyond that present in repeatable read, but there is some overhead to the monitoring, and detection of the conditions which could cause a serialization anomaly will trigger a serialization failure.

> Declare transactions as READ ONLY when possible.

> A-ha! It seems that SERIALIZABLE has race conditions into account.

[PostgreSQL anti-patterns: read-modify-write cycles](https://blog.2ndquadrant.com/postgresql-anti-patterns-read-modify-write-cycles/)

[PostgreSQL anti-patterns: Unnecessary json/hstore dynamic columns](https://blog.2ndquadrant.com/postgresql-anti-patterns-unnecessary-jsonhstore-dynamic-columns/)

[Solving Schema Bloat with Postgresql's JSONB](http://middlepathdevelopment.com/blog/solving-schema-bloat-with-jsonb.html) [counterpoints](https://www.reddit.com/r/programming/comments/7sxwbn/solving_schema_bloat_with_postgresqls_jsonb/)

[Postgres Indexes Under the Hood](https://rcoh.me/posts/postgres-indexes-under-the-hood/)

[The internals of Postgres](https://news.ycombinator.com/item?id=16970686)

[Parallel Index Scans In PostgreSQL](http://amitkapila16.blogspot.com.es/2018/05/parallel-index-scans-in-postgresql.html)

[transaction isolation](https://www.postgresql.org/docs/9.1/static/transaction-iso.html) [concurrency in Postgres slides](https://www.postgresql.org/files/developer/concurrency.pdf) [Why is CTE open to lost updates?](https://dba.stackexchange.com/questions/78510/why-is-cte-open-to-lost-updates) [read-modify-update cycles](https://blog.2ndquadrant.com/postgresql-anti-patterns-read-modify-write-cycles/)

> Predicate locks in PostgreSQL, like in most other database systems, are based on data actually accessed by a transaction. These will show up in the pg_locks system view with a mode of SIReadLock. The particular locks acquired during execution of a query will depend on the plan used by the query, and multiple finer-grained locks (e.g., tuple locks) may be combined into fewer coarser-grained locks (e.g., page locks) during the course of the transaction to prevent exhaustion of the memory used to track the locks. 

> The Repeatable Read mode provides a rigorous guarantee that each transaction sees a completely stable view of the database. However, this view will not necessarily always be consistent with some serial (one at a time) execution of concurrent transactions of the same level. For example, even a read only transaction at this level may see a control record updated to show that a batch has been completed but not see one of the detail records which is logically part of the batch because it read an earlier revision of the control record. Attempts to enforce business rules by transactions running at this isolation level are not likely to work correctly without careful use of explicit locks to block conflicting transactions.

[Scalable incremental data aggregation on Postgres and Citus](https://www.citusdata.com/blog/2018/06/14/scalable-incremental-data-aggregation/) [hn](https://news.ycombinator.com/item?id=17338401)

[postgres features](https://pgdash.io/blog/postgres-features.html?h=)

[PostgreSQL 11’s Support for SQL Standard GROUPS and EXCLUDE Window Function Clauses](https://blog.jooq.org/2018/07/05/postgresql-11s-support-for-sql-standard-groups-and-exclude-window-function-clauses/)

[Have you ever chosen Postgres over Mongo and regretted it?](https://news.ycombinator.com/item?id=17497164)

[Batch Updates and Concurrency](https://tapoueh.org/blog/2018/07/batch-updates-and-concurrency/)

[Fast Full-Text Search in PostgreSQL](https://austingwalters.com/fast-full-text-search-in-postgresql/)

[psql Tips and Tricks](https://pgdash.io/blog/postgres-psql-tips-tricks.html?p)

[What is the difference between LATERAL and a subquery in PostgreSQL?](https://stackoverflow.com/a/28557803/1364288).

[PostgreSQL 11’s Support for SQL Standard GROUPS and EXCLUDE Window Function Clauses](https://blog.jooq.org/2018/07/05/postgresql-11s-support-for-sql-standard-groups-and-exclude-window-function-clauses/).

> ROWS counts the exact number of rows in the frame. RANGE performs logical windowing where we don’t count the number of rows, but look for a value offset. GROUPS counts all groups of tied rows within the window.

[Standard SQL Gap Analysis -- PGCon 2018](https://www.youtube.com/watch?v=XkyOgz9APdI).

[Bye bye Mongo, Hello Postgres](https://www.theguardian.com/info/2018/nov/30/bye-bye-mongo-hello-postgres).

[The Internals of PostgreSQL for database administrators and system developers](http://www.interdb.jp/pg/index.html)

[vertically scaling pg](https://pgdash.io/blog/scaling-postgres.html)

[PostgreSQL Concurrency: Isolation and Locking](https://tapoueh.org/blog/2018/07/postgresql-concurrency-isolation-and-locking/)

> It took about 20 years for the research community to come up with a satisfying mathematical model for implementing serializable snapshot isolation in an efficient way, and then a single year for that major progress to be included in PostgreSQL!

[Serializable](https://wiki.postgresql.org/wiki/Serializable#Serializable_and_Snapshot_Transaction_Isolation_Levels)

> Serializable transaction isolation is attractive for shops with active development by many programmers against a complex schema because it guarantees data integrity with very little staff time -- if a transaction can be shown to always do the right thing when it is run alone (before or after any other transaction), it will always do the right thing in any mix of concurrent serializable transactions. Where conflicts with other transactions would result in an inconsistent state within the database or an inconsistent view of the data, a serializable transaction will block or roll back to prevent the anomaly. The SQL standard provides a specific SQLSTATE for errors generated when a transaction rolls back for this reason, so that transactions can be retried automatically.

> Before version 9.1, PostgreSQL did not support a full serializable isolation level. A request for serializable transaction isolation actually provided snapshot isolation. This has well known anomalies which can allow data corruption or inconsistent views of the data during concurrent transactions; although these anomalies only occur when certain patterns of read-write dependencies exist within a set of concurrent transactions. Where these patterns exist, the anomalies can be prevented by introducing conflicts through explicitly programmed locks or otherwise unnecessary writes to the database. Snapshot isolation is popular because performance is better than serializable isolation and the integrity guarantees which it does provide allow anomalies to be avoided or managed with reasonable effort in many environments.

> A new technique for implementing full serializable isolation in an MVCC database appears in the literature beginning in 2008[1][2]. This technique, known as Serializable Snapshot Isolation (SSI) has many of the advantages of snapshot isolation. In particular, reads don't block anything and writes don't block reads. Essentially, it runs snapshot isolation but monitors the read-write conflicts between transactions to identify dangerous structures in the transaction graph which indicate that a set of concurrent transactions might produce an anomaly, and rolls back transactions to ensure that no anomalies occur. It will produce some false positives (where a transaction is rolled back even though there would not have been an anomaly), but will never let an anomaly occur. In the two known prototype implementations, performance for many workloads (even with the need to restart transactions which are rolled back) is very close to snapshot isolation and generally far better than an S2PL implementation.

[	A short list of common mistakes in PostgreSQL](https://wiki.postgresql.org/wiki/Don%27t_Do_This). [hn](https://news.ycombinator.com/item?id=19817531).

[Postgres 11](https://news.ycombinator.com/item?id=19867943)

> I use transactional DDL in my tests. All the tables, triggers, etc. are set up inside a transaction, and then the actual tests run inside nested transactions. At the end of the test run, the outer transaction gets rolled back, and everything disappears.
I don't know if it accomplishes anything truly new (other than ideas that aren't very useful in practice like being able to have multiple test runs going in parallel), but it's a pretty neat way to be able to do it and works well.

> Transactional tests have some downsides, unfortunately. If your tests test transactional code, that code itself cannot create transactions; they have to use savepoints, which aren't quite the same. Transactional tests also don't work with testing anything concurrent, unless you share the session across threads/goroutines/whatever.
Lastly, if a test fails you'd typically like to leave the data behind so that you can inspect it. A transactional test that rolls back on failure won't allow that.

> Save points, with proper management of them, seem to match a conceptual nested transaction as far as I've seen. We've got a test bed connection manager that mocks savepoint creation, rollback and committal into transaction management functions so doing something like beginTransaction && beginTransaction works fine.

[atomic transactions](https://news.ycombinator.com/item?id=21000754)

[Generated columns](https://news.ycombinator.com/item?id=21134339)

[PostgreSQL example of self-contained stored procedures](https://news.ycombinator.com/item?id=21362190)

> For data integrity, I've always found databases not expressive enough. Sanity checks, okay, but you can't capture a non-trivial domain in some custom data types, check constraints and foreign keys. Even if you introduce stored procedures that will be responsible for keeping everything proper, you need to go crazy with permissions to block circumventing those. Might as well build your own API then. (I do find it difficult where to draw the line when it comes to what to enforce in the database still.)

> "But you don't need another API! Just use the database as one!" Then I ask how they do testing, and the answer basically is: "We don't make mistakes or we find out about them (in production) soon enough." That pretty much ends the discussion for me. Surely there must be ways to devise a basic testing framework for stored procedures, but why bother? I don't want to spin up a database just to test some logic. Never mind testing, what about refactoring?

[System design hack: Postgres is a great pub/sub and job server ](https://news.ycombinator.com/item?id=21484215)

[analysis of a performance regression](https://twitter.com/felixge/status/1219268882416001025)

[Let's dig into some #postgres and #linux internals](https://twitter.com/felixge/status/1221512507690496001)

[Postgresqlco.nf: a PostgreSQL configuration guide](https://news.ycombinator.com/item?id=22216504)

[The State of (Full) Text Search in PostgreSQL 12](https://fosdem.org/2020/schedule/event/postgresql_the_state_of_full_text_search_in_postgresql_12/)

[opinions on postgres](https://twitter.com/lukaseder/status/1226804513069260800)

[How do PostgreSQL triggers work depending on the current transaction isolation level](https://www.reddit.com/r/programming/comments/f2a1r3/how_do_postgresql_triggers_work_depending_on_the/?utm_source=ifttt)

[things I hate about postgres](https://medium.com/@rbranson/10-things-i-hate-about-postgresql-20dbab8c2791)

[How do PostgreSQL advisory locks work](https://vladmihalcea.com/how-do-postgresql-advisory-locks-work/)

[Our love story with Deadlocks (PostgreSQL Edition)](https://auto1.tech/event-store-deadlock/). [lobsters](https://lobste.rs/s/utiwy0/our_love_story_with_deadlocks_postgresql)

[PostgreSQL repeatable read isn't repeatable read: it's snapshot isolation, which allows a specific class of G2-item anomalies (those with nonadjacent rw edges prohibited under formalizations of repeatable read.)](https://twitter.com/jepsen_io/status/1271427955525185536). [hn](https://news.ycombinator.com/item?id=23498781)

[Mastering PostgreSQL Administration](https://news.ycombinator.com/item?id=24606163)

[Measuring the Memory Overhead of a Postgres Connection](https://news.ycombinator.com/item?id=24735012)

> I have followed various snippets of community folklore advice on this topic over the years (many of them suggesting that the proper number of connections should relate somehow to the number of CPU cores). It was, therefore, refreshing to see one of the core developers, Bruce Momjian, publish modern advice[0] based on empirical observations he made while working on real client problems through Enterprise DB. Spoiler: on modern hardware, without an over-agressive shared_buffer config setting[1], up to 250 direct connections to the DB may be made without detrimental impact.

[partial indexes](https://news.ycombinator.com/item?id=25988871)

> Partial indexes are amazing but you have to keep in mind some pecularities.

> If your query doesn't contain a proper match with the WHERE clause of the index - the index will not be used. It is easy to forget about it or to get it wrong in subtle ways.

[Do You Really Need Redis? How to Get Away with Just PostgreSQL](https://spin.atomicobject.com/2021/02/04/redis-postgresql/)

[Prevent Overlapping Ranges with Database-Level Exclusion Constraints](https://twitter.com/atomicobject/status/1378014361906712577)

[operating PostgreSQL at scale over the long run](https://twitter.com/jer_s/status/1383199349673394183)

[Debugging random slow writes in PostgreSQL](https://news.ycombinator.com/item?id=27152507)

[	Hierarchical Structures in PostgreSQL ](https://news.ycombinator.com/item?id=27631765). [Models for hierarchical data
](https://de.slideshare.net/billkarwin/models-for-hierarchical-data)

[READ COMMITTED anomalies in PostgreSQL](https://dev.to/aws-heroes/read-committed-anomalies-in-postgresql-1ieg). [tweet](https://twitter.com/FranckPachot/status/1414897704610717697).

[Postgres Full-Text Search: A search engine in a database ](https://news.ycombinator.com/item?id=27973497).

[How PostgreSQL aggregation works and how it inspired our hyperfunctions’ design](https://news.ycombinator.com/item?id=28075774)

[	In Praise of PostgreSQL ](https://news.ycombinator.com/item?id=28075204)

[	Working with Postgres Types ](https://news.ycombinator.com/item?id=28095264)

[PostgreSQL Subtransactions Considered Harmful](https://news.ycombinator.com/item?id=28374333)

[Using PostgreSQL’s JSONB for NoSQL (2019) [video]](https://news.ycombinator.com/item?id=28406334)

[Why we spent the last month eliminating PostgreSQL subtransactions](https://lobste.rs/s/zyyoma/why_we_spent_last_month_eliminating)

[Lessons learned from sharding Postgres at Notion](https://news.ycombinator.com/item?id=28776786)

[Projecting Monthly Revenue Run Rate in Postgres](https://blog.crunchydata.com/blog/postgres-queries-for-projecting-monthly-revenue-run-rate)

> What I have found through the years is that it's best to work through SQL queries inside-out. 

[Encrypting Postgres Data at Rest in Kubernetes](https://news.ycombinator.com/item?id=29057505)

[A read query can write to disk: a Postgres story](https://news.ycombinator.com/item?id=29056405)

[How partial, covering, and multicolumn indexes may slow down UPDATEs in PostgreSQL](https://postgres.ai/blog/20211029-how-partial-and-covering-indexes-affect-update-performance-in-postgresql)

[Postgres, Kafka, and a mysterious 100 GB](https://news.ycombinator.com/item?id=29462140)

[Postgres is a great pub/sub and job server (2019)](https://news.ycombinator.com/item?id=29599132)

[Tips for a Healthier Postgres Database](https://news.ycombinator.com/item?id=29858083)

[The world of PostgreSQL wire compatibility](https://datastation.multiprocess.io/blog/2022-02-08-the-world-of-postgresql-wire-compatibility.html) 

[How PostgreSQL stores rows](https://news.ycombinator.com/item?id=30279986)

[When PostgreSQL locks](https://news.ycombinator.com/item?id=30316653)

[PostgreSQL Schema Change Guide](https://www.reddit.com/r/PostgreSQL/comments/t10cew/postgresql_schema_change_guide/)

[Postgres Auditing in 150 lines of SQL](https://news.ycombinator.com/item?id=30615470)

[How we optimized PostgreSQL queries 100x](https://towardsdatascience.com/how-we-optimized-postgresql-queries-100x-ff52555eabe)

[hooks in Postgres](https://ctodive.com/hooks-the-secret-feature-powering-the-postgres-ecosystem-f05b3b82e0ba)

[The Surprising Impact of Medium-Size Texts on PostgreSQL Performance](https://hakibenita.com/sql-medium-text-performance)

[Simple Anomaly Detection Using Plain SQL](https://hakibenita.com/sql-anomaly-detection)

[Amazon Aurora: Design Considerations](https://twitter.com/muratdemirbas/status/1505718394334687236)

[How PostgreSQL stores rows](https://news.ycombinator.com/item?id=30279986)

[Postgres Connection Strings and psql](https://tapoueh.org/blog/2019/09/postgres-connection-strings-and-psql/). [official docs](https://www.postgresql.org/docs/current/libpq-connect.html#LIBPQ-CONNSTRING).

[Amazon Aurora Serverless v2 is Generally Available: Instant Scaling for Demanding Workloads](https://aws.amazon.com/blogs/aws/amazon-aurora-serverless-v2-is-generally-available-instant-scaling-for-demanding-workloads/)

[Parquet and Postgres in the Data Lake](https://www.crunchydata.com/blog/parquet-and-postgres-in-the-data-lake)

[The FILTER clause in Postgres 9.4](https://medium.com/little-programming-joys/the-filter-clause-in-postgres-9-4-3dd327d3c852)

[OpenTelemetry Traces and PostgreSQL](https://news.ycombinator.com/item?id=31397145)

[materializing query results as JSON right away within #Postgres (based on typed tables, no JSON(B) columns)](https://twitter.com/gunnarmorling/status/1535305484697231360)

[Postgres data flow](https://www.crunchydata.com/blog/postgres-data-flow)

[Postgres Full Text Search vs. the Rest](https://news.ycombinator.com/item?id=33203370)

[Push-based outbox pattern with Postgres logical replication](https://news.ycombinator.com/item?id=33370649)

[Postgres: Safely renaming a table with no downtime using updatable views](https://brandur.org/fragments/postgres-table-rename)

[Implementing failover of logical replication slots](https://twitter.com/gunnarmorling/status/1591736378114523138)

[pagila](https://github.com/devrimgunduz/pagila)

[Preferred Index Types for Text Search](https://www.postgresql.org/docs/current/textsearch-indexes.html)

[views and optimization](https://dba.stackexchange.com/questions/151169/are-views-harmful-for-performance-in-postgresql)

> Selecting from a view is exactly as fast or slow as running the underlying SQL statement – you can easily check that using explain analyze.

> The Postgres optimizer (and the optimizer for many other modern DBMSes) will be able to push down predicates on the view into the actual view statement – provided this is a simple statement (again, this can be verified using explain analyze).

[How to map a PostgreSQL Range column type with JPA and Hibernate](https://twitter.com/vlad_mihalcea/status/1612437289044529152)

[How to JSON in PostgreSQL®](https://ftisiot.net/postgresqljson/main/)

[Building a PostgreSQL Wire Protocol Server using Vanilla, Modern Java 21](https://gavinray97.github.io/blog/postgres-wire-protocol-jdk-21). [tweet](https://twitter.com/GavinRayDev/status/1615043478857125897)

[Choosing a Postgres Primary Key](https://news.ycombinator.com/item?id=34451344)

[optimising LATERAL](https://twitter.com/lukaseder/status/1617869849723650050)

[What is a valid use case for using TIMESTAMP WITHOUT TIME ZONE?](https://dba.stackexchange.com/questions/59006/what-is-a-valid-use-case-for-using-timestamp-without-time-zone). [discussion in postgresql-simple](https://hackage.haskell.org/package/postgresql-simple-0.6.5/docs/Database-PostgreSQL-Simple-Time.html). [STORING UTC IS NOT A SILVER BULLET](https://codeblog.jonskeet.uk/2019/03/27/storing-utc-is-not-a-silver-bullet/)

> Booking future appointments

> If you do have users, logs, or anything on different timezones, store the timezone they are coming from somewhere and choose and use timestamp with time zone.

> TIMESTAMP WITHOUT TIME ZONE values are not a point on the timeline, not actual moments. They represent a rough idea about potential moments,

[What is a valid use case for using TIME WITH TIME ZONE?](https://dba.stackexchange.com/questions/187351/what-is-a-valid-use-case-for-using-time-with-time-zone)

> none

[Parquet and Postgres in the Data Lake](https://www.crunchydata.com/blog/parquet-and-postgres-in-the-data-lake). [parquet_fdw](https://github.com/adjust/parquet_fdw/).

> What if there was a storage option that was still durable, allowed access via multiple query tools, and could integrate transparently into your operational transactional database?

> How about: storing the static data in Parquet format but retaining database access to the data via the parquet_fdw?

[Don't Do This](https://fosdem.org/2023/schedule/event/postgresql_dont_do_this/)

[Schema design for products with multiple variants/attributes?](https://dba.stackexchange.com/questions/123467/schema-design-for-products-with-multiple-variants-attributes)

[How PostgreSQL Views and Materialized Views Work and How They Influenced TimescaleDB Continuous Aggregates](https://www.timescale.com/blog/how-postgresql-views-and-materialized-views-work-and-how-they-influenced-timescaledb-continuous-aggregates/)

[TEMPORARY views](https://www.postgresql.org/docs/current/sql-createview.html). [Using PostgreSQL temporary views for expressing business logic](https://vvvvalvalval.github.io/posts/using-postgresql-temporary-views-for-expressing-business-logic.html). [for COPY](https://hakibenita.com/postgresql-unknown-features)

> If specified, the view is created as a temporary view. Temporary views are automatically dropped at the end of the current session. 

[to EAV or not to EAV](https://www.cybertec-postgresql.com/en/entity-attribute-value-eav-design-in-postgresql-dont-do-it/)

[Postgres performance cliffs with large JSONB values and TOAST](https://pganalyze.com/blog/5mins-postgres-jsonb-toast). [understanding JSONB performance](https://postgresql.us/events/pgconfnyc2021/schedule/session/891-understanding-of-jsonb-performance/). [PGConf NYC 2021 - Understanding of Jsonb Performance ](https://www.youtube.com/watch?v=v_s-DH4PEVA)

> how JSONB performance can behave badly when the JSONB value exceeds the two kilobyte limit where Postgres starts storing data in TOAST.

[SELECT null, 'null'::jsonb, '"null"'::jsonb](https://github.com/jOOQ/jOOQ/issues/9607#issuecomment-561126445) 

[Database DevOps and Code management with PostgreSQL](https://www.softwareandbooz.com/database-devops-and-code-management-with-postgresql/)

[PostgreSQL Unlogged Tables - Look Ma, No WAL!](https://www.crunchydata.com/blog/postgresl-unlogged-tables)

[Partial Indexes](https://use-the-index-luke.com/sql/where-clause/partial-and-filtered-indexes)

[Psql tips](https://news.ycombinator.com/item?id=34909670)

[Index Merges vs Composite Indexes in Postgres and MySQL](https://sirupsen.com/index-merges)

[PostgreSQL, The Time-Series Database You Want](https://www.youtube.com/watch?v=k1xVlS6hdxU)

[things I wish I knew while learning Postgres](https://mastodon.social/@astroidex/109964159927896918)

[On the Ascendance of PostgreSQL](https://thenewstack.io/from-a-fan-on-the-ascendance-of-postgresql/)

[The Wonders of Postgres Logical Decoding Messages](https://www.infoq.com/articles/wonders-of-postgres-logical-decoding-messages/). [video](https://www.youtube.com/watch?v=rZzmu1KuyTc)

[PostgreSQL Logical Replication Explained](https://news.ycombinator.com/item?id=35203571)

[Postgres: The Graph Database You Didn't Know You Had](https://lobste.rs/s/gryb1f/postgres_graph_database_you_didn_t_know)

[Is your Postgres ready for production?](https://www.crunchydata.com/blog/is-your-postgres-ready-for-production)

[Why We Ditched RabbitMQ And Replaced It With A Postgres Queue](https://lobste.rs/s/zdpsir/why_we_ditched_rabbitmq_replaced_it_with). [hn](https://news.ycombinator.com/item?id=35526846).

[psql tips](https://twitter.com/PostgresqlStan/status/1647070399954386944). [original](https://psql-tips.org/psql_tips_all.html).

[The part of Postgres we hate the most: Multi-version concurrency control ](https://ottertune.com/blog/the-part-of-postgresql-we-hate-the-most/). [hn](https://news.ycombinator.com/item?id=35716963). [An Empirical Evaluation of In-Memory Multi-Version Concurrency Control](https://db.cs.cmu.edu/papers/2017/p781-wu.pdf)

[job queues](https://twitter.com/gwenshap/status/1652018783404576768)

[understanding postgresql indexes](https://blog.mastermind.dev/indexes-in-postgresql)

[postgres concurrency](https://dev.to/yet_anotherdev/series/23077)

[Postgres Repeatable Read vs Serializable](https://dba.stackexchange.com/questions/284744/postgres-repeatable-read-vs-serializable). [Deeply understand Isolation levels and Read phenomena in MySQL & PostgreSQL](https://dev.to/techschoolguru/understand-isolation-levels-read-phenomena-in-mysql-postgres-c2e). [serialization anomaly](https://dev.to/techschoolguru/understand-isolation-levels-read-phenomena-in-mysql-postgres-c2e#serialization-anomaly-in-postgres). [Understanding Database isolation level via examples — MySQL and Postgres](https://amirsoleimani.medium.com/understanding-database-isolation-level-via-examples-mysql-and-postgres-a86b5502d404). [In Postgres, is there a need to lock a row in a table using FOR UPDATE if the query is contained in a transaction with serializable isolation level?](https://stackoverflow.com/questions/75761088/in-postgres-is-there-a-need-to-lock-a-row-in-a-table-using-for-update-if-the-qu). [TRANSACTION ANOMALIES WITH SELECT FOR UPDATE](https://www.cybertec-postgresql.com/en/transaction-anomalies-with-select-for-update/). [Postgres's serializable transaction blocks concurrent write](https://stackoverflow.com/questions/50745282/postgress-serializable-transaction-blocks-concurrent-write). [](). [Canceled on identification as a pivot](https://stackoverflow.com/questions/69015476/what-does-canceled-on-identification-as-a-pivot-mean). [Unexpected failure in transactions with isolation level serializable](https://dba.stackexchange.com/questions/156645/unexpected-failure-in-transactions-with-isolation-level-serializable).

[SI vs. SSI](https://wiki.postgresql.org/wiki/SSI) This is a *great* resource!

> When two concurrent transactions each determine what they are writing based on reading a data set which overlaps what the other is writing, you can get a state which could not occur if either had run before the other. This is known as write skew, and is the simplest form of serialization anomaly against which SSI protects you.

> Serialization anomalies can result from more complex patterns of access, involving three or more transactions.

[Repeatable Read vs Serializable Isolation Level in Postgres](https://peter.grman.at/postgres-repeatable-read-vs-serializable/)

> Because we had previously experienced the pain of inconsistent databases due to the lost update problem, we decided to trade stability for performance

[PostgreSQL in the Cloud](https://www.youtube.com/watch?v=TD4qMsnSqHQ)

[Postgres Partition Pains - LockManager Waits](https://www.kylehailey.com/post/postgres-partition-pains-lockmanager-waits). [video](https://www.youtube.com/watch?v=YPorP8BsF_c).

[Postgres schema changes are still a PITA](https://xata.io/blog/postgres-schema-changes-pita)

[Postgresql tips](https://twitter.com/gwenshap/status/1679971835549724672)

[Postgres Subquery Powertools: CTEs, Materialized Views, Window Functions, and LATERAL Join](https://www.crunchydata.com/blog/postgres-subquery-powertools-subqueries-ctes-materialized-views-window-functions-and-lateral)

[Introducing pg_later: Asynchronous Queries for Postgres, Inspired by Snowflake](https://tembo.io/blog/introducing-pg-later/)

[explaining the postgres meme](https://www.avestura.dev/blog/explaining-the-postgres-meme). 

[data-modifying CTEs](https://stackoverflow.com/a/20561627/1364288). [docs](https://www.postgresql.org/docs/current/queries-with.html#QUERIES-WITH-MODIFYING)

[How do I insert a row which contains a foreign key?](https://dba.stackexchange.com/questions/46410/how-do-i-insert-a-row-which-contains-a-foreign-key).

[nextval()](https://dba.stackexchange.com/questions/292199/insert-duplicate-rows-for-multiple-cascading-1m-child-tables)

> Unfortunately, the RETURNING clause of an INSERT can only work with columns from the inserted row. Columns added by a FROM clause are invisible there

> To work around this limitation, I suggest to SELECT before each INSERT, and generate prospective new serial IDs in advance with nextval(). Then you have each old and new ID in the same row to make necessary connections.

[don't do this](https://wiki.postgresql.org/wiki/Don't_Do_This)

[Database Concurrency in PostgreSQL](https://www.red-gate.com/simple-talk/databases/postgresql/database-concurrency-in-postgresql/)

[rise of the anti-join](https://www.reddit.com/r/PostgreSQL/comments/wqqe4h/comment/ikoxlzk/)

[How to optimise anti-join SQL queries](https://stackoverflow.com/questions/75790849/how-to-optimise-anti-join-sql-queries). [in Oracle](https://www.remote-dba.net/t_op_sql_anti_join.htm). [SQL server](https://sqlperformance.com/2018/03/sql-performance/row-goals-part-4-anti-join-anti-pattern).

> Even with index support this kind of anti-join grows expensive with very big numbers of used resources.

[Goodbye etcd, Hello PostgreSQL: Running Kubernetes with an SQL Database](https://lobste.rs/s/tzbluo/goodbye_etcd_hello_postgresql_running)

[How to write high-performance SQL for your Postgres database](https://stackoverflow.blog/2023/09/28/how-to-write-high-performance-sql-for-your-postgres-database/)

[How to work with pg_stat_statements](https://twitter.com/samokhvalov/status/1709069225762095258).

["Find-or-insert" using a single query](https://twitter.com/samokhvalov/status/1719635712545591630)

[companion databases — when and why you might want to add another database to your stack](https://postgres.fm/episodes/companion-databases)

[Designing Your Postgres Database for Multi-tenancy](https://www.crunchydata.com/blog/designing-your-postgres-database-for-multi-tenancy)

[Row Level Security with an ARRAY of tenants set in session parameter](https://dev.to/yugabyte/postgresql-row-level-security-with-an-array-of-tenants-2136)

[transaction isolation in Postgres](https://www.thenile.dev/blog/transaction-isolation-postgres)

[PostgreSQL internals: Things to know about update statements](https://news.ycombinator.com/item?id=38781442)

[notify for queues](https://twitter.com/tonialaribe/status/1742924612135198801)

[The Surprising Impact of Medium-Size Texts on PostgreSQL Performance](https://hakibenita.com/sql-medium-text-performance)

[I wish I could have a "weak" or optional foreign key](https://ryanguill.com/postgresql/sql/2024/01/08/postgresql-wishlist.html)

> I want to be able to say that if this key exists, it is in this table, but it might not exist any longer.

[Transactionally Staged Job Drains in Postgres](https://brandur.org/job-drain). [lobsters](https://lobste.rs/s/jtarg2/lessons_learned_from_payments_startups).

[Transforming Postgres into a Fast OLAP Database](https://news.ycombinator.com/item?id=39263760)

[What’s new in the Postgres 16 query planner / optimizer](https://www.citusdata.com/blog/2024/02/08/whats-new-in-postgres-16-query-planner-optimizer/)

[Postgres as queue](https://news.ycombinator.com/item?id=39323542)

[Postgres for everything](https://www.amazingcto.com/postgres-for-everything/)

[My Notes on Gitlab's Postgres Schema Design ](https://news.ycombinator.com/item?id=39413972)

> It is generally a good practice to not expose your primary keys to the external world. This is especially important when you use sequential auto-incrementing identifiers with type integer or bigint since they are guessable.

> In my work I have made the mistake of standardizing on primary key types. This means standardizing on either bigint or uuid so all tables will have the same type irrespective of their structure, access patterns, and growth rate.

[When to use JSON data type in database schema design?](https://shekhargulati.com/2022/01/08/when-to-use-json-data-type-in-database-schema-design/)

[Introduction to 'WITH' Queries and their Materialization](https://www.youtube.com/watch?v=0zf4HmWsISI). [slides](https://pgconf.in/files/presentations/2023/Divya_Sharma_CTE-pgconfInd2023.pdf). [rel8](https://hackage.haskell.org/package/rel8-1.5.0.0/docs/Rel8.html#v:materialize).

[JIT](https://news.ycombinator.com/item?id=39742916)

[vector similarity](https://twitter.com/denismagda/status/1775929905101877398)

[generated columns](https://www.postgresql.org/docs/current/ddl-generated-columns.html)

[Designing one-to-one relationships in PostgreSQL](https://gajus.com/blog/designing-one-to-one-relationships-in-postgresql)

[Crunchy Bridge for Analytics: Your Data Lake in PostgreSQL](https://news.ycombinator.com/item?id=40212811)

[psql's \d](https://news.ycombinator.com/item?id=40299761)

[transaction isolation in Postgres](https://www.thenile.dev/blog/transaction-isolation-postgres)


