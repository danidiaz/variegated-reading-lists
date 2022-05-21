Minimizing real-time prediction serving latency in machine learning https://cloud.google.com/solutions/machine-learning/minimizing-predictive-serving-latency-in-machine-learning

> You have too many entities (high cardinality), which makes it challenging to precompute prediction in a limited amount of time. An example is forecasting daily sales by item when you have hundreds of thousands or millions items. In that case, you can use a hybrid approach, where you precompute predictions for the top N entities, such as for the most active customers or the most viewed products. You can then use the model directly for online prediction for the rest of the long-tail entities.

https://liqixu.github.io/papers/needletail-hilda.pdf Optimally Leveraging Density and Locality
for Exploratory Browsing and Sampling

> , we would need B+Trees on every single attribute or combination of attributes

[druid](https://towardsdatascience.com/introduction-to-druid-4bf285b92b5a)

> At the time, we were handling approximately 100 millions events per day, and some of our reports were taking 30 seconds to generate. We currently handle billions of events per day, and the reporting takes less than 1 second most of the time.

https://hevodata.com/blog/druid-vs-redshift-data-warehouse/ https://towardsdatascience.com/introduction-to-druid-4bf285b92b5a 

[dynamo db](https://medium.com/@nabtechblog/advanced-design-patterns-for-amazon-dynamodb-354f97c96c2)

> With NoSQL, it is best practice to precalculate aggregates values out of band, and store them back into the table as a single item for quick retrieval.

> There are many data enrichment use cases that would fit this model.

[Why you should use a relational database instead of NoSQL for your IoT application](https://blog.timescale.com/use-relational-database-instead-of-nosql-for-iot-application/)

[Do we need pre-computed aggregates?](https://developer.jboss.org/thread/249480?_sscc=t)

> When querying time series data, resolution refers to the number of data points for a given time range. The highest resolution would provide every available data point for a time range. So if I want a query to use the highest resolution and if there are 100 data points, then the query result should include every one of those 100 points.

> As the number of data points increases, providing results at higher resolutions becomes less effective. For instance, increasing the resolution to the point where a graph in the UI includes 1 million points is probably no more effective than if the graph included only 10,000 or even 1,000 data points. The higher resolution could degrade user experience as rendering time increases. Latency on server response time is also likely to increase.

> Pre-computed aggregation is the process of continually downsampling a time series and storing the lower resolution data for future analysis or processing. Pre-computed aggregates are often combined with data expiration/retention policies to address the aforementioned storage problem. Higher resolution data is stored for shorter periods of time than lower resolution data. Pre-computed aggregation can also alleviate the CPU utilization and latency problems. Instead of downsampling 1 million data points, we can query the pre-computed aggregated data points and perform downsampling on 10,000 data points.

[time series databases to watch](https://news.ycombinator.com/item?id=19825566)

> I have used TimescaleDB for several purposes. As it is built on top of Postgres, all the existing tools, libraries and processes work out of the box. This is a huge advantage if you are operating Postgres anyway: Your existing backup tools will work, as does your user Managment.

> We ingest a lot of time series (IoT) data and use Postgres for other data so Timescale works quite well for us. One thing Timescale treats as second class citizen though is updates to existing data points which are 1-2 areas of magnitude slower than inserts. Granted this is also the case for all other TSDB solutions out there which are for obvious reasons optimized for inserts and reads aggregated along the time dimension. Still would be amazing if you could add to the already existing differentiation of allowing fast updates for cases like ours where we dont store events relating to a singular point in time but rather time-spans so new incoming data points might be "merged" into existing time-spans.

[Narrow-table Model](https://docs.timescale.com/v1.2/introduction/data-model)

> In this model, each metric/tag-set combination is considered an individual "time series" containing a sequence of time/value pairs.

> Using our example above, this approach would result in 9 different "time series", each of which is defined by a unique set of tags.

> The number of such time series scales with the cross-product of the cardinality of each tag, i.e., (# names) × (# device ids) × (# location ids) × (device types). Some time-series databases struggle as cardinality increases, ultimately limiting the number of device types and devices you can store in a single database.

> TimescaleDB supports narrow models and does not suffer from the same cardinality limitations as other time-series databases do. A narrow model makes sense if you collect each metric independently. It allows you to add new metrics as you go by adding a new tag without requiring a formal schema change.

> TimescaleDB easily supports wide-table models. Queries across multiple metrics are easier in this model, since they do not require JOINs. Also, ingest is faster since only one timestamp is written for multiple metrics.

> Of course, this is not a new format: it's what one would commonly find within a relational database.

[Relational Database schema design for metric storage](https://stackoverflow.com/questions/54823674/relational-database-schema-design-for-metric-storage) good SO answer

[Schema Design for Time Series Data](https://cloud.google.com/bigtable/docs/schema-design-time-series)

> For time series, you should generally use tall and narrow tables. This is for two reasons: Storing one event per row makes it easier to run queries against your data.

[Timeseries: How long can the elephant remember?](https://theplateisbad.blogspot.com/2016/08/timeseries-how-long-can-elephant.html)

[Wide narrow data](https://en.wikipedia.org/wiki/Wide_and_narrow_data)

[BigQuery Best Practices For High Performance ETL](https://hevodata.com/blog/bigquery-best-practices-etl/)

[Continuous Queries in InfluxDB – Part I](https://www.influxdata.com/blog/continuous-queries-in-influxdb-part-i/). [more](https://docs.influxdata.com/influxdb/v1.7/). [Under the hood with Continuous Queries – Part II](https://www.influxdata.com/blog/under-the-hood-with-continuous-queries-part-ii/). [downsampling and retention](https://docs.influxdata.com/influxdb/v1.7/guides/downsampling_and_retention/). [Resolution 1: Downsample to get your database in shape](https://www.influxdata.com/blog/tldr-influxdb-tech-tips-december-29-2016/).

> Queries returning aggregate, summary, and computed data are frequently used in application development. For example, if you’re building an online dashboard application to report metrics, you probably need to show summary data. These summary queries are generally expensive to compute since they have to process large amounts of data, and running them over and over again just wouldn’t scale. Now, if you could pre-compute and store the aggregates query results so that they are ready when you need them, it would significantly speed up summary queries in your dashboard application, without overloading your database. Enter InfluxDB’s continuous queries feature!

> Series cardinality is the number of unique database, measurement, and tag set combinations in an InfluxDB instance. We talk about it quite a bit because extremely high series cardinality can kill your InfluxDB process.

[Using Data Transformations for Low-latency Time Series Analysis](http://www.pdl.cmu.edu/PDL-FTP/CloudComputing/CMU-PDL-15-106.pdf)

> While a row can have arbitrary number of fields, we encourage users to define their table schema as narrow tables, such as the OpenTSDB [8] table format: {metric, tags, time, value},

[Is the EAV model still a decent way to store misc model data?](https://www.reddit.com/r/PHP/comments/9g2orz/is_the_eav_model_still_a_decent_way_to_store_misc/)

> JSON columns. The peformance issues where fixed so there's no reason for EAV anymore

[Re-architecting Slack’s Workspace Preferences: How to Move to an EAV Model to Support Scalability](https://slack.engineering/re-architecting-slacks-workspace-preferences-how-to-move-to-an-eav-model-to-support-scalability-d480a7c5c655)

[Failed Solution II: Pre-compute the World in NoSQL](http://druid.io/blog/2011/04/30/introducing-druid.html)

> In short, we took all of our data and pre-computed aggregates for every combination of dimensions. At query time we need only locate the specific pre-computed aggregate and and return it: an O(1) key-value lookup. This made things fast and worked wonderfully when we had a six dimension beta data set. But when we added five more dimensions – giving us 11 dimensions total – the time to pre-compute all aggregates became unmanageably large (such that we never waited more than 24 hours required to see it finish).

> So we decided to limit the depth that we aggregated to. By only pre-computing aggregates of five dimensions or less, we were able to limit some of the exponential expansion of the data. The data became manageable again, meaning it only took about 4 hours on 15 machines to compute the expansion of a 500k beta rows into the full multi-billion entry output data set.

[What distinguishes the time series workload?](https://www.influxdata.com/time-series-database/)

> With time series databases, it’s common to keep high precision data around for a short period of time. This data is aggregated and downsampled into longer term trend data. This means that for every data point that goes into the database, it will have to be deleted after its period of time is up. This kind of data lifecycle management is difficult for application developers to implement on top of regular databases. They must devise schemes for cheaply evicting large sets of data and constantly summarizing that data at scale. With a Time Series Database, this functionality is provided out of the box.

[How To Resample and Interpolate Your Time Series Data With Python](https://machinelearningmastery.com/resample-interpolate-time-series-data-python/). [more](https://www.oreilly.com/library/view/getting-started-with/9781785285110/ch05s04.html)

> Downsampling: Where you decrease the frequency of the samples, such as from days to months.

> Downsampling reduces the number of samples in the data. During this reduction, we are able to apply aggregations over data points. 

[on time series](https://grisha.org/blog/2015/03/28/on-time-series/)

> Very often TS data is used to generate charts. This is an artifact of the human brain being spectacularly good at interpreting a visual representation of a relationship between streams of numbers while nearly incapable of making sense of data in tabular form. When plotting, no matter how much data is being examined, the end result is limited to however many pixels are available on the display. Even plotting aside, most any use of time series data is in an aggregated form.

[Implementing Multidimensional Data Warehouses into NoSQL](https://www.researchgate.net/publication/274632591_Implementing_Multidimensional_Data_Warehouses_into_NoSQL)

[mondrian aggregate tables](https://mondrian.pentaho.com/documentation/aggregate_tables.php)

[Time Series Aggregate Store](https://help.sap.com/viewer/080fabc6cae6423fb45fca7752adb61e/1903a/en-US/8e70388fc8814b77a7c0567de93a035e.html). [Read Time Series Data for Multiple Property Types of a Thing Applying M4 Algorithm](https://help.sap.com/viewer/080fabc6cae6423fb45fca7752adb61e/1903a/en-US/816689cc6e5349c8adc488a1edf6a33d.html)

> The Time Series Aggregate Store stores the pre-calculated aggregates for the time series data of Things

> With this service, you can read the time series data for multiple property types of the specified thing by applying the M4 algorithm.

[M4: A Visualization-Oriented Time Series Data Aggregation](http://www.vldb.org/pvldb/vol7/p797-jugel.pdf)

> M4 Aggregation. M4 is a composite value-preserving
aggregation (see Section 4.1) that groups a time series relation into w equidistant time spans, such that each group
exactly corresponds to a pixel column in the visualization.
For each group, M4 then computes the aggregates min(v),
max(v), min(t), and max(t) – hence the name M4

[A Review of Aggregation Algorithms for the Internet of Things](https://www.researchgate.net/publication/321400876_A_Review_of_Aggregation_Algorithms_for_the_Internet_of_Things). [Data aggregation mechanisms in the Internet of things](https://www.researchgate.net/publication/319283535_Data_aggregation_mechanisms_in_the_Internet_of_things_A_systematic_review_of_the_literature_and_recommendations_for_future_research). [Efficiently Validating Aggregated IoT Data Integrity](http://www.csl.sri.com/users/gehani/papers/BDS-2018.Homomorphic.pdf). [Comparison of Data Aggregation Techniques in Internet of Things (IoT)](https://www.academia.edu/27855477/Comparison_of_Data_Aggregation_Techniques_in_Internet_of_Things_IoT_?auto=download)

[FAQs for Big Data & Analytics on Timeseries within SAP IoT Application Enablement (Leonardo Foundation)](https://blogs.sap.com/2017/02/06/faqs-for-big-data-analytics-on-timeseries-within-sap-iot-application-enablement-leonardo-foundation/)

[Storing time-series data, relational or non?](https://stackoverflow.com/questions/4814167/storing-time-series-data-relational-or-non). [](https://stackoverflow.com/questions/8816429/is-there-a-powerful-database-system-for-time-series-data). [Is there a powerful database system for time series data? [closed]](https://stackoverflow.com/questions/8816429/is-there-a-powerful-database-system-for-time-series-data). [storing massive ordered time series data in bigtable derivatives](https://stackoverflow.com/questions/1623399/storing-massive-ordered-time-series-data-in-bigtable-derivatives). [Database and large Timeseries - Downsampling - OpenTSDB InfluxDB Google DataFlow](https://stackoverflow.com/questions/34431775/database-and-large-timeseries-downsampling-opentsdb-influxdb-google-dataflow)

> typical evaluations are hard to formulate in SQL and slow in the execution. E.g. find the maximum value with time stamp per 15 minutes for all measurements during the last month.

> The need is since we can query vast amount of data, for instance a year, if the DB downsample at the query and is not pre-computed, it may take a very long time.

> As well, downsampling needs to be "updated" when ever "delayed" datapoint are added.

> For time series databases period aggregations (aka downsampling, averaging, summarization, etc) is one of standard use cases. They are all pretty good at it, at least the basics - avg, min, max, percentiles, first/last, etc. opentsdb for instance reads raw data and returns aggregates and then queues these aggregates for re-use. This is how it works last time I checked. 

[Time-series data: Why (and how) to use a relational database instead of NoSQL](https://blog.timescale.com/time-series-data-why-and-how-to-use-a-relational-database-instead-of-nosql-d0cd6975e87c/)

[time aggregation - DB2](https://www.ibm.com/support/knowledgecenter/en/SSBNJ7_1.4.2/dataView/Concepts/ctnpm_dv_use_timeaggregation.html)

> Time aggregation is the aggregation of all data points for a single resource over a specified period (the granularity). Data aggregations in Resource Time Series reports are of the time aggregation type.

> The result of the aggregation is one data point that reflects a statistical view of the collected and aggregated data points. For example, average, minimum, maximum, sum, or count. Typically, multiple aggregated data points are presented in a report for a given reporting period.

[Benchmarking Time Series Databases with IoTDB-Benchmark for IoT Scenarios](https://arxiv.org/pdf/1901.08304.pdf)

[What time series database can support high cardinality?](https://softwareengineering.stackexchange.com/questions/359754/what-time-series-database-can-support-high-cardinality)

[Procella: unifying serving and analytical data at YouTube](https://blog.acolyer.org/2019/09/11/procella/)

> "For real-time tables, the user can also specify how to age-out, down-sample or compact the data"

[Influxdb use case](https://twitter.com/DZoneInc/status/1175790675603939329)

[Datadog](https://twitter.com/InfoQ/status/1178001930657914884)

[Why You Should NOT be Using an RDBS for Tme-Stamped Data](https://www.youtube.com/watch?v=VDbTrk1ed3E&feature=youtu.be)

[Redis and Grafana for real-time analytics](https://www.infoq.com/articles/redis-time-series-grafana-real-time-analytics/ )

[GOTO 2019 • Temporal Modelling • Mathias Verraes](https://www.youtube.com/watch?v=KNqOWT0lOYY&list=PLEx5khR4g7PKT9RvuVyQxJLO8CZUJzNMy&index=27)

[high cardinality data and stuff](https://twitter.com/copyconstruct/status/1197292286628876296)

[Influxdb on Kubernetes - should I be doing this?](https://docs.influxdata.com/platform/integrations/kubernetes/#should-i-run-influxdb-in-kubernetes)

[Apache Druid vs. Time-Series Databases ](https://news.ycombinator.com/item?id=22868286)

[from batch to streaming to both](https://www.infoq.com/presentations/skyscanner-streaming/?)

[How to Get Started Using CrateDB and Grafana to Visualize Time-Series Data](https://dzone.com/articles/how-to-get-started-using-cratedb-and-grafana-to-vi?fromrel=true)

[things we learned about sums](https://questdb.io/blog/2020/05/12/interesting-things-we-learned-about-sums)

[	MetricsDB: TimeSeries Database for storing metrics at Twitter ](https://news.ycombinator.com/item?id=23547327)

[How Time Series Databases Work, and Where They Don’t](https://news.ycombinator.com/item?id=28901063)

## clickhouse

[ClickHouse: New Open Source Columnar Database](https://www.percona.com/blog/2017/02/13/clickhouse-new-opensource-columnar-database/)

[clickhouse](https://clickhouse.yandex/)

[interview about clickhouse](https://www.dataengineeringpodcast.com/clickhouse-data-warehouse-episode-88/)

[Raspberry Pi IoT: Sensors, InfluxDB, MQTT, and Grafana](https://dzone.com/articles/raspberry-pi-iot-sensors-influxdb-mqtt-and-grafana)

[How Netflix uses Druid](https://netflixtechblog.com/how-netflix-uses-druid-for-real-time-insights-to-ensure-a-high-quality-experience-19e1e8568d06)

[Handling Real-Time Updates in ClickHouse](https://dzone.com/articles/handling-real-time-updates-in-clickhouse)

> Mutable data is generally unwelcome in OLAP databases. 

> Under the pressure of GDPR, requirements the ClickHouse team delivered UPDATEs and DELETEs in 2018. 

[	ClickHouse as an alternative to Elasticsearch for log storage and analysis](https://news.ycombinator.com/item?id=26316401)

[clickhouse vs postgresql](https://blog.timescale.com/blog/what-is-clickhouse-how-does-it-compare-to-postgresql-and-timescaledb-and-how-does-it-perform-for-time-series-data/). [timescaledb vs. clickhouse](https://news.ycombinator.com/item?id=29096541).

[Monarch: Google’s Planet-Scale In-Memory Time Series Database](https://news.ycombinator.com/item?id=31379383)

## grafana datasources

[grafana datasources](https://grafana.com/docs/features/datasources/)

- [Graphite](https://grafana.com/docs/features/datasources/graphite/)
- [Prometheus](https://grafana.com/docs/features/datasources/prometheus/)
- [InfluxDB](https://grafana.com/docs/features/datasources/influxdb/)
- [Elasticsearch][https://grafana.com/docs/features/datasources/elasticsearch/)
- [Google Stackdriver](https://grafana.com/docs/features/datasources/stackdriver/)
- AWS CloudWatch
- Azure Monitor
- Loki
- MySQL
- PostgreSQL
- Microsoft SQL Server (MSSQL)
- [OpenTSDB](https://grafana.com/docs/features/datasources/opentsdb/)
- Testdata

## Timescaledb

[Zabbix, Time Series Data and TimescaleDB](https://blog.zabbix.com/zabbix-time-series-data-and-timescaledb/6642/). [hn](https://news.ycombinator.com/item?id=19850071).

> By clever sharding, you can work around the performance issues somewhat but it'll never be as efficient as an OLAP column store like ClickHouse or MemSQL:

> Timestamps and metric values compress very nicely using delta-of-delta encoding.

> Compression dramatically improves scan performance.

> Aligning data by columns means much faster aggregation. A typical time series query does min/max/avg aggregations by timestamp. You can load data straight from disk into memory, use SSE/AVX instructions and only the small subset of data you aggregate on will have to be read from disk.

[PG Partition Manager](https://github.com/pgpartman/pg_partman)

[timescale multi cloud](https://www.infoq.com/news/2019/06/timescale-multi-cloud/)

[Building a distributed time-series database on PostgreSQL](https://news.ycombinator.com/item?id=20760324)

[TimescaleDB adds native compression for any PostgreSQL type](https://www.reddit.com/r/programming/comments/dpsiz3/timescaledb_adds_native_compression_for_any/)

> Reading this post is frustrating. What they are describing is where column store databases were 20 years ago. Perhaps at some point the folks at TimescaleDB will read Daniel Abadi’s 2008 paper, which describes the key elements of how all modern column stores work: http://db.csail.mit.edu/pubs/abadi-column-stores.pdf

> The key takeaway is that columnar compression only accounts for a small minority of the speed up that you get for scan-oriented workloads; the real big win comes when you implement a block-oriented query processor and pipelined execution. Of course you can’t do this by building inside the Postgres codebase, which is why every good column store is built more or less from scratch.

> Anyone considering a “time series database” should first set up a modern commercial column store, partition their tables on the time column, and time their workload. For any scan-oriented workload, it will crush a row store like Timescale.

[Multi-node TimescaleDB is now free](https://news.ycombinator.com/item?id=23272992)

[ListenBrainz moves to TimescaleDB](https://news.ycombinator.com/item?id=23915509)

[	TimescaleDB vs. Amazon Timestream ](https://news.ycombinator.com/item?id=25287793)

[   Time-Series Compression Algorithms](https://news.ycombinator.com/item?id=31379344)

[Apache Druid](https://thenewstack.io/apache-druid-a-real-time-database-for-modern-analytics/)

## graphite

[whisper](https://graphite.readthedocs.io/en/latest/whisper.html)

> Whisper is a fixed-size database, similar in design and purpose to RRD (round-robin-database). It provides fast, reliable storage of numeric data over time. Whisper allows for higher resolution (seconds per point) of recent data to degrade into lower resolutions for long-term retention of historical data.

## opntsdb

[opend tdsd downsampling](http://opentsdb.net/docs/build/html/user_guide/query/downsampling.html). [Rollup And Pre-Aggregates](http://opentsdb.net/docs/build/html/user_guide/rollups.html). [aggregators](http://opentsdb.net/docs/build/html/user_guide/query/aggregators.html). [Understanding Metrics and Time Series](http://opentsdb.net/docs/build/html/user_guide/query/timeseries.html). [Rollup And Pre-Aggregates]() **IMPORTANT**.

> Downsampling (or in signal processing, decimation) is the process of reducing the sampling rate, or resolution, of data. For example, lets say a temperature sensor is sending data to an OpenTSDB system every second. If a user queries for data over an hour time span, they would receive 3,600 data points, something that could be graphed fairly easily. However now if the user asks for a full week of data they'll receive 604,800 data points and suddenly the graph may become pretty messy. Using a downsampler, multiple data points within a time range for a single time series are aggregated together with a mathematical function into a single value at an aligned timestamp. This way we can reduce the number of values from say, 604,800 to 168.

> When storing rollups, it's best to avoid functions such as average, median or deviation. When performing further downsampling or grouping aggregations, such values become meaningless. Instead it's much better to always store the sum and count from which, at least, the average can be computed at query time. For more information, see the section below.

>  OpenTSDB was designed to efficiently combine multiple, distinct time series during query execution. The reason for this is that when users are looking at their data, most often they start at a high level asking questions like "what is my total throughput by data center?" or "what is the current power consumption by region?". After looking at these high level values, one or more may stick out so users drill-down into more granular data sets like "what is the throughput by host in my LAX data center?". We want to make it easy to answer those high level questions but still allow for drilling down for greater detail.

> But how do you merge multiple individual time series into a single series of data? Aggregation functions provide the means of mathematically merging the different time series into one. Filters are used to group results by tags and aggregations are then applied to each group. Aggregations are similar to SQL's GROUP BY clause where the user selects a pre-defined aggregation function to merge multiple records into a single result. However in TSDs, a set of records is aggregated per timestamp and group.

> This document focuses on how aggregators are used in a group by context, i.e. when merging multiple time series into one. Additionally, aggregators can be used to downsample time series (i.e. return a lower resolution set of results). For more information, see Downsampling.

> While rollups help with wide time span queries, you can still run into query performance issues with small ranges if the metric has high cardinality (i.e. the unique number of time series for the given metric). In the example above, we have 4 web servers. But lets say that we have 10,000 servers. Fetching the sum or average of interface traffic may be fairly slow. If users are often fetching the group by (or some think of it as the spatial aggregate) of large sets like this then it makes sense to store the aggregate and query that instead, fetching much less data.

> Notice that these time series have dropped the tags for host and interface. That's because, during aggregation, multiple, different values of the host and interface have been wrapped up into this new series so it no longer makes sense to have them as tags. Also note that we injected the new _aggregate tag in the stored data. Queries can now access this data by specifying an _aggregate value.

> While pre-aggregates certainly help with high-cardinality metrics, users may still want to ask for wide time spans but run into slow queries. Thankfully you can roll up a pre-aggregate in the same way as raw data. Just generate the pre-aggregate, then roll it up using the information above.

> One method that is commonly used by other time series databases is to read the data out of the database after some delay, calculate the pre-aggs and rollups, then write them. This is the easiest way of solving the problem and works well at small scales. However there are still a number of issues:

[How to Handle the Influx of Data](https://dzone.com/articles/how-to-handle-the-influx-of-data)

[timescale cloud](https://news.ycombinator.com/item?id=24132602)

# bitemporal data

https://martinfowler.com/bliki/DataLake.html

It is important that all data put in the lake should have a clear provenance in place and time. Every data item should have a clear trace to what system it came from and when the data was produced. The data lake thus contains a historical record. This might come from feeding Domain Events into the lake, a natural fit with Event Sourced systems. But it could also come from systems doing a regular dump of current state into the lake - an approach that's valuable when the source system doesn't have any temporal capabilities but you want a temporal analysis of its data. A consequence of this is that data put into the lake is immutable, an observation once stated cannot be removed (although it may be refuted later), you should also expect ContradictoryObservations.

https://martinfowler.com/bliki/ContradictoryObservations.html
https://blog.bi-geek.com/arquitectura-bi-introduccion-al-data-lake/
https://tdwi.org/articles/2017/12/04/arch-all-data-time-and-the-data-lake.aspx

Business state data tagged with business and DBMS start and end timestamps is called bitemporal data. This structure is one of the most useful ways that relational database designers record and manage time-related data. Several databases, including IBM DB2 and Teradata, have included internal support for bitemporal data since early this decade.

Bitemporality is at the heart of data warehouse consistency and enables operational systems to manage the creation of state data from time series. As relational databases are the basis of both operational systems and data warehouses, extensive design and development effort has been expended over the decades to handle time properly in this environment.

“The lake's one-dimensional time series approach can give rise to significant implementation challenges in more complex data warehouse use cases.” https://tdwi.org/articles/2017/12/04/arch-all-data-time-and-the-data-lake.aspx

https://www.elsevier.com/books/bitemporal-data/johnston/978-0-12-408067-6
https://www.dataversity.net/bitemporal-data-modeling-learn-history/
https://martinfowler.com/eaaDev/timeNarrative.html
https://en.wikipedia.org/wiki/Temporal_database

Bi-Temporal[edit]

A bi-temporal database has two axis of time.

valid time.
transaction time or decision time.
 
https://www.marklogic.com/blog/bitemporal/
https://www.sciencedirect.com/topics/computer-science/bitemporal-data
https://www.sciencedirect.com/science/article/pii/B9780123750419000029
https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.5.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0058476.html

A bitemporal table is a table that combines the historical tracking of a system-period temporal table with the time-specific data storage capabilities of an application-period temporal table. Use bitemporal tables to keep user-based period information as well as system-based historical information.

Bitemporal tables behave as a combination of system-period temporal tables and application-period temporal tables. All the restrictions that apply to system-period temporal tables and application temporal tables also apply to bitemporal tables.

https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.5.0/com.ibm.db2.luw.admin.dbobj.doc/doc/c0058481.html
https://www.ibm.com/support/knowledgecenter/en/SSEPGG_11.5.0/com.ibm.db2.luw.admin.dbobj.doc/doc/r0052344.html
