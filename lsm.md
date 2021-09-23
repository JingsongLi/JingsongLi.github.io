<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

## LSM Learning materials

LSM is widely used. It can be said that most distributed systems have its shadow:
- KV: RocksDb
- Database: MyRocks
- Distributed KV: HBase, Cassandra
- Distributed Database: TiDB, CockroachDB
- OLAP: Clickhouse, Hologres
- Streaming State: Flink, KSQL

In particular, the latest MPP OLAP and streaming systems expand the boundary of LSM.

### Comprehensive

[LSM-based Storage Techniques: A Survey](https://arxiv.org/pdf/1812.07527v1.pdf)

[LSM-based Storage Techniques: A Survey (Chinese) 1](https://zhuanlan.zhihu.com/p/400293980)

[LSM-based Storage Techniques: A Survey (Chinese) 2](https://zhuanlan.zhihu.com/p/403396976)

### Compaction

[Scylla’s Compaction Strategies Series: Space Amplification in Size-Tiered Compaction](https://www.scylladb.com/2018/01/17/compaction-series-space-amplification/)

[Scylla’s Compaction Strategies Series: Write Amplification in Leveled Compaction](https://www.scylladb.com/2018/01/31/compaction-series-leveled-compaction/)

[Dostoevsky: Better Space-Time Trade-Offs for LSM-Tree Based Key-Value Stores via Adaptive Removal of Superfluous Merging (2018)](https://nivdayan.github.io/dostoevsky.pdf)

[Dostoevsky Chinese Guide reading](https://www.jianshu.com/p/8fb8f2458253)

[Blog of Dostoevsky Author: Niv Dayan](https://nivdayan.github.io/)

LSM Merge in Clickhouse
Clickhouse/src/Storages/MergeTree/SimpleMergeSelector

LSM Compaction analysis (Chinese)
https://zhuanlan.zhihu.com/p/140325974

### Read

[Monkey: Optimal Navigable Key-Value Store](https://stratos.seas.harvard.edu/files/stratos/files/monkeykeyvaluestore.pdf)

[WiscKey: Separating Keys from Values in SSD-conscious Storage](https://www.usenix.org/system/files/conference/fast16/fast16-papers-lu.pdf)

[Introducing Badger: A fast key-value store written purely in Go](https://dgraph.io/blog/post/badger/)

[TerarkDB was forked from RocksDB v5.18.3 and aims to build a better replacement of RocksDB in most cases](https://bytedance.feishu.cn/docs/doccnZmYFqHBm06BbvYgjsHHcKc#)

[Titan: A RocksDB Plugin to Reduce Write Amplification](https://en.pingcap.com/blog/titan-storage-engine-design-and-implementation)

[WiscKey 发布的五年后，工业界用上了 KV 分离吗？](https://zhuanlan.zhihu.com/p/397466422)

### Optimization for OLAP

[Clickhouse Merge Tree Engines (Collapsing tree: Aggregation for CDC)](https://clickhouse.tech/docs/en/engines/table-engines/mergetree-family/collapsingmergetree/)

[Alibaba Hologres: A Cloud-Native Service for Hybrid Serving/Analytical Processing (Delete Bitmap)](http://www.vldb.org/pvldb/vol13/p3272-jiang.pdf)
