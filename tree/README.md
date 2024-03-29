### 树类题目
#### **1.树的遍历**

**1)前序遍历**

前序遍历：https://github.com/AntonioSu/leetcode/blob/master/problems/144.BinaryTreePreorderTraversal.md

两个树的叶子节点值相同——分别对两棵树保存list，而后判断list是否相等：https://github.com/AntonioSu/leetcode/blob/master/problems/872.Leaf-SimilarTrees.md

两个节点为同一深度，但是不能是同一个父节点下的左右子节点：https://github.com/AntonioSu/leetcode/blob/master/problems/993.二叉树的堂兄弟节点.md

多叉树的前序遍历：https://github.com/AntonioSu/leetcode/blob/master/problems/589.n-ary-tree-preorder-traversal.md



**2)中序遍历** 

中序遍历：https://github.com/AntonioSu/leetcode/blob/master/problems/94.BinaryTreeInorderTraversal.md

中序遍历的一种应用：https://github.com/AntonioSu/leetcode/blob/master/problems/173.BinarySearchTreeIterator.md

给定二叉搜索树，任意两个相邻的节点差值最小——中序遍历则可：https://github.com/AntonioSu/leetcode/blob/master/problems/783.MinimumDistanceBetweenBSTNodes.md

将树节点都变为是右子节点：https://github.com/AntonioSu/leetcode/blob/master/problems/897.IncreasingOrderSearchTree.md




**3)后序遍历**

后序遍历：https://github.com/AntonioSu/leetcode/blob/master/problems/145.BinaryTreePostorderTraversal.md   

寻找子树和出现次数最多的值：https://github.com/AntonioSu/leetcode/blob/master/problems/508.MostFrequentSubtreeSum.md 

求区间内的和：https://github.com/AntonioSu/leetcode/blob/master/problems/938.RangeSumofBST.md

多叉树的后续遍历：https://github.com/AntonioSu/leetcode/blob/master/problems/590.n-ary-tree-postorder-traversal.md



**4)层次遍历**

按层输出值：https://github.com/AntonioSu/leetcode/blob/master/problems/102.BinaryTreeLevelOrderTraversal.md 

zigzag遍历方法：https://github.com/AntonioSu/leetcode/blob/master/problems/103.BinaryTreeZigzagLevelOrderTraversal.md 

树的层次遍历，使用队列：https://github.com/AntonioSu/leetcode/blob/master/problems/429.n-ary-tree-level-order-traversal.md



#### **2.BST**

给定二叉搜索树，第k个最小的值 :https://github.com/AntonioSu/leetcode/blob/master/problems/230.KthSmallestElementinaBST.md  

给定二叉搜索树，找第k大节点——中序逆操作：https://github.com/AntonioSu/leetcode/blob/master/problems/剑指Offer54.二叉搜索树的第k大节点.md

二叉搜索树中查找值：https://github.com/AntonioSu/leetcode/blob/master/problems/700.SearchinaBinarySearchTree.md  

给定二叉搜索树，插入值：https://github.com/AntonioSu/leetcode/blob/master/problems/701.InsertintoaBinarySearchTree.md  

最近公共父节点，树是二叉搜索树：https://github.com/AntonioSu/leetcode/blob/master/problems/235.LowestCommonAncestorofaBinarySearchTree.md 

判断是否是二叉搜索树：https://github.com/AntonioSu/leetcode/blob/master/problems/98.ValidateBinarySearchTree.md


最近公共父节点，树是普通的树：https://github.com/AntonioSu/leetcode/blob/master/problems/236.LowestCommonAncestorofaBinaryTree.md 

完全二叉树的节点个数——只要把左子树和右子树的节点个数相加在加根节点个数即可：https://github.com/AntonioSu/leetcode/blob/master/problems/222.CountCompleteTreeNodes.md 



**3.构建树**

给定先序和中序，构建树：https://github.com/AntonioSu/leetcode/blob/master/problems/105.ConstructBinaryTreefromPreorderandInorderTraversal.md 

给定排序的数组，构建二叉搜索树：https://github.com/AntonioSu/leetcode/blob/master/problems/108.ConvertSortedArraytoBinarySearchTree.md 


**4.树的深度**

给定二叉树，计算树的最大深度：https://github.com/AntonioSu/leetcode/blob/master/problems/104.maximum-depth-of-binary-tree.md

给定二叉树，计算任意两个节点的最大距离,树深度的一个应用题目：https://github.com/AntonioSu/leetcode/blob/master/problems/543.diameter-of-binary-tree.md

**5.前缀树**

建立一颗前缀树：https://github.com/AntonioSu/leetcode/blob/master/problems/208.ImplementTrie(PrefixTree).md

建立前缀树，而后再判断：https://github.com/AntonioSu/leetcode/blob/master/problems/421.数组中两个数的最大异或值.md

https://github.com/AntonioSu/leetcode/blob/master/problems/1707.与数组中元素的最大异或值.md



判断一棵树是否为另一棵树的子树：https://github.com/AntonioSu/leetcode/blob/master/problems/572.SubtreeofAnotherTree.md

搜索自动补全系统，利用前缀树完成：https://github.com/AntonioSu/leetcode/blob/master/problems/642.DesignSearchAutocompleteSystem.md