数组array简介

> Arrays a kind of data structure that can store a fixed-size sequential collection of elements of the same type.

数组是一种数据结构，用来存储一个固定大小的相同类型的集合类型的数据。

可以把数组理解为一个相同类型的变量的集合。

> All arrays consist of contiguous memory locations.

![](/assets/arrays.jpg)

声明一个数组

语法：

```
type arrayName [ arraySize ];
```

上面声明的是一个单维数组。

arraySize必须是一个大于0的整数，type可以是任意C的数据类型。

比如下面的

```
double balance[10];
```

初始化数组

```
double balance[5] = {1000.0, 2.0, 3.4, 7.0, 50.0};
```

示例

```
#include <stdio.h>

int main () {

   int n[ 10 ]; /* n is an array of 10 integers */
   int i,j;

   /* initialize elements of array n to 0 */         
   for ( i = 0; i < 10; i++ ) {
      n[ i ] = i + 100; /* set element at location i to i + 100 */
   }

   /* output each array element's value */
   for (j = 0; j < 10; j++ ) {
      printf("Element[%d] = %d\n", j, n[j] );
   }

   return 0;
}
```

输出

```
Element[0] = 100
Element[1] = 101
Element[2] = 102
Element[3] = 103
Element[4] = 104
Element[5] = 105
Element[6] = 106
Element[7] = 107
Element[8] = 108
Element[9] = 109
```



