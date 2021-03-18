#### 判断是否为回文串

判断一个字符串是否为回文串：https://github.com/AntonioSu/leetcode/blob/master/problems/125.ValidPalindrome.md   

给定一个数字，判断是否是回文串——转化为string，再判断：https://github.com/AntonioSu/leetcode/blob/master/problems/9.PalindromeNumber.md  

最多删除一个字符，判断是否为回文串——从两头向中间移动，只要不相等，就左边跳过一个字符或者右边跳过一个字符，而后在判断：https://github.com/AntonioSu/leetcode/blob/master/problems/680.ValidPalindromeII.md



从字符串中寻找最长回文子串——以每个字符作为中心，向两端遍历，同时保持最长子串：https://github.com/AntonioSu/leetcode/blob/master/problems/5.LongestPalindromicSubstring.md



判断一个字符串有多少个回文串——从中心向两端扩展：https://github.com/AntonioSu/leetcode/blob/master/problems/647.PalindromicSubstrings.md



#### 分割之后再判断，动态规划

将给定的字符串分割为各个list，使得每个list都为回文串，返回这样的list——从头开始遍历，只要是子串是回文串，就放到路径中https://github.com/AntonioSu/leetcode/blob/master/problems/131.PalindromePartitioning.md  

将字符串分割为list，使每个list都为回文，最小的分割数是多少——对于0~i之间的字符串，0<=j<=i,判断每个j是否为最小，同时j到i为回文串https://github.com/AntonioSu/leetcode/blob/master/problems/132.PalindromePartitioningII.md