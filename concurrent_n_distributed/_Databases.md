# Videos

[Modern SQL algorithms](https://www.youtube.com/watch?v=wTPGW1PNy_Y)

[Transactions and Concurrency Control Patterns by Vlad Mihalcea](https://www.youtube.com/watch?v=onYjxRcToto)

> [in MVCC] readers block readers to prevent dirty writes

> Hibernate provides many application-level concurrency control strategies.

[High-performance Hibernate](https://www.youtube.com/watch?v=BTdTEe9QL5k)

[The Bits of Postgres You Haven't Found Yet](https://devcenter.heroku.com/articles/postgres-the-bits-you-havent-found-yet)

[Transactions: myths, surprises and opportunities](https://www.youtube.com/watch?v=5ZjhNTM8XU8)

[distributed transactions lecture](https://www.youtube.com/watch?v=Npsy_zaQEWc)

[CMU Advanced Database Systems - 17 Cost Models (Spring 2018)](https://www.youtube.com/watch?v=kHrXCeB6jy0) [2016](https://www.youtube.com/watch?v=MyQzjba1beA&list=PLSE8ODhjZXjbisIGOepfnlbfxeH7TW-8O) [2017](https://www.youtube.com/watch?v=UGMLKsma_VU&list=PLSE8ODhjZXjYgTIlqf4Dy9KQpQ7kn1Tl0) [2018](https://www.youtube.com/watch?v=poEfLYH9W2M&list=PLSE8ODhjZXjYplQRUlrgQKwIAV3es0U6t)

[modern sql](https://www.reddit.com/r/Database/comments/a8aw2u/the_mother_of_all_query_languages_sql_in_modern/ec9hw99)

> I must admit to personally seeing the primary benefit of ORMs being for CRUD operations, namely when wiring entities and their relationships up to create / edit forms. And then lesser so on more simplistic (application-level) views using those entities where the query is real straightforward. When needing more complicated queries to get at a set of entities, or fast access to a subset of attributes, I prefer handrolled SQL as opposed to leaky abstraction DSLs atop SQL and / or in-language constructs like SQLAlchemy's expression syntax for static queries.

> That said, when it comes to non-uniform (say, form-driven queries), SQLAlchemy's expression syntax is much easier to work with and much more flexible than building query strings up by hand.

[The Mother of all Query Languages: SQL in Modern Times](https://www.youtube.com/watch?v=swR33jIhW8Q).

[6 Technical Challenges Developing a Distributed SQL Database](https://blog.yugabyte.com/6-technical-challenges-developing-a-distributed-sql-database/). []().

[Presto summit recap](https://www.starburstdata.com/technical-blog/nyc-presto-summit-recap)

# Slides

[Row Pattern Matching in SQL:2016](https://www.slideshare.net/MarkusWinand/row-pattern-matching-in-sql2016)

[Pagination Done the Right Way](https://www.slideshare.net/MarkusWinand/p2d2-pagination-done-the-postgresql-way)

[SQL Transactions - What they are good for and how they work](https://www.slideshare.net/MarkusWinand/sql-transactions-what-they-are-good-for-and-how-they-work)

[Linearizability](http://pub.ist.ac.at/courses/ppc10/slides/Linearizability.pptx)

[Implementing Dragon, Uber's data-integration tool for property graphs](https://www.reddit.com/r/haskell/comments/mbicfg/implementing_dragon_ubers_dataintegration_tool/). [Algebraic Property Graphs](https://www.youtube.com/watch?v=W3rpPnhw-nM). [data warehousing with cql](https://conexus.com/data-warehousing-with-cql/). [What is Enterprise Category Theory](https://conexus.com/what-is-enterprise-category-theory/). [Data Exchange Podcast (Episode 67): Ryan Wisnesky – Co-Founder of Conexus](https://conexus.com/data-exchange-podcast-episode-67-ryan-wisnesky-co-founder-of-conexus/). [Fast Left-Kan Extensions Using The Chase](https://conexus.com/fast-left-kan-extensions-using-the-chase/). [Informal Data Transformation Considered Harmful](https://conexus.com/informal-data-transformation-considered-harmful/). [Informal Data Transformation Considered Harmful](https://conexus.com/financial-reporting-data-warehousing-with-cql/). [Compositional Models for Power Systems](https://conexus.com/compositional-models-for-power-systems/). [Algebraic Property Graphs](https://conexus.com/algebraic-property-graphs/). [Categorical Data Integration for Computational Science](https://conexus.com/categorical-data-integration-for-computational-science/). [Dragon: Schema Integration at Uber Scale](https://eng.uber.com/dragon-schema-integration-at-uber-scale/). [meetup link](https://www.meetup.com/graph-database-south-bay/events/277103848/). [Categories for (Big) Data models and optimization](https://link.springer.com/article/10.1186/s40537-018-0132-9). [another meetup with more links](https://twitter.com/ConexusAI/status/1377349222131920897)

[How Database Cursors Help in Fetching Large Result sets from your SQL](https://www.youtube.com/watch?v=C1Y6P6vDFts). [Best Practices Working with Billion-row Tables in Databases
](https://www.youtube.com/watch?v=wj7KEMEkMUE). [Redis In-Memory Database Crash Course](https://www.youtube.com/watch?v=V7FPk4J10KI).

# Papers

[Serializable Snapshot Isolation in PostgreSQL](https://drkp.net/papers/ssi-vldb12.pdf)

[An Optimality Theory of Concurrency Control for Databases](http://www.eecs.harvard.edu/~htk/publication/1979-sigmod-kung-papadimitriou.pdf)

> Granted, serializability is (more or less) the most general means of maintaining database correctness. In what’s becoming one of my favorite “underground” (i.e., relatively poorly-cited) references, H.T. Kung and Christos Papadimitriou dropped a paper in SIGMOD 1979 on “An Optimality Theory of Concurrency Control for Databases.” In it, they essentially show that, if all you have are transactions’ syntactic modifications to database state (e.g., read and write) and no information about application logic, serializability is, in some sense, “optimal”: in effect, a schedule that is not serializable might modify the database state in a way that produces inconsistency for some (arbitrary) notion of correctness that is not known to the database.

[Serializability of concurrent database updates](http://publications.csail.mit.edu/lcs/pubs/pdf/MIT-LCS-TR-210.pdf)

[Serializable Isolation for Snapshot Databases](http://cahill.net.au/wp-content/uploads/2009/01/real-serializable.pdf)

[Highly Available Transactions: Virtues and Limitations](https://blog.acolyer.org/2014/11/07/highly-available-transactions-virtues-and-limitations/)

[A Critique of ANSI SQL Isolation Levels](http://www.cs.umb.edu/cs734/CritiqueANSI_Iso.pdf)

[Why do computer systems stop?](http://www.hpl.hp.com/techreports/tandem/TR-85.7.pdf)

[Spanner: Becoming a SQL System](http://dl.acm.org/citation.cfm?id=3056103&CFID=762920104&CFTOKEN=69453038) [hackernews](https://news.ycombinator.com/item?id=14337817)

[Amazon Aurora: Design Considerations for High Throughput Cloud-Native Relational Databases](http://dl.acm.org/citation.cfm?id=3056101)

[saner event sourcing](http://files.movereem.nl/2017saner-eventsourcing.pdf) [HN](https://mail.google.com/mail/u/0/?ui=2&ik=f79e395673&view=lg&msg=15cf024b9a2df3b9)

> I have worked on, or cleaned up, 4 different CQRS/ES projects. They have all failed. Each time the people leading the project and championing the architecture were smart, capable, technically adept folks, but they couldn't make it work.
There's more than one flavor of this particular arch, but Event Sourcing in general is simply not very useful for most projects. I'm sure there are use cases where it shines, but I have a hard time thinking of any. Versioning events, projection, reporting, maintenance, administration, dealing with failures, debugging, etc etc are all more challenging than with a traditional approach.

[D. Richard Hipp - SQLite - CMU Fall 2015](https://www.youtube.com/watch?v=gpxnbly9bz4) [earlier](https://news.ycombinator.com/item?id=17387851)

[Modern SQL](https://vimeo.com/289497563)

[Google Spanner podcast](https://overcast.fm/+E6UCazRsI)

# Posts

[Oracle serializable is not serializable](https://blog.dbi-services.com/oracle-serializable-is-not-serializable/)

[Quantifying isolation anomalies](https://blog.acolyer.org/2015/09/03/quantifying-isolation-anomalies/)

[Distributed Consistency and Session Anomalies](https://blog.acolyer.org/2016/02/26/distributed-consistency-and-session-anomalies/)

> In the database systems community, the gold standard is serializability. [...] In the distributed systems community, the gold standard is linearizability. 

> Both serializability and linearizability require (potentially expensive) coordination. Therefore just as we consider weaker isolation levels than serializable, we can also consider weaker consistency levels than linearizable. At weaker consistency levels non-linearizable phenomena (anomalies) can be observed.

> Serialisability is not stronger than SI or causal consistency. They are mutually incomparable. Serialisability allows the folowing anomaly w.r.t. Causality: user performs transaction T1 followed by T2; database executes them in the order T2 followed by T1. SI allows the write-skew anomaly, which SER disallows. The Strict Serialisability model is the only one stronger than both SI and CC (and Serialisability for that matter).

[The many faces of consistency](https://blog.acolyer.org/2017/01/12/the-many-faces-of-consistency/)

[A Beginner’s Guide to the True Order of SQL Operations](https://blog.jooq.org/2016/12/09/a-beginners-guide-to-the-true-order-of-sql-operations/)

[A beginner’s guide to database locking and the lost update phenomena](https://vladmihalcea.com/2014/09/14/a-beginners-guide-to-database-locking-and-the-lost-update-phenomena/)

[Quantified Comparison Predicates – Some of SQL’s Rarest Species](https://blog.jooq.org/2016/07/12/quantified-comparison-predicates-some-of-sqls-rarest-species/)

[NOT IN vs. NOT EXISTS vs. LEFT JOIN / IS NULL: MySQL](https://blog.jooq.org/2012/07/27/not-in-vs-not-exists-vs-left-join-is-null-mysql/)

[A True SQL Gem You Didn’t Know Yet: The EVERY() Aggregate Function](https://blog.jooq.org/2014/12/18/a-true-sql-gem-you-didnt-know-yet-the-every-aggregate-function/)

[serializable (for Oracle)](https://asktom.oracle.com/pls/asktom/f?p=100:11:0::::P11_QUESTION_ID:3233191441609)

[A beginner’s guide to read and write skew phenomena](https://vladmihalcea.com/2015/10/20/a-beginners-guide-to-read-and-write-skew-phenomena/)

[A beginner’s guide to the Phantom Read anomaly, and how it differs between 2PL and MVCC](https://vladmihalcea.com/2017/01/31/a-beginners-guide-to-the-phantom-read-anomaly-and-how-it-differs-between-2pl-and-mvcc/)

[group](http://mysqlmusings.blogspot.com.es/2012/06/binary-log-group-commit-in-mysql-56.html) [commit](https://mariadb.com/kb/en/mariadb/group-commit-for-the-binary-log/)

[info](http://www.remote-dba.net/t_op_sql_tuning_subqueries.htm) on [correlated](http://stackoverflow.com/questions/2577174/join-vs-sub-query) [subqueries](http://www.sqlservice.se/sql-server-performance-death-by-correlated-subqueries/) [correlated](https://en.wikipedia.org/wiki/Correlated_subquery) [correlated vs non-correlated](http://javarevisited.blogspot.com.es/2012/07/subquery-example-in-sql-correlated-vs.html) [in from](https://www.essentialsql.com/get-ready-to-learn-sql-server-22-using-subqueries-in-the-from-clause/)

[semijoins](https://en.wikipedia.org/wiki/Relational_algebra#Semijoin_.28.E2.8B.89.29.28.E2.8B.8A.29) [Semi Join and Anti Join Should Have Their Own Syntax in SQL](https://blog.jooq.org/2015/10/13/semi-join-and-anti-join-should-have-its-own-syntax-in-sql/) 

[Non-semi-join Subquery Optimizations in MariaDB](https://mariadb.com/kb/en/mariadb/non-semi-join-subquery-optimizations/) [mysql Optimizing Subqueries with the EXISTS Strategy](https://dev.mysql.com/doc/refman/5.7/en/subquery-optimization-with-exists.html)

[What is semi-join in database?](http://stackoverflow.com/questions/42249690/what-is-semi-join-in-database)

[lateral join](https://blog.heapanalytics.com/postgresqls-powerful-new-join-type-lateral/)

[How to Calculate Multiple Aggregate Functions in a Single Query](https://blog.jooq.org/2017/04/20/how-to-calculate-multiple-aggregate-functions-in-a-single-query/)

[The Sakila Database](https://www.jooq.org/sakila)

["The key, all the key, and nothing but the key"](https://en.wikipedia.org/wiki/Third_normal_form)

[UPSERT](https://wiki.postgresql.org/wiki/UPSERT) [MERGE](https://en.wikipedia.org/wiki/Merge_(SQL))

[SQL Select only rows with Max Value on a Column](http://stackoverflow.com/questions/7745609/sql-select-only-rows-with-max-value-on-a-column) [greatest n per group](http://stackoverflow.com/questions/tagged/greatest-n-per-group?sort=votes&pageSize=15)

[Mode Analytics on SQL Window Functions](https://community.modeanalytics.com/sql/tutorial/sql-window-functions/)

[transaction-log at DBA stack exchange](https://dba.stackexchange.com/questions/tagged/transaction-log?sort=votes&pageSize=15)

[PostgreSQL anti-patterns: read-modify-write cycles](https://blog.2ndquadrant.com/postgresql-anti-patterns-read-modify-write-cycles/) [HN discussion](https://news.ycombinator.com/item?id=13227078) [more on race conditions](http://stackoverflow.com/questions/6477574/do-database-transactions-prevent-race-conditions) [more](http://stackoverflow.com/questions/21464406/handling-race-conditions-in-postgresql) [more](http://stackoverflow.com/questions/40173258/prevent-race-condition-in-sql-transactions-for-data-integrity) [more](http://stackoverflow.com/questions/26081236/update-where-race-conditions-postgres-read-committed) [more](https://www.leighhalliday.com/avoid-race-conditions-with-postgres-locks) [more on DBA stack exchange](https://dba.stackexchange.com/questions/148/how-do-you-test-for-race-conditions-in-a-database) [Do database transactions prevent race conditions?](http://stackoverflow.com/questions/6477574/do-database-transactions-prevent-race-conditions)

> Optimistic concurrency control (or “optimistic locking”) is usually implemented as an application-side method for handling concurrency, often by object relational mapping tools like Hibernate.

> In this scheme, all tables have a version column or last-updated timestamp, and all updates have an extra WHERE clause entry that checks to make sure the version column hasn’t changed since the row was read. The application checks to see if any rows were affected by the UPDATE and if none were affected, treats it as an error and aborts the transaction.

> Unlike SERIALIZABLE isolation, it works even in autocommit mode or if the statements are in separate transactions. For this reason it’s often a good choice for web applications that might have very long user “think time” pauses or where clients might just vanish mid-session, as it doesn’t need long-running transactions that can cause performance problems.

> A key feature of this approach is that it lets you span work across multiple transactions, which is a big plus with systems that have high user counts and may have long delays between interactions with any given user.

> Rather than using locking and/or high isolation levels, it's common for ORMs like Hibernate, EclipseLink, etc to use optimistic concurrency control (often called "optimistic locking") to overcome the limitations of weaker isolation levels while preserving performance.

> Even with strong isolation some systems (like PostgreSQL) will abort conflicting transactions, rather than making them wait and running them serially. Your app must remember what it was doing and re-try the transaction. So while the transaction has prevented concurrency-related anomalies from being stored to the DB, it's done so in a manner that is not transparent to the application.

>  Some RDBMSs have stronger abilities than others. For example, PostgreSQL 9.2 and newer have quite good SERIALIZABLE isolation that detects most (but not all) possible interactions between transactions and aborts all but one of the conflicting transactions. So it can run transactions in parallel quite safely.

[select .. for update](http://stackoverflow.com/questions/10935850/when-to-use-select-for-update) [more](https://dev.mysql.com/doc/refman/5.7/en/innodb-locking-reads.html) [more](http://www.toadworld.com/platforms/oracle/w/wiki/1875.select-for-update)

[Clustered and Nonclustered Indexes Described](https://docs.microsoft.com/en-us/sql/relational-databases/indexes/clustered-and-nonclustered-indexes-described)

[PostgreSQL doesn't have the concept of clustered indexes at all. Instead, all tables are heap tables and all indexes are non-clustered indexes.](http://stackoverflow.com/questions/27978157/cluster-and-non-cluster-index-in-postgresql)

[Slow Postgres updates if OTHER columns are indexed?](https://dba.stackexchange.com/questions/84802/slow-postgres-updates-if-other-columns-are-indexed) [Efficient Use of PostgreSQL Indexes](https://devcenter.heroku.com/articles/postgresql-indexes)

> When this happens, a sequential scan is actually most likely much faster than an index scan, so the query planner has in fact correctly judged that the cost of performing the query that way is lower.

>  Postgres will decide to perform a sequential scan on any query that will hit a significant portion of a table. If you do have an index on that column, it will be a dead index that’s never used - and indexes are not free: they come at a cost in terms of storage and maintenance.

[Batch Writing, and Dynamic vs Parametrized SQL, how well does your database perform?](http://java-persistence-performance.blogspot.com.es/2013/05/batch-writing-and-dynamic-vs.html)

[Why Use Postgres (Updated for Last 5 Years)](http://www.craigkerstiens.com/2017/04/30/why-postgres-five-years-later/)

> Upsert was a work in progress for several years. It was one of those features that most people hacked around with CTEs, but that could create race conditions.

[you can create constraints to ensure only unique ranges in a table](https://news.ycombinator.com/item?id=14232074)

[Use row constructors to compare several values at once](https://dzone.com/articles/dont-use-the-string)

[Do you need a database transaction for reading data?](http://stackoverflow.com/questions/26327274/do-you-need-a-database-transaction-for-reading-data/26327536#26327536)

[rank in mysql](http://stackoverflow.com/questions/1895110/row-number-in-mysql)

[Understanding Weak Isolation Is a Serious Problem](http://www.bailis.org/blog/understanding-weak-isolation-is-a-serious-problem/)

[SQL/MED](https://en.wikipedia.org/wiki/SQL/MED) [Hacker News](https://news.ycombinator.com/item?id=14446350)

[UUID or GUID as Primary Keys? Be Careful!](https://tomharrisonjr.com/uuid-or-guid-as-primary-keys-be-careful-7b2aa3dcb439) [hacker news](https://news.ycombinator.com/item?id=14523523)

[Testing PostgreSQL for Fun](https://medium.com/@jonathangfischoff/testing-postgresql-for-fun-af891047e5fc)

[Postgres Transactions Aren’t Fully Isolated (clickbaity)](https://lobste.rs/s/wqw4s7/postgres_transactions_aren_t_fully)

[Is my implementation of type/subtype design pattern (for mutually exclusive subclasses) correct?](https://dba.stackexchange.com/questions/139092/is-my-implementation-of-type-subtype-design-pattern-for-mutually-exclusive-subc)

[Inventory management in MongoDB: A design philosophy I find baffling](https://ayende.com/blog/178785/inventory-management-in-mongodb-a-design-philosophy-i-find-baffling?Key=e9d8f617-cd97-4328-a380-e30e30c4f450) [HN](https://news.ycombinator.com/item?id=14625702)

[How do you update your production codebase/database schema without causing downtime?](https://softwareengineering.stackexchange.com/questions/35063/how-do-you-update-your-production-codebase-database-schema-without-causing-downt)

[How to handle unexpected schema changes to production database](https://softwareengineering.stackexchange.com/questions/235785/how-to-handle-unexpected-schema-changes-to-production-database)

[Zero Downtime Deployment with a Database](https://spring.io/blog/2016/05/31/zero-downtime-deployment-with-a-database)

[Customizing My Postgres Shell](https://www.citusdata.com/blog/2017/07/16/customizing-my-postgres-shell-using-psqlrc/)

[Practical Guide to SQL Transaction Isolation](https://begriffs.com/posts/2017-08-01-practical-guide-sql-isolation.html)

[Falsehoods programmers believe about geography](https://wiesmann.codiferes.net/wordpress/?p=15187)

[Using ENUM vs other types](https://dba.stackexchange.com/questions/6962/advantages-and-disadvantages-to-using-enum-vs-integer-types)

[JOIN Elimination: An Essential Optimiser Feature for Advanced SQL Usage](https://pay.reddit.com/r/programming/comments/6xdqeg/join_elimination_an_essential_optimiser_feature/)

[The best way to soft delete with Hibernate](https://vladmihalcea.com/2017/03/08/the-best-way-to-soft-delete-with-hibernate/)

[Deferrable Constraints in SQL Server](https://stackoverflow.com/questions/998095/deferrable-constraints-in-sql-server)

[How to update only a subset of entity attributes using JPA and Hibernate](https://vladmihalcea.com/2016/10/11/how-to-update-only-a-subset-of-entity-attributes-using-jpa-and-hibernate/)

[Hibernate: save, persist, update, merge, saveOrUpdate](http://www.baeldung.com/hibernate-save-persist-update-merge-saveorupdate)

[Database Decay and What To Do About It](https://cacm.acm.org/blogs/blog-cacm/208958-database-decay-and-what-to-do-about-it/fulltext)

[10 Cool SQL Optimisations That do not Depend on the Cost Model](https://www.reddit.com/r/programming/comments/7300db/10_cool_sql_optimisations_that_do_not_depend_on/)

[Storing JSON in database vs. having a new column for each key](https://stackoverflow.com/questions/15367696/storing-json-in-database-vs-having-a-new-column-for-each-key)

[sql optimization](https://stackoverflow.com/questions/tagged/sql+optimization) & [performance](https://stackoverflow.com/questions/tagged/sql+performance) on SO.

[Retrieving n rows per group](https://dba.stackexchange.com/questions/86415/retrieving-n-rows-per-group)

[apply](https://www.mssqltips.com/sqlservertip/1958/sql-server-cross-apply-and-outer-apply/) [so](https://stackoverflow.com/a/5180700/1364288)

> Note: Informix 12.10 xC2+ has Lateral Derived Tables and Postgresql (9.3+) has Lateral Subqueries which can be used to a similar effect.

[lateral clauses in SQL](http://www.hostitwise.com/hosting-blog/lateral-clauses-in-sql/)

> SQL;2003 allows a subquery in the from clause that is prefixed by lateral key word to access the attributes of preceding tables or sub queries in the from clause. Example SQL is given in the question.  Without the lateral clause, the sub query cannot access the correlation variable I1 from the outer query. Currently only few SQL implementations such as IBM DB2 support the lateral clause.

[Optimize GROUP BY query to retrieve latest record per user](https://stackoverflow.com/questions/25536422/optimize-group-by-query-to-retrieve-latest-record-per-user/25536748#25536748)

> There are things that a LATERAL join can do, but a (correlated) subquery cannot (easily). A correlated subquery can only return a single value, not multiple columns and not multiple rows

[Correlated subquery](https://en.wikipedia.org/wiki/Correlated_subquery)

> The effect of correlated subqueries can in some cases be obtained using joins. 

> Correlated subqueries may appear elsewhere besides the WHERE clause

[Taking a look at CROSS APPLY](http://weblogs.sqlteam.com/jeffs/archive/2007/10/18/sql-server-cross-apply.aspx)

> I think the easiest way to think of CROSS APPLY is that it is like doing a CROSS JOIN with a correlated sub-query instead of a derived table.  Let's see if I can explain that .... A derived table is "self-contained", in that all tables and columns in the parent SELECT are not accessible (though variables and parameters can be referenced).

[Subqueries](https://momjian.us/main/writings/pgsql/aw_pgsql_book/node2.html)

> A subquery can represent a fixed value, a correlated value, or a list of values. You can use any number of subqueries. You can also nest subqueries inside other subqueries.

[lateral](https://www.itjungle.com/2016/08/02/fhg080216-story03/) [lateral as alternative to group by](https://iggyfernandez.wordpress.com/2012/04/15/part-1-the-hitchhikers-guide-tosql/) [more lateral](https://blog.heapanalytics.com/postgresqls-powerful-new-join-type-lateral/) [even more lateral](https://medium.com/kkempin/postgresqls-lateral-join-bfd6bd0199df) [yet even more lateral](https://www.geekytidbits.com/lateral-join/) [and more](http://malisper.me/postgres-lateral-joins/) [on JOOQ](https://blog.jooq.org/tag/lateral-join/)

[10 Common Mistakes Java Developers Make when Writing SQL](https://blog.jooq.org/2013/07/30/10-common-mistakes-java-developers-make-when-writing-sql/)

> If you’re UPSERTING by chaining INSERT and UPDATE or by chaining SELECT .. FOR UPDATE and then INSERT or UPDATE, think again. Apart from risking race conditions, you might be able to express a simpler MERGE statement.

[Managing concurrency when using SELECT-UPDATE pattern](https://dba.stackexchange.com/questions/12698/managing-concurrency-when-using-select-update-pattern) [SQL Server 2012 potential race condition on select or insert](https://stackoverflow.com/questions/23446409/sql-server-2012-potential-race-condition-on-select-or-insert) [PostgreSQL anti-patterns: read-modify-write cycles](https://blog.2ndquadrant.com/postgresql-anti-patterns-read-modify-write-cycles/) [Handling race conditions in PostgreSQL
](https://stackoverflow.com/questions/21464406/handling-race-conditions-in-postgresql)

> While SERIALIZABLE transaction isolation is a clean solution, it is also rather expensive. 

[A (Probably Incomplete) Comprehensive Guide to the Many Different Ways to JOIN Tables in SQL](https://dzone.com/articles/a-probably-incomplete-comprehensive-guide-to-the-many-different-ways-to-join-tables-in-sql)

> This of course has nothing to do with relational algebra anymore, because it imposes a JOIN order (from left to right). But sometimes, that’s OK and sometimes, your table-valued function (or subquery) is so complex, that’s the only way you can actually use it.

[Postgres LATERAL JOIN](https://illuminatedcomputing.com/posts/2015/02/postgres_lateral_join/) [follow-up](https://illuminatedcomputing.com/posts/2015/02/lateral_join_alternatives)

> other options: Use GROUP BY in a subquery to get the latest inspection date, then use that date to get the rest of the inspection info. / Use a window function. / Use DISTINCT ON.

> Results for me take about 25ms. I’ve gotta say I love window functions, but it looks like in this case at least lateral join is a better choice.

[What is the difference between LATERAL and a subquery in PostgreSQL?](https://stackoverflow.com/questions/28550679/what-is-the-difference-between-lateral-and-a-subquery-in-postgresql) [https://stackoverflow.com/questions/1139160/when-should-i-use-cross-apply-over-inner-join]

> For returning more than one column, a LATERAL join is typically simpler, cleaner and faster.

> CROSS APPLY works better on things that have no simple JOIN condition.

> When there is a LIMIT in the subquery.

> You could probably do something like that using CTE's and window function [...]  but this is less readable and probably less efficient.

> See the end of Ariel's link. A row_number() query is just as nice and doesn't even require a join. So I don't think I should use cross apply for this situation (select top 3, partition by t1.id).

[What's the Hi/Lo algorithm?](https://stackoverflow.com/questions/282099/whats-the-hi-lo-algorithm)

[Managing database schemas without downtime](https://samsaffron.com/archive/2018/03/22/managing-db-schema-changes-without-downtime) [HN](https://news.ycombinator.com/item?id=16665447)

> We're using FlywayDB [0] and many of the ideas in Martin Fowler's _Evolutionary DB_ article [1]. When database changes are breaking, we use a pre-deploy and post-deploy "pair" to create an intermediate DB state that both application versions will run against.

[Evolutionary Database Design](https://www.martinfowler.com/articles/evodb.html)

[How do UPSERT and MERGE work in Oracle, SQL Server, PostgreSQL and MySQL](https://vladmihalcea.com/how-do-upsert-and-merge-work-in-oracle-sql-server-postgresql-and-mysql/)

[A beginner's guide to database locking and the lost update phenomena](https://vladmihalcea.com/a-beginners-guide-to-database-locking-and-the-lost-update-phenomena/)

[Volcano Iterator Model](https://db.in.tum.de/~grust/teaching/ws0607/MMDBMS/DBMS-CPU-5.pdf)

[Encapsulation of parallelism in the Volcano query processing system](https://blog.acolyer.org/2015/02/11/encapsulation-of-parallelism-in-the-volcano-query-processing-system/)

[Presto query optimizer at DataWorks Summit 2018](https://www.slideshare.net/kbajda/presto-query-optimizer-at-dataworks-summit-2018)

[Big News In Databases — Summer 2018](https://winand.at/newsletter/2018-07/sql-over-the-cloud-fsyncgate)

[A Simple Approach to Comparing Database Structures](https://spin.atomicobject.com/2018/07/10/compare-database-structures/)

[The most sucky thing about SQL's 3VL is how it breaks != predicates.](https://twitter.com/lukaseder/status/1040540300601683969). [NOT IN clause and NULL values](https://stackoverflow.com/questions/129077/not-in-clause-and-null-values).

> it's tricky to remember that NULLs are *always* excluded from such results, *except* if checked explicitly with the IS NULL predicate.

> This gets much worse when working with NOT IN, which is just != in disguise.

[How does the GROUP BY clause manage the NULL values?](https://stackoverflow.com/questions/22802078/how-does-the-group-by-clause-manage-the-null-values)

[10 SQL tricks that you didn’t think were possible](https://jaxenter.com/10-sql-tricks-that-you-didnt-think-were-possible-125934.html)

[Modern SQL: Evolution of a dinosaur](https://www.reddit.com/r/programming/comments/9gab4u/my_javazone_talk_modern_sql_evolution_of_a/)

[How to Use SQL UPDATE .. RETURNING to Run DML More Efficiently](https://blog.jooq.org/2018/09/26/how-to-use-sql-update-returning-to-run-dml-more-efficiently/).

[You can insert rows into many tables in one statement](https://twitter.com/sqldaily/status/1045342336841121792). [video](https://www.youtube.com/watch?v=lyRGbetFz9g).

[SQL Tricks And Tuning](https://blog.jooq.org/sql/). Great resource!

[How to Calculate Multiple Aggregate Functions in a Single Query](https://blog.jooq.org/2017/04/20/how-to-calculate-multiple-aggregate-functions-in-a-single-query/). GROUPING SETS works in DB2.

> Now, in the outer query, we’re using once COUNT(*), which simply counts all the rows regardless of any predicates in the CASE expressions. The other COUNT(expr) aggregate functions do something that surprisingly few people are aware of (yet a lot of people use this form “by accident”). They count only the number of non-NULL rows.

[values — Create Rows out of Nothing](https://modern-sql.com/feature/values).

[EXPLAIN EXTENDED](https://explainextended.com/2009/09/30/in-vs-join-vs-exists-oracle/).

> It builds a hash table on the outer query (the one that is probed). I repeat: it is the outer query that is hashed, not the inner one. Everything that needs to be returned in SELECT clause goes to the hash table

[Questions About CUBE, ROLLUP and GROUPING SETs That You Were Too Shy to Ask](https://www.red-gate.com/simple-talk/sql/t-sql-programming/questions-about-cube-rollup-and-grouping-sets-that-you-were-too-shy-to-ask/).

[Summarizing Data Using the GROUPING SETS Operator](https://www.red-gate.com/simple-talk/sql/t-sql-programming/summarizing-data-using-grouping-sets-operator/).

["Just because you are using @Hibernate, it does not mean you should not write SQL queries."](https://twitter.com/vlad_mihalcea/status/1050822977531629568). 

> Window Functions are the answer to many Query-related problems.

> Hibernate is an alternative to JDBC, not to SQL. Otherwise, why do you think there’s a createNativeQuery? The example is fairly simple in terms of SQL, and you don’t need to make everything generic, especially since this kind of query is business use case-oriented anyway.

[How to fetch entities multiple levels deep with Hibernate](https://vladmihalcea.com/hibernate-facts-multi-level-fetching/).

[How to map table rows to columns using SQL PIVOT or CASE expressions](https://vladmihalcea.com/how-to-map-table-rows-to-columns-using-sql-pivot-or-case-expressions/).

Ah, the multiple-join trick!!!!

[SQL Server UPSERT Patterns and Antipatterns](http://michaeljswart.com/2017/07/sql-server-upsert-patterns-and-antipatterns/).

[What are the most common SQL anti-patterns?](https://stackoverflow.com/questions/346659/what-are-the-most-common-sql-anti-patterns).

[Query pagination with JPA and Hibernate](https://vladmihalcea.com/query-pagination-jpa-hibernate/).

> The JPA query pagination is not limited to entity queries that return entities only. You can use it for DTO projections as well.

> Markus Winand, who wrote the SQL Performance Explained book, advocates for Keyset pagination instead of Offset.

[Entities or DTOs – When should you use which projection?](https://www.thoughts-on-java.org/entities-dtos-use-projection/). [SO](https://stackoverflow.com/questions/23719237/mapping-jpa-or-hibernate-projection-query-to-dto-data-transfer-object). [The best way to map a projection query to a DTO (Data Transfer Object) with JPA and Hibernate](https://vladmihalcea.com/the-best-way-to-map-a-projection-query-to-a-dto-with-jpa-and-hibernate/).

[How to Extract a Date Part in SQL](https://blog.jooq.org/2015/02/25/how-to-extract-a-date-part-in-sql/).

[How to Get NULLs Horribly Wrong in SQL Server](https://www.red-gate.com/simple-talk/sql/t-sql-programming/how-to-get-nulls-horribly-wrong-in-sql-server/).

> As great as the NULLIF function is for handling certain situations, such as avoiding divide-by-zero errors

[Consider Using [NOT] EXISTS Instead of [NOT] IN](https://dzone.com/articles/consider-using-not-exists-instead-of-not-in-subque).

[Is your query too complex for JPA and Hibernate?](https://www.thoughts-on-java.org/query-complex-jpa-hibernate/).

[What the SQL?!? Lateral Joins](https://ddrscott.github.io/blog/2017/what-the-sql-lateral/). [BULK NEAREST NEIGHBOR USING LATERAL JOINS](https://carto.com/blog/lateral-joins/). [Reuse Calculations in the Same Query with Lateral Joins](https://www.periscopedata.com/blog/reuse-calculations-in-the-same-query-with-lateral-joins). [lateral join pgcast](https://www.pgcasts.com/episodes/6/lateral-joins/). [Optimise a LATERAL JOIN query on a big table](https://dba.stackexchange.com/questions/143044/optimise-a-lateral-join-query-on-a-big-table).

> In SQL, a lateral join can basically be seen as some sort of loop. 

> Reusing parts of computations has long been a wart in SQL. Let’s say you want to compute confidence intervals for your signup rate. You’ll have to use the standard error calculation twice: once for the upper bound, and once for the lower bound.

> This is where lateral joins shine. Postgres’s latest join type solves this problem by letting you make the calculation in one join, and then reference the results of that calculation in subsequent joins.

> Careful readers will notice we’re using a cartesian join. This is a join of the form from a, b, c, which is shorthand for from a join b on true join c on true. It creates a row for every possible combination of rows in the joined table. In our case, where each joined table computes a single value, this just has the effect of appending calculations and then reusing them for the next calculation.

> The final version is almost as easy to read as a mathematical formula! We simply define a variable, use it in the next calculation, rinse and repeat.

[GROUP BY + CASE statement](https://stackoverflow.com/a/19849537/1364288).

> An output column's name can be used to refer to the column's value in  ORDER BY and GROUP BY clauses, but not in the WHERE or HAVING clauses; there you must write out the expression instead.

[Select first row in each GROUP BY group?](https://stackoverflow.com/questions/3800551/select-first-row-in-each-group-by-group). [https://stackoverflow.com/a/25536748/1364288](https://stackoverflow.com/a/25536748/1364288). [Optimize groupwise maximum query](https://stackoverflow.com/questions/24244026/optimize-groupwise-maximum-query/24377356#24377356). [Query last N related rows per row](https://stackoverflow.com/questions/25957558/query-last-n-related-rows-per-row).

[FIRST_VALUE and LAST_VALUE Window Function Examples](https://docs.aws.amazon.com/redshift/latest/dg/r_Examples_of_firstlast_WF.html).

[Naming unnamed columns](https://modern-sql.com/use-case/naming-unnamed-columns).

[Query drafting without table](https://modern-sql.com/use-case/query-drafting-without-table)

https://use-the-index-luke.com/sql/myth-directory/dynamic-sql-is-slow

https://modern-sql.com/use-case/reduce-network-latency-for-insert

https://modern-sql.com/use-case/pivot

https://sqlperformance.com/2014/06/t-sql-queries/dirty-secrets-of-the-case-expression

https://jaxenter.com/10-sql-tricks-that-you-didnt-think-were-possible-125934.html

https://www.sqlteam.com/articles/how-to-use-group-by-with-distinct-aggregates-and-derived-tables

https://dba.stackexchange.com/questions/77130/how-do-i-select-data-with-a-case-statement-and-group-by

https://modern-sql.com/concept/null#aggregates

https://docs.microsoft.com/es-es/sql/connect/jdbc/using-sql-escape-sequences

http://media.datadirect.com/download/docs/slnk/devref/scalarfn.html

[High-Performance Hibernate Tutorial](https://vladmihalcea.com/tutorials/hibernate/).

[How does a Recursive CTE run, line by line?](https://stackoverflow.com/questions/3187850/how-does-a-recursive-cte-run-line-by-line). [great answer](https://stackoverflow.com/a/3187907/1364288). [SQL Server: are the recursive CTE’s really set-based?](https://explainextended.com/2009/11/18/sql-server-are-the-recursive-ctes-really-set-based/). [Average sum with start end end date](https://stackoverflow.com/questions/51463233/average-sum-with-start-end-end-date). [7 Unfolding | Set Based Approach | Create Attendance Report](https://www.youtube.com/watch?v=CWrR6U9n-8E). [Recursive CTE SQL Get all Levels](https://stackoverflow.com/questions/46814736/recursive-cte-sql-get-all-levels). [Connection between codata and greatest fixed points](https://mathoverflow.net/questions/128262/connection-between-codata-and-greatest-fixed-points). [Recursive CTEs Explained](https://www.essentialsql.com/recursive-ctes-explained/). [Re-Inventing the Recursive CTE](http://dataeducation.com/re-inventing-the-recursive-cte/).

[Oracle Database Express Edition (XE) Release 18.4.0.0.0 (18c) was released on October 19, 2018].(https://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html)

The Data Geekery SQL masterclass. [Day 1](https://www.jooq.org/training/SQL/Day1.pdf). [Day 2](https://www.jooq.org/training/SQL/Day2.pdf).

[More stuff on lateral joins, including comparisons with other approaches. When are they a valid alternative to window functions?](https://blog.jooq.org/tag/lateral-join/)

> Note that thanks to the aggregation step “happening before” the windowing step, we can use aggregation functions inside of window functions.

> In the old days when databases like Oracle didn’t really support LIMIT (or when using DB2, SQL Server, and Sybase, which support “LIMIT” but not “OFFSET”), people used to resort to using window functions. 

[basic CTEs](https://dev.to/helenanders26/why-you-should-use-sql-ctes-25lk).

[The LATERAL join](https://www.geekytidbits.com/lateral-join/)

> This is a non-obvious use of LATERAL but one I use often. Since you can reference columns from other records in the query, you can use LATERAL to calculate values and then reuse them in the main SELECT statement. Otherwise, you would have to recalculate values for each usage of them in the SELECT statement.

[How to Reduce Syntactic Overhead Using the SQL WINDOW Clause](https://dzone.com/articles/how-to-reduce-syntactic-overhead-using-the-sql-win).

[Been helping a customer tune their SQL](https://twitter.com/lukaseder/status/1057325329155571713).

> many devs, even seasoned ones, don't think of pivoting in SQL.

> we're still investigating if there could be more composite indexes rather than individual column indexes

> using a "projection" (or just use SQL, e.g. through jOOQ) is almost always worth it if you don't really need the entity. Why? - data transfer size - memory consumption on client and server - join elimination

[“Hidden” Efficiencies of Non-Partitioned Indexes on Partitioned Tables Part III](https://richardfoote.wordpress.com/2018/10/25/hidden-efficiencies-of-non-partitioned-indexes-on-partitioned-tables-part-iii-ricochet/).

[How to merge entity collections with JPA and Hibernate](https://vladmihalcea.com/merge-entity-collections-jpa-hibernate/).

[SQL does not cease to amaze me](https://twitter.com/lukaseder/status/1060528326152986627).

> 6-digit daily customer sessions with roughly 1.5B SQL queries per day. Its Oracle database uses 4 cores only. The median number of operations in v$sql_plan is 50. The max is 2670.

> The impressive thing here is how many execution plans are more complex than 50 operations. Some are monster SQL queries with tons of complex business logic encoded in them. Still no problemo for Oracle.

[Random slowdown](https://jonathanlewis.wordpress.com/2013/12/23/plan-changes/).

https://use-the-index-luke.com/blog/2011-07-16/planning-for-reuse
https://use-the-index-luke.com/sql/where-clause/obfuscation/smart-logic
https://use-the-index-luke.com/sql/where-clause/bind-parameters
https://use-the-index-luke.com/sql/myth-directory/dynamic-sql-is-slow
https://use-the-index-luke.com/sql/where-clause/bind-parameters
https://use-the-index-luke.com/sql/myth-directory
https://use-the-index-luke.com/sql/myth-directory/most-selective-first
https://use-the-index-luke.com/sql/myth-directory/dynamic-sql-is-slow

column histograms

https://docs.oracle.com/database/121/TGSQL/tgsql_histo.htm#TGSQL366
http://www.dba-oracle.com/art_otn_cbo_p4.htm
http://www.dba-oracle.com/art_builder_histo.htm

> Important note:  If your database exclusively uses bind variables, Oracle recommends deleting any existing Oracle histograms and disabling Oracle histogram generation (method opt) for any future dbms_stats analysis.  This approach will use the number if distinct values to determine the selectivity of a column.

> The central problem with cardinality estimation is the in cases of complex WHERE clauses the optimizer does not have enough information about inter-join result set sizes to determine the optimal table join order. 

> Column histograms should be created only when you have highly-skewed values in a column. This rarely occurs, and a common mistake that a DBA can make is the unnecessary collection of histograms in the statistics. Histograms tell the CBO when a column's values aren't distributed evenly, and the CBO will then use the literal value in the query's WHERE clause and compare it to the histogram statistics buckets.

[Query Tuning Fundamentals: Density, Predicates, Selectivity, and Cardinality](https://blogs.msdn.microsoft.com/bartd/2011/01/25/query-tuning-fundamentals-density-predicates-selectivity-and-cardinality/)

[Cost Control: Inside the Oracle Optimizer](http://www.dba-oracle.com/art_otn_cbo_p8.htm)

> A column histogram should only be created when we have data skew exists or is suspected. In the real world,   that happens rarely, and one of the most common mistakes with the optimizer is the unnecessary introduction of histograms into optimizer statistics

[an overview of query optimization](https://web.stanford.edu/class/cs345d-01/rl/chaudhuri98.pdf)

[Optimize SQL Server Queries with Index Statistics](https://blog.learningtree.com/optimize-sql-server-queries-index-statistics/).

> What happened? SQL Server will not auto-parameterize a query plan unless the optimal plan is the same for all possible values of the parameter. Now that there is an index, there are some regions, like Delaware, for which the optimal plan uses the index, and there are other regions, like California, for which using the index would be a poor choice.

> For this index, the cutoff between using an index and not using an index was somewhere between 1.6 and 1.9% of the number of rows in the table. These numbers will vary for other indexes and other tables since they depend on more than just number of rows. The depth of the clustered index depends on things like the width of the index keys and does not scale linearly as the table grows in size. Nevertheless, the lesson is clear; once you are requesting more than a relatively small percentage of rows in a table, an index will probably not be useful.

[13 Things You Should Know About Statistics and the Query Optimizer](https://www.red-gate.com/simple-talk/sql/t-sql-programming/13-things-you-should-know-about-statistics-and-the-query-optimizer/).

[Getting the Most from Oracle's Cost-Based Optimizer](https://www.akadia.com/services/oratips/costbased_optimizer/optm.htm).

[bind variable peeking](https://blogs.sap.com/2013/06/13/oracle-db-optimizer-part-vi-effects-of-disabled-bind-variable-peeking-adaptive-cursor-sharing-and-cardinality-feedback-on-the-cbo-in-sap-environments/). [more](https://asktom.oracle.com/pls/apex/asktom.search?tag=bind-variable-peeking). [Understanding SQL Query Parsing: Part 4 – Understanding Bind Variable Peeking](https://www.red-gate.com/simple-talk/sql/oracle/understanding-sql-query-parsing-part-4-understanding-bind-variable-peeking/). [hard parse vs. soft parse](http://www.dba-oracle.com/t_hard_vs_soft_parse_parsing.htm).

> We have seen that the optimizer does nonsense cardinality calculations in various cases by using bind variables

[Planning For Reuse](https://use-the-index-luke.com/blog/2011-07-16/planning-for-reuse)

> Oracle uses bind peeking and introduced adaptive cursor sharing with 11g. SQL Server uses parameter sniffing and query hints. DB2 has the re-optimizing hint REOPT.

> The hint based approaches will essentially disable execution plan re-use for the respective statement. Oracle's adaptive cursor sharing supports multiple execution plans per SQL string and learns from slow executions.

[How to configure DB2 REOPT Property within Websphere Console?](https://developer.ibm.com/answers/questions/401186/how-to-configure-db2-reopt-property-within-websphe/)

> REOPT can only be changed for static SQL but not dynamic SQL. Websphere uses the JDBC driver for connectivity to DB2. There are no JDBC driver properties which can be set to change the REOPT level.

[Thomas Müller's (author of H2) answers on Stack Overflow](https://stackoverflow.com/users/382763/thomas-mueller?tab=answers).

[Does one get ever used to writing JPA criteria query?](https://twitter.com/lukaseder/status/1072493710930272256). [JPA Criteria vs JOOQ](https://twitter.com/lukaseder/status/1072491086180954112). [jooq javadocs](http://www.jooq.org/javadoc/3.7.0/org/jooq/Select.html). [jooq aliases](https://www.jooq.org/doc/3.0/manual/sql-building/column-expressions/aliased-columns/).

[Why Did We Shift Away From Database-Generated Ids?](https://medium.com/ingeniouslysimple/why-did-we-shift-away-from-database-generated-ids-7e0e54a49bb3).

[database migration example](https://geshan.com.np/blog/2018/05/how-to-do-a-zero-downtime-database-db-migration-schema-change-with-a-practical-example/).

[what if you delete without where](https://news.ycombinator.com/item?id=15188619)

[A Primer on Database Replication](https://www.brianstorti.com/replication/).

[Indexing Group By](https://use-the-index-luke.com/sql/sorting-grouping/indexed-group-by)

[SQL GROUP BY and Functional Dependencies: A Very Useful Feature](https://blog.jooq.org/2015/12/10/sql-group-by-and-functional-dependencies-a-very-useful-feature/).

[How to Find the Longest Consecutive Series of Events in SQL](https://blog.jooq.org/2015/11/07/how-to-find-the-longest-consecutive-series-of-events-in-sql/)

[Row pattern matching](https://twitter.com/sqldaily/status/1090927713257488385)

[Indexes: the neglected performance all-rounder](https://www.slideshare.net/MarkusWinand/indexes-neglectedperformanceallrounder)

[Support for LATERAL derived tables added to MySQL 8.0.14](https://mysqlserverteam.com/support-for-lateral-derived-tables-added-to-mysql-8-0-14/).

[Rolling Retention Done Right in SQL](https://twitter.com/ModernSQL/status/1094187760506818561)

[SQL in Haskell](https://twitter.com/acid2/status/1100733724273139713)

[How to log the database transaction id using MDC (Mapped Diagnostic Context)](https://vladmihalcea.com/log-database-transaction-id-mdc-logging/).

[sum types in SQL](https://www.parsonsmatt.org/2019/03/19/sum_types_in_sql.html). [so](https://stackoverflow.com/questions/46655478/database-super-type-sub-type-design?noredirect=1&lq=1). [more](https://dba.stackexchange.com/questions/193394/is-it-a-bad-practice-to-have-several-mutually-exclusive-one-to-one-relationships).

[How to Calculate Multiple Aggregate Functions in a Single Query](https://blog.jooq.org/2017/04/20/how-to-calculate-multiple-aggregate-functions-in-a-single-query/)

[The Cost of Useless Surrogate Keys in Relationship Tables](https://blog.jooq.org/2019/03/26/the-cost-of-useless-surrogate-keys-in-relationship-tables/)

[unreasonable effectiveness of SQL](https://blog.couchbase.com/unreasonable-effectiveness-of-sql/)

[let's build a simple database](https://news.ycombinator.com/item?id=19581721)

[Alternative to EAV for dynamic fields in a star schema data warehouse](https://dba.stackexchange.com/questions/64689/alternative-to-eav-for-dynamic-fields-in-a-star-schema-data-warehouse)

[Writing a simple bank schema: How should I keep my balances in sync with their transaction history?](https://dba.stackexchange.com/questions/5608/writing-a-simple-bank-schema-how-should-i-keep-my-balances-in-sync-with-their-t)

[CDC with Kafka](https://www.infoq.com/news/2019/04/change-data-capture-debezium)

[How does MVCC (Multi-Version Concurrency Control) work](https://vladmihalcea.com/how-does-mvcc-multi-version-concurrency-control-work/)

> The only use case that can still generate contention is when two concurrent transactions try to modify the same record since, once modified, a row is always locked until the transaction that modified this record either commits or rolls back.

[How does database pessimistic locking interact with INSERT, UPDATE, and DELETE SQL statements](https://vladmihalcea.com/how-does-database-pessimistic-locking-interact-with-insert-update-and-delete-sql-statements/)

> Once the database records are locked, no UPDATE statement can modify them, even on a MVCC database engine.

[A beginner’s guide to Java Persistence locking](https://vladmihalcea.com/a-beginners-guide-to-java-persistence-locking/)

> As previously explained, there are two types of explicit locking mechanisms: pessimistic (physical) and optimistic (logical). In this post, I’m going to explain how explicit pessimistic locking interacts with non-query DML statements (e.g. insert, update, and delete).

> Once the database records are locked, no UPDATE statement can modify them, even on a MVCC database engine.

[How to deadlock yourself in three simple steps](https://www.idug.org/p/bl/et/blogaid=535) very good!

> (about UR) This is obviously not suitable for transactional applications, but can have perfect uses in the Business Intelligence or Analytics type applications.

> Cursor Stability (CS) in which DB2, like RR and RS, ensures that an application with isolation level CS doesn’t read a row that another process has changed until that other process has released the row. Unlike RR, however, CS allows other applications to change rows that the application with isolation level CS has read. This provides for a high level of stability with a high level of concurrency and is the default isolation level.

[FOR UPDATE WITH RS USE AND KEEP UPDATE LOCKS](https://stackoverflow.com/a/3916426/1364288)

[Ways of Avoiding the Read-Modify-Write Anti-Pattern When Using Spring Data?](https://stackoverflow.com/questions/48228458/ways-of-avoiding-the-read-modify-write-anti-pattern-when-using-spring-data)

[Optimistic locking automatic retry](https://enterprisecraftsmanship.com/2017/09/18/optimistic-locking-automatic-retry/)

> You generally want to avoid situations when one user overrides changes made by another user without even looking at them. 

[How to retry JPA transactions after an OptimisticLockException](https://vladmihalcea.com/optimistic-locking-retry-with-jpa/)

[Optimistic locking in ws](https://www.ibm.com/support/knowledgecenter/en/SSZLC2_7.0.0/com.ibm.commerce.admin.doc/concepts/cpmoptlock.htm)

> Optimistic locking allows you to lower the isolation level that you use in an application so that fewer locks are placed on the database assets. It allows more applications to run concurrently against the database, and potentially increase the throughput of your applications.

> To protect against potential database integrity problems brought on by lowering the isolation level, an optimistic locking implementation has to ensure that no integrity problems occur. The WebSphere Commerce implementation utilizes an optimistic predicate column for each table in the WebSphere Commerce database - OPTCOUNTER. 

> In this way, the implementation can guarantee that a row in the database has not changed between the time it was read and the time it was written, to protect the integrity of the database.

[When to use select for update?](https://stackoverflow.com/questions/10935850/when-to-use-select-for-update)

[Locking in JBoss](https://docs.jboss.org/hibernate/orm/4.0/devguide/en-US/html/ch05.html)

> When your application uses long transactions or conversations that span several database transactions, you can store versioning data, so that if the same entity is updated by two conversations, the last to commit changes is informed of the conflict, and does not override the other conversation's work. This approach guarantees some isolation, but scales well and works particularly well in Read-Often Write-Sometimes situations.

> Hibernate provides two different mechanisms for storing versioning information, a dedicated version number or a timestamp.

> Typically, you only need to specify an isolation level for the JDBC connections and let the database handle locking issues. If you do need to obtain exclusive pessimistic locks or re-obtain locks at the start of a new transaction, Hibernate gives you the tools you need.

> WebSphere Commerce uses an optimistic locking scheme that allows the database transaction isolation level to be lowered from repeatable read to read committed. Using that scheme, database rows not normally accessed concurrently are not locked with an intent to update when they are read. Instead, when the update is eventually made, the row is checked to make sure it has not been updated concurrently since it was read. If it has been updated concurrently, then the transaction is rolled back and the command may be restarted from the beginning in a new transaction, if appropriate.

[Isolation level: pessimistic vs. optimistic](https://social.msdn.microsoft.com/Forums/windows/en-US/c74fe52d-6305-4110-b429-2091c5a4de6a/isolation-level-pessimistic-vs-optimistic?forum=sqldatabaseengine)

> Let me add to the confusion.  From an application perspective, optimistic concurrency can be implemented in the application layer even though the database engine uses pessimistic locking.  This is often done by checking to see if the row was changed since initially retrieved by comparing the before/current values (or just rowversion column) when performing updates and deletes. This technique allows a row to be retrived without holding long-term locks.

[A beginner’s guide to database locking and the lost update phenomena](https://vladmihalcea.com/a-beginners-guide-to-database-locking-and-the-lost-update-phenomena/). [How to prevent lost updates in long conversations](https://vladmihalcea.com/a-beginners-guide-to-database-locking-and-the-lost-update-phenomena/).

[Data masking](https://www.ibm.com/support/knowledgecenter/en/SSBLQQ_9.2.0/com.ibm.rational.rit.ref.doc/topics/c_ritref_data_masking.html). [wiki](https://en.wikipedia.org/wiki/Data_masking).

[Well-known Databases Use Different Approaches for MVCC](https://www.enterprisedb.com/blog/well-known-databases-use-different-approaches-mvcc)

[MVCC Part 2: Pretty Pictures and Some Examples](https://www.nuodb.com/techblog/mvcc-part-2-pretty-pictures-and-some-examples)

[skip locked](https://vladmihalcea.com/database-job-queue-skip-locked/)

[Entity-Attribute-Value (EAV) The Antipattern Too Great to Give-up](https://www.sqlsaturday.com/SessionDownload.aspx?suid=12267). [eav horror](https://stackoverflow.com/questions/55745721/compare-numerically-in-varchar-column/55749407#55749407). [EAV - is it really bad in all scenarios?](https://softwareengineering.stackexchange.com/questions/93124/eav-is-it-really-bad-in-all-scenarios). [The Anti-Pattern – EAV(il) Database Design ?](https://mikesmithers.wordpress.com/2013/12/22/the-anti-pattern-eavil-database-design/). [Avoiding the EAV of Destruction](https://www.red-gate.com/simple-talk/sql/t-sql-programming/avoiding-the-eav-of-destruction/). [To EAV, or not to EAV? Choosing your data model](https://wq.io/1.1/docs/eav-vs-relational). [EAV is an anti-pattern?](https://news.ycombinator.com/item?id=12410808). [Should I use EAV database design model or a lot of tables](https://stackoverflow.com/questions/15249562/should-i-use-eav-database-design-model-or-a-lot-of-tables).

> If you want to allow user-defined fields in a relational database, your realistic are either EAV or stuff json into a text column. EAV, if done extremely carefully, can be a good solution, but 99% of the time, it's going to be a huge pain.

> Users could add attributes (columns) at any time without you being involved?

> There are other approaches however. You could consider an XML field with extended data or, if you are on PostgreSQL 9.2, a JSON field (XML is easier to search though). This would give you a significantly larger range of possible searches without the headaches of EAV. The tradeoff would be that schema enforcement would be harder.

[The JPA EntityManager createNativeQuery is a Magic Wand](https://vladmihalcea.com/the-jpa-entitymanager-createnativequery-is-a-magic-wand/)

[table functions](https://stevenfeuersteinonplsql.blogspot.com/2015/04/table-functions-introduction-and.html)

[Managing database schema changes without downtime](https://news.ycombinator.com/item?id=16665447). [DPC2018: Zero Downtime Database Migrations and Deployments - Ondrej Mirtes](https://www.youtube.com/watch?v=hMO63IC6R7c). [Managing db schema changes without downtime](https://samsaffron.com/archive/2018/03/22/managing-db-schema-changes-without-downtime). [Expand-contract](https://news.ycombinator.com/item?id=11051295).

More videos on database migrations https://www.youtube.com/watch?v=RUIUUZehGgI https://www.youtube.com/watch?v=hMO63IC6R7c https://www.youtube.com/watch?v=SAkNBiZzEX8 https://www.youtube.com/watch?v=CsGb3X7W9P0

[What is faster, one big query or many small queries?](https://dba.stackexchange.com/questions/76973/what-is-faster-one-big-query-or-many-small-queries).

[time series database](https://news.ycombinator.com/item?id=19825566)

> Apache Druid. The killer for us is that we allow essentially ad-hoc querying over long time intervals, but require the results to be returned quickly. And the dataset, while not Google proportions, isn't small.

[What is Druid?](http://druid.io/docs/latest/design/index.html). [How To Use Kafka and Druid to Tame Your Router Data
](https://kafka-summit.org/sessions/use-kafka-druid-tame-router-data-2/). [Aggregations](http://druid.io/docs/latest/querying/aggregations).

> Approximate algorithms. Druid includes algorithms for approximate count-distinct, approximate ranking, and computation of approximate histograms and quantiles. These algorithms offer bounded memory usage and are often substantially faster than exact computations. For situations where accuracy is more important than speed, Druid also offers exact count-distinct and exact ranking.

> Automatic summarization at ingest time. Druid optionally supports data summarization at ingestion time. This summarization partially pre-aggregates your data, and can lead to big costs savings and performance boosts.

> In addition to stream processing, data needs to be stored in a redundant, operationally focused database to provide fast, reliable answers to critical questions. Together, Kafka and Druid work together to create such a pipeline.

> Aggregations can be provided at ingestion time as part of the ingestion spec as a way of summarizing data before it enters Apache Druid (incubating). Aggregations can also be specified as part of many queries at query time.

[Druid -- A Real-time Analytical Data Store](https://twitter.com/gunnarmorling/status/1599129860277866496). [post](https://www.micahlerner.com/2022/05/15/druid-a-real-time-analytical-data-store.html).

[Snapshot Isolation in SQL Server](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/sql/snapshot-isolation-in-sql-server).

> SQL Server introduced extensions to the SQL-92 isolation levels with the introduction of the SNAPSHOT isolation level and an additional implementation of READ COMMITTED. 

> A snapshot transaction always uses optimistic concurrency control, withholding any locks that would prevent other transactions from updating rows. If a snapshot transaction attempts to commit an update to a row that was changed after the transaction began, the transaction is rolled back, and an error is raised.

[If Eventual Consistency Seems Hard, Wait Till You Try MVCC](https://www.xaprb.com/blog/2014/12/08/eventual-consistency-simpler-than-mvcc/).

> One of the logical necessities, for example, is that you can only modify the latest version of a row (eventually, at least). If you try to update an old version (the version contained in your consistent snapshot), you’re going to get into trouble. 

[Am I designing this database right?](https://twitter.com/lukaseder/status/1125758226488811525)

[To ORM or not to ORM?](https://news.ycombinator.com/item?id=19850452)

[modern SQL slides](https://twitter.com/MarkusWinand/status/1126480424157569024)

[How to expose Hibernate Statistics via JMX](https://vladmihalcea.com/hibernate-statistics-jmx/)

[How to store schema-less EAV (Entity-Attribute-Value) data using JSON and Hibernate](https://vladmihalcea.com/how-to-store-schema-less-eav-entity-attribute-value-data-using-json-and-hibernate/)

[a tale of query optimization](https://parallelthoughts.xyz/2019/05/a-tale-of-query-optimization/)

[Persisting Enums in JPA](https://www.baeldung.com/jpa-persisting-enums-in-jpa)

[LSM-based Storage Techniques: A Survey](https://arxiv.org/pdf/1812.07527.pdf)

[Experiences with approximating queries in Microsoft’s production big-data clusters](https://blog.acolyer.org/2019/09/09/ms-approx-query/)

[FoundationDB Record Layer](http://smalldatum.blogspot.com/2019/09/foundationdb-record-layer.html)

[Procella: unifying serving and analytical data at YouTube](https://blog.acolyer.org/2019/09/11/procella/)

[Even more amazing papers at VLDB 2019](https://twitter.com/adriancolyer/status/1175074645072130048)

[Notes on data modeling from Handbook of Relational Database Design](https://lobste.rs/s/fanuhi/notes_on_data_modeling_from_handbook)

[Just learn SQL](https://news.ycombinator.com/item?id=21031187)

[cool SQL queries you have written](https://twitter.com/b0rk/status/1175068822107279362)

[Choosing a cloud DBMS: architectures and tradeoffs](https://blog.acolyer.org/2019/08/30/choosing-a-cloud-dbms/)

[Modern Data Practice and the SQL Tradition](https://tselai.com/modern-data-practice-and-the-sql-tradition.html). [HN](https://news.ycombinator.com/item?id=21482114)

[we do not use foreign keys](https://news.ycombinator.com/item?id=21486494)

[The next 50 years of databases](http://www.cs.cmu.edu/~pavlo/blog/2015/09/the-next-50-years-of-databases.html). [HN](https://news.ycombinator.com/item?id=21508210).

[Why do databases cry at night?](https://www.youtube.com/watch?v=CUbZ5tNZi7M)

[The joy of database configuration](http://smalldatum.blogspot.com/2019/11/the-joy-of-database-configuration.html)

[Throttling writes: LSM vs B-Tree](http://smalldatum.blogspot.com/2019/11/throttling-writes-lsm-vs-b-tree.html)

[sqlite is serverless](https://news.ycombinator.com/item?id=22151153)

[tombstone removal in an LSM](http://smalldatum.blogspot.com/2020/01/deletes-are-fast-and-slow-in-lsm.html)

[Debezium at Google](https://twitter.com/gunnarmorling/status/1225829835945259009)

[What are some examples of good database schema designs?](https://news.ycombinator.com/item?id=22324691)

[Benchmarks vs real workloads](http://smalldatum.blogspot.com/2020/02/benchmarks-vs-real-workloads.html)

[Tuning space and write amplification to minimize cost](http://smalldatum.blogspot.com/2020/03/tuning-space-and-write-amplification-to.html)

[How do you update multiple disparate databases?](https://news.ycombinator.com/item?id=22690743)

https://use-the-index-luke.com/sql/myth-directory/most-selective-first

[Nested Intervals Tree Encoding in SQL](https://lobste.rs/s/niwtoh/nested_intervals_tree_encoding_sql)

[write skews, external consistency, clock skews, database-generated IDs, nested transaction issues, caches & more.](https://twitter.com/rakyll/status/1249771259023392768) [oops databases](https://lobste.rs/s/2ayklq/erase_your_darlings_immutable#c_vvdziw).

[Things I Wished More Developers Knew About Databases](https://medium.com/@rakyll/things-i-wished-more-developers-knew-about-databases-2d0178464f78) [hn](https://news.ycombinator.com/item?id=22942278)

>  It is worth to also note that applications can handle a bit of inconsistency or programmers might have enough insights about the problem to add additional logic in the application to handle it without heavily relying on their database.

[How to prevent lost updates in long conversations](https://vladmihalcea.com/preventing-lost-updates-in-long-conversations/)

[Migrating a 40TB SQL Server Database](https://news.ycombinator.com/item?id=23998503)

[If All You Have Is a Database, Everything Looks Like a Nail](https://pathelland.substack.com/p/if-all-you-have-is-a-database-everything). [HN](https://news.ycombinator.com/item?id=25330223).

[Database as a Queue](https://lobste.rs/s/ukhpmn/database_as_queue). [9 yrs ago](https://news.ycombinator.com/item?id=3919507). [2013](https://news.ycombinator.com/item?id=21536698).

[Many small queries are efficient in SQLite](https://news.ycombinator.com/item?id=26151302)

[Some opinionated thoughts on SQL databases](https://blog.nelhage.com/post/some-opinionated-sql-takes/)

[Is the JDBC ResultSet an application-level query cursor](https://stackoverflow.com/questions/32644665/is-the-jdbc-resultset-an-application-level-query-cursor).

[Data Cleaning IS Analysis, Not Grunt Work](https://counting.substack.com/p/data-cleaning-is-analysis-not-grunt). [Learning SQL 201: Optimizing Queries, Regardless of Platform](https://counting.substack.com/p/learning-sql-201-optimizing-queries-regardless-of-platform-918a3af9c8b1).

[Bitemporality: More Than a Design Pattern](https://juxt.pro/blog/bitemporality-more-than-a-design-pattern). [Bitemporal History](https://martinfowler.com/articles/bitemporal-history.html). [temporal patterns](https://martinfowler.com/eaaDev/timeNarrative.html)

[read from databases, write to APIs](https://acco.io/read-from-dbs)

[the importance of idempotence for DataOps](https://www.dataops.live/blog/the-challenges-of-repeatable-and-idempotent-schema-management-introduction) [2](https://www.dataops.live/blog/the-challenges-of-repeatable-and-idempotent-schema-management-idempotence-in-snowflake) [3](https://www.dataops.live/blog/the-challenges-of-repeatable-and-idempotent-schema-management-conclusions)

[sql & normalization](https://twitter.com/lveronese65/status/1253214310333059073)

[Common data model mistakes made by startups](https://news.ycombinator.com/item?id=27248093)

[database horror stories](https://twitter.com/BrentO/status/1396723909274357762)

[One Database Transaction Too Many](https://hakibenita.com/django-nested-transaction)

[Against SQL](https://scattered-thoughts.net/writing/against-sql/). [hn](https://news.ycombinator.com/item?id=27791539).

[Duoquest: A Dual-Specification System for Expressive SQL Queries](https://arxiv.org/pdf/2003.07438.pdf)

> You can use as to name scalar values anywhere they appear. Except in a group by.

[Cool Stuff in Snowflake – Part 4: Aliasing all the things](https://sqlkover.com/cool-stuff-in-snowflake-part-4-aliasing-all-the-things/)

> In Snowflake, you can re-use your aliases in other expressions and in the WHERE, GROUP BY and HAVING clause.

[The Database Ruins All Good Ideas](https://lobste.rs/s/nsrhor/database_ruins_all_good_ideas)

[the relationship between DISTINCT and ORDER BY in SQL](https://twitter.com/lukaseder/status/1445406542166114319?s=03)

[Things I learned from building a production database](https://news.ycombinator.com/item?id=29322515)

[ERD rediscovered](https://twitter.com/FranckPachot/status/1463397158716071936)

[Databases in 2021: A Year in Review](https://news.ycombinator.com/item?id=29731885).

[have you tried rubbing a database on it?](https://www.hytradboi.com/)

[Which locking scheme and isolation level should one use for sequence number generation?](https://stackoverflow.com/questions/3325458/which-locking-scheme-and-isolation-level-should-one-use-for-sequence-number-gene). [avoiding concurrent insert multiple same id in mysql](https://stackoverflow.com/questions/18598535/avoiding-concurrent-insert-multiple-same-id-in-mysql)

> Anything you do within transaction scope is subject to race conditions.

> If an INSERT is aborted, a number from the sequence is consumed still

[Optimistic Locks and Interleaving](https://stackoverflow.com/questions/31639539/optimistic-locks-and-interleaving?rq=1)

[good answers on DBA SE](https://dba.stackexchange.com/users/3684/erwin-brandstetter?tab=answers).

[Understanding Bitemporal Data](https://www.abhinavomprakash.com/posts/understanding-bitemporal-data/)

[zero-downtime migrations](https://news.ycombinator.com/item?id=30945448)

[Creating read-optimized views](https://twitter.com/gunnarmorling/status/1518546545687379968)

[Why is Propagation.REQUIRED the default in Spring?](https://twitter.com/lukaseder/status/1519624738137686016)

[DOMAIN types](https://twitter.com/lukaseder/status/1520045361301184513). [The Public Interface of a Database](https://twitter.com/chrisoldwood/status/1520111550186631171)

[There's always an events table](https://lobste.rs/s/njzpec/there_s_always_events_table)

[Identity Crisis: Sequence v. UUID as Primary Key](https://brandur.org/nanoglyphs/026-ids)    

[the only scalable (and largely language agnostic (1)) solution is to break these down and deploy incremental versions of the app.](https://news.ycombinator.com/item?id=31331849)

[persistence programming](https://queue.acm.org/detail.cfm?id=3526210&doi=10.1145/3526210)

[How Airbnb Built “Wall” to prevent data bugs](https://news.ycombinator.com/item?id=31426206)

[Power BI DAX: Previous Month-to-Date, Quarter-to-Date, and Year-to-Date Calculations](https://radacad.com/power-bi-dax-previous-month-to-date-quarter-to-date-and-year-to-date-calculations)

[soft deletion](https://lobste.rs/s/xryce5/soft_deletion_probably_isn_t_worth_it)

[the slotted counter pattern](https://planetscale.com/blog/the-slotted-counter-pattern) [HN](https://news.ycombinator.com/item?id=32307947)

[The evolution of the data engineer role](https://news.ycombinator.com/item?id=33317126)

[Modern Data Modeling: Start with the End?](https://www.adventofdata.com/modern-data-modeling-start-with-the-end/). [hn](https://news.ycombinator.com/item?id=33846087).

>  In ye olden times, this was overthought and created friction - "If you don't know what you're going to exactly do with the data how am I going to know what to bring in and how to land it"."But how am I to know what to do with the data if I can't query it and see what opportunities there are."

>  Most of the other "big data" approaches that I've worked with seemed to make it worse not better. A lot more complexity, not thinking in sets, layers and layers of nothing I care about that can go wrong. I can't believe I'm still working with SQL.

[what tool to use for database migrations?](https://towardsdatascience.com/which-tool-should-you-use-for-database-migrations-4e0b9c44b790)


[Domain Logic and SQL (2003)](https://martinfowler.com/articles/dblogic.html)

[the principles of zero-downtime database migrations](https://teamplify.com/blog/zero-downtime-DB-migrations/). [see also](https://functional.cafe/@DiazCarrete/109573652212360085). [github/gh-ost: GitHub's Online Schema-migration Tool for MySQL](https://github.com/github/gh-ost). [Stop worrying about PostgreSQL locks in your Rails migrations](https://medium.com/doctolib/stop-worrying-about-postgresql-locks-in-your-rails-migrations-3426027e9cc9). [reddit](https://www.reddit.com/r/PostgreSQL/comments/kit0g3/comment/gh2o2pd/)

> AIUI adding columns with (most common kinds of) defaults is a table metadata change in sufficiently new Postgres versions, and won't touch every row anymore. It shouldn't always need special handling in that case as there's no row locks.

[Druid and SQL syntax](https://imply.io/blog/druid-and-sql-syntax/)

[You might as well timestamp it (2021)](https://news.ycombinator.com/item?id=34163748)

[Easy, alternative soft deletion](https://brandur.org/fragments/deleted-record-insert)

[Materialized View: SQL Queries on Steroids](https://dinesh.wiki/posts/materialized_view_sql_queries_on_steroids/). [Materialized View: SQL Queries on Steroids](https://lobste.rs/s/y76rvj/materialized_view_sql_queries_on).

[query engines: push vs pull](https://twitter.com/gunnarmorling/status/1609101693932675072)

[Databases in 2022: A Year in Review ](https://news.ycombinator.com/item?id=34220524).

[Understanding the N + 1 queries problem ](https://news.ycombinator.com/item?id=34207974)

[Trade-offs from using ULIDs](https://www.reddit.com/r/programming/comments/10278o0/tradeoffs_from_using_ulids_at_incidentio/)

[generating SQL in real-time based on user's interactions](https://twitter.com/davidad/status/1611639674799276032)

[Advanced DB Lecture #1: Andy's History of Databases](https://www.youtube.com/watch?v=LWS8LEQAUVc&t=747s). [tweet](https://twitter.com/andy_pavlo/status/1618794803772428288?t=hde__LosACLAdgq6P2MCHA&s=03)

[how do you test SQL?](https://news.ycombinator.com/item?id=34602318)

[db offline: Redis and ElasticSearch](https://www.linkedin.com/posts/vladmihalcea_because-it-caches-everything-in-redis-and-activity-7026472081244499968-NKC9)

> Because it caches everything in Redis and ElasticSearch, StackOverflow can function in read-only mode even when they disconnect it from SQL Server to upgrade the DB version or the underlying hardware.

# Podcasts

[Database Choices and Uber with Markus Winand](https://softwareengineeringdaily.com/tag/postgresql/)

[PostgreSQL Intermediate to Advanced (playlist)](https://www.youtube.com/playlist?list=PLxtrcgLvnR2Zx2h4VYqCkwIb_vQ6WKp3L)

# Courses

[Introduction to databases](http://cse.unl.edu/~cbourke/CSCE156/module-SQL/)

[CMU 15-721: In-Memory Databases / Advanced Database Systems [video]](https://news.ycombinator.com/item?id=21666250)

# Books

[Foundations of Databases A book published by Addison Wesley](http://webdam.inria.fr/Alice/)
