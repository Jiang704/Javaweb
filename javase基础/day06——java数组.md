# 数组

## 声明数组

建议int [] num;

int num[];也行

int[] nums = new int[10];	//动态 所有元素被初始化为0

int [] nums ={1,2,3,4,5};	//静态

数组的长度是确定的，一旦确立，不可改变。

数组本身就是对象属于引用类型。

数组对象本身是在堆中的。但数组引用对象的变量（即num本身）在栈中。

```java
int[][] arr = new int[3][4];
int[][] arr = new int[3][];
```

快捷遍历

for(int x: nums)

输入nums.for回车

sout快速打出输出命令



## Arrays类

java.util.Arrays

该类包含排序，操作等多种内置静态方法。

Arrays.toString(nums)

Arrays.sort(nums)

Arrays.fill(nums,0)	//把nums数组都填充为0

Arrays.fill(nums,2,4,0)