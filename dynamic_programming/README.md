#### **动态规划题目**

#### **一、其中dp[i]表示i节点的最终要求，i指示的是位置**  

1. 连续子数组的和最大：https://github.com/AntonioSu/leetcode/blob/master/problems/53.MaximumSubarray.md  
2. 爬楼梯；step[i]=step[i-1]+step[i-2]：https://github.com/AntonioSu/leetcode/blob/master/problems/70.ClimbingStairs.md  
3. 将数字转化为字母，有多少种转化法，有条件的跳台阶：https://github.com/AntonioSu/leetcode/blob/master/problems/剑指Offer46.把数字翻译成字符串.md
4. 抢劫房屋，不偷相邻的：rob(i) = max(rob(i-2)+currentHouseValue,rob(i - 1))：https://github.com/AntonioSu/leetcode/blob/master/problems/198.HouseRobber.md  
5. 抢劫房屋，不偷相邻的，同时是环形数组——需要两次，一次遍历不包含头，一次不包含结尾：https://github.com/AntonioSu/leetcode/blob/master/problems/213.HouseRobberII.md
6. 给定三角形， 求从顶到底最短路径：https://github.com/AntonioSu/leetcode/blob/master/problems/120.Triangle.md 
7. 给定词组和字符串，求是否通过词组的组合变成字符串：https://github.com/AntonioSu/leetcode/blob/master/problems/139.WordBreak.md 
8. 给定字符串，字符串中包含负数，寻找连续的乘积最大值：https://github.com/AntonioSu/leetcode/blob/master/problems/152.MaximumProductSubarray.md 
9. 一个字符串能够由另一种字符串多少种表示：https://github.com/AntonioSu/leetcode/blob/master/problems/115.DistinctSubsequences.md
10. 给定一个字符串，求子串的个数——如果一个字符没有出现过，则当前个数是前一个的两倍，否则，需要去重：https://github.com/AntonioSu/leetcode/blob/master/problems/940.DistinctSubsequencesII.md
11. 第n个丑数——通过数组记录丑数序列：https://github.com/AntonioSu/leetcode/blob/master/problems/264.UglyNumberII.md
12. 青蛙是否可以从开始节点跳到尾结点——设置二维dp[i] [k],表示青蛙能否达到「现在所处的石子编号」为 i且「上一次跳跃距离」为 k 的状态:https://github.com/AntonioSu/leetcode/blob/master/problems/403.FrogJump.md
13. 从位置0开始，既可以左移、右移、原地，给定steps，求有多少种移动方法可以移动到原地：https://github.com/AntonioSu/leetcode/blob/master/problems/1269.NumberofWaystoStayintheSamePlaceAfterSomeSteps.md

https://github.com/AntonioSu/leetcode/blob/master/problems/664.奇怪的打印机.md



#### 二、最长公共子串问题

1. 给定两个list，找最长公共子list的长度，连续——只考虑相等情况，samecount[row] [col]=samecount[row-1] [col-1]+1：https://github.com/AntonioSu/leetcode/blob/master/problems/718.MaximumLengthofRepeatedSubarray.md  

2. 给定两个字符串，找最长子串，不连续——不相等取最大值，相等则加1：https://github.com/AntonioSu/leetcode/blob/master/problems/1143.LongestCommonSubsequence.md

3. 和最长公共子串的思路相同：https://github.com/AntonioSu/leetcode/blob/master/problems/1035.Uncrossed-Lines.md

4. 最长递增子序列——https://github.com/AntonioSu/leetcode/blob/master/problems/300.LongestIncreasingSubsequence.md

5. 最长整除子集——记录最长长度和最长长度路径：https://github.com/AntonioSu/leetcode/blob/master/problems/368.LargestDivisibleSubset.md



#### 三、编辑距离问题

1. 增、删、改三种操作，使两个字符串相等，求最短的编辑距离：https://github.com/AntonioSu/leetcode/blob/master/problems/72.EditDistance.md  

2. 删除两个字符串中的字符，使其相等：https://github.com/AntonioSu/leetcode/blob/master/problems/583.DeleteOperationforTwoStrings.md   



#### 四、背包问题

##### 1）01背包 ——需要将物品数也表示在下表中，第一维一般表示物品，一般至少需要2维数组

