#### **动态规划题目**

**1.其中dp[i]表示i节点的最终要求**   

70. Climbing Stairs # step[i] = step[i - 1] + step[i - 2]
53. Maximum Subarray
198. House Robber #rob(i) = max(rob(i-2)+currentHouseValue,rob(i - 1))
718.Maximum Length of Repeated Subarray 
//samecount[row][col]=samecount[row-1][col-1]+1;

给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下。
https://github.com/AntonioSu/leetcode/blob/master/problems/64.MinimumPathSum.md  

**2.背包问题——下标具有意义**  

322. Coin Change
二维数组V(i,j)：前 i 个物品，背包容量 j，所能取得的最大价值。
1) j<w(i)      V(i,j)=V(i-1,j)  //如果当前容量小于第i个物品的重量，则不会装入此物品，故而最大价值仍然为V(i-1,j)
2) j>=w(i)     V(i,j)=max｛ V(i-1,j)，V(i-1,j-w(i))+v(i) ｝//表示装入物品，但同时需要预留w[i]空间，才可装入当前物品，但是装入不一定价值最大，所以需要比较
https://github.com/AntonioSu/leetcode/blob/master/problems/322_Coin_Change.md  

**3.dp[i] [j]表示i，j之间具有的最值**   
https://github.com/AntonioSu/leetcode/blob/master/problems/312.BurstBalloons.md

**4.dp[i] [j]表示只是记录中间结果，最值不在数组中，需要保存一个max，或者min**   
https://github.com/AntonioSu/leetcode/blob/master/problems/221.MaximalSquare.md
https://github.com/AntonioSu/leetcode/blob/master/problems/85.MaximalRectangle.md

**5.符合特定条件的转移方程** 
https://github.com/AntonioSu/leetcode/blob/master/problems/72.EditDistance.md

62. Unique Paths  
63. Unique Paths II  
120. Triangle

