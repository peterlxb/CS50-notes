在C语言里有三个地方可以用来定义变量

> Inside a function or a block which is called **local **variables.
>
> Outside of all functions which is called **global **variables.
>
> In the definition of function parameters which are called **formal **parameters.

本地变量，全局变量以及形式参数。

## Local Variables 本地变量

定义在一个函数或者块中的变量称为本地变量也叫局部变量。

它们只能被这个函数或块中的表达式使用。

本地变量如何使用的示例代码

```
#include <stdio.h>
 
int main () {

  /* local variable declaration */
  int a, b;
  int c;
 
  /* actual initialization */
  a = 10;
  b = 20;
  c = a + b;
 
  printf ("value of a = %d, b = %d and c = %d\n", a, b, c);
 
  return 0;
}
```

## Global Variables 全局变量

全局变量定义在函数外面，一般在程序的最上面。在整个程序的生命周期里全局变量都是可用的。

全局变量可以被所有函数使用。

全局变量如何使用的示例代码

```
#include <stdio.h>
 
/* global variable declaration */
int g;
 
int main () {

  /* local variable declaration */
  int a, b;
 
  /* actual initialization */
  a = 10;
  b = 20;
  g = a + b;
 
  printf ("value of a = %d, b = %d and g = %d\n", a, b, g);
 
  return 0;
}
```

上面代码执行后输出的结果

```
value of g = 10
```

## Formal Parameters 形式参数

> Formal parameters, are treated as local variables with-in a function and they take precedence over global variables.

形式参数在函数内部被当作局部变量对待。优先级高于全局变量。

使用示例

```
#include <stdio.h>
 
/* global variable declaration */
int a = 20;
 
int main () {

  /* local variable declaration in main function */
  int a = 10;
  int b = 20;
  int c = 0;

  printf ("value of a in main() = %d\n",  a);
  c = sum( a, b);
  printf ("value of c in main() = %d\n",  c);

  return 0;
}

/* function to add two integers */
int sum(int a, int b) {

   printf ("value of a in sum() = %d\n",  a);
   printf ("value of b in sum() = %d\n",  b);

   return a + b;
}
```

上面的代码编译和执行后，输出的结果

```
value of a in main() = 10
value of a in sum() = 10
value of b in sum() = 20
value of c in main() = 30
```

## Initializing Local and Global Variables 初始化局部和全局变量

当定义一个局部变量，系统不会自动去初始化它，需要自己去初始化。

全局变量定义后，系统会自动初始化。

![](/assets/initial-global.png)



