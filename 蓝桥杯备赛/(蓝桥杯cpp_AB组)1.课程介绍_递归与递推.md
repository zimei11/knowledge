# (acwing蓝桥杯c++AB组）1.课程介绍+递归

[toc]

### 课程介绍

> 整理自AcWing y总课程[蓝桥杯C++ AB组辅导课（试听课）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV15J411z7J7/)

题目描述->抽象出数据类型->（dfs，图论，dp，贪心等）

- check

  1. 正确性

  2. 时间是否超时

     ![image-20211017170243393](https://gitee.com/youwozimei/picture-bed/raw/master/picture/image-20211017170243393.png)

     - 一般来说一层循环O(n)，两层循环O(n^2^)，三层循环O(n^3^)。

     - 计算机中的 *logn* 一般指的以二为底的。

     - int 范围大概正负10^9^ ，long long 范围大概正负10^18^。

### 第一讲 递归与递推

##### 递归

###### 引入

自己调用自己

列如斐波那契数列1,2,3,5,8,13.......

```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int f(int n)
{
    if(n==1)
        return 1;
    if(n==2)
        return 2;
    return f(n-1)+f(n-2);
}
```

> tip:
>
> - 对于c语言风格scanf printf 速度巨快。（#include<cstdio>）
>
> - 对于c++语言风格cin cout 速度稍慢。
>
> 在数据规模小于10^5^时一般无所谓选择哪种
>
> 用scanf只是因为部分题目可能会卡输入输出的时间。

###### 递归的底层调用顺序

递归调用思路可以借助栈的后进先出思维理解，这里我们借助递归搜索树帮助理解。

对于上一题的斐波那契数列可以得到递归搜索树

![image-20211017174400897](https://gitee.com/youwozimei/picture-bed/raw/master/picture/image-20211017174400897.png)

所谓剪枝就是把其中的一些分支减掉以降低复杂度

###### 例题与练习

[92. 递归实现指数型枚举 - AcWing题库](https://www.acwing.com/problem/content/94/)

![image-20211017185920003](https://gitee.com/youwozimei/picture-bed/raw/master/picture/image-20211017185920003.png)

> tip:常见2的几次方
>
> ![image-20211017190410321](https://gitee.com/youwozimei/picture-bed/raw/master/picture/image-20211017190410321.png)