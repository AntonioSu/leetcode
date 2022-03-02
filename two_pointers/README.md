## 双指针
### 1.左右指针


#### 1.1计算面积

计算在坐标上围成的面积最大，坐标轴不计算在内：https://github.com/AntonioSu/leetcode/blob/master/problems/11.ContainerWithMostWater.md  

计算在坐标上围成的面积最大，坐标轴计算在内：https://github.com/AntonioSu/leetcode/blob/master/problems/42.TrappingRainWater.md  



#### 1.2数值计算

求取数组中三个数字的和等于某值https://github.com/AntonioSu/leetcode/blob/master/problems/15.3Sum.md   

一个整数能否等于两个整数的平方和——左右指针：https://github.com/AntonioSu/leetcode/blob/master/problems/633.SumofSquareNumbers.md

求固定长度窗口内的最大值，使用优先队列进行固定窗口内的值排序：https://github.com/AntonioSu/leetcode/blob/master/problems/239.SlidingWindowMaximum.md

使数组中的奇数在前，偶数在后——首尾指针即可：https://github.com/AntonioSu/leetcode/blob/master/problems/剑指Offer21.调整数组顺序使奇数位于偶数前面.md



### 2.快慢指针——这种类型题目一般需要借助map来实现  

`Input: S = "ADOBECODEBANC", T = "ABC", Output: "BANC"`字符串S中包含T的最短字符串：https://github.com/AntonioSu/leetcode/blob/master/problems/76.MinimumWindowSubstring.md  

找到最短子序列，和大于等于某值：https://github.com/AntonioSu/leetcode/blob/master/problems/209.MinimumSizeSubarraySum.md

给定一个字符串，找到最长的包含最多k个不同字符的子串——快慢指针，同时需要一个hash表记录区间的字符个数：https://github.com/AntonioSu/leetcode/blob/master/problems/340.LongestSubstringwithAtMostKDistinctCharacters.md

无重复字符的最长子串——借用一个map，记录窗口内不重复的值：https://github.com/AntonioSu/leetcode/blob/master/problems/3.LongestSubstringWithoutRepeatingCharacters.md

