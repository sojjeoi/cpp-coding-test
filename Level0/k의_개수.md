# k의 개수 (Level 0)

## 문제
정수 i, j, k가 주어질 때 i부터 j까지의 정수 중 k가 몇 번 등장하는지(자릿수 포함) 반환하라.

## 접근
i~j 각 숫자를 문자열로 바꾸고 count()로 숫자 k('0'+k)의 등장 횟수를 누적.

## 코드
```cpp
#include <algorithm>
int solution(int i, int j, int k) {
    int answer = 0;
    for (int x = i; x <= j; x++) {
        string xx = to_string(x);
        answer += count(xx.begin(), xx.end(), '0' + k);
    }
    return answer;
}
```

## 사용 함수
| 함수 | 용도 |
|---|---|
| `to_string` | 정수를 문자열로 변환 |
| `count` | 문자열 내 특정 숫자 문자 개수 세기 |
