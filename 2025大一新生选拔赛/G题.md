夹角 ≥ 45° 等价于斜率 ≥ 1。

郭靖在 (x1, y1)，大雕在 (x2, y2)，由于大雕在右上方：

角度 ≥ 45° ⇔ (y2 - y1) / (x2 - x1) ≥ 1

即：

y2 - y1 ≥ x2 - x1

## C 代码
```c
#include <stdio.h>
int main(){
    int x1,y1,x2,y2;
    while(scanf("%d%d%d%d",&x1,&y1,&x2,&y2)==4)
        printf("%s\n",(y2-y1>=x2-x1)?"GUOJING-V5!":"GUOJING-BUG!");
}
```

## C++ 代码
```c++
#include <bits/stdc++.h>
using namespace std;
int main(){
    int x1,y1,x2,y2;
    while(cin>>x1>>y1>>x2>>y2)
        cout<<((y2-y1>=x2-x1)?"GUOJING-V5!":"GUOJING-BUG!")<<"\n";
}
```
## Python 代码
```python
import sys
for line in sys.stdin:
    x1,y1,x2,y2 = map(int,line.split())
    print("GUOJING-V5!" if y2-y1 >= x2-x1 else "GUOJING-BUG!")
```
