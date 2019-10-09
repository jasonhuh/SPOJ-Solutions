

### Python
```py
A = []
while True:
  num = int(input())
  if num == 42:
    break  
  A.append(num)

for i in range(len(A)):
	print(A[i])
```

***

### Java

```java
import java.util.*;

class Main
{
	public static void main (String[] args) throws java.lang.Exception
	{
		List<Integer> arr = new ArrayList<>();
		try(Scanner sc = new Scanner(System.in)) {
			while (true) {
				int num = sc.nextInt();
				if (num == 42) {
					break;
				}
				arr.add(num);				
			}
		}
		for (int num : arr) {
			System.out.println(num);
		}
	}
}
```

***

### C++
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
	// your code goes here
	int num;
	vector<int> arr;
	while(true) {
		cin >> num;
		if (num == 42) {
			break;
		}
		arr.emplace_back(num);
	}
	for (int num : arr) {
		cout << num << endl;
	}
	return 0;
}
```

***

##### Comment:
This is my first problem with Spoj.
