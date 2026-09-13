# A로 B 만들기 (Level 0)

## 문제
문자열 before를 재배열해서 after를 만들 수 있는지 여부를 1/0으로 반환하라.

## 접근
두 문자열을 각각 정렬해서 같으면 1, 다르면 0.

## 코드
```cpp
#include <algorithm>
int solution(string before, string after) {
    sort(before.begin(), before.end());
    sort(after.begin(), after.end());
    return before == after ? 1 : 0;
}
```

## 사용 함수
| 함수 | 용도 |
|---|---|
| `sort` | 두 문자열을 정렬해 구성 문자가 같은지 비교 |
