# java流程控制

## 1.Scanner 类
    通过scanner 类的next() 与nextLine() 方法获取输入的字符串，在读取我们一般需要使用hasNext() 与 hasNextLine() 判断是否还有输入的数据。

### next()
    一定要读取到有效字符后才可以结束输入。
    对输入有效字符之前遇到的空白，next（）方法会自动将其去掉。
    只有输入有效字符后才将其后面输入的空白作为分隔符或者结束符。
    next（）方法不能得到有空格的不能得到有空格的字符串

### nextLine():
    以Enter为结束符，也就是说 nextLine() 方法返回的是输入回车之前的所有字符
    可以获得空白。

## 2.顺序结构
    Java的基本结构就是顺序结构，除非特别指明，否则按照顺序一句一句执行。
  语句与语句之间，框与框之间是按从上到下的顺序进行的，它是由若干个依次执行的处理步骤组成的，它是任何一个算法都离不开的一种基本算法结构。

## 3.选择结构
   我们很多时候需要去判断一个东西是否可行，然后我们才去执行，这样一个过程在程序中用if语句来表示语法

## 4.switch 多选择语句
   switch case 语句判断一个变量和与一系列值中某个值相等，每个值称为一个分支。
  switch 语句中的变量类型可以是：

    byte、short、int、或者是char
    从 Java SE 7开始
    switch 开始支持字符串 String 类型了
    同时case 标签必须为字符串常量或字面量

## 5.循环结构
while循环

while(布尔表达式){
    //循环内容
}

  只要布尔表达式为true，循环就会一直执行下去
  大多数情况是会让循环停止下来，我们需要一个让表达式失效的方式来结束循环
  少部分情况需要循环一直执行，比如服务器的请求响应监听等。

  do…while循环

do…while 循环至少会让 循环体里的语句执行一遍。
while 先判断后执行
do…while x 先执行后判断
do{
    
}while(布尔表达式)


  for循环
    for循环的执行次数在执行前就确定了。

for(初始值;布尔表达式;迭代){
    //代码语句
}

打印99乘法

for (int i = 1;i<=9;i++){
    for (int j = 1;j<= i;j++){
        System.out.print(i+"*"+j+"="+i*j+"\t");
    }
    System.out.println();
}

  break、 continue
    break 用于强行退出循环，不执行中循环体中剩余代码。

  continue 用于终止某次循环过程，即跳过循环体尚未执行的语句，继续下一次循环。
