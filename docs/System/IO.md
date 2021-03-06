## IO的数据结构
一个打开的文件在内核中使用三种数据结构表示

* 文件描述符表
    * 文件描述符标志
    * 文件表项指针
* 文件表项
    * 文件状态标志：读，写，追加，同步和非阻塞等状态标志
    * 当前文件偏移量
    * i节点表项指针
* i节点
    * 文件类型和对该文件的操作函数指针
    * 当前文件长度
    * 文件所有者
    * 文件所在的设备，文件访问权限
    * 指向文件数据在磁盘块上所在位置的指针等
  

## 原子操作

## 文件锁
当多个用户共同使用，操作一个文件的时间，通常采用的方法是给文件上锁，来避免共享资源
才是竞争的状态。文件锁按功能分为：

* 共享读锁
    * 文件描述符必须读打开
    * 一个进程上了读锁，其他进程也可以上读锁进行读取
* 独占写锁
    * 文件描述符必须打开
    * 一个进程上了写锁，其他进程就不能上锁和读锁进行读写操作