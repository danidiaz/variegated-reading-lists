# Data Engineering

[Data Engineering Podcast](https://www.dataengineeringpodcast.com/).

[Data-Mesh-Learning Slack Channel](https://launchpass.com/data-mesh-learning)

[97 Things Every Data Engineer Should Know](https://www.goodreads.com/book/show/56916802-97-things-every-data-engineer-should-know)

[DataOps: PART 1: THE CHALLENGES OF REPEATABLE AND IDEMPOTENT SCHEMA MANAGEMENT: INTRODUCTION](https://www.dataops.live/blog/the-challenges-of-repeatable-and-idempotent-schema-management-introduction).

[Data Lineage at Slack](https://slack.engineering/data-lineage-at-slack/)

> backfill a table after a bug is fixed in its source data. [...] all downstream tables might need to be rerun, depending on if the columns impacted by the bug fix were consumed by that table [...] dashboard lineage [...] SQL parsing

[One of the biggest lessons I've learned from analytics engineering is the value of wide, flat, denormalized tables / views. Maintaining "One Wide Table" per downstream task is so much easier than requiring consumers (viz, BI, ML) to do their own joins....](https://twitter.com/pbailis/status/1428801544367984645).

[In theory, UDFs should make deploying cloud analytics easy.](https://twitter.com/pbailis/status/1428458584040374280).

[Build Trust In Your Data By Understanding Where It Comes From And How It Is Used With Stemma](https://www.dataengineeringpodcast.com/stemma-data-discovery-episode-211/)

> [12:46] somebody deprecated a column. If you're lucky, someone told you they have deprecated a column in the upstream store

> [24:50] parsing your query log and understanding what are the common ways the data gets joined or filtered 

[Data Mesh and Domain Ownership](https://www.youtube.com/watch?v=GCNOOB9cFdU). 

[Data Driven with Data Mesh – Pragmatism in Practice](https://www.youtube.com/watch?v=e6lqj5PpxOs).

[Data Mesh Principles and Logical Architecture](https://martinfowler.com/articles/data-mesh-principles.html)

[Just One More Stratification!](https://greatexpectations.io/blog/one-more-stratification/).

[Making dashboards faster](https://www.metabase.com/learn/administration/making-dashboards-faster).

> Ask for less data.
> Cache answers to questions.
> Organize data to anticipate common questions.
> Ask efficient questions.

[Design a data mesh architecture using AWS Lake Formation and AWS Glue](https://aws.amazon.com/blogs/big-data/design-a-data-mesh-architecture-using-aws-lake-formation-and-aws-glue/)

[schema-on-write, or not?](https://news.ycombinator.com/item?id=28260328)

[What the Heck is a Data Mesh?!](https://cnr.sh/essays/what-the-heck-data-mesh)

[Taking what I understand about data mesh and applying portions to the modern stack](https://twitter.com/sethrosen/status/1425594775986659328)

[Is data mesh simply an organization having a separate dbt projects per unit all producing their own marts?](https://twitter.com/sethrosen/status/1425595435301883907)

[What Is an OLAP Cube? An Exhaustive Explainer](https://www.holistics.io/blog/what-is-an-olap-cube-an-exhaustive-explainer/). [hn](https://news.ycombinator.com/item?id=28401230).

> Depends if you want to go the vendor route, where "cube" is very specific to the implementation of the tool you're implementing. Dealing with semi-additive measures and drill-down/drill-through will differ between SSAS, Pentaho, or Cognos.

> I think the real value in the process comes from all the data modeling decisions, which involves a lot of interactions with the business users that are asking for data/reports. Something as simple as an e-commerce order can look very different between CEO KPI reports, marketing, purchasing, and accounting. For example, accounting cares only when the product ships while marketing cares when it's sold. Multiply this by a hundred, and you end up with nuanced data pipelines that encapsulate all this domain-specific logic.

> Multidimensional modeling is very useful even if you're not adopting cubes specifically, and just using dbt on a read-only replica of your database to create aggregate table for a few dozen reports.

> people can really get hung up on jargon like this. the real concept is dimensional modeling which is a whole strategy and toolkit of ideas for doing online analytical processing. you can do it with anything, the data warehouse toolkit was calling it "rowlap" when you did in a regular database. you would be dead lost trying to use a proper "olap" tool with special sparse matrix data structures and MDX queries without understanding concepts like the various types of dimension tables and how they can be nested etc.

[semi-additive measure](https://www.oraylis.de/blog/2012/semi-additive-measures-in-sql-server-standard-edition)

> Semi additive measures are measures that have a different way of aggregation over time (or other specific dimensions). For example, thinking of stock values you want to sum them up by product, location, country etc. but not by time (here you may want to see the last value, the average, the minimum/maximum or whatever).

[what the heck is a data mesh?](https://news.ycombinator.com/item?id=27999348). [another HN link](https://news.ycombinator.com/item?id=26581271).

> Without the right data infrastructure technology, the data mesh will lead to an overwhelming number of data silos, that makes accessing the data products from other teams inconvenient, intractable, or infeasible.

[How to Move Beyond a Monolithic Data Lake to a Distributed Data Mesh](https://martinfowler.com/articles/data-monolith-to-mesh.html).

[Minerva](https://medium.com/airbnb-engineering/airbnb-metric-computation-with-minerva-part-2-9afe6695b486)

[at Zalando](https://databricks.com/session_na20/data-mesh-in-practice-how-europes-leading-online-platform-for-fashion-goes-beyond-the-data-lake)

[what is a Data Lakehouse](https://www.snowflake.com/guides/what-data-lakehouse)

[the rise of the analytics engineer](https://twitter.com/pbailis/status/1436021624927494154)

[Is BI dead? – On dismantling data's ship of Theseus](https://news.ycombinator.com/item?id=28580298)

