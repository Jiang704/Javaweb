# 抽象类与接口

## 隐藏代码块

类运行顺序

1. static块
2. 隐藏代码快  {  };
3. 构造方法



# 抽象类

## abstract

```java

//抽象类

public abstract class Action{
    //约束，有人帮我们实现，抽象方法，只有方法名字，没有实现。
    public abstract void do();

}
```



抽象类不能new,只能继承后再用

类里面如果有抽象方法，一定为抽象类，抽象类中可以有普通方法。





## 接口

java都是单继承，但是可以通过接口实现多继承



普通类：只有具体实现

抽象类：具体实现和规范（抽象方法）都有

接口：只有抽象方法。专业的约束，约束和实现分离。面向接口编程。接口的本质是契约。

关键字：interface

接口内属性不写的话默认都是public static final ,一般不这么用

接口内方法不写的话默认都是public abstract的，可以不写

```java
public interface Us{
    void run();
}
```



接口都要有实现类（结尾加Impl)

关键词implements

```java
public class UserImpl implements Us{
    public void run(){
        
    };
}
```

要重写接口中的所有方法



接口不能被实例化