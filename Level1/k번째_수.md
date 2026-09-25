# K번째수 (Level 1)

## 문제
배열 array와 쿼리 배열 commands(각 원소는 [i, j, k])가 주어질 때, 각 쿼리마다 array의 i번째부터 j번째까지(1-indexed) 자른 뒤 오름차순 정렬해서 k번째 수를 구해 배열로 return 하라.

## 접근
쿼리마다 필요한 구간만 잘라 정렬한다. 매 쿼리마다 `nums`를 반복문 **안에서** 새로 선언하면, 이전 쿼리의 값이 남아있는 문제 자체가 생기지 않는다.

## 코드
```cpp
#include <algorithm>
using namespace std;

vector<int> solution(vector<int> array, vector<vector<int>> commands) {
    vector<int> answer;
    for (vector<int> command : commands) {
        int i = command[0], j = command[1], k = command[2];
        vector<int> nums(array.begin() + i - 1, array.begin() + j);
        sort(nums.begin(), nums.end());
        answer.push_back(nums[k - 1]);
    }
    return answer;
}
```

## 사용 함수
| 함수 | 용도 |
|---|---|
| `sort` | 잘라낸 구간을 오름차순 정렬 |
