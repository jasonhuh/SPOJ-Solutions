[PRIME1 - Prime Generator](https://www.spoj.com/problems/PRIME1/)

### C++
```cpp
#include <iostream>
#include <vector>
#include <string>
#include <cmath>
#include <sstream>
#include <unordered_map>

using namespace std;

bool is_prime(int n) {
    if (n <= 1) return false;
    if (n <= 3) return true;
    if (n%2 == 0 || n %3 == 0) return false;
    for (int i=5; i<=sqrt(n);i=i+6) {
        if (n % i == 0 || n%(i+2) == 0) {
            return false;
        }
    }
    return true;
}

void solve(unordered_map<int, bool>& map, int m, int n) {
    for (int i=max(2, m); i<=n; ++i) {
        if (!map.count(i)) {
            map[i] = is_prime(i);
            for (int j=2*i; j<=n;j=j+i) {
                map[j] = false;
            }
        }
        if (map[i]) {
            cout << i << endl;
        }
    }
    cout << endl;
}

int main() {
    unordered_map<int, bool> map;
    int tc, m, n, hi = 0;
    vector<pair<int,int>> inputs;
    cin >> tc;
    while (tc--) {
        cin >> m >> n;
        inputs.push_back(make_pair(m, n));
    }
    for (auto &it : inputs) {
        solve(map, it.first, it.second);
    }
    return 0;
}
```
