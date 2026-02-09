[Inserting One Billion Rows in SQLite Under a Minute ](https://news.ycombinator.com/item?id=27872575)

[Atomic Commit In SQLite ](https://lobste.rs/s/ysri9z/atomic_commit_sqlite)

[Consider SQLite](https://blog.wesleyac.com/posts/consider-sqlite)

[SQLite 3.38.0](https://lobste.rs/s/gdu6pt/sqlite_release_3_38_0)

> JSON was not first class

[JSON improvements in SQLite 3.38.0](https://tirkarthi.github.io/programming/2022/02/26/sqlite-json-improvements.html)

[Database Migration: SQLite to PostgreSQL](https://bytebase.com/blog/database-migration-sqlite-to-postgresql)

[Getting Started with SQLite on macOS / Mac OS X](https://razorsql.com/articles/sqlite_mac.htm)

[SQLite and Go](https://twitter.com/kelseyhightower/status/1516293351384834048)

[Have you used SQLite as a primary database?](https://news.ycombinator.com/item?id=31152490)

[I'm all-in on server-side SQLite](https://news.ycombinator.com/item?id=31318708)

[JSON and Virtual Columns in SQLite](https://news.ycombinator.com/item?id=31396578)

[Temporary tables in SQLite](https://antonz.org/temp-tables/)

[SQLite Data Starter Packs | Public Affairs Data Journalism at Stanford | Fall 2016](http://2016.padjo.org/tutorials/sqlite-data-starterpacks/). [Public Affairs Data Journalism, Fall 2017 — Padjo 2017 0.1 documentation
](http://2017.padjo.org/)

[SQLite or PostgreSQL? It's Complicated](https://news.ycombinator.com/item?id=31908186)

[SQLite: Past, Present, and Future](https://news.ycombinator.com/item?id=32909167)

[history of SQLite](https://twitter.com/aboodman/status/1633351940833947654)

[Data analysis with SQLite and Python](https://twitter.com/simonw/status/1649100818841501696)

[why sqlite in Epic Stack](https://twitter.com/kentcdodds/status/1657417017069277186)

[Code Generator for SQLite](https://news.ycombinator.com/item?id=35981828)

[sqlite on the edge](https://news.ycombinator.com/item?id=36208568)

[Select random row from a sqlite table](https://stackoverflow.com/questions/2279706/select-random-row-from-a-sqlite-table)

> SELECT * FROM table ORDER BY RANDOM() LIMIT 1;

[random sampling gist](https://gist.github.com/alecco/9976dab8fda8256ed403054ed0a65d7b#file-random-sampling-sql-L11). [more](https://gist.github.com/swayson/84fc86da20db89b56eac). 

[Random value duplicated, cannot select N random pairings, subquery not refreshing - sqlite](https://dba.stackexchange.com/questions/302614/random-value-duplicated-cannot-select-n-random-pairings-subquery-not-refreshin)

[Datasette tutorial: Data analysis with SQLite and Python](https://twitter.com/simonw/status/1675546706468044803)

[Building a pivot table in SQLite](https://antonz.org/sqlite-pivot-table/)

[Why you should probably be using SQLite](https://news.ycombinator.com/item?id=38036921)

[user_version PRAGMA](https://www.sqlite.org/pragma.html#pragma_user_version). [in golang](https://stackoverflow.com/questions/41646639/retrieving-sqlite-pragma-user-version-with-golang). [Tracking SQLite Database Changes in Git](https://lobste.rs/s/gnv9ho/tracking_sqlite_database_changes_git).

[Database generated columns ⁽¹⁾: Django & SQLite](https://www.paulox.net/2023/11/07/database-generated-columns-part-1-django-and-sqlite/)

[sqlite has landed](https://news.ycombinator.com/item?id=38540421)

[SQLite: Wal2 Mode](https://news.ycombinator.com/item?id=38988949)

[starting with sqlite](https://twitter.com/simonw/status/1752043154445074643)

[Optimizing SQLite for servers](https://kerkour.com/sqlite-for-servers)

[Best practices for in-app database migration for Sqlite](https://stackoverflow.com/questions/989558/best-practices-for-in-app-database-migration-for-sqlite). [related](https://stackoverflow.com/questions/752298/database-migrations-manage-with-build-script-or-automatic-on-app-startup).

> When the app starts, I check the current user-version, apply any changes that are needed to bring the schema up to date, and then update the user-version. I wrap the updates in a transaction so that if anything goes wrong, the changes aren't committed.

[Why SQLite Uses Bytecode](https://sqlite.org/draft/whybytecode.html). [hn](https://news.ycombinator.com/item?id=40206752).

[generated columns](https://lobste.rs/s/imyxxn/modern_sqlite_generated_columns)

[Why does SQLite (in production) have such a bad rep?](https://lobste.rs/s/fxkk7v/why_does_sqlite_production_have_such_bad)

[Yggdrasil - Schema migrations made easy, in Haskell](https://www.reddit.com/r/haskell/comments/1fk3pw0/yggdrasil_schema_migrations_made_easy_in_haskell/)

[one sqlite database per user](https://x.com/iavins/status/1850036886938497410)

[PSA: SQLite does not do checksums](https://avi.im/blag/2024/sqlite-bit-flip/)

[SQLite or PostgreSQL? It's Complicated](https://www.twilio.com/en-us/blog/sqlite-postgresql-complicated). [rs](https://lobste.rs/s/2etd7f/sqlite_postgresql_it_s_complicated).

[Siren Call of SQLite on the Server](https://pid1.dev/posts/siren-call-of-sqlite-on-the-server/). [rs](https://lobste.rs/s/t1enph/siren_call_sqlite_on_server). [migrations](https://lobste.rs/s/iypstr/simple_declarative_schema_migration_for). [at what scale?](https://rivet.gg/blog/2025-02-16-sqlite-on-the-server-is-misunderstood)

[Why ALTER TABLE is such a problem for SQLite](https://lobste.rs/s/nsjybj/why_alter_table_is_such_problem_for_sqlite).

[Many Small Queries Are Efficient in SQLite](https://news.ycombinator.com/item?id=46742635).

[SQLite is a Self Contained System](https://sqlite.org/selfcontained.html). [hn](https://news.ycombinator.com/item?id=46838361).

> Default builds of SQLite contain appropriate VFS objects for talking to the underlying operating system, and those VFS objects will contain operating system calls such as open(), read(), write(), fsync(), and so forth. All of these interfaces are readily available on most platforms, and custom VFSes can be designed to run SQLite on even the most austere embedded devices.

[SQLite databases are recommended by the US Library of Congress as a storage format for long-term preservation of digital content.](https://www.sqlite.org/appfileformat.htm)

[sqlite concurrency and DEFERRED transaction](https://news.ycombinator.com/item?id=45781519). [SQLITE_BUSY](https://simonwillison.net/tags/sqlite-busy/). [What to do about SQLITE_BUSY errors despite setting a timeout](https://berthub.eu/articles/posts/a-brief-post-on-sqlite3-database-locked-despite-timeout/)





