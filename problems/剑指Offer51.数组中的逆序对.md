#### **题目描述**
在数组中的两个数字，如果前面一个数字大于后面的数字，则这两个数字组成一个逆序对。输入一个数组，求出这个数组中的逆序对的总数。
逆序对: 0 <= i < j < n 且 nums[i] > nums[j],其中n为数组大小


**Example 1:**

```
输入: [7,5,6,4]
输出: 5

```


**Example 2:**

```
输入: [3,2,1]
输出: 3

```

**限制：**
0 <= 数组长度 <= 50000

**难度系数**    

Hard  

**题目链接：**
https://leetcode-cn.com/problems/shu-zu-zhong-de-ni-xu-dui-lcof/

解法一：分治的思想,在每次归并的时候，统计逆序数即可，使用一个全局值

```c++
class Solution {
public:
    /* 合并有序数组 */
    void merge(vector<int>& nums, int left, int mid, int right) {
        int idx = 0;
        int i = left;
        int j = mid + 1;
        while (i <= mid && j <= right) {
            if (nums[i] > nums[j]) {
                ans += mid - i + 1; /* 统计逆序对 */
                tmp[idx++] = nums[j++];
            } else {
                tmp[idx++] = nums[i++];
            }
        }

        /* 处理剩余数组 */
        while (i <= mid) {
            tmp[idx++] = nums[i++];
        }
        while (j <= right) {
            tmp[idx++] = nums[j++];
        }

        /* 写到原数组中 */
        for (int k = 0; k < idx; k++) {
            nums[left + k] = tmp[k];
        }
    }

    /* 归并排序 */
    void mergeSort(vector<int>& nums, int l, int r) {
        if (l >= r) {
            return;
        }
        int m = l + (r - l) / 2;
        mergeSort(nums, l, m);
        mergeSort(nums, m + 1, r);
        merge(nums, l, m ,r);
    }

    int reversePairs(vector<int>& nums) {
        int n = nums.size();
        tmp = vector<int>(n);
        mergeSort(nums, 0, n - 1);
        return ans;
    }
    vector<int> tmp;
    int ans=0;
};


```


解法二：分治的思想，返回值是对应的逆序数

```c++
class Solution {
public:
    /* 合并有序数组 */
    int merge(vector<int>& nums, int left, int mid, int right) {
        int idx = 0;
        int i = left;
        int j = mid + 1;
        int ans = 0;
        while (i <= mid && j <= right) {
            if (nums[i] > nums[j]) {
                ans += mid - i + 1; /* 统计逆序对 */
                tmp[idx++] = nums[j++];
            } else {
                tmp[idx++] = nums[i++];
            }
        }

        /* 处理剩余数组 */
        while (i <= mid) {
            tmp[idx++] = nums[i++];
        }
        while (j <= right) {
            tmp[idx++] = nums[j++];
        }

        /* 写到原数组中 */
        for (int k = 0; k < idx; k++) {
            nums[left + k] = tmp[k];
        }
        return ans;
    }

    /* 归并排序 */
    int mergeSort(vector<int>& nums, int l, int r) {
        if (l >= r) {
            return 0;
        }
        int m = l + (r - l) / 2;
        int revCnt = mergeSort(nums, l, m) + mergeSort(nums, m + 1, r);
        return revCnt + merge(nums, l, m ,r);
    }

    int reversePairs(vector<int>& nums) {
        int n = nums.size();
        tmp = vector<int>(n);
        return mergeSort(nums, 0, n - 1);
    }
    vector<int> tmp;
};


```
