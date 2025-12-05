对于数组a，不管是什么情况，最大值要么是a[n - 1] * a[n - 2] * a[n - 3]，要么就是 a[0] * a[1] * a[n - 1], 所以，取大的那个就行了。<br>
## python代码
```python
n = int(input())
a = list(map(int, input().split()))
print(max(a[0] * a[1] * a[-1], a[-1] * a[-2] * a[-3]))
```
## c++代码
```c++
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    int n;
    cin >> n;
    
    vector<int> a(n);
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    int p1 = a[0] * a[1] * a[n - 1];
    int p2 = a[n - 1] * a[n - 2] * a[n - 3];

    cout << max(p1, p2) << "\n";

    return 0;
}
```
## c代码
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    int a[n];
    
    
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    int p1 = a[0] * a[1] * a[N - 1];
    int p2 = a[n - 1] * a[n - 2] * a[n - 3];
    if(p1 > p2){
      printf("%d\n", p1);
    }
    else{
      printf("%d\n", p1);
    }
    return 0;
}
```
