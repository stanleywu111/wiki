## 1 进程环境
进程

* 程序的执行实例被称为进程(process)
* 进程具有独立的权限与职责。如果系统中某个进程崩溃，它不会影响到其余的进程。
* 每个进程运行在其各自的虚拟地址空间中，进程之间可以通过由内核控制的机制相互通讯。  

进程ID：每个linux进程都一定有一个唯一的数字。

启动例程

* 在进程的main函数执行之前内核会启动
* 编译器在编译时会将启动例程编译进可执行文件中

启动例程作用

* 搜集命令行的参数传递给main函数中的argc和argv
* 搜集环境信息构建环境表并传递给main函数
* 登记进程的终止函数

进程终止

* 正常终止
    * 从main函数返回
    * 调用exit(标准c库函数)
    * 调用_exit或_Exit(系统调用)
    * 最后一个线程从其启动例程返回
    * 最后一个线程调用pthread_exit
* 异常终止
    * 调用abort
    * 接受到一个信号并终止
    * 最后一个线程对取消请求做处理响应

## 2 进程控制
查看进程命令
```
ps
```
查看进程详细参数命令
```
ps -aux
```

* USER 进程的宿主
* PID 进程的ID
* PPID 父进程
* %CPU 进程占用的CPU百分比
* %MEM 进程占用内存的百分比
* NI 进程的NICE值，数值大，表示较少占用CPU的时间
* VSZ 进程虚拟大小
* RSS 驻留中页的数量
* TTY 终端ID
* WCHAN 正在等待的进程资源
* START 启动进程的时间
* TIME 进程消耗CPU的时间
* COMMAND 命令的名称和参数

进程的常见状态

* 运行状态
* 等待状态
* 停止状态
* 僵尸状态

### 2.1 进程调度

1. 处理内核中的工作
2. 处理当前进程
3. 选择进程
    1. 实施进程
    2. 普通进程
4. 进程交互

启动进程后，在内核中创建task_struct结构体：

* 策略
    * 轮流策略
    * 先进先出策略
* 优先权
    * Jiffies变量
* 实时优先权
    * 实时进程之间
* 计数器

### 2.2 进程创建
父进程使用fork函数创建子进程
```c
#include <unistd.h>

pid_t fork(void);
pid_t vfork(void);
```
fork创建的新进程被称为子进程，该函数被调用一次，但是返回两次。两次返回的的区别是：在子进程中的返回值是0，而在父进程中的返回值是新子进程的ID。创建子进程，父进程哪个先运行根据系统调度且复制父进程的内存空间。vfork也可以创建子进程，但是子进程先运行且不复制父进程的内存空间。

#### 2.2.1 子进程继承
