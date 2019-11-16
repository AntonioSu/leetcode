/*You are given coins of different denominations and a total amount of money amount. Write a function to compute the fewest number of coins that you need to make up that amount. If that amount of money cannot be made up by any combination of the coins, return -1.

Example 1:

Input: coins = [1, 2, 5], amount = 11
Output: 3
Explanation: 11 = 5 + 5 + 1
Example 2:

Input: coins = [2], amount = 3
Output: -1
Note:
You may assume that you have an infinite number of each kind of coin.*/
```
class Solution {
public:
    Solution(){}
    int coinChange(vector<int>& coins, int amount) {
        int size=coins.size();
        vector< vector<int> > vec(size+1, vector<int> (amount+1, INT_MAX-1));
        //初始赋值，第一列赋值为0，vec[i][j]表示第i个硬币，能组成j的最小硬币数
        for (int k = 0; k < size+1; ++k) {
            vec[k][0]=0;
        }
        //计算第一行的值，否则结果就都是0
        for (int i = 0; i < amount+1; ++i) {
            if(i>=coins[0])
                vec[1][i]=min(vec[0][i],vec[1][i-coins[0]]+1);
        }
        for(int i=1;i<=size;i++){
            for (int j=1;j<=amount;j++){
                if(j<coins[i-1])
                    vec[i][j]=vec[i-1][j];
                else
                    vec[i][j]=min(vec[i-1][j],vec[i][j-coins[i-1]]+1);

            }
        }
        //当无法满足的时候返回-1
        return vec[size][amount]>INT_MAX-10?-1:vec[size][amount];
    }
};
```
