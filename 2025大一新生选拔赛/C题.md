
**定理1**若b为零，则直接输出YES，因为任何一个非负整数都能通过有限次的/2变为0<br>
**定理2**若b为偶数，则如果a能变为b/2，则a就能变为b<br>
**定理3**若b为奇数，则a只能通过a/2来变成b<br>

**因此，我们第一步先将b不断/2，直到b变成奇数，记为b’,然后不断将a/2，观察在这个过程中是否等于b‘即可**

#### C++ 语言

```cpp
#include <iostream>
#include <algorithm> 

using namespace std;

void solve() {
    long long a, b;
    
    // 读取输入
    if (!(cin >> a >> b)) {
        return;
    }

    if (b == 0) {
        cout << "YES" << endl;
        return;
    }

    while (b % 2 == 0) {
        b /= 2;
    }

    while (a != b && a != 0) {
        a /= 2;
    }

    if (a == b) {
        cout << "YES" << endl;
    } else {
        cout << "NO" << endl;
    }
}

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    
    solve();

    return 0;
}
```

#### C 语言

```c
#include <stdio.h>
void solve() {
    int a, b;
    
    if (scanf("%d %d", &a, &b) != 2) {
        return;
    }

    if (b == 0) {
        printf("YES\n");
        return;
    }

    while (b % 2 == 0) {
        b /= 2;
    }

    while (a != b && a != 0) {
        a /= 2;
    }

    if (a == b) {
        printf("YES\n");
    } else {
        printf("NO\n");
    }
}

int main() {
    solve();
    return 0;
}
```

#### python 语言

```python
a, b = map(int, input().split())
if b == 0:
    print("YES")
else:
    while b % 2 == 0:
        b /= 2
    while a != b and a:
        a /= 2
    if a == b:
        print("YES")
    else:
        print("NO")
```
