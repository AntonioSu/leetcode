**题目描述**   

 迪杰斯特拉(**Dijkstra**)算法是典型最短路径算法，用于计算一个节点到其他节点的最短路径。
它的主要特点是以起始点为中心向外层层扩展(广度优先搜索思想)，直到扩展到终点为止。

大概就是这样一个有权图，**Dijkstra**算法可以计算**任意节点**到**其他节点**的最短路径，比如起始定点是D

 对应的算法步骤如下：

https://github.com/AntonioSu/leetcode/blob/master/picture/Dijkstra.png?raw=true

解法一：先合并两个链表，而后再循环的合并每一个。

```c++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

const int inf = 0x3f3f3f3f;
int edge[5][5] =
        {
                {-1,-1,-1,-1,-1},
                {-1, 0, 2, 6, 4},
                {-1, inf, 0,3, inf},
                {-1, 7, inf, 0, 1},
                {-1, 5, inf, 12, 0}
        };

int main() {
    const int n = 4;//点的数量
    vector<int> dis(n+1,0);//当前各点到源点的距离
    vector<bool> book(n+1,false);//各点到源点是否为最小值

    //初始化，设源点为n1
    for (int i = 1; i <= n; ++i)dis[i] = edge[1][i];

    book[1] = true;
    for (int i = 1; i <= n - 1; ++i) {
        //找到离1号顶点最近的顶点
        pair<int,int>min_point={inf,0};
        for (int j = 1; j <= n; ++j) {
            if (!book[j]  && dis[j] < min_point.first) min_point={dis[j],j};
        }
        int u=min_point.second;
        //每轮迭代都可以确定一个点到源点的最短距离，因此只要迭代n-1轮
        book[u] = true;
        //通过已经确定的点，对dis数组进行更新
        //（未确定的点通过点u，缩小了到源点的距离）
        for (int v = 1; v <= n; ++v) {
            if (edge[u][v] < inf) {
                if (dis[v] > dis[u] + edge[u][v])
                    dis[v] = dis[u] + edge[u][v];
            }
        }
    }
    //输出结果
    for (int i = 1; i <= n; ++i)cout << dis[i] << ' ';
    system("pause");
    return 0;
}

```

