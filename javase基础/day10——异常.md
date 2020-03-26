# 异常

![1580870192541](C:\Users\57246\AppData\Roaming\Typora\typora-user-images\1580870192541.png)

三种异常

1. 检查性异常
2. 运行时异常
3. 错误ERROR



Java把异常当做对象来处理，并定义一个基类java.lang.Throwable作为所有异常的超类。这些异常类分为两大类，ERROR(不可预见)和Exception(可预见)

## 异常处理机制

1. 抛出异常
2. 捕获异常
3. 关键字：try，catch，finally,throw,throws

```java
try{
    
}catch(Exception e){
    
}finally{
    
}

//finally 可以不用，一般处理善后工作。

//多个catch要有顺序，先子类后父类,否则报错
try{
    
}catch(Exception e){
    e.printStackTrace();	//打印错误的栈信息
}catch(Throwable e){
    
}


//throw 主动抛出异常，一般在方法中使用。

try{
    if(b==0)
        throw new Exception();	//
    
}catch(Exception e){
    e.printStackTrace();	//打印错误的栈信息
}catch(Throwable e){
    
}


void test () throws Exception{}
    if(b==0)
        throw new Exception();	//
    
}


//最后尽量添加finally去释放占用资源
```



## 自定义异常

自定义的话，只需继承Exception类即可。