1. 给定整数和数组，只能使用+或者-，使数组的值等于整数，有多种表达式——dp[i] [j] 为 前i个数字运算结果等于 j 的不同表达式的数目:https://github.com/AntonioSu/leetcode/blob/master/problems/494.Target-Sum.md
2. dp[k] [i] [j] 代表考虑前 k 件物品，在数字 1 容量不超过 i，数字 0 容量不超过 j的条件下的"最大价值":https://github.com/AntonioSu/leetcode/blob/master/problems/474.Ones-and-Zeroes.md
3. 给定数组，将数组分割为两个子list，是否使得两个list的和相等——dp[i] [j]表示前i个数字是否存在和为j：https://github.com/AntonioSu/leetcode/blob/master/problems/416.PartitionEqualSubsetSum.md
4. 给定数字，将其写成是和的形式，求其中和中每个值乘积最大：https://github.com/AntonioSu/leetcode/blob/master/problems/343.IntegerBreak.md 



##### 2）完全背包——不需要记录物品，dp[i]就表示所求，一般一维数组则可

1. 给定各种钱币面值，求需要最少的硬币和为给定值：https://github.com/AntonioSu/leetcode/blob/master/problems/322_Coin_Change.md  
2. 给定总金额和数组，数组中的元素有无限个，求有多少种取法，使得从数组中取出的总和等于给定金额——dp[i]表示满足金额是i的方案数：https://github.com/AntonioSu/leetcode/blob/master/problems/518.Coin-Change-2.md
3. 给定数组，求子数组的和为给定值的个数；完全背包问题：https://github.com/AntonioSu/leetcode/blob/master/problems/377.CombinationSumIV.md  
4. 给定整数n，找寻组成和为n的完全平方数最少——dp[i]表示组合和为i的个数最少：https://github.com/AntonioSu/leetcode/blob/master/problems/279.Perfect-Squares.md
5. 完全背包问题：有N种物品和一个容量为T的背包，每种物品可以选择任意多个，第i种物品的价值为P[i]，体积为V[i]，求解：选哪些物品放入背包，可卡因使得这些物品的价值最大，并且体积总和不超过背包容量。  
   二维数组dp(i,j)：前 i 个物品，背包容量 j，所能取得的最大价值。  
   1) j<V(i)      dp(i,j)=dp(i-1,j)  // 如果当前容量小于第i个物品的重量，则不会装入此物品，故而最大价值仍然为V(i-1,j)  
   2) j>=V(i)     dp(i,j)=max｛ dp(i-1,j)，dp(i-1,j-V(i))+P(i) ｝//表示装入物品，但同时需要预留V(i)空间，才可装入当前物品，但是装入不一定价值最大，所以需要比较 



#### 五、矩阵从左上角到右下角走法 

1. 给定两个数，表示m行n列，只能向右、向下从左上角到右下角，这样的路径数：https://github.com/AntonioSu/leetcode/blob/master/problems/62.UniquePaths.md  

2. 给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下：https://github.com/AntonioSu/leetcode/blob/master/problems/64.MinimumPathSum.md   

3. 给定二维矩阵，矩阵中不同的整数值，找到一条最短路径，只能右、下，加入了阻挡：https://github.com/AntonioSu/leetcode/blob/master/problems/63.UniquePathsII.md



#### 六、矩形最大化问题 

给定二维数组，正方形面积最大；动态规划，主要记录左边、上边、左上边的最小值：https://github.com/AntonioSu/leetcode/blob/master/problems/221.MaximalSquare.md  

给定二维数组，子矩形面积最大;把为1的值加到后一列，得到了长方形的长，再通过循环寻找宽即可：https://github.com/AntonioSu/leetcode/blob/master/problems/85.MaximalRectangle.md  

给定二维数组，子矩阵的和最大 ;先把每行的值加到下一行，而后就是连续数组最大值：https://github.com/AntonioSu/leetcode/blob/master/problems/%E9%9D%A2%E8%AF%95%E9%A2%9817.24.%E6%9C%80%E5%A4%A7%E5%AD%90%E7%9F%A9%E9%98%B5.md (https://github.com/AntonioSu/leetcode/blob/master/problems/面试题17.24.最大子矩阵.md)  

给定数组，求矩形最大面积：https://github.com/AntonioSu/leetcode/blob/master/problems/84.LargestRectangleinHistogram.md







#### 七、匹配问题

给定字符串和正则表达式，判断是否匹配：https://github.com/AntonioSu/leetcode/blob/master/problems/10.RegularExpressionMatching.md    
给定字符串和正则表达式，判断是否匹配：https://github.com/AntonioSu/leetcode/blob/master/problems/44.WildcardMatching.md 


#### 八、 最短路径

限制最多K次中转：https://github.com/AntonioSu/leetcode/blob/master/problems/787.Cheapest-Flights-Within-K-Stops.md

#### 九、 其他

给定偶数堆石子，每堆石子是一个整型，只能从两端取，求先手是否赢得比赛：https://github.com/AntonioSu/leetcode/blob/master/problems/877.Stone-Game.md

https://github.com/AntonioSu/leetcode/blob/master/problems/312.BurstBalloons.md 


