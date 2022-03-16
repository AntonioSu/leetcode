#### 链表问题
链表问题一般有逆转、合并、删除、排序、是否有环等问题

##### 逆转

链表逆转：https://github.com/AntonioSu/leetcode/blob/master/problems/206.ReverseLinkedList.md  

逆转指定区间的链表：https://github.com/AntonioSu/leetcode/blob/master/problems/92.ReverseLinkedListII.md 

旋转链表——将链表转化为环，而后再寻找断开节点位置：https://github.com/AntonioSu/leetcode/blob/master/problems/61.RotateList.md   

将链表按照此种方式逆转，L0 → Ln → L1 → Ln - 1 → L2 → Ln - 2 ——寻找中间节点，逆转后半部分，合并前半部分和后半部分： https://github.com/AntonioSu/leetcode/blob/master/problems/143.reorder-list.md



##### 合并

将两个有序链表合并到一起：https://github.com/AntonioSu/leetcode/blob/master/problems/21.MergeTwoSortedLists.md  

将一个数组的有序链表合并到一起：https://github.com/AntonioSu/leetcode/blob/master/problems/23.MergekSortedLists.md   



##### 排序

给链表排序；用vector存储值，利用快排：https://github.com/AntonioSu/leetcode/blob/master/problems/148.SortList.md   

将链表首一个尾一个变成一个新的链表：https://github.com/AntonioSu/leetcode/blob/master/problems/143.ReorderList.md 



##### 删除重复

将重复的数字只保留一个——提前一个节点判断：https://github.com/AntonioSu/leetcode/blob/master/problems/83.RemoveDuplicatesfromSortedList.md

将重复的数字都删除——提前两个节点判断：https://github.com/AntonioSu/leetcode/blob/master/problems/82.RemoveDuplicatesfromSortedListII.md

移除链表中给定值的节点——需要两个指针，保存即将要删除节点的前一个节点和当前节点：https://github.com/AntonioSu/leetcode/blob/master/problems/203.RemoveLinkedListElements.md



##### 其他

找寻两个链表公共开始节点：https://github.com/AntonioSu/leetcode/blob/master/problems/160.IntersectionofTwoLinkedLists.md 

链表是否有环：https://github.com/AntonioSu/leetcode/blob/master/problems/141.LinkedListCycle.md 

删除倒数第n个节点：https://github.com/AntonioSu/leetcode/blob/master/problems/19.RemoveNthNodeFromEndofList.md

将链表变成有序，这里使用的是直接插入法：https://github.com/AntonioSu/leetcode/blob/master/problems/147.InsertionSortList.md