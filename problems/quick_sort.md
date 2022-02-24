#### **题目描述**
输入整数数组 arr ，使用快排，排序数组，并返回

**Example 1:**

```
输入：arr = [8,4,9,3,7,10]
输出：[3,4,7,8,9,10] 

```

**难度系数**    

Easy  

解法一：分治的思想


```c++
#include <iostream>
#include "vector"
using namespace std;
void quickSort(vector<int> &nums, int low, int high);
int partition_1(vector<int> &nums, int low, int high);
int partition_2(vector<int> &nums, int low, int high);

void quickSort(vector<int> &nums, int low, int high) {
    if (low < high) {
        int pos = partition_1(nums, low, high);
        quickSort(nums, low, pos - 1);
        quickSort(nums, pos + 1, high);
    }
}

//一趟排序，实现方式一
int partition_1(vector<int> &nums, int low, int high) {
    int pivot = nums[low];
    while (low < high) {
        while (low<high && nums[high] >= pivot)high--;	
        nums[low] = nums[high];
        while (low <high && nums[low]<= pivot)low++;				
        nums[high] = nums[low];
    }
    nums[low] = pivot;

    return low;
}

//一趟排序，实现方式二
int partition_2(vector<int> &nums, int l, int r) {
    int left=l;
    int pivot = nums[l];
    while (l < r) {
        while (l<r&&pivot<=nums[r])r--;
        while (l<r&&pivot>=nums[l])l++;
        swap(nums[l], nums[r]);
    }
    nums[left]=nums[l];
    nums[l]=pivot;
    return l;
}

int main(){
	vector<int> nums = {8,4,9,3,7};
	int low = 0, high = nums.size()-1;
	quickSort(nums, low, high);
	for (int i = 0; i < nums.size(); i++){
		cout << nums[i] << " ";
	}
    return 0;
}

```
