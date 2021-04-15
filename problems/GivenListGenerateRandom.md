#### **题目描述**

有一组数字，他们都带有不同的权重，现在要从中“随机”抽一个数字，但是抽到某个数字的概率要正比于他的权重。假设这个集合中的元素和其对应权重为{‘A’：50，‘B’：10，‘C’：100，‘D’：3，‘E’：60，‘F’：25}。

**难度系数**    

Medium

解法一：将value求和，然后对生成的数字在key中取上界，然后获取最终结果

```python
import bisect
import random

data = {'A': 30, 'B': 10, 'C': 100, 'D': 20, 'E': 40}
key_list,value_list=[],[]
for key,value in data.items():
    key_list.append(key)
    value_list.append(value)
prefix_sum = []
tmp_sum = 0
for value in value_list:
    tmp_sum += value
    prefix_sum.append(tmp_sum)#递增子序列
t = random.randint(0, tmp_sum-1)#必须减1，否则如果生成tmp_sum，会越界
pick_value = key_list[bisect.bisect_right(prefix_sum, t)]
```

