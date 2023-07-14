#### **题目描述**
给定list，和list中各元素出现的权重，实现按照对应权重的方法选取list中的元素；就是python中random.choices带权重的函数。

**Example 1:**

```python
import random
list1 = [1, 2, 3, 4, 5]
choose1 = random.choices(list1, k=5) #list1中各个元素出现次数基本持平
choose2 = random.choices(list1, weights=[1, 1, 1, 1, 5], k=5) #list1中各元素的出现符合对应权重，比如第5个元素出现的概率为5/(1+1+1+1+5)
print(choose1) # [1, 3, 4, 1, 2]
print(choose2) # [5, 4, 5, 5, 5]
```

**难度系数**    

Easy  

解法一：给权重求和，设置总的长度，然后将各个值按权重映射到坐标区间


```python
import random
def random_weight(weight_data):
  total = sum(weight_data.values())  # 权重求和
  ra = random.randint(0, total)  # 在0与权重和之前获取一个随机数 
  curr_sum = 0
  ret = None
  for k,v in weight_data.items():
    curr_sum += weight_data[k]       # 在遍历中，累加当前权重值
    if ra <= curr_sum:     # 当随机数<=当前权重和时，返回权重key
      ret = k
      break
  return ret
weight_data = {'a': 10, 'b': 15, 'c': 50}
random_weight(weight_data)
```
