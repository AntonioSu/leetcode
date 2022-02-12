
### 题目描述
给定整数数组 numbers ，该数组已按非递减顺序排列，请你从数组中找出满足相加之和等于目标数 target 的两个数。其中数组元素有重复的。

**Note:**

- Your returned answers (both index1 and index2) are not zero-based.
- You may assume that each input would have *exactly* one solution and you may not use the *same* element twice.

**Example:**

```
Input: numbers = [2,2,7,7,15], target = 9
Output: 4
Explanation: The sum of 2 and 7 is 9. 共4种组合.
```

**难度系数**    
Medium

思路：因为给定数组无序，且可能重复，故而需要借助map容器来保存每个数字出现的个数，在遍历数组的时候，每次判断target-nums[i]是否在map中，如果在，就将map[target-nums[i]] 加到结果中

```c++
#include <iostream>
#include "vector"
#include "unordered_map"
using namespace std;

int sum_K(vector<int> nums,int target){
	int n=nums.size();
	int ans=0;
	unordered_map<int,int> map;
	for (size_t i = 0; i < n; i++){
        int val=target-nums[i];
        if(map.find(val)!=map.end()){
            ans += map[val];
        }
        map[nums[i]]+=1;
    }
	return ans;   
}
int main()
{
	vector<int> nums={2,3,6,7,7,11,15,2};
	cout<<sum_K(nums,9);
    return 0;
}
```

