###  dp-of-yfy-1 ACWiNG902 
```
#include<iostream>
#include<string>
using namespace std;
int n,m;
const int N =1010;
char str1[1001],str2[1002];
int dp[N][N];
void init(){
    for(int i = 1;i <= n;++i)dp[i][0]=i;
    for(int j = 1;j <= m;++j)dp[0][j]=j; 
}
int main(){
    cin>>n>>str1+1;
    cin>>m>>str2+1;
    init();//---------------------------初始化边界情况(initialization boundary condition)
    for(int i = 1;i <= n;++i)
        for(int j = 1;j <= m;++j){
            dp[i][j]=min(dp[i-1][j]+1,dp[i][j-1]+1);
            if(str1[i]==str2[j])dp[i][j]=min(dp[i-1][j-1],dp[i][j]);
            else dp[i][j]=min(dp[i][j],dp[i-1][j-1]+1);
        }
    
    cout<<dp[n][m]<<endl;
}
```
