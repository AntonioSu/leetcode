#### **滑动窗口题目**

**通过下标控制窗口的大小**  
在**字符串s**中找到和**字符串p**相等，只要字母相等，不包含顺序，对应的在s中的起始位置，通过两个数组解决 ：https://github.com/AntonioSu/leetcode/blob/master/problems/438.FindAllAnagramsinaString.md  

找到窗口内的最大值，双向队列解决 ：https://github.com/AntonioSu/leetcode/blob/master/problems/239.SlidingWindowMaximum.md  

`Input: S = "ADOBECODEBANC", T = "ABC", Output: "BANC"`字符串S中包含T的最短字符串：https://github.com/AntonioSu/leetcode/blob/master/problems/76.MinimumWindowSubstring.md  

求固定长度窗口内的最大值：分别左右两个指针滑动求和：https://github.com/AntonioSu/leetcode/blob/master/problems/643.MaximumAverageSubarrayI.md

无重复字符的最长子串——借用一个map，记录窗口内不重复的值：https://github.com/AntonioSu/leetcode/blob/master/problems/3.LongestSubstringWithoutRepeatingCharacters.md

窗口内的值最大——只需要循环窗口内的值即可：https://github.com/AntonioSu/leetcode/blob/master/problems/643.MaximumAverageSubarrayI.md