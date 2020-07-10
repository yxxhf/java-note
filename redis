# Redis理论及应用经验总结 #
 

  **`Redis是一个键值缓存和存储框架（KV Cache and Store）主要实现功能：`**

      1、In-Memory缓存：所有的数据查询都在缓存中，100万KV键值对，其中V是String类型，仅仅占用100M内存；
    
      2、持久化：缓存中的数据能够自动持久化到硬盘中，目的不是存储数据，而是防止分布式系统雪崩，内存数据丢失；持久化主要采用两种方式：快照（采用异步的方式把内存中的数据同步到硬盘上，格式是RDB）和附加文件（把每次的写操作，都写在一个文件中，采用日志的方式恢复数据，文件格式：AOF）；
    
      3、主从模式：支持Master-Slave Replication，其中Master负责读写操作，Slave负责读操作；同时支持分布、订阅模式（Pub/Sub)。
    
      4、分布式：能够支持分布式缓存、存储；

 **Redis同时也是一个数据结构服务器，是 因为KV中V支持String、List、hash、Set、Sorted Set、BitMap、happerloglogs共六种数据结构。**


    Redis与Memcached的区别：
    
    1、Memcached是一个分布式内存对象缓存系统，而Redis是一个缓存和存储系统，能够把内存数据进行持久化
    
    2、Memcached支持多线程，而 Redis支持单线程，由于Redis是主要是缓存数据，对于CPU要求不高，单线程对于性能没有太大影响
    
    3、Memcached的KV中V只支持String，也可以缓存一些图片和视频，而Redis支持多种数据类型，包括String、List、Set、Hash、Sorted Set、Bitmap、 Happerloglogs
    
    4、对于性能上两者相似
    
    5、对于两者的KV中Value值存储大小不同，Redis的Value值能够 支持1G，而Memcached的Value值只能存储字符，存储数据最大是1M
    
    6、从 架构角度来Redis支持主从模式和分布式，而Memcached只支持分布式缓存

**数据 存储系统目前有三类：**

    1、RDBMS：关系数据库，主要有Oracle、Mysql、Sqlserver、DB2
    
    2、Nosql：就是 非关系 数据库：redis、Hbase（列簇存储）、 Memcached（这个只是缓存存放数据）、MongoDB（文档数据库），其中Nosql数据库有分种类型：KV存储、文档存储、 图片存储（neo4j）、列簇存储
    
    3、Newsql：对种新的可扩展、分布式数据库简称，不仅有Nosql数据库大量数据存储和查询能力，也具有RDBMS 数据库的ACID和   SQL特性；主要 代表有：FoundationDB、RethinkDB.....

Redis守护进程监听端口：6379
