#### **枚举**

* 有返回值类型  
https://github.com/AntonioSu/leetcode/blob/master/problems/50.Pow(x,n).md  
https://github.com/AntonioSu/leetcode/blob/master/problems/38.CountandSay.md  
https://github.com/AntonioSu/leetcode/blob/master/problems/230.KthSmallestElementinaBST.md

* 整个遍历，返回型是bool  
https://github.com/AntonioSu/leetcode/blob/master/problems/79.WordSearch.md
https://github.com/AntonioSu/leetcode/blob/master/problems/416.PartitionEqualSubsetSum.md //尽量少递归，做好剪枝 
https://github.com/AntonioSu/leetcode/blob/master/problems/207.CourseSchedule.md  //判断是否有环

* 无返回值类型，通过传参解决
https://github.com/AntonioSu/leetcode/blob/master/problems/39.CombinationSum.md  

* 搜索整个二维矩阵空间  
单词搜索—改变之后需要还原：https://github.com/AntonioSu/leetcode/blob/master/problems/79.WordSearch.md
寻找陆地的个数，相连1的块数—改变之后不需要还原：https://github.com/AntonioSu/leetcode/blob/master/problems/200.NumberofIslands.md
包围的区域，改变不与边界相连的块的值：https://github.com/AntonioSu/leetcode/blob/master/problems/130.SurroundedRegions.md  


* 整个遍历——for循环型  
1.for循环--起始位置是不断变化的，写法：for (int i = index; i < candidates.size(); i++) 
有重复的数字，求和等于某值：https://github.com/AntonioSu/leetcode/blob/master/problems/40.CombinationSumII.md  
无重复数字全排列：https://github.com/AntonioSu/leetcode/blob/master/problems/46.Permutations.md  
有重复数字全排列：https://github.com/AntonioSu/leetcode/blob/master/problems/47.PermutationsII.md  
将整个字符串分割为单个是回文的字符串：https://github.com/AntonioSu/leetcode/blob/master/problems/131.PalindromePartitioning.md   


2.使用index，每一向前移动1
https://github.com/AntonioSu/leetcode/blob/master/problems/39.CombinationSum.md