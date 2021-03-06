# 方法
Java 方法是语句的集合，他们在一起执行一个功能。

方法是解决一类问题的步骤的有序组合
方法包含于类或对象中
方法在程序中被创建，在其他第被调用
  设计方法的时候要保证方法的原子性，就是一个方法只完成一个功能。

## 方法的定义：
    Java 方法是语句的集合，他们在一起执行一个功能。

方法是解决一类问题的步骤的有序组合
方法包含于类或对象中
方法在程序中被创建，在其他第被调用
  设计方法的时候要保证方法的原子性，就是一个方法只完成一个功能。

方法的定义：
  Java的方法类似于其他语言的函数，是一段用来完成特定功能的代码片段，一般情况下，定义一个方法包含以下语法。

1.修饰符：
  修饰符，这个是可选的，告诉编译器如何调用该方法，定义该方法的访问类型。

2.返回值类型：
  方法可能会有返回值。return Value Type 是方法返回值的数据类型。
  有些方法可能没有返回值。在这种情况下，return Value Type 是关键字void

3.方法名：
  是方法的实际名称。

4.参数类型：
  参数像一个占位符。当方法被调用时，传值给参数，。这个值被称为 实参 或者 变量。
  参数列表是指方法的参数类型、顺序、参数个数。
  参数是可选的，方法可以不包含任何参数

5.方法体：
  方法体包含具体的语句，定义该方法的功能。

## 2.方法重载
    重载就是在 一个类中，有相同的函数名称，但是形参不同的函数。

方法重载的规则：
  方法名称必须相同

  参数列表必须不同
    参数个数、参数类型、参数位置排列不同等

返回值类型可以相同也可以不相同。
    仅仅返回值类型不同不足以成为方法的重载

实现理论：
    方法名称相同时，编译器会根据调用方法的参数个数，参数类型等去逐个匹配，以选择对应的方法，如果匹配失败，编译器报错。

## 3.可变参数
    jdk1.5 开始，Java支持传递同类型的可变参数给一个方法

在方法声明中，在指定参数类型后加一个省略号(…)。
    一个方法中只能传递一个可变参数，它必须是方法的font color=blue>最后一个参数。任何普通参数必须在它之前声明。

## 4.递归
    A方法调用B方法，很容易理解。

递归就是：A方法调用A方法！就是自己调用自己。

递归结构包含两个部分：
递归头：什么时候不调用自身方法，如果没有头，将陷入死循环。
递归体：什么时候调用自身方法。

什么是阶层？
阶乘指从1乘以2乘以3乘以4一直乘到所要求的数。
例如所要求的数是4，则阶乘式是1×2×3×4，得到的积是24，24就是4的阶乘。
