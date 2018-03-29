一个简单的函数示例

接受两个参数，都为int类型，返回较大的值

```
/* function returning the max between two numbers */
int max(int num1, int num2) {

   /* local variable declaration */
   int result;
 
   if (num1 > num2)
      result = num1;
   else
      result = num2;
 
   return result; 
}
```

函数声明

> A function **declaration **tells the compiler about a function name and how to call the function.

一个函数声明由下面几部分组成

```
return_type function_name( parameter list );
```

返回类型，函数名，里面是参数列表。

上面的max函数，声明的话可以写成下面形式

```
int max(int num1, int num2);
```

在声明时参数名不是必须的，下面的格式也是合法的

```
int max(int, int);
```

## Calling a Function调用一个函数

当程序\(program\)开始调用一个函数,程序的控制权转移到这个被调用的函数上。

然后这个被调用的函数开始执行已经定义的task，当执行到内部的返回语句或是函数底部。

将控制权返回给主函数。

示例

```
#include <stdio.h>
 
/* function declaration */
int max(int num1, int num2);
 
int main () {

   /* local variable definition */
   int a = 100;
   int b = 200;
   int ret;
 
   /* calling a function to get max value */
   ret = max(a, b);
 
   printf( "Max value is : %d\n", ret );
 
   return 0;
}
 
/* function returning the max between two numbers */
int max(int num1, int num2) {

   /* local variable declaration */
   int result;
 
   if (num1 > num2)
      result = num1;
   else
      result = num2;
 
   return result; 
}
```



