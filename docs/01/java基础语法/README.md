# java基础语法

## 1.注释：
    注释并不会被执行，是写给我们写代码的人看的

## 2.标识符
    Java 所有的组成部分都需要名字。类名、变量名、以及方法名都被称为标识符。
  所有的标识符都应该以 A-Z或者a-z 、美元符号$、下划线_ 开始。

## 3.数据类型
    强类型语言：要求变量的使用要严格规符合定，所有变量都必须先定义后才能使用。
  弱类型语言：JS
  强类型语言安全，但是速度慢！
  java是一种强类型语言，要求十分严格。

## 4.什么是字节
    位（bit）：
是计算机 内部数据 存储的最小单位，11001100是一个八位二进制数。
    字节（byte）
是计算机中 数据处理 的基本单位，习惯上用大写B来表示；1B（byte字节）1B（byte字节） = 8bit （位）
    字符：
是指计算机中使用的字母、数字、和符号
常见单位换算

  1bit 表示 1位
  1byte 表示一个字节 1B=8b
  1024b = 1kb
  1024kb = 1M
  1024M = 1G
  1024G = 1TB

## 5.进制问题
二进制：0b
十进制：默认
八进制：0 逢八进一
十六进制：0x 逢十六进一

银行业务用什么表示？用BigDecimal类 数学工具类
不能使用浮点数。

所有的字符本质还是数字
编码问题 Unicode 表：（97 = a，65 = A） 编码 占了两个字节

转义字符
\t 制表符
\n 换行

## 6.类型转换

    由于java是强类型语言，所以要进行有些运算的时候，需要用到类型转换。

 低 ---------------------------------------------->高
 byte，short，char—>，int—>，float—>，long—>，double

 运算中，不同类型的数据先转换为同一类型，然后进行运算。（小数优先级高于整数）


 不能对布尔类型进行转换。（不能把人转成猪，可以把男人转女人）
 不能把对象类型转换为不相干的类型。
 在把高容量转换为低容量的时候，需要强制转换。
 转换的时候可能存在内存溢出，或者精度问题。

## 7.变量
    变量是什么？
    就是可以变的量！

  Java是一门强类型语言，每一个变量必须声明其类型。

  Java变量是程序中最基本的存储单元，其要素包括变量名、变量类型和作用域。
  格式：
    数据类型 变量名 值；

  作用域
    局部变量：类中方法内 ：局部变量必须声明和赋值
    成员变量：类中方法外： 示例变量从属于对象，如果不自行初始化，这个类型的默认值： 0 、0.0、布尔值默认是：false、除了基本类型，其余的默认是null
## 8.常量常量是什么?
    初始化之后不能再改变值！不会变动的值。

  所谓常量可以理解成一种特殊的变量，它的值被设定后，在程序运行过程中不允许被改变。

final 数据类型 常量名  = 常量值
final double PI = 3.14;
1
2
  修饰符不存在先后顺序。
## 9.运算符
算术运算符：+、-、*、/、++、--
赋值运算符：=
关系运算符：==、 != 、<、>、<=、>= 、instanceof
逻辑运算符：&& || ！
位运算符：& | ^ ~ >> << >>>
条件运算符：?
扩展赋值运算符：+=、-+、*=、/=

## 10.包机制
为了更好地组织类，Java提供了包机制，用于区别类名的命名空间。
  包语句的语法格式为：

package  pgk1[.pck2[.pck3]];

1 package 必须放在类中所有语句的最上面（第一行代码）

导包

1  import   pgk1[.pck2[.pck3]].(classname | *);





