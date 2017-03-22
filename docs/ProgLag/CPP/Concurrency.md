## Thread
Thread is a sequence of instructions executed independently. This implies that thread must have its own state, enough to be executed:

* program encounter or equivalent
* stack
* registers

Threads share momeory space, processes(mostly) don`t. Thread has smaller state, process has much more state(signal handlers, interrupts, parent and child process infromation, access and user data, secheduling information, etc). And threads are contained in a process. 操作系统中的线程类型：

* 硬件线程
* 内核线程
* 用户线程（内核线程的抽象）
* 程序线程

线程的启动和执行非常昂贵，所有应用程序有时需要复用线程。多线程执行任务的流程：

1. 有一个任务需要执行
2. 为该任务创建一个线程
3. 为其他独立的任务创建一个线程
4. Join线程

### Threads in C++

## Data Race

## 线程和内存
