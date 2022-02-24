#### **题目描述**
输入整数数组 arr ，找出其中最小的 k 个数。例如，输入4、5、1、6、2、7、3、8这8个数字，则最小的4个数字是1、2、3、4。

**Example 1:**

```
输入：arr = [3,2,1], k = 2
输出：[1,2] 或者 [2,1]

```

**Example 2:**

```
输入：arr = [0,1,2,1], k = 1
输出：[0]

```


**Constraints:**
0 <= k <= arr.length <= 10000
0 <= arr[i] <= 10000

**难度系数**    

Easy  

解法一：建立一个大小为k的大顶堆，时间复杂度O(n*logk)


```c++
class Solution {
public:
    vector<int> getLeastNumbers(vector<int>& arr, int k) {
        vector<int> vec(k, 0);
        if (k == 0) { // 排除 0 的情况
            return vec;
        }
        if(k==arr.size()) return arr;
        priority_queue<int> pq;//最大值堆
        //保持堆的大小为k
        for (int i = 0; i < k; ++i) {
            pq.push(arr[i]);
        }
        //当前数据小于堆顶元素的时候，弹出堆顶元素，插入当前数据
        for (int i = k; i < (int)arr.size(); ++i) {
            if (pq.top() > arr[i]) {
                pq.pop();
                pq.push(arr[i]);
            }
        }
        // 堆中的元素就是前k个最小元素
        for (int i = 0; i < k; ++i) {
            vec[i] = pq.top();
            pq.pop();
        }
        return vec;
    }
};

```

解法二：快排的思想，逼近k，那么左边元素都小于k，期望时间复杂度O(n)，最坏情况是O(n^2)

```c++
class Solution {
public:
    vector<int> getLeastNumbers(vector<int>& arr, int k) {
        vector<int> ans;
        if(k==0) return ans;
        if(k==arr.size()) return arr;
        int left = 0, right = arr.size() - 1;
        while (true) {
            int pos = partition(arr, left, right);
            if (pos == k - 1) break;
            if (pos > k - 1) right = pos - 1;
            else left = pos + 1;
        }
        for(int i=0;i<k;i++){
            ans.push_back(arr[i]);
        }
        return ans;
    }
    //一趟快排
    int partition(vector<int>& nums, int l, int r) {
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
};

```
