#### **题目描述**
输入整数数组 arr ，使用归并排序

**Example 1:**

```
输入：arr = [8,4,9,3,7,10]
输出：[3,4,7,8,9,10] 

```

**难度系数**    

Easy  

解法一：分治的思想

```c++
#include<iostream>
#include"vector"
using namespace std;
 
//一趟将两个有序数组融合
void Merge(vector<int> &arr, int l, int mid, int r){
    int n=r-l+1;
    vector<int> tmp(n);//临时数组大小为n，保存合并后的有序数组
    int i=0,left=l,right=mid+1;
    while(left<=mid && right<=r)
        tmp[i++] = arr[left]<= arr[right]?arr[left++]:arr[right++];
    //将未merge的数组再次放到tmp中
    while(left<=mid)
        tmp[i++]=arr[left++];
    while(right<=r)
        tmp[i++]=arr[right++];
    //将tmp数组的值赋给arr
    for(int j=0;j<n;++j)
        arr[l+j]=tmp[j];
}
 
void MergeSort(vector<int> &arr, int l, int r){
    if(l<r){
        int mid = (l + r)/2;
        MergeSort(arr, l, mid);
        MergeSort(arr, mid + 1, r);
        Merge(arr, l, mid, r);
        
    }
}
 
int main(){
    vector<int> nums = {3,1,2,4,5,8,7,6,4};
    MergeSort(nums,0,nums.size()-1);
    for(int i=0;i<nums.size();++i)
        cout<<nums[i]<<" ";
}

```
