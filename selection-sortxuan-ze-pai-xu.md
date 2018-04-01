第一个选择排序Selection Sort。时间复杂度Ο\($$n^2$$\).

原理就是找到最小值，移到最左边。接着剩余的继续找最小的排在最左边。

初始情况还未排序的Array。暂时设定第一个元素14最小的。

![](/assets/unsorted_array.jpg)

第一次先搜索所有元素，找到比14小的就与它进行交换。最后10为最小的值。

![](/assets/selection_sort_2.jpg)

10已经排序完，循环继续，初始值应该从索引1开始，同样暂时设置33为最小值。

剩余的值再与它进行比较得出最小值，索引为2。

![](/assets/selection_sort_4.jpg)

![](/assets/selection_sort_5.jpg)

然后遵循同样的原理依次找出剩余未排序的元素中的最小值。

![](/assets/selection_sort.jpg)

用c语言代码，主要看selectionSort\(\)中的两个循环。

```
#include <stdio.h>
#include <stdbool.h>
#define MAX 12

int intArray[MAX] = {3, 44, 38, 5, 47, 15, 36, 26, 27, 2, 46, 4};

void printline(int count) {
   int i;
	
   for(i = 0;i <count-1;i++) {
      printf("=");
   }
	
   printf("=\n");
}

void display() {
   int i;
   printf("[");
	
   // navigate through all items 
   for(i = 0;i<MAX;i++) {
      printf("%d ", intArray[i]);
   }
	
   printf("]\n");
}

void selectionSort() {

   int indexMin,i,j;
	
   // loop through all numbers 
   for(i = 0; i < MAX-1; i++) { 
	
      // set current element as minimum 
      indexMin = i;
		
      // check the element to be minimum 
      for(j = i+1;j<MAX;j++) {
         if(intArray[j] < intArray[indexMin]) {
            indexMin = j;
         }
      }

      if(indexMin != i) {
         printf("Items swapped: [ %d, %d ]\n" , intArray[i], intArray[indexMin]); 
			
         // swap the numbers 
         int temp = intArray[indexMin];
         intArray[indexMin] = intArray[i];
         intArray[i] = temp;
      }          

      printf("Iteration %d#:",(i+1));
      display();
   }
}  

main() {
   printf("Input Array: ");
   display();
   printline(50);
   selectionSort();
   printf("Output Array: ");
   display();
   printline(50);
}
```











