### 一、与运算

求两个数的和，不用加减：https://github.com/AntonioSu/leetcode/blob/master/problems/371.SumofTwoIntegers.md  

判断一个数是否是2的幂——n&(n-1)： https://github.com/AntonioSu/leetcode/blob/master/problems/231.PowerofTwo.md

判断一个数是否是4的幂： https://github.com/AntonioSu/leetcode/blob/master/problems/342.4的幂.md

将给定的int型数字转化为二进制，而后逆转：https://github.com/AntonioSu/leetcode/blob/master/problems190.ReverseBits.md

给定字符串，找长度为10的字符串至少重复2次的子串：https://github.com/AntonioSu/leetcode/blob/master/problems/187.RepeatedDNASequences.md 



### 二、异或

#### 1. 数字出现次数

只有一个数字出现一次，其他数字均出现两次：https://github.com/AntonioSu/leetcode/blob/master/problems/136.SingleNumber.md 

只有两个数字出现一次，其他数字均出现两次：https://github.com/AntonioSu/leetcode/blob/master/problems/260.SingleNumberIII.md 

只有一个数字出现一次，其他数字均出现三次：https://github.com/AntonioSu/leetcode/blob/master/problems/137.SingleNumberII.md 



#### 2. 前缀树

建立前缀树，而后再判断：https://github.com/AntonioSu/leetcode/blob/master/problems/421.数组中两个数的最大异或值.md

给定list和query=[x,m]，求list中小于m的值和x异或的最大值，对应的query也是一个list，就是queries=[query_i...]——建立前缀树，对list和query.m排序，而后对每个query，将小于query.m的值插入到树中，然后寻找最大值：https://github.com/AntonioSu/leetcode/blob/master/problems/1707.与数组中元素的最大异或值.md



#### 3. 异或运算的性质

给定一个异或之后的数组，求原数组——先求第一个值，而后再求之后的值：https://github.com/AntonioSu/leetcode/blob/master/problems/1734.DecodeXORedPermutation.md

区间内的结果异或——利用一个数组，先异或前n个值：https://github.com/AntonioSu/leetcode/blob/master/problems/1310.XORQueriesofaSubarray.md

形成两个异或相等数组的三元组数目：https://github.com/AntonioSu/leetcode/blob/master/problems/1442.形成两个异或相等数组的三元组数目.md



#### 4. 其他

对两个数字异或，而后统计1的个数:https://github.com/AntonioSu/leetcode/blob/master/problems/461.汉明距离.md

对start+2*i的数异或——遍历一遍即可：https://github.com/AntonioSu/leetcode/blob/master/problems/1486.XOROperationinanArray.md

