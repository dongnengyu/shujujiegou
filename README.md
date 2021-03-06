### 个人算法学习
 
#### 面试题目
 
 ```
 /**
  * @param
  * @Author: 董能宇
  * @Email:dongnengyu@gmail.com
  * @Description: 酷狗笔试题目 编程题
  * 小明去附近的水果店买橙子，水果商贩只提供整袋购买，有每袋6个和每袋8个的包装（包装不可拆分）。
  * 可是小明只想购买恰好n个橙子，并且尽量少的袋数方便携带。如果不能购买恰好n个橙子，小明将不会购买
  * 请根据此实现一个程序，要求：
  * <p>
  * 输入一个整数n，表示小明想要购买n（1≤n≤100）个橙子
  * 输出一个整数表示最少需要购买的袋数，如果不能买恰好n个橙子则输出-1
  * 例如，输入20，输出3。
  * @Date: 2018/5/10
  */
  
  位置：src/WrittenTest/KuGouTest
  
 ```
 
 #### 文本匹配
 
 ```
 /**
  * @param
  * @Author: 董能宇
  * @Email:dongnengyu@gmail.com
  * @Description:
  *
  * 1.序列模式匹配问题，给定一个输入文本text，和一个待匹配文本pattern，要求在text文本中匹配到的pattern的最短字符串，
  * 匹配结果可不连续，例如输入text为:abaacxbcbbbacc，pattern为cbc，则匹配为：abaacxbcbbbbacc。
  * 要求输出结果为在text中所匹配的起始位置。
  *
  * 例如，输入为：abaacxbcbbbacc  cbc 则输出为：4 7
  *
  *            输入为：aaabcac ac    则输出为:5 6
  *
  *  遇到匹配不到的情况，如：abc x  则输出为:-1 -1
  *
  * @Date: 2018/5/10
  *
  * 位置：/Users/xiaomu/Documents/ideaProject/data-structure/src/WrittenTest/TextPatten.java
  */

```


#### ACM题目

```


/**
 * @param
 * @Author: 董能宇
 * @Email:dongnengyu@gmail.com
 * @Description:
 * @Date: 2018/5/11
 * <p>
 * 问题描述：把m个同样的苹果放在n个同样的盘子里，允许有的盘子空着不放，问有多少种不同的分法？
 * <p>
 * (注：5,1,1和1,1,5是同一种分法)
 *
 * 解法：
 * 通过分类讨论，将规模较大的问题转换成规模较小的相同问题，学会”降维“，将索引值不断降小，就可以递归求解。
 *
 * 设f(m,n)为把m个苹果放到n个盘子中的方法数，m>=0,n>=0.
 *
 * 若m和n中任何一个等于0，那么f(m,n) = 1，注意不是等于0，因为相当于就那么一种结果，就是不往盘子
 * 里面放（没有苹果），或者，连盘子都没有。
 * 若n=1,显然对于任意的m>=0 有f(m,1) = 1
 * 若m=1,显然对于任意的n>=0 有f(1,n) = 1
 * 接下来讨论m>1 && n>1的情况：
 * 若 m < n 则 f(m,n) = f(m,m)。即空哪几个盘子都是一样的
 * 若 m>=n 则 大体有两种放法：
 *  第1种情况：至少有一个盘子为空，即什么也不放，这部分的方法数为f(m,n-1);
 *  第2种情况：全部盘子都有苹果，那么先从m个苹果中抽取出n个出来，各个盘子分一个，考虑剩下的m-n个苹果
 * 放到n个盘子里的放法，这样就成功把f(m,n)降到了f(m-n,n)。
 * 所以，m>=n时，有f(m,n) = f(m,n-1) + f(m-n,n);
 */
 
位置：/Users/xiaomu/Documents/ideaProject/data-structure/src/ACM/NToMApple.java

```