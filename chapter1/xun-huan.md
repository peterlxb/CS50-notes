基本的循环示意图

![](/assets/loop_architecture.jpg)

## 第一种就是while循环

语法很简单

```
while(condition) {
   statement(s);
}
```

流程图

![](/assets/cpp_while_loop.jpg)

示例代码

```
#include <stdio.h>
 
int main () {

   /* local variable definition */
   int a = 10;

   /* while loop execution */
   while( a < 20 ) {
      printf("value of a: %d\n", a);
      a++;
   }
 
   return 0;
}
```

## 第二种for循环

```
for ( init; condition; increment )
{
    statement(s);
}
```

中间的condition可以省略掉，就成了无限循环。

流程示意图也很简单

![](/assets/cpp_for_loop.jpg)

```
#include <stdio.h>
 
int main () {

   int a;
	
   /* for loop execution */
   for( a = 10; a < 20; a = a + 1 ){
      printf("value of a: %d\n", a);
   }
 
   return 0;
}
```

## 第三种do....while循环

这个循环的优点是至少执行一次

```
do {
   statement(s);
} while( condition );
```

![](/assets/cpp_do_while_loop.jpg)

示例代码

```
#include <stdio.h>
 
int main () {

   /* local variable definition */
   int a = 10;

   /* do loop execution */
   do {
      printf("value of a: %d\n", a);
      a = a + 1;
   }while( a < 20 );
 
   return 0;
}
```



