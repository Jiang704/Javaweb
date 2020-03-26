# 死锁

![1581387590472](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581387590472.png)

多个线程互相抱着对方需要的资源

解决方法：分成多个同步块

![1581388967186](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581388967186.png)





# Lock（锁)

![1581389032434](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581389032434.png)

```java
private final ReentrantLock lock = new  ReentrantLock();

//
lock.lock();	//加锁
lock.unlock();	//解锁
```

