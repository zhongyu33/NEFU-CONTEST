三条边 a、b、c 能组成三角形，当且仅当满足三角形不等式：

a + b > c<br>
a + c > b<br>
b + c > a<br>

若全部满足输出 `YES`，否则输出 `NO`。

## 代码示例（C++）
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    long long a,b,c;
    cin>>a>>b>>c;
    cout<<((a+b>c && a+c>b && b+c>a)?"YES":"NO");
}
```
## 代码示例（C）
```c
#include <stdio.h>
int main(){
    long long a,b,c;
    scanf("%lld%lld%lld",&a,&b,&c);
    if(a+b>c && a+c>b && b+c>a) printf("YES");
    else printf("NO");
}
```

## 代码示例（python）
```python
a,b,c = map(int, input().split())
print("YES" if a+b>c and a+c>b and b+c>a else "NO")
```
