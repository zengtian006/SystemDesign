## 面试的时候如何理清头绪

1. 讨论用户是谁
2. 根据用户讨论 feature and funtion
3. 问一下系统需要 estimate traffic
4. 根据 feature 讨论系统需要存储和 serve 哪些 data, 这些 data 用什么存， 讨论 sql/nosql/cache/object storage/hdfs 取舍
5. 根据数据， 设计 service。 画图。
6. work through 一个 use case, 把所有 service 连起来， 同时修改刚才画好的图。 比如 做 uber eats, 讨论用户要 order 一个食物，到餐馆接到订单， 到司机接到订单。。。。
7. 讨论 use case 细节， 比如 uber eats 司机进入某个区域怎么识别啊， cache 里怎么存啊。面试官全程都会 drive 你的 design 的， 不会丢你在那里自言自语。
8. 面试官会问， 某些环节挂掉了，怎么处理。 主要是避免 Single point of Failure
   - Replica， master slave, active-passive 或者
   - 周期存 snapshot 在磁盘上，然后存 action log... 挂了可以重新恢复。
9. 最后会问怎么 scale out. multi instance, partition，Load balance。 偶尔说说 Service Mesh, Microservice.

以上流程参考一亩三分地，适用与没有太多工作经验者面试较紧张没头绪的同学或，可以简单参考
