# 数组

## 1.数组的定义
数组是相同类型数据的有序集合。
数组描述的是相同类型的若干个数据，按照一定的先后次序排列组合而成。
其中，每一个数据称作一个数组元素，每一个数组元素通过一个下标来访问他们。数组下标从0开始

## 2.数组声明和创建
在类型后面加 [ ] 或者在数组名后面加 [ ]

## 3.Java内存分析
堆
  存储new 出来的对象和数组
  可以被所有的线程共享，不会存放别的对象引用

栈
  存放基本变量类型（会包括这个基本类型的具有数值）
  引用类型变量（会存放这个引用在堆里面的具体地址）

方法区
  可以被所有线程共享
  包含了所有的class和 static 变量

## 4.三种初始化
### 1.静态初始化 --创建+赋值

int[] a = {1,2,3};

### 2.动态初始化 – 包含默认初始化

int[] a = new int[3];
a[0] = 1;

动态初始化包含：数组的默认初始化
  数组是引用类型，它的元素相当于类的实例变量，因此数组已经分配空间，其中的每个元素也被按照实例变量同样的方式被隐式初始化。

## 5.数组的四个基本特点
其长度是确定的。数组一旦被创建，它的大小就是不可以改变的。
其元素必须是相同类型，不允许出现混合类型。
数组的元素可以是任意数据类型，包括基本类型和引用类型。
数组变量属引用类型，数组也可以看成是对象，数组中的每个元素相当于该对象的成员变量。数组本身就是对象，Java中对象是在堆中的，因此数组无论保存原始类型还是其他对象类型，数组对象本身在堆中的。
### ArrayIndexOutOfBoundsException：
数组下标越界异常！

总结：

数组是相同数据类型的有序集合
数组也是对象。数组元素相当于对象的成员变量
数组长度是确定的，不可改变。
## 6.求数组最大值
public static void main(String[] args) {
    int[] nums = {1, 5, 2, 39, 2, 5, 72, 24};
    int max = nums[0];
    for (int i = 1; i < nums.length; i++) {
        if (nums[i] > max){
            max = nums[i];
        }
    }
    System.out.println("数组的最大值是："+max);
}

## 7.打印数组
public static void main(String[] args) {
    int[] nums = {1, 5, 2, 39, 2, 5, 72, 24};
    for (int i : nums){
        System.out.print(i+" ");
    }
    System.out.println();
    System.out.println("===================");
    for (int i = 0;i<nums.length;i++){
        System.out.print(nums[i]+" ");
    }
}

## 8.反转数组
public static void main(String[] args) {
    int[] nums = {1, 5, 2, 39, 2, 5, 72, 24};
    for (int i = nums.length - 1; i >= 0; i--) {
        System.out.print(nums[i] + " ");
    }
}

## 9.多维数组
多维数组可以看成是数组的数组，比如二维数组就是一个特殊的一维数组，其每一个元素都是一个一维数组。

## 10.Arrays 类
数组的工具类java.utils.Arrays
由于数组对象本身没有什么方法可以供我们调用，但API中提供了一个工具类Arrays供我们使用，从而可以对数据对象进行一些基本操作。
Arrays 类中的方法都是 static 修饰的静态方法，在使用的时候可以直接使用类名 进行调用。
具备以下常用功能
1.给数组赋值：通过fill方法
2.对数组排序：通过sort方法，按升序
3.比较数组：通过equals方法比较数组中元素值是否相等
4.查找数组元素：通过binarySearch 方法对排序好的数组进行二分查找法操作

## 11.冒泡排序
public static void main(String[] args) {
    int[] arr = {1, 23, 6, 6, 2, 2, 23, 34, 5};
    //1.比较数组中两个相邻的元素，如果第一个数比第二个数大，就交互位置
    //2.每一次比较，都会产生一个最大，或者最小的数字
    //3.下一轮可以少一次排序
    //4.依次循环，直到结束！
    System.out.println(Arrays.toString(arr));
    sort(arr);
    System.out.println(Arrays.toString(arr));
}

public static void sort(int[] arr) {
    //外层循环，判断我们这个要走几次
    for (int i = 0; i < arr.length - 1; i++) {
        //内层循环，比较判断两个数，如果第一个数比第二个数大，则交换位置
        for (int j = 0; j < arr.length - 1 - i; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j+ 1];
                arr[j + 1] = temp;
            }
        }
    }
}






