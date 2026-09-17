# a와 b 출력하기 (Level 0)

## 문제
정수 a, b를 입력받아 "a = (a의 값)"과 "b = (b의 값)" 형태로 각각 출력하라. (반환값 없음, 표준입출력)

## 접근
cin으로 입력받은 뒤 cout으로 "a = " 같은 고정 문자열과 변수 값을 이어서 출력한다.

## 코드
```cpp
#include <iostream>
using namespace std;
int main() {
    int a, b;
    cin >> a >> b;
    cout << "a = " << a << "\n";
    cout << "b = " << b << "\n";
    return 0;
}
```

## 사용 함수
| 함수 | 용도 |
|---|---|
| – | cin/cout 기본 입출력만 사용 |
