**题目描述**   

 一个台阶总共有n级，如果一次可以跳1级，也可以跳2级......它也可以直接跳上n级。此时该青蛙跳上一个n级的台阶总共有多少种跳法？

**Example 1:**

```
Input: 0 
Output: 0
```

**Example 2:**

```
Input: 1
Output: 1
```

**Example 3:**

```
Input: 3
Output: 4
```

**Example 4:**

```
Input: 5
Output: 32
```

**难度系数**    
Medium



Fib(n) = Fib(0)+Fib(1)+Fib(2)+.......+Fib(n-1)

Fib(n-1)=Fib(0)+Fib(1)+Fib(2)+.......+Fib(n-2)

两式相减得：Fib(n)-Fib(n-1)=Fib(n-1) -> Fib(n) = 2*Fib(n-1)  ，可以得出是等比数列。

解法一：递归解法
```c++
int solution(int n){
    if(n == 0 || n == 1)
        return 1;
    else
        return 2*solution4(n-1);
}

```

解法二：非递归解法

```c++
//变态跳滚动数组
int solution5(int n){ 
    int F[2]={0,1};
    if(n < 2)return F[n];
    for(int i=2;i<=n;i++){
        F[0]=F[1];
        F[1]=2*F[0];
    }
    return F[1];
}
```

