#### 单调栈问题

##### 基础问题

给定两个数组，第一个数组是第二个数组的子集，求第一个数组中每个元素在第二个数组对应位置之后的下一个更大元素——单调栈：https://github.com/AntonioSu/leetcode/blob/master/problems/496.NextGreaterElementI.md

循环数组求下一个更大元素——单调栈，需要循环两次：https://github.com/AntonioSu/leetcode/blob/master/problems/503.NextGreaterElementII.md

高于当前温度需要等待多少天：https://github.com/AntonioSu/leetcode/blob/master/problems/739.DailyTemperatures.md

求固定长度窗口内的最大值，解法三的**双端队列**中保存的是有front到back**递减**的num：https://github.com/AntonioSu/leetcode/blob/master/problems/239.SlidingWindowMaximum.md

最长递增子序列，设置单调栈：https://github.com/AntonioSu/leetcode/blob/master/problems/300.LongestIncreasingSubsequence.md

##### 进一步融合问题

子数组最小乘积的最大值，找数组中连续的子数组，里面的最小值*子数组的和最大——通过单调栈获取到每个值左右窗口，用到前缀和、窗口、单调栈：https://github.com/AntonioSu/leetcode/blob/master/problems/1856.MaximumSubarrayMin-Product.md

