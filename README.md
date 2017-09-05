<h1 align="center">:whale: 用 PHP 的方式实现的各类算法合集 :whale: </h1>

<p align="center">
<a href="https://github.com/PuShaoWei/arithmetic-php#简易结构">
  <img src="https://img.shields.io/badge/php-done-brightgreen.svg" alt="php">
</a>
<a href="https://github.com/PuShaoWei/arithmetic-php">
    <img src="https://img.shields.io/github/issues-pr-raw/arithmetic-php/cdnjs.svg">
</a>
<a href="https://github.com/PuShaoWei/arithmetic-php">
    <img src="https://img.shields.io/codacy/grade/e27821fb6289410b8f58338c7e0bc686.svg">
</a>
<a href="https://github.com/PuShaoWei/arithmetic-php">
    <img src="https://img.shields.io/travis/rust-lang/rust.svg">
</a>
<a href="https://github.com/PuShaoWei/arithmetic-php">
    <img src="https://img.shields.io/github/license/mashape/apistatus.svg">
</a>
</p>


## About

>  如果说各种编程语言是程序员的招式,那么数据结构和算法就相当于程序员的内功。

## 简易结构
        
    ├──Package
    │    ├── Sort  排序篇
    │    │    ├── BubbleSort.php          冒泡排序
    │    │    ├── QuickSort.php           快速排序
    │    │    ├── ShellSort.php           希尔排序
    │    │    ├── MergeSort.php           归并排序
    │    │    ├── InsertSort.php          插入排序
    │    │    └── SelectSort.php          选择排序
    │    │ 
    │    ├── Query 查找篇
    │    │    ├── BinaryQuery.php         二分查找
    │    │    ├── InseertQuery.php        插入查找
    │    │    ├── FibonacciQuery.php      斐波那契查找
    │    │    └── QulickQuery.php         快速查找 
    │    │     
    │    └── Other 其他 
    │         ├──  MonkeyKing.php         猴子选大王
    │         ├──  DynamicProgramming.php 动态规划
    │         ├──  Fibonacci.php          斐波那契数列
    │         ├──  StealingApples.php     偷苹果求余
    │         ├──  HanoiGames.php         汉诺塔游戏
    │         ├──  ColorBricks.php        彩色砖块
    │         ├──  GetCattle.php          牛年求牛
    │         ├──  OnlyNumbers.php        求唯一数
    │         └──  BigSmallReplace.php    Hello World 输出 Olleh Dlrow
    │     
    ├──LICENSE 
    └──README.md
    
## 时间复杂度

> #### 时间频度 
    一个算法执行所耗费的时间，从理论上是不能算出来的，必须上机运行测试才能知道。
    但我们不可能也没有必要对每个算法都上机测试，只需知道哪个算法花费的时间多，哪个算法花费的时间少就可以了。
    并且一个算法花费的时间与算法中语句的执行次数成正比例，哪个算法中语句执行次数多，它花费时间就多。
    一个算法中的语句执行次数称为语句频度或时间频度。记为 `T(n)`。
    
> #### 时间复杂度 
    在刚才提到的时间频度中，n称为问题的规模，当n不断变化时，时间频度T(n)也会不断变化。
    但有时我们想知道它变化时呈现什么规律。为此，我们引入时间复杂度概念。
    一般情况下，算法中基本操作重复执行的次数是问题规模n的某个函数，用T(n)表示，
    若有某个辅助函数f(n),使得当n趋近于无穷大时，T（n)/f(n)的极限值为不等于零的常数，则称f(n)是T(n)的同数量级函数。
    记作T(n)=Ｏ(f(n)),称Ｏ(f(n)) 为算法的渐进时间复杂度，简称时间复杂度。时间频度不同，但时间复杂度可能相同。
    如：T(n)=n2+3n+4与T(n)=4n2+2n+1它们的频度不同，但时间复杂度相同，都为O(n2)。
    按数量级递增排列，常见的时间复杂度有：常数阶O(1),对数阶O(log2n),线性阶O(n), 线性对数阶O(nlog2n),平方阶O(n2)，立方阶O(n3),...， k次方阶O(nk),指数阶O(2n)。
    随着问题规模n的不断增大，上述时间复杂度不断增大，算法的执行效率越低。
    
> #### 最坏时间复杂度和平均时间复杂度 　
     最坏情况下的时间复杂度称最坏时间复杂度。一般不特别说明，讨论的时间复杂度均是最坏情况下的时间复杂度。 
     这样做的原因是：最坏情况下的时间复杂度是算法在任何输入实例上运行时间的上界，这就保证了算法的运行时间不会比任何更长。
     在最坏情况下的时间复杂度为T(n)=0(n)，它表示对于任何输入实例,该算法的运行时间不可能大于0(n)。 
     平均时间复杂度是指所有可能的输入实例均以等概率出现的情况下，算法的期望运行时间。指数阶0(2n)，显然，时间复杂度为指数阶0(2n)的算法效率极低，当n值稍大时就无法应用。

