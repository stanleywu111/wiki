## 为什么要使用Disruptor
### 基于队列的生产者，消费者模型的弊端
why is the blocking queue slow? Write contention induced thread arbitrage and false sharing cause lots of memory access
### Cache Line Padding

### Mechanical Sympathy

### Memory Barrier
### Producer Barrier
### Design of Disruptor
Avoid write principle:

* Single Writer principle, multiple consumer
* No locks
    * Sequencing
    * Memory barrier(volatile)
    * CAS(compare and swap)
* Avoid false sharing
    * Padding
* Bonus
    * Batching effect
    * Dependence graph