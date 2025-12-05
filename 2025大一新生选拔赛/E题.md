**选择这个数字+1，其余都不变，等价于该数字-1，其余数字不变**

因此题目变成了：对于数组a，每次选择一个数字-1，至少多少次，能使得所有数字相等，很显然，答案为sum(a) - min(a) * n<br>

## python代码
```python
n = int(input())
a = list(map(int, input().split()))
print(sum(a) - min(a) * n)
```

## c++代码
```c++
#include <bits/stdc++.h>
using namespace std;
int main(){
    int n,x,m=1e9,s=0;
    cin>>n;
    while(cin>>x){
        s+=x;
        m=min(m,x);
    }
    cout<<s-m*n;
}

```

## c代码
```c
#include <stdio.h>
int main(){
    int n,x,m=1000000000,s=0;
    scanf("%d",&n);
    while(scanf("%d",&x)==1){
        s+=x;
        if(x<m) m=x;
    }
    printf("%d",s-m*n);
}
```
