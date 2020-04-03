#### **动态规划题目**

**一、其中dp[i]表示i节点的最终要求，i指示的是位置**  
1.连续子数组的和最大：https://github.com/AntonioSu/leetcode/blob/master/problems/53.MaximumSubarray.md  
2.爬楼梯；step[i]=step[i-1]+step[i-2]：https://github.com/AntonioSu/leetcode/blob/master/problems/70.ClimbingStairs.md  
3.抢劫房屋，不偷相邻的：rob(i) = max(rob(i-2)+currentHouseValue,rob(i - 1))：https://github.com/AntonioSu/leetcode/blob/master/problems/198.HouseRobber.md  
4.给定两个字符串，找最长公共子串的长度；samecount[row] [col]=samecount[row-1] [col-1]+1：https://github.com/AntonioSu/leetcode/blob/master/problems/718.MaximumLengthofRepeatedSubarray.md  
5.求到第row行路径最短：https://github.com/AntonioSu/leetcode/blob/master/problems/120.Triangle.md 



6.给定两个数，表示m行n列，只能向右、向下从左上角到右下角，这样的路径数：https://github.com/AntonioSu/leetcode/blob/master/problems/62.UniquePaths.md  
7.给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下：https://github.com/AntonioSu/leetcode/blob/master/problems/64.MinimumPathSum.md   
8.给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下，加入了阻挡：https://github.com/AntonioSu/leetcode/blob/master/problems/63.UniquePathsII.md



**二、背包问题——下标具有意义**    
1.给定各种钱币面值，求需要最少的硬币和为给定值：https://github.com/AntonioSu/leetcode/blob/master/problems/322_Coin_Change.md  
2.给定数组，求子数组的和为给定值的个数；完全背包问题：https://github.com/AntonioSu/leetcode/blob/master/problems/377.CombinationSumIV.md  
3.完全背包问题：有N种物品和一个容量为T的背包，每种物品可以选择任意多个，第i种物品的价值为P[i]，体积为V[i]，求解：选哪些物品放入背包，可卡因使得这些物品的价值最大，并且体积总和不超过背包容量。  
二维数组dp(i,j)：前 i 个物品，背包容量 j，所能取得的最大价值。  
1) j<V(i)      dp(i,j)=dp(i-1,j)  // 如果当前容量小于第i个物品的重量，则不会装入此物品，故而最大价值仍然为V(i-1,j)  
2) j>=V(i)     dp(i,j)=max｛ dp(i-1,j)，dp(i-1,j-V(i))+P(i) ｝//表示装入物品，但同时需要预留V(i)空间，才可装入当前物品，但是装入不一定价值最大，所以需要比较 



**三、dp[i] [j]表示i，j之间具有的最值**   
https://github.com/AntonioSu/leetcode/blob/master/problems/312.BurstBalloons.md  



**四、矩形最大化问题**   
给定二维数组，正方形面积最大；动态规划，主要记录左边、上边、左上边的最小值：https://github.com/AntonioSu/leetcode/blob/master/problems/221.MaximalSquare.md  
给定二维数组，子矩形面积最大;把为1的值加到后一列，得到了长方形的长，再通过循环寻找宽即可：https://github.com/AntonioSu/leetcode/blob/master/problems/85.MaximalRectangle.md  
给定二维数组，子矩阵的和最大 ;先把每行的值加到下一行，而后就是连续数组最大值：https://github.com/AntonioSu/leetcode/blob/master/problems/%E9%9D%A2%E8%AF%95%E9%A2%9817.24.%E6%9C%80%E5%A4%A7%E5%AD%90%E7%9F%A9%E9%98%B5.md (https://github.com/AntonioSu/leetcode/blob/master/problems/面试题17.24.最大子矩阵.md)  
给定数组，求矩形最大面积：https://github.com/AntonioSu/leetcode/blob/master/problems/84.LargestRectangleinHistogram.md



**五、编辑距离问题**

换、改、变三种操作，使两个字符串相等，求最短的编辑距离：https://github.com/AntonioSu/leetcode/blob/master/problems/72.EditDistance.md  
删除两个字符串中的字符，使其相等：https://github.com/AntonioSu/leetcode/blob/master/problems/583.DeleteOperationforTwoStrings.md   
只能删除第一个字符串中的字符，求最长的公共子串的长度：https://github.com/AntonioSu/leetcode/blob/master/problems/1143.LongestCommonSubsequence.md 



**六、正则匹配问题**

给定字符串和正则表达式，判断是否匹配：https://github.com/AntonioSu/leetcode/blob/master/problems/10.RegularExpressionMatching.md    
给定字符串和正则表达式，判断是否匹配：https://github.com/AntonioSu/leetcode/blob/master/problems/44.WildcardMatching.md 