> #### 求时间复杂度
> 如果算法的执行时间不随着问题规模n的增加而增长，即使算法中有上千条语句，其执行时间也不过是一个较大的常数。此类算法的时间复杂度是O(1)。
```
    x=91; y=100;
    while(y>0) if(x>100) {x=x-10;y--;} else x++;
```    
解答： T(n)=O(1)，
这个程序看起来有点吓人，总共循环运行了1100次，但是我们看到n没有?
没。这段程序的运行是和n无关的，
就算它再循环一万年，我们也不管他，只是一个常数阶的函数
- 当有若干个循环语句时，算法的时间复杂度是由嵌套层数最多的循环语句中最内层语句的频度f(n)决定的。
```
 x=1; 
for(i=1;i<=n;i++) 
        for(j=1;j<=i;j++)
           for(k=1;k<=j;k++)
               x++; 　　
```
该程序段中频度最大的语句是(5)，内循环的执行次数虽然与问题规模n没有直接关系，但是却与外层循环的变量取值有关，而最外层循环的次数直接与n有关，
因此可以从内层循环向外层分析语句(5)的执行次数：  则该程序段的时间复杂度为T(n)=O(n3/6+低次项)=O(n3)
- 算法的时间复杂度不仅仅依赖于问题的规模，还与输入实例的初始状态有关。
在数值A[0..n-1]中查找给定值K的算法大致如下：   
```
i=n-1;            
while(i>=0&&(A[i]!=k))       
      i--;        
return i;
```
此算法中的语句(3)的频度不仅与问题规模n有关，还与输入实例中A的各元素取值及K的取值有关: 
   - ①若A中没有与K相等的元素，则语句(3)的频度f(n)=n； 
   - ②若A的最后一个元素等于K, 则语句(3)的频度f(n)是常数0。

- 时间复杂度评价性能 
     有两个算法A1和A2求解同一问题，时间复杂度分别是T1(n)=100n2，T2(n)=5n3。
    （1）当输入量n＜20时，有T1(n)＞T2(n)，后者花费的时间较少。
    （2）随着问题规模n的增大，两个算法的时间开销之比5n3/100n2=n/20亦随着增大。即当问题规模较大时，算法A1比算法A2要有效地多。
        它们的渐近时间复杂度O(n2)和O(n3)从宏观上评价了这两个算法在时间方面的质量。
        在算法分析时，往往对算法的时间复杂度和渐近时间复杂度不予区分，而经常是将渐近时间复杂度T(n)=O(f(n))简称为时间复杂度，
        其中的f(n)一般是算法中频度最大的语句频度。

## 空间复杂度
    一个程序的空间复杂度是指运行完一个程序所需内存的大小。
    利用程序的空间复杂度，可以对程序的运行所需要的内存多少有个预先估计。一个程序执行时除了需要存储空间和存储本身所使用的指令、常数、变量和输入数据外，
    还需要一些对数据进行操作的工作单元和存储一些为现实计算所需信息的辅助空间。程序执行时所需存储空间包括以下两部分。　　
> #### 固定部分
    这部分空间的大小与输入/输出的数据的个数多少、数值无关。主要包括指令空间（即代码空间）、数据空间（常量、简单变量）等所占的空间。这部分属于静态空间。
> #### 可变空间，这部分空间的主要包括动态分配的空间，以及递归栈所需的空间等。这部分的空间大小与算法有关。
    一个算法所需的存储空间用f(n)表示。S(n)=O(f(n))　　其中n为问题的规模，S(n)表示空间复杂度。

## 递归和循环的简单比较：
    1、从程序上看，递归表现为自己调用自己，循环则没有这样的形式。
    2、递归是从问题的最终目标出发，逐渐将复杂问题化为简单问题，并且简单的问题的解决思路和复杂问题一样，同时存在基准情况，就能最终求得问题，是逆向的。而循环是从简单问题出发，一步步的向前发展，最终求得问题，是正向的。
    3、任意循环都是可以用递归来表示的，但是想用循环来实现递归（除了单向递归和尾递归），都必须引入栈结构进行压栈出栈。
    4、一般来说，非递归的效率高于递归。而且递归函数调用是有开销的，递归的次数受堆栈大小的限制。


## 一起进步学习
 1. Fork 我的项目并提交你的 `idea`
 2. Pull Request 
 3. Merge 

## 纠错 

如果大家发现有什么不对的地方，可以发起一个[issue](https://github.com/PuShaoWei/arithmetic-php/issues)或者[pull request](https://github.com/PuShaoWei/arithmetic-php/pulls),我会及时纠正
> 补充:发起pull request的commit message请参考文章[Commit message 和 Change log 编写指南](http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)

## 致谢
感谢以下朋友的issue或pull request：

- [hailwood ](https://github.com/hailwood)
- [zhangxuanru](https://github.com/zhangxuanru)
- [ifreesec](https://github.com/ifreesec)
- [openset](https://github.com/openset)