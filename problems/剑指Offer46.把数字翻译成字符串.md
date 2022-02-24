#### **题目描述**
给定一个数字，我们按照如下规则把它翻译为字符串：0 翻译成 “a” ，1 翻译成 “b”，……，11 翻译成 “l”，……，25 翻译成 “z”。一个数字可能有多个翻译。请编程实现一个函数，用来计算一个数字有多少种不同的翻译方法。不可以有前导0，比如01是不可以的



**Example 1:**

```
输入: 12258
输出: 5
解释: 12258有5种不同的翻译，分别是"bccfi", "bwfi", "bczi", "mcfi"和"mzi"
```

**Example 2:**

```
输入: 101
输出: 2
解释: 101有2种不同的翻译，分别是"bab", "kb"
```



**题目链接**

https://leetcode-cn.com/problems/ba-shu-zi-fan-yi-cheng-zi-fu-chuan-lcof/

**难度系数**  

Medium

解法一： 用 dp[i]表示前 i 个数字的翻译方法数，属于有条件的跳台阶

```python

class Solution:
    def translateNum(self, num: int) -> int:
        str_num = str(num)
        n = len(str_num)
        dp = [1 for _ in range(n + 1)] 
        for i in range(2, n + 1):
            temp=str_num[i-2:i]
            # 大于10是不让前导0的出现，09之类就不行
            if 10<=int(temp)<26:# 两个数字必须小于26，字母最大是25，因为a和0对应
                # 这样有两种情况，一种是两个数字分开，那么是dp[i - 1]，合在一起，是dp[i - 2]
                dp[i] = dp[i - 2] + dp[i - 1]
            else:# 两个数字不能组合在一起
                dp[i] = dp[i - 1]
        return dp[n]


```

