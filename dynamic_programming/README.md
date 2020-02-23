#### **动态规划题目**

**一、其中dp[i]表示i节点的最终要求**  
1.连续子数组的和最大：https://github.com/AntonioSu/leetcode/blob/master/problems/53.MaximumSubarray.md  
2.爬楼梯；step[i]=step[i-1]+step[i-2]：https://github.com/AntonioSu/leetcode/blob/master/problems/70.ClimbingStairs.md  
3.抢劫房屋，不偷相邻的：rob(i) = max(rob(i-2)+currentHouseValue,rob(i - 1))：https://github.com/AntonioSu/leetcode/blob/master/problems/198.HouseRobber.md  
4.给定两个数组，找最长公共长度；samecount[row] [col]=samecount[row-1] [col-1]+1：https://github.com/AntonioSu/leetcode/blob/master/problems/718.MaximumLengthofRepeatedSubarray.md  

5.给定两个数，表示m行n列，只能向右、向下从左上角到右下角，这样的路径数：https://github.com/AntonioSu/leetcode/blob/master/problems/62.UniquePaths.md
6.给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下：https://github.com/AntonioSu/leetcode/blob/master/problems/64.MinimumPathSum.md
7.给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下，加入了阻挡：https://github.com/AntonioSu/leetcode/blob/master/problems/63.UniquePathsII.md

**二、背包问题——下标具有意义**    
1.给定各种钱币面值，求需要最少的硬币和为给定值：https://github.com/AntonioSu/leetcode/blob/master/problems/322_Coin_Change.md
2.给定数组，求子数组的和为给定值的个数；完全背包问题：https://github.com/AntonioSu/leetcode/blob/master/problems/377.CombinationSumIV.md
3.完全背包问题：有N种物品和一个容量为T的背包，每种物品可以选择任意多个，第i种物品的价值为P[i]，体积为V[i]，求解：选哪些物品放入背包，可卡因使得这些物品的价值最大，并且体积总和不超过背包容量。  
二维数组dp(i,j)：前 i 个物品，背包容量 j，所能取得的最大价值。  
1) j<V(i)      dp(i,j)=dp(i-1,j)  // 如果当前容量小于第i个物品的重量，则不会装入此物品，故而最大价值仍然为V(i-1,j)  
2) j>=V(i)     dp(i,j)=max｛ dp(i-1,j)，dp(i-1,j-V(i))+P(i) ｝//表示装入物品，但同时需要预留V(i)空间，才可装入当前物品，但是装入不一定价值最大，所以需要比较 


**三、dp[i] [j]表示i，j之间具有的最值**   
https://github.com/AntonioSu/leetcode/blob/master/problems/312.BurstBalloons.md



**四、dp[i] [j]表示只是记录中间结果，最值不在数组中，需要保存一个max，或者min**   
https://github.com/AntonioSu/leetcode/blob/master/problems/221.MaximalSquare.md  
https://github.com/AntonioSu/leetcode/blob/master/problems/85.MaximalRectangle.md  



**五、符合特定条件的转移方程**   
https://github.com/AntonioSu/leetcode/blob/master/problems/72.EditDistance.md  

120. Triangle

