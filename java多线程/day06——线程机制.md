# 线程机制

## 线程优先级

![1581329084699](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581329084699.png)

先设置优先级再启动

![1581329350557](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581329350557.png)



## 守护线程

```java
Thread thread =new Thread(god);
thread.setDaemon(true);	//默认是false表示是用户线程，正常的线程都是用户线程。

```

![1581330090245](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581330090245.png)



## 并发

同一个对象被多个线程同时操作



## 线程同步

![1581330408811](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581330408811.png)

队列+锁（synchronized）

每个对象都有一把锁

![1581330667132](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581330667132.png)



![1581383860125](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581383860125.png)

synchronized关键词

只读代码不需要同步，修改代码才需要同步

synchronized方法默认锁的是this对象。

锁错对象无法同步。

锁的对象是变化的量（增删改查）

## 同步块

![1581384326567](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581384326567.png)

要锁另一个对象，就要用同步块。

## JUC安全类型

ArrayList 线程不安全

CopyOnWriteArrayList线程安全

（源码用了volatile)

 JUC就是java.util.concurrent包，俗称java并发包 