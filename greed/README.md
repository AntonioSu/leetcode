#### 原理

贪心算法中，是以自顶向下的方式使用最优子结构，贪心算法会先做选择，在当时看起来是最优的选择，然后再求解一个结果的子问题。

贪心算法是使所做的选择看起来都是当前最佳的，期望通过所做的局部最优选择来产生一个全局最优解  

#### 具体题目

给定list，每个值表示可以跳的步数，判断是否能到最后： https://github.com/AntonioSu/leetcode/blob/master/problems/55.JumpGame.md

给定list，每个值表示可以跳的步数，用最少的步数调到最后：https://github.com/AntonioSu/leetcode/blob/master/problems/45.Jump-Game-II.md

将字符串分割为最多的字符串，要求每个字符必须出现在同一个片段中：https://github.com/AntonioSu/leetcode/blob/master/problems/763.PartitionLabels.md

快乐字符串，每次添加一个字符，然后重新排序，再次添加最多的字符：https://github.com/AntonioSu/leetcode/blob/master/problems/1405.LongestHappyString.md