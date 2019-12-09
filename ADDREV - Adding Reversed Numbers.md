# [ADDREV - Adding Reversed Numbers](https://www.spoj.com/problems/ADDREV/)

### C++
```cpp
#include <iostream>

using namespace std;

int reverse(int n) {
    int res = 0;
    while (n) {
        res = res*10 + n%10;
        n /= 10;
    }
    return res;
}

int solve(int m, int n) {
    int a = reverse(m), b = reverse(n);
    return reverse(a+b);
}

int main() {
    int tc, m, n;
    cin >> tc;
    while (tc--) {
        cin >> m >> n;
        cout << solve(m,n) << endl;
    }
    return 0;
}

```
