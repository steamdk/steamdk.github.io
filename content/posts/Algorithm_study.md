+++
title = '算法学习记录'
date = 2024-09-10T08:33:32+08:00

categories = ["算法" ] 
tags = ["算法", "记录"]

+++



# 测试数据范围



| 时间复杂度 | 对应数据量 |
| :--------: | :--------: |
|    O(n)    | 1,000,000  |
|  O(log N)  |  100,000   |
|   O(n^2)   |   1,000    |
|   O(n^3)   |    100     |
|  特殊情况  |     10     |





# 滑动窗口





# 动态规划 DP



dp分析, 两个角度

- **状态表示**

1. 集合: 前`i`个数, 总和为`j`的所有方案
2. 属性: 

- **状态计算**



## 01背包



```c
n = 4 // 4件物品
m = 5 // 背包最大容量为 5 
```

```c
测试样例
4 5
1 2
2 4
3 4
4 5
```



|      |  j   |      |      |      |      |
| :--: | :--: | ---- | ---- | ---- | ---- |
|  i   |      |      |      |      |      |


状态`f[i][j]`定义：**前 i 个物品**，**背包容量 j** 下的最优解（**最大价值**）                      

| 前i个物品的价值 |  1   |  2   |  3   |  4   |  5   |
| :-------------: | :--: | :--: | :--: | :--: | :--: |
|        0        |  0   |  0   |  0   |  0   |  0   |
|        1        |  2   |  2   |  2   |  2   |  2   |
|        2        |  2   |  4   |  6   |  6   |  6   |
|        3        |  2   |  4   |  6   |  6   |  8   |
|        4        |  2   |  4   |  6   |  6   |  8   |


| 第i个物品的数据 |  1   |  2   |  3   |  4   |      |
| :-------------: | :--: | :--: | :--: | :--: | :--: |
|     volume      |  1   |  2   |  3   |  4   |      |
|     weight      |  2   |  4   |  4   |  5   |      |





# 单调栈









# 合并区间

**模板**

1. 排序数组
2. 更新合并左右端点

```cpp

    vector<vector<int>> merge(vector<vector<int>> &intervals)
    {

        vector<vector<int>> ans;
        if (intervals.empty())
            return ans;

        sort(intervals.begin(), intervals.end()); // 先排序

        int l = intervals[0][0], r = intervals[0][1]; // 左右端点

        for (int i = 1; i < intervals.size(); i++) // 第二数组开始遍历
        {
            if (intervals[i][0] > r) // 第二数组的左端点大于上一数组的右端点, 则保存上一数组
            {
                ans.push_back({l, r});
                l = intervals[i][0], r = intervals[i][1]; // 更新左右端点
            }
            else
            {
                r = max(r, intervals[i][1]); // 否则更新右端点
            }
        }
        ans.push_back({l, r});
        return ans;
    }

```

# 迪杰斯特拉算法 









# 快速幂

模板

快速幂 —— 模板题 AcWing 875. 快速幂
求 m^k mod p，时间复杂度 O(logk)。

```c
int qmi(int m, int k, int p)
{
    int res = 1 % p, t = m;
    while (k)
    {
        if (k&1) res = res * t % p;
        t = t * t % p;
        k >>= 1;
    }
    return res;
}
```



# 并查集

