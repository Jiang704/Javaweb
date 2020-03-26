# 可变参数

jdk1.5加入

当不确定函数有多少个参数时使用，只能有一个，且必须在最后。

传参时可以传多个数，也可以传递一个数组。

```java
public void max(double ... x){

    for(int i=0;i<x.length;i++)
​  		System.out.println(x[i]);

}
```



