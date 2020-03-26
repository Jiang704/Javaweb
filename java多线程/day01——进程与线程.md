# 进程与线程

进程是执行程序的一次执行过程，是一个动态的概念。是系统资源分配的单位。

通常一个进程包含多个线程。线程是CPU调度和执行的单位。

程序运行时，后台会有多个线程，如主线程，gc线程。

由调度器安排调度。

## 多线程

三种创建方式

1. Thread class（重点）
2. Runnable 接口（重点）
3. Callable 接口



### Thread class

1. 自定义类继承Thread
2. 重新写run()方法
3. 创建线程对象，调用start()方法启动线程。



## Runnable接口

1. implements Runnable

2. 实现run()方法，重写线程执行体
3. 创建线程对象(new Thread)，需要丢入实现类，调用start()（这与Thread类方法实现不同)

```java
new Thread(testThreads).start();
```

因为java是单继承，所以推荐使用Runnable 接口，且方便一个对象被多个线程使用。



## Callable接口

1. 需要返回值类型
2. 重写call方法，需要抛出异常
3. 创建目标对象
4. 创建执行服务:ExecutorService ser = Executors.newFixedThreadPool(1);
5. 提交执行: Future<Boolen>result1 = ser.submit(t1)
6. 获取结果: boolean r1= result1.get()
7. 关闭服务:ser.shutdownNow();