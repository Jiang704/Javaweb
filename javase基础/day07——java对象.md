# 对象

## 方法

java 方法一般都是值传递

但如果参数传入一个对象或数组，则为引用传递

new的时候会分配空间，并进行构造器的调用，并初始化值

### 构造器

就算不写,class文件中也有默认构造器（方法）

构造器

1. 必须和类的名字相同
2. 必须没有返回类型，也不能写void 
3. 一旦定义了有参构造，无参构造就必须显示定义

例：

public Person(){

}

IDEA alt+insert快捷生成构造器



### 重写(重载 override)

test为静态方法时

A a = new A();

a.test();	//输出a=>test

B b = new A();

b.test();	//输出b=>test

重写静态方法只和定义时左边有关。

//因为放在方法区，不用new分配空间即可调用。



test为非静态方法时

A a = new A();

a.test();	//输出a=>test

B b = new A();

b.test();	//输出a=>test

重写动态方法只和定义时右边有关。非静态才算重载



重写时修饰符范围可以扩大 但不能缩小

public>protected>default>private



抛出的异常，范围可以缩小，但不能扩大。







## 属性

假如有成员变量name,类型为String,则声明为String name ;
此时该变量的默认权限修饰符就是default.
下附Java成员权限修饰符权限 :
private : 只能在当前类中访问
default : 只能在当前类以及同一个包下访问
protected : 除了当前类以及同一个包下访问外,还为不在同一个包下的子类提供了一种访问父类成员的方式
public : 同一个工程下,所有包均可访问. 



## 继承

java中只有单继承——一个儿子只能有一个爸爸

子类初始化时，默认调用父类的初始化方法,

​	super();	//调用父类的构造器，必须放在代码第一行。（如果没写，系统会自动执行父类的无参构造方法）



### super注意点：

1. super调用父类的构造方法，必须在构造方法的第一个。
2. super必须只能出现在子类的方法或者构造方法中
3. super和this不能同时调用构造方法（因为都要在第一行）



this:本身调用者这个对象

super:父类的对象



## 多态

父类的引用指向子类

Object a =new Person();

多态是方法的多态

static，final,private方法不能重写



## instanceof

  instanceof通过返回一个布尔值来指出， 这个对象是否是这个特定类或者是它的子类的一个实例。 

instanceof  判断两个类是否有父子关系；

a instanceof Student  //true

b instanceof Object //true

总结

X instanceof Y

若X与Y存在父子关系，则编译成功，否则报错

如果X所指实际类型是Y的子类型，则 返回true，反之返回false.



## 类型转换

高转低（person->student)

((Student)obj).go()



子类转父类可能会丢失自己本来的一些方法。