- See [here](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04) to install mysql on ubuntu.

- ```mysqladmin``` to create databases.

- ```mysql -p -u username userdb``` to connect.

- ```mysql -p -u username userdb < foo.sql``` to load a file

- MySQL lacks the RANK() analytic function.

- [string functions](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html)

- [Splittin comma-separated values in MySQL](https://www.periscopedata.com/blog/splitting-comma-separated-values-in-mysql.html)

- [cursors in mysql](https://dev.mysql.com/doc/refman/5.7/en/cursors.html) [cursor trouble](http://rpbouman.blogspot.com.es/2005/09/why-repeat-and-while-are-usually-not.html) [continue handlers](https://dev.mysql.com/doc/refman/5.7/en/declare-handler.html)

- [substring](https://dev.mysql.com/doc/refman/5.7/en/string-functions.html#function_substring)

> For all forms of SUBSTRING(), the position of the first character in the string from which the substring is to be extracted is reckoned as 1.

- [MySQL and CTEs](http://stackoverflow.com/questions/1382573/how-do-you-use-the-with-clause-in-mysql)

- [range of dates](http://stackoverflow.com/questions/9295616/how-to-get-list-of-dates-between-two-dates-in-mysql-select-query) [another solution](http://stackoverflow.com/questions/510012/get-a-list-of-dates-between-two-dates) [with recursive cte, not posible in MySQL](http://stackoverflow.com/questions/7824831/generate-dates-between-date-ranges)

- [MySQL infrastructure testing automation at GitHub](https://news.ycombinator.com/item?id=14711814)

- [How to Deal with XA Transactions Recovery](https://www.percona.com/blog/2017/09/22/how-to-deal-with-xa-transactions-recovery/)

- [MySQL vs. MariaDB: Reality Check](https://www.percona.com/blog/2017/11/02/mysql-vs-mariadb-reality-check/)

- [memory saturated mysql](https://blog.koehntopp.info/2021/02/28/memory-saturated-mysql.html)

# example custom function 

    DELIMITER ;;

    CREATE FUNCTION hello (s CHAR(20))
    RETURNS CHAR(50) DETERMINISTIC
    BEGIN
        RETURN CONCAT('Hello, ',s,'!');
    END;;

    DELIMITER ;

- [MySQL High Availability at GitHub](https://githubengineering.com/mysql-high-availability-at-github/) [hn](https://news.ycombinator.com/item?id=17357319)

>  a kind of interesting tradeoff in distributed databases: using consensus to store your data, or using consensus to point at the master for the data.

> Replicating data in consensus groups gives some nice guarantees, in particular it can guarantee monotonic read consistency even if you're not reading from the leader, at the cost of a network round-trip. Switching between master-slave replicas might cause you to go back and forth in time, even if replication is synchronous.

> There are also some potential availability benefits to storing data in consensus groups, though most implementations use leader leases to improve performance, which reduces availability in case of leader failure. A master-slave system that does synchronous replication could do failovers that are just as fast as leader changes in a consensus protocol.

> The pain of storing data in consensus groups is in performance, especially concurrency. Every write to the log requires some synchronization with a quorum to ensure consensus on the order. That introduces extra round-trips and makes it hard to handle high concurrency.

[REPEATABLE-READ and READ-COMMITTED Transaction Isolation Levels](https://www.percona.com/blog/2012/08/28/differences-between-read-committed-and-repeatable-read-transaction-isolation-levels/)

[Deadlocks 101 – MySQL](https://sergiuoltean.com/2019/04/25/deadlocks-101-mysql/)

[choose something else](https://grimoire.ca/mysql/choose-something-else)

