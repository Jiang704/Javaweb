# 内部类

1.类内定义内部类

2.一个文件中

public class{}

class A{}		//也是一个内部类

一个java类中可以有多个class 类，但只能有一个public class类

3.方法里面也可以定义内部类——叫局部内部类

4.匿名类

## 实例化

通过外部类实例内部类

Outer  outer = new Outer();

Outer.Inner  inner = outer.new Inner();



内部类可以获得外部类的私有属性

 