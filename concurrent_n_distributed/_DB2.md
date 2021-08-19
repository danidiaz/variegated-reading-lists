- [Manual](https://www.ibm.com/support/knowledgecenter/SSEPGG) / [Version 11.1.0](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.welcome.doc/doc/welcome.html)

- IBM DB2 doesn't have a separate JSON datatype. It stores BSON BLOBs and provides conversion & manipulation functions. [docs](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.swg.im.dbclient.json.doc/doc/c0070285.html).

- [Schemas](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0004105.html)

> A schema is a collection of named objects; it provides a way to group those objects logically. A schema is also a name qualifier; it provides a way to use the same natural name for several objects, and to prevent ambiguous references to those objects.

- [Data types](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.sql.ref.doc/doc/r0008483.html?pos=2)

- [User-defined types](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.structypes.doc/doc/c0006438.html)

- [Storing LOBs inline in table rows](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0054525.html)

- [Time Travel Query using temporal tables](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0058476.html)

- [Creating tables](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.dbobj.doc/doc/t0020123.html)

- [Shadow tables](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0061564.html)

- [Best practices](https://www.ibm.com/support/knowledgecenter/SSEPGG_11.1.0/com.ibm.db2.luw.common.doc/doc/c0060073.html)

- [Questions at DBA Stack Exchange](https://dba.stackexchange.com/questions/tagged/db2)

- [Questions at Stack Overflow](https://stackoverflow.com/questions/tagged/db2?sort=votes&pageSize=30)

- [Oracle and DB2 compared (by Oracle)](https://docs.oracle.com/cd/E39885_01/doc.40/e18460/oracle_db2_compared.htm#RPTID114)

> IBM DB2 supports the ON DELETE and ON UPDATE clauses in referential integrity constraints. Oracle only supports the ON DELETE clause in referential integrity constraints.

> In IBM DB2 identity columns provide a way to automatically generate unique, sequential and recoverable values for each row in a table. [...] When you define it with the GENERATED ALWAYS command, the database manager always generates the values used.

- [DB2 vs Oracle on dates](http://db2commerce.com/2011/04/19/db2-vs-oracle-handling-dates/)

- [Newbie differences between DB2 and Oracle](http://db2commerce.com/2011/05/16/newbie-differences-between-db2-and-oracle/)

- [If you do not specify ORDER BY, the rows of the result table have an arbitrary order.](https://dba.stackexchange.com/questions/86855/does-db2-order-data-by-the-primary-key)

- [How to do SQL select top N … in AS400](https://stackoverflow.com/questions/2850423/how-to-do-sql-select-top-n-in-as400)

- [Using Lateral Correlation To Define Expressions In DB2](https://www.itjungle.com/2016/08/02/fhg080216-story03/)

- [Selecting values while inserting data](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/apsg/src/tpc/db2z_selectvalueinsert.html)

>  FROM FINAL TABLE 

- [OLAP specification](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/sqlref/src/tpc/db2z_olapspecification.html)

> The aggregation group of a given row is a set of rows that is defined in relation to the given row (in the ordering of the rows in the partition of the given row). window-aggregation-group-clause specifies the aggregation group. If this clause is not specified and a window-order-clause is also not specified, the aggregation group consists of all rows of the window partition. The aggregation group of all rows of the window partition can be explicitly specified using the RANGE or ROWS clauses.

> If window-order-clause is specified, but window-aggregation-group-clause is not specified, the window aggregation group consists of all rows that precede a given row of the partition of the given row or all rows that are peers of the given row in the window ordering of the window partition that is defined by the window-order-clause

> [db2 lateral](https://www.mcpressonline.com/programming/sql/what-are-the-differences-between-db2-for-i-and-sql-server-sql-syntax)

> CROSS APPLY (similar to a row-based INNER JOIN) and OUTER APPLY (similar to a row-based LEFT JOIN) are not supported in DB2 for i, although sometimes the same thing can be accomplished. For example, a table function that is participating in a join in DB2 can have the input parameters vary (say, from a column in another table) from row to row, whereas SQL Server table functions can't be used in this manner without using one of the APPLY operators. So in the case of table functions, the APPLY operators aren't even required in DB2.

> Additionally, LATERAL correlation can be used to mimic the behavior of CROSS APPLY. However, I'm not aware of any way to use LATERAL to mimic OUTER APPLY.

[db2 pdf docs](https://www-01.ibm.com/support/docview.wss?uid=swg27039165#manuals) [for Windows and Linux](http://www-01.ibm.com/support/docview.wss?uid=swg27050624) [SQL reference](http://public.dhe.ibm.com/ps/products/db2/info/vr111/pdf/en_US/sqlbook.pdf)

[How to Limit Query Results for DB2 Databases](http://www.channeldb2.com/profiles/blogs/porting-limit-and-offset)

> Opensource databases such as MySQL and PostgreSQL supports non standard SELECT extension for limiting number of returned rows from query. You can see description in PostgreSQL manual. Look for keywords LIMIT and OFFSET. LIMIT specifies the maximum number of rows to return, while OFFSET specifies the number of rows to skip before starting to return rows. When both are specified, OFFSET rows are skipped before starting to count the LIMIT rows to be returned.

> Returning TOP N rows (emulating LIMIT) from query is easy. This functionality is in every database but syntax is database specific. DB2 follows SQL2008 standard and syntax for TOP N rows in DB2 is SELECT * FROM T FETCH FIRST 10 ROWS ONLY.

> Starting with DB2 9.7.2, LIMIT and OFFSET are supported in DB2

[Seven Surprising Findings About DB2](http://use-the-index-luke.com/blog/2014-11/seven-surprising-findings-about-DB2)

> Imagine you've already fetched a bunch of rows and need to get the next few ones. For that you'd use the time_stamp value of the last entry you've got for the bind value (?). The query then just return the rows from there on. But what if there are two rows with the very same time_stamp value? Then you need a tiebreaker: a second column—preferably a unique column—in the order by and where clauses that unambiguously marks the place till where you have the result. 

[perf tips 1](http://davebeulke.com/5-db2-sql-performance-tips/). [perf tips 2])http://davebeulke.com/another-5-db2-sql-performance-tips/)

> Since DB2 is the big data operational engine these days, creating prototype indexes on multi-billion row tables is impractical.  To quickly and easily prototype indexes on these large tables create Virtual Indexes that leverage the DB2 V10 INCLUDE Column feature, Index on Expression and any different index column combinations.

[db2 big data tuning](https://www.ibm.com/developerworks/community/blogs/DB2PerfTune/entry/SQL_Big_Data_Performance_Tips?lang=en)

> The first and most important SQL tip in all the SQL tip blogs I have written, continues to be the most common Let the DB2 database engine do all or as much of the work as possible! Doing the work inside the DB2 database engine continues to be the best performance advantage because DB2 does it faster than your application code. By supplying as much WHERE clause criteria statements as possible and using the correct WHERE clause criteria, you achieve faster performance than executing a SQL statement and then applying application code for filtering, comparing and quantifying the SQL result set data.

> When doing data qualification through the proper SQL WHERE clauses, the I/O of data from the database engine to the application program is minimized for the most efficient performance. Also, through DB2 and the processor chip technology, the SIMD operations can more efficiently skip over unneeded data. With database tables in the tens of billions of rows and SQL statements which need to be executed tens of millions of times to process daily transactions, every extra byte of data transferred can make a huge performance impact on overall I/Os, CPU and SQL performance.

[How to do bitwise operations in DB2](https://stackoverflow.com/questions/13401926/how-to-do-bitwise-operations-in-db2). [SQL Tips for DB2 LUW](https://www.ibm.com/developerworks/community/blogs/SQLTips4DB2LUW/entry/bit_arithmetic19?lang=en). [BITAND, BITANDNOT, BITOR, BITXOR, and BITNOT](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/sqlref/src/tpc/db2z_bif_bitwise.html). 

> Use SMALLINT, INTEGER, BIGINT types?

(Aggregate Bitwise OR on a column)[https://www.sqlservercentral.com/Forums/Topic1627609-3077-1.aspx]

> You can do it by breaking each permission down into a sum of powers of two.

[IN predicate](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_inpredicate.html). [values — Create Rows out of Nothing](https://modern-sql.com/feature/values).

> When a row-value-expression is specified, the IN predicate compares values with a collection of values. 

> expression1 IN (expressiona, expressionb, ...)

[Examples of grouping sets, rollup, and cube queries](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/sqlref/src/tpc/db2z_sql_groupingexamples.html).

[group-by-clause](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/sqlref/src/tpc/db2z_sql_groupbyclause.html).

[GROUPING](https://www.ibm.com/support/knowledgecenter/SSEPEK_11.0.0/sqlref/src/tpc/db2z_bif_grouping.html).

> When used in conjunction with grouping-sets and super-groups, the GROUPING function returns a value that indicates if a row returned in a GROUP BY result is a row generated by a grouping set that excludes the column represented by expression.

Pivoting tables in DB2 (rows to columns)

https://www.ibm.com/developerworks/community/blogs/SQLTips4DB2LUW/entry/pivoting_tables56?lang=en
https://stackoverflow.com/questions/13579143/how-can-i-pivot-a-table-in-db2
https://stackoverflow.com/questions/47561974/pivoting-a-table-in-iseries-db2-dynamically
https://stackoverflow.com/questions/42492501/db2-pivot-rows-to-columns
https://stackoverflow.com/questions/26603519/db2-convert-rows-to-column
https://stackoverflow.com/questions/15529107/pivoting-in-db2

- [Creation of materialized query tables](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/intro/src/tpc/db2z_creationofmqts.html). [paper](https://www.researchgate.net/publication/221210992_Recommending_Materialized_Views_and_Indexes_with_IBM_DB2_Design_Advisor). [Creating and Editing Materialized Query Tables](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/intro/src/tpc/db2z_creationofmqts.html). [Immediate refresh materialized views (MQT) with OUTER JOIN under DB2](https://dba.stackexchange.com/questions/39548/immediate-refresh-materialized-views-mqt-with-outer-join-under-db2). [An introduction to materialized query tables](https://www.ibm.com/developerworks/data/library/techarticle/dm-0509melnyk/index.html).

> A materialized query table (MQT) is a table whose definition is based upon the result of a query. The data that is contained in an MQT is derived from one or more tables on which the materialized query table definition is based. Summary tables (or automatic summary tables, ASTs), which are familiar to IBM® DB2® Universal Database™ (UDB) for Linux, UNIX®, and Windows® (DB2 UDB) users, are considered to be a specialized type of MQT. The fullselect that is part of the definition of a summary table contains a GROUP BY clause summarizing data from the tables that are referenced in the fullselect.

[Summary tables](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_10.5.0/com.ibm.dwe.cubeserv.doc/topics/coptsummarytbl.html).

> DB2® Warehouse uses DB2 summary tables to improve the performance of queries issued to cube models and cubes. A summary table is a special type of a materialized query table (MQT) that specifically includes summary data.
Because the Optimization Advisor always recommends MQTs with summarized data, the term summary table is used in the DB2 Warehouse documentation to describe the recommended MQTs.

> You can complete expensive calculations and joins for your queries ahead of time and store that data in a summary table. When you run queries that can use the precomputed data, DB2 will reroute the queries to the summary table. A query does not need to match the precomputed calculations exactly. If you use simple analytics like SUM and COUNT, DB2 can dynamically aggregate the results from the precomputed data. Many different queries can be satisfied by one summary table. Using summary tables can dramatically improve query performance for queries that access commonly used data or that involve aggregated data over one or more dimensions or tables.

[OLAP specification](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/sqlref/src/tpc/db2z_olapspecification.html).

[DB2 advanced OLAP](http://www.omniuser.org/downloads/omni201806JimDentonDb2foriAdvOLAPFunctions.pdf).

[LAG, LEAD, FIRST_VALUE, LAST_VALUE](https://www.ibm.com/developerworks/community/blogs/dbtrue/entry/lag_lead_first_value_last_value_totally_new_in_db21?lang=en). [more](https://www.itjungle.com/2016/07/12/fhg071216-story03/).

[Distinct types](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_distincttypessql.html).

[Date arithmetic](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_datearithmetic.html).

[Using recursive queries](https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_73/sqlp/rbafyrecursivequeries.htm). [generating a range of dates](https://www.idug.org/p/fo/et/thread=39026).

[Examples of recursive common table expressions](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/apsg/src/tpc/db2z_xmprecursivecte.html). [Recursive query in DB2 to get all items in the chain](https://stackoverflow.com/questions/25963799/recursive-query-in-db2-to-get-all-items-in-the-chain).

[WEEK_ISO](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_bif_weekiso.html). [WEEK](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_bif_week.html). [Fun with dates and times
](https://www.ibm.com/developerworks/data/library/techarticle/0211yip/0211yip3.html). [DAYOFWEEK_ISO](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/sqlref/src/tpc/db2z_bif_dayofweekiso.html).

[Writing and tuning queries for optimal performance
](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.1.0/com.ibm.db2.luw.admin.perf.doc/doc/c0054702.html). [Writing SQL statements](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.1.0/com.ibm.db2.luw.admin.perf.doc/doc/c0054707.html). [Using constraints to improve query optimization](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.1.0/com.ibm.db2.luw.admin.perf.doc/doc/c0055081.html). [Improving insert performance](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.1.0/com.ibm.db2.luw.admin.perf.doc/doc/c0009677.html). [Understanding DB2 Query Access Plans](http://etutorials.org/Misc/advanced+dba+certification+guide+and+reference/Chapter+6.+The+DB2+Optimizer/Understanding+DB2+Query+Access+Plans/). 

[Check query plan](https://www.ibm.com/support/knowledgecenter/ru/SSWSR9_11.4.0/com.ibm.pim.trb.doc/pim_ref_issue72.html). [DB2 LUW Execution Plan Operations](https://use-the-index-luke.com/sql/explain-plan/db2/operations). [Paging Through Results](https://use-the-index-luke.com/sql/partial-results/fetch-next-page).

[Fetching a limited number of rows](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/perf/src/tpc/db2z_fetchfirstnrows.html). [The (unknown) benefits of FETCH FIRST in DB2 for z/OS SQL](https://www.idug.org/p/bl/et/blogid=278&blogaid=567). [Equivalent of LIMIT for DB2
](https://stackoverflow.com/questions/3885193/equivalent-of-limit-for-db2). [DB2 and PHP Best practices on IBM i](https://www.zend.com/topics/DB2-and-PHP-best-practices-on-IBM-i.pdf). [optimize-clause](https://www.ibm.com/support/knowledgecenter/SSEPEK_12.0.0/sqlref/src/tpc/db2z_sql_optimizeforclause.html). [Optimizing retrieval for a small set of rows](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_12.0.0/apsg/src/tpc/db2z_optimizeretrievalsmallset.html).

> OPTIMIZE FOR 100 ROWS tells the optimizer to “optimize” for that number. But if you specify OPTIMIZE FOR 100 ROWS, DB2 does not limit how many rows you can fetch 

> The optimize-clause tells Db2® to assume that the program does not intend to retrieve more than integer rows from the result table. Without this clause, Db2 assumes that all rows of the result table will be retrieved, unless the FETCH FIRST clause is specified. Optimizing for integer rows can improve performance. If this clause is omitted and the FETCH FIRST is specified, OPTIMIZE FOR integer ROWS is assumed, where integer is the value that is specified in the FETCH FIRST clause. Db2 will optimize the query based on the specified number of rows.

[Spring Batch using Db2](https://www.idug.org/p/bl/et/blogid=278&blogaid=786).

[queryno-clause](https://www.ibm.com/support/knowledgecenter/SSEPEK_12.0.0/sqlref/src/tpc/db2z_sql_querynoclause.html).

> For correlating SQL statement text with EXPLAIN output in the plan table

https://www.ibm.com/blogs/cloud-computing/2018/05/08/ibm-red-hat-expand-partnership-cloud/
https://developer.ibm.com/recipes/tutorials/ibm-db2-on-ibm-cloud-private-with-redhat-openshift/
https://developer.ibm.com/articles/dm-1602-db2-docker-trs/
https://access.redhat.com/documentation/en-us/red_hat_jboss_bpm_suite/6.0/html/installation_guide/special_setup_for_ibm_db2_database
https://www.ibm.com/cloud/partners/ibm-redhat
https://access.redhat.com/solutions/3530941
https://blog.openshift.com/openshift-connecting-database-using-port-forwarding/
One of the benefits of OpenShift over a traditional Platform-as-a-Service (PaaS) is that you can have access to persistent volumes. This means you can attach storage to your web applications or run applications such as databases.
https://docs.openshift.com/container-platform/3.3/dev_guide/integrating_external_services.html
http://www.middlecon.se/wp-content/uploads/Data_Server_Day-Db2_Private_Cloud-2018-May-09.pdf

https://use-the-index-luke.com/sql/explain-plan/db2/filter-predicates
https://use-the-index-luke.com/sql/explain-plan/db2/operations

[REOPT](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/comref/src/tpc/db2z_bindoptreopt.html)

> The REOPT option specifies whether DB2® determines an access path at run time by using the values of host variables, parameter markers, and special registers.

[Differences between static and dynamic SQL](https://www.ibm.com/support/knowledgecenter/SSEPEK_10.0.0/apsg/src/tpc/db2z_differencesstaticdynamic.html).

> For static SQL statements that have input host variables, the time at which DB2 determines the access path depends on the REOPT bind option that you specify: REOPT(NONE) or REOPT(ALWAYS). REOPT(NONE) is the default. Do not specify REOPT(AUTO) or REOPT(ONCE); these options are applicable only to dynamic statements. DB2 ignores REOPT(ONCE) and REOPT(AUTO) for static SQL statements, because DB2 caches only dynamic SQL statements.

[Reoptimizing SQL statements at run time](https://www.ibm.com/support/knowledgecenter/SSEPEK_10.0.0/perf/src/tpc/db2z_managereopt.html).

[Specifying optimization parameters at the statement level](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_11.0.0/perf/src/tpc/db2z_createzparmhint.html). [DSN_USERQUERY_TABLE](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/usrtab/src/tpc/db2z_dsnuserquerytable.html).

> The unique identifier of the query, used to correlate with PLAN_TABLE rows for statement-level access paths.

[DB2 How To Measure Transaction Log Write Time ?](https://www.raghu-on-tech.com/2019/02/28/howtomonitor-transactionlog-writetime/)

[dependent tables in DB2](https://twitter.com/erwin_hattingh/status/1110539359596482560). [post](http://db2geek.triton.co.uk/dependent-tables-in-db2/).

[recursive sql in DB2](https://www.idug.org/p/bl/et/blogid=278&blogaid=839)

[predicate manipulation](https://www.ibm.com/support/knowledgecenter/en/SSEPEK_10.0.0/perf/src/tpc/db2z_db2simplifiesjoins.html)

[db2 isolation levels](https://tapoueh.org/blog/2018/07/postgresql-concurrency-isolation-and-locking/)

[know your isolation levels](http://db2portal.blogspot.com/2009/06/know-your-isolation-levels.html)

> If the program used an RR isolation level rather than CS, an UPDATE that occurs after the production of the first report but before the second would not have been allowed. The program would have maintained the locks it held from the generation of the first report and the updater would be locked out until the locks were released.

[Currently committed semantics](https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.1.0/com.ibm.db2.luw.admin.perf.doc/doc/c0053760.html)

> The potential for deadlocks also varies with the isolation level.

[A Close Look at the Index Include Clause](https://use-the-index-luke.com/blog/2019-04/include-columns-in-btree-indexes).

[The #IBM #Db2 Samples are now available on GitHub to share, improve and extend!](https://twitter.com/ARSDB2/status/1176164752386646016)
