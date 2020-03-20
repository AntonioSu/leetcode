#### 数值查找   

**旋转数组问题**

1.旋转数组，寻找给定值的具体位置，数值无重复；二分法，先寻找有序区间，不在有序区间，则在另外的区间：https://github.com/AntonioSu/leetcode/blob/master/problems/33.SearchinRotatedSortedArray.md  
2.旋转数组，寻找是否存在给定值，数值有重复；二分法，思路与不重复数组相同：https://github.com/AntonioSu/leetcode/blob/master/problems/81.SearchinRotatedSortedArrayII.md  
3.旋转数组，查找最小值；最小值一定在无序区间： https://github.com/AntonioSu/leetcode/blob/master/problems/153.FindMinimuminRotatedSortedArray.md  
4.旋转数组，查找最小值，数值有重复；最小值一定在无序区间： https://github.com/AntonioSu/leetcode/blob/master/problems/154.FindMinimuminRotatedSortedArrayII.md

**查找峰值问题**

1.查找峰值下标，只有一个峰值；二分查找，通过比较相邻的两个数，确定峰值在那一边：https://github.com/AntonioSu/leetcode/blob/master/problems/852.PeakIndexinaMountainArray.md  
2.查找峰值下标，存在多个峰值；二分查找：https://github.com/AntonioSu/leetcode/blob/master/problems/162.FindPeakElement.md



寻找第K大的数值；使用大小为K的最小值堆，或者是快排：https://github.com/AntonioSu/leetcode/blob/master/problems/215.KthLargestElementinanArray.md  
寻找K个常见的数值；利用最大值堆：https://github.com/AntonioSu/leetcode/blob/master/problems/347.TopKFrequentElements.md   



1.寻找给定值的起始和结束位置，数组元素有重复：https://github.com/AntonioSu/leetcode/blob/master/problems/34.FindFirstandLastPositionofElementinSortedArray.md



**二维数组问题**

给定二维数组蛇形有序；先二分查找寻找行，而后再二分查找列：https://github.com/AntonioSu/leetcode/blob/master/problems/74.Searcha2DMatrix.md   
行有序，列有序，查找给定值；左下角到右上角：https://github.com/AntonioSu/leetcode/blob/master/problems/240.Searcha2DMatrixII.md 

**二分查找总结**

查找值，结束条件需要包含“=”；  
left=(mid+1|mid)和right=(mid-1|mid)：考虑是否漏掉数据   
死循环：一般需要考虑right-left==1的这种情况，针对死循环加入if条件判断