# algorithm_study_c

## 투포인터 

1. https://www.acmicpc.net/problem/2018

```python
#include <iostream>
using namespace std;
int main() {
	long long n;
	cin >> n;
	//prefix구하기
	
	long long sidx = 1;
	long long eidx = 1;
	long long sum = 1;
	long long cnt = 0;
	while (eidx<=n) {
		
		if (sum == n) {//합이 target일때 
			eidx++;
			cnt++;
			sum += eidx;
		}
		else if (sum < n) {//합이 target보다 작을때 
			eidx++;
			sum += eidx;
		}
		else {
			sum -= sidx;
			sidx++;
		}

	}
	
	cout << cnt;
	return 0;
}
```
