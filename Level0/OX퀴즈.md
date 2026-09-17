# OX퀴즈 (Level 0)

## 문제
"3 + 4 = 7"처럼 공백으로 구분된 수식 문자열들의 배열 quiz가 주어질 때, 각 수식이 맞으면 "O", 틀리면 "X"를 담은 배열을 반환하라.

## 접근
문자열마다 stringstream으로 "a 연산자 b = c"를 순서대로 읽어 실제 계산값과 c를 비교한다.

답 배열이 `vector<string>`이라는 점에 주의: `string`에는 `+=`와 `push_back` 둘 다 쓸 수 있지만,
`vector<string>`/`vector<char>`처럼 컨테이너에 원소를 추가할 때는 `+=`가 안 되고 `push_back`만 가능하다.

## 코드
```cpp
#include <sstream>
vector<string> solution(vector<string> quiz) {
    vector<string> answer;
    for (string s : quiz) {
        int a, b, c, num;
        char op, opp;
        stringstream ss(s);
        ss >> a >> op >> b >> opp >> c;
        if (op == '+') num = a + b;
        else num = a - b;

        if (num == c) answer.push_back("O");
        else answer.push_back("X");
    }
    return answer;
}
```

## 사용 함수
| 함수 | 용도 |
|---|---|
| `stringstream` | "a 연산자 b = c" 형태를 토큰 단위로 읽기 |
| `push_back` | vector에는 `+=`가 아니라 `push_back`으로 원소 추가 |
