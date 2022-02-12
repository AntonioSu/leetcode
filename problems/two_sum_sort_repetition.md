
### 题目描述
给定整数数组 numbers ，该数组已按非递减顺序排列，请你从数组中找出满足相加之和等于目标数 target 的两个数。其中数组元素有重复的。

**Note:**

- O(n)的时间复杂度，O(1)的空间复杂度

**Example1:**

```
Input: numbers = [2,2,7,7,15], target = 9
Output: 4
Explanation: The sum of 2 and 7 is 9. 共4种组合.
```

**Example2:**
```
Input: numbers = [2,2,3,6,7,7,11,15], target = 9
Output: 5
```

**难度系数**    
Medium

思路：因为给定数组有序，设置左右指针，来找到目标值，对于有重复的数字，跳过则可。

```c++
#include <iostream>
#include "vector"
#include "unordered_map"
using namespace std;

int sum_K(vector<int> nums,int target){
	int l=0,r=nums.size()-1;
	int ans=0;
	while (l<r){
		int left_dup=1,right_dup=1;
		if(nums[l]+nums[r]==target){
			//如果有重复的，则判断左右重复的个数
			while(l<r && nums[l]==nums[l+1]){
				left_dup+=1;
				l +=1;
			}               
			while(l<r && nums[r]==nums[r-1]){
				right_dup +=1;
				r -=1;
			}
			ans+=right_dup*left_dup;
			// 因为当前结果已计算，所以需要跳过这一组数据对
			l += 1;
			r -= 1;
		}
		else if(nums[l]+nums[r]<target)
			l += 1;
		else
			r -= 1;
	}   
	return ans;   
}

int main()
{
	vector<int> nums={2,2,3,6,7,7,11,15};
	cout<<sum_K(nums,9);
    return 0;
}
```

