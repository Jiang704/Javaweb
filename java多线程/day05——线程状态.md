# 线程状态

## 线程停止



![1581233383749](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581233383749.png)![1581233436280](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581233436280.png)![1581233489193](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581233489193.png)



测试stop

1. 建议线程正常停止——利用次数，不建议死循环
2. 建议使用标志位
3. 不要使用stop或者destory



## 线程休眠

![1581233788455](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581233788455.png)



## 线程礼让

![1581317675373](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581317675373.png)

Thread.yield();



## join

![1581318031731](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581318031731.png)

thread().join();

（插队的线程走完，其他线程才能走。



## 观测线程状态

![1581318364331](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581318364331.png)

![1581318777150](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1581318777150.png)