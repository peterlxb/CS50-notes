主要是if语句和switch语句。

if..else...语法

![](/assets/if-else.png)

switch语法

![](/assets/switch.png)

流程图

![](/assets/switch_statement.jpg)

示例代码

```
#include <stdio.h>
 
int main () {

   /* local variable definition */
   char grade = 'B';

   switch(grade) {
      case 'A' :
         printf("Excellent!\n" );
         break;
      case 'B' :
      case 'C' :
         printf("Well done\n" );
         break;
      case 'D' :
         printf("You passed\n" );
         break;
      case 'F' :
         printf("Better try again\n" );
         break;
      default :
         printf("Invalid grade\n" );
   }
   
   printf("Your grade is  %c\n", grade );
 
   return 0;
}
```



