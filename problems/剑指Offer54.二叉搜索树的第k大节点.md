#### **题目描述**
给定一棵二叉搜索树，请找出其中第 k 大的节点的值。



**Example 1:**

```
输入: root = [3,1,4,null,2], k = 1
   3
  / \
 1   4
  \
   2
输出: 4

```

**Example 2:**

```
输入: root = [5,3,6,2,4,null,null,1], k = 3
       5
      / \
     3   6
    / \
   2   4
  /
 1
输出: 4

```


**限制：**
1 ≤ k ≤ 二叉搜索树元素个数

**难度系数**    

Easy  

**题目链接：**
https://leetcode-cn.com/problems/er-cha-sou-suo-shu-de-di-kda-jie-dian-lcof/

解法一：中序遍历的逆序即可，中序：左根右；中序逆序：右根左

```c++
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public: 
    int res;
    int kthLargest(TreeNode* root, int k) {
        dfs(root,k);
        return res;
    }
    void dfs(TreeNode* root ,int &k) //传引用 这里需要保证所有dfs函数共用一个k 
    {
        if(!root) return;
        dfs(root->right,k); //右
        k--;
        if(!k) res = root->val; //根
        dfs(root->left,k); //左
    }
};

```
