#### 题目描述
输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有奇数位于数组的前半部分，所有偶数位于数组的后半部分。
**示例：**

```html
输入：nums = [1,2,3,4]
输出：[1,3,2,4] 
注：[3,1,2,4] 也是正确的答案之一。
```

**说明：**

- 1 <= nums.length <= 50000；
- 1 <= nums[i] <= 10000；

**难度系数**  

Easy

解法一：使用两个指针，原理就是一趟快排

```python
class Solution:
    def exchange(self, nums: List[int]) -> List[int]:
        s,e=0,len(nums)-1
        while s<e:
            if nums[s]&1==1:
                s+=1
            elif nums[e]&1==0:
                e-=1
            else:
                nums[s],nums[e]=nums[e],nums[s]
        return nums
```

