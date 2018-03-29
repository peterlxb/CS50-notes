## 五种基本数据类型

The type of a variable determines how much space it occupies in storage and how the bit pattern stored is interpreted.

在C里面声明变量需要指定类型，每种类型占据的空间是不一样的。也就是站的bit位也是不一样的。

数据类型可以分为四类

1.**Basic Types基本类型**

算术类型: \(a\) integer types and \(b\) floating-point types.整数和浮点型

2.**Enumerated types 枚举类型**

也是算术类型，只能被定义为离散的数字

3.**The type void 空类型**

4.**Derived types 派生类型**They include \(a\) Pointer types, \(b\) Array types, \(c\) Structure types, \(d\) Union types and \(e\) Function types.



CS50的定义

#### int

The int data type is used for variables that will store integers.

integers always take up 4 bytes of memory\(32 bits\).This means the range of values they can store is necessarily limited to 32 bits worth of information.

#### unsigned int

unsigned is a qualifier that can be applied to certain types\(including int\) .

#### char

The char data type is used for variables that will store single characters.

Characters always take up 1 bytes of memory\(b bits\).This means the range of values they can store is necessarily  limited to 8 bits worth of information. -128 ------  128

#### float

The float data type is used for variables that will store floating-point values.also known as real numbers.

Floating points always take up 4 bytes of memory\(32 bits\).

#### double

The double data type is used for variables that will store floating-point values.also known as real numbers.

They always take up 8 bytes of memory\(64 bits\).

#### void

is a type but not a data type.

Functions can have a void return type, which just mean they don't return a value.

The parameters list of a function can also be a void.It simple means  the function takes no parameters.

#### create a variable

```
int number; //declaration 声明
number = 17; //assignment 赋值
char letter; ////declaration
letter = 'H' //assignment

int number = 17; //initialization
char letter = 'H';//initialization
```

In general ,it's good to practice to only declare variables when you need them.

---------------------------





