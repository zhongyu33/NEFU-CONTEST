

### 💡 问题描述

在一个林场里，鸡有 2 只脚，兔子有 4 只脚。已知脚的总数为 $N$ ($1 \le N \le 200$)，求满足条件的鸡和兔子的**组合方案**有多少种。

**输入:** 一个整数 $N$ ($1 \le N \le 200$)。
**输出:** 不同的组合方案数。

| 示例输入 $N$ | 示例输出 |
| :----------: | :--------: |
| 4            | 2          |
| 6            | 2          |
| 5            | 0          |

---

### 🔍 解题思路与数学推导

设鸡的数量为 $x$，兔子的数量为 $y$。$x$ 和 $y$ 必须为非负整数 ($x \ge 0, y \ge 0$)。

总脚数 $N$ 满足等式：

$$2x + 4y = N$$

#### 1. 奇偶性判断

由于 $2x$ 和 $4y$ 都是偶数，它们的和 $N$ 必然是偶数。

* 如果 $N$ 是**奇数**，则等式无非负整数解，方案数为 **0**。

#### 2. 偶数情况求解

当 $N$ 是偶数时，等式变为 $x + 2y = N/2$。

令 $M = N/2$，解得 $x = M - 2y$。

根据 $x \ge 0$，可得 $y \le M/2$。

兔子的数量 $y$ 的取值范围是：
$$0 \le y \le \lfloor \frac{M}{2} \rfloor$$

方案数即为 $y$ 的可能取值个数：

$$\text{方案数} = \lfloor \frac{M}{2} \rfloor + 1 = \lfloor \frac{N}{4} \rfloor + 1$$

---

### 💻 代码实现

#### C 语言

```c
#include <stdio.h>

int main() {
    int N;

    if (scanf("%d", &N) != 1) {
        return 0;
    }

    int solutions = 0;


    if (N % 2 != 0) {
        ans = 0;
    } else {
        ans = (N / 4) + 1; 
    }
    printf("%d\n", solutions);

    return 0;
}
```

#### C++ 语言

```c++
#include <iostream>

using namespace std;

int main() {

    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    
    int N;
    while (cin >> N) {
        int ans = 0;


        if (N % 2 != 0) {
            ans = 0;
        } else {
            ans = (N / 4) + 1;
        }
        cout << ans << endl;
    }

    return 0;
}
```
#### Python 语言

```python
N = int(input())

ans = 0

if N % 2 != 0:
    ans = 0
else:
    ans = (N // 4) + 1

print(ans)
```
