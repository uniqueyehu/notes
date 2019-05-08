分布式系统研究大致分为三大部分：

1. **分布式存储系统**
2. **分布式计算系统**
3. **分布式管理系统**

**分布式存储系统**主要涵盖四个方向：

1. **结构化存储**
2. **非结构化存储**
3. **半结构化存储**
4. **In-memory存储**

**结构化存储**典型的场景是关系型数据库，强调（1）[结构化的数据](https://www.webopedia.com/TERM/S/structured_data.html)；（2）强一致性；（3）随机访问（索引，增删改查）。通常为高性能单机，导致可扩展性不好。

**非结构化存储**强调可扩展性，高吞吐量，随机访问性能差。典型的系统是分布式文件系统，如GFS等。

**半结构化存储**介于结构化和非结构化之间，兼顾随机访问，可扩展性，通常为NoSQL的键值存储系统，Bigtable、HBase等。

**In-memory存储**针对高并发，低延时的需求，利用内存做高性能缓存，如memcached、Redis等。

**NewSQL**兼具RDBMS特性，又有NoSQL强大的可扩展性，如Spanner、F1等，拥有Google的众多黑科技。

---

分布式基础理论：

1. CAP理论原理、ACID、BASE
2. 一致性算法：Paxos/Raft
3. 一致性层次：强一致性、弱一致性、最终一致性
4. 分布式事务：两阶段、三阶段提交协议
5. MVCC：多版本并发控制，copy-on-write与snapshot
6. consistent hashing、range partion
7. 分布式锁、乐观锁

经典论文：

1. [The Google File System.](https://github.com/uniqueyehu/notes/blob/master/distributed-system/The%20Google%20File%20System.pdf)
2. [Bigtable: A Distributed Storage System for Structured Data.](https://github.com/uniqueyehu/notes/blob/master/distributed-system/Bigtable%EF%BC%9AA%20Distributed%20Storage%20System%20for%20Structured%20Data.pdf)
3. [Spanner: Google’s Globally-Distributed Database.](https://github.com/uniqueyehu/notes/blob/master/distributed-system/Spanner%EF%BC%9AGoogle%E2%80%99s%20Globally-Distributed%20Database.pdf)
4. [Ceph: Reliable, Scalable, and High-Performance Distributed Storage.](https://github.com/uniqueyehu/notes/blob/master/distributed-system/Ceph%EF%BC%9AReliable%20Scalable%20and%20High-Performance%20Distributed%20Storage.pdf)
5. [Windows Azure Storage: A Highly Available Cloud Storage Service with Strong Consistency.](https://github.com/uniqueyehu/notes/blob/master/distributed-system/Windows%20Azure%20Storage.pdf)

分布式集群搭建：

1. Redis
2. TiDB