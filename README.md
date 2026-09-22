# C++ 코딩테스트 스터디

프로그래머스 코딩테스트 연습 문제를 C++로 풀며 정리하는 저장소.

## 구조
```
Level0/   Level 0 (코딩테스트 입문) 문제 정리
Level1/   (추후 레벨업 시 추가)
```

각 문제 파일은 `문제 / 접근 / 코드 / 사용 함수` 형식으로 정리되어 있습니다.

## 개념 메모

특정 문제가 아니라 여러 문제에 걸쳐 쓰이는 개념/문법 정리.

| 메모 | 내용 |
|---|---|
| [최대공약수 / 최소공배수](Notes/최대공약수_gcd.md) | `gcd`, `lcm` |
| [정렬(sort) 사용법](Notes/정렬_sort.md) | `sort`, 커스텀 비교자 |

## Level 0 목록

| 문제 | 사용 함수 |
|---|---|
| [배열 2배 만들기](Level0/배열_2배_만들기.md) | – |
| [최댓값 만들기 (1)](Level0/최댓값_만들기.md) | `sort` |
| [특정 문자 제거하기](Level0/특정_문자_제거하기.md) | `remove`, `erase` |
| [순서쌍 구하기](Level0/순서쌍_구하기.md) | – |
| [숨어있는 숫자의 덧셈 (1)](Level0/숨어있는_숫자의_덧셈.md) | `isdigit` |
| [편지](Level0/편지.md) | – |
| [배열의 유사도](Level0/배열의_유사도.md) | `find` |
| [369게임](Level0/369게임.md) | `to_string`, `count` |
| [중복된 숫자 개수](Level0/중복된_숫자_개수.md) | `count` |
| [A로 B 만들기](Level0/A로_B_만들기.md) | `sort` |
| [최빈값 구하기](Level0/최빈값_구하기.md) | `max_element`, `count` |
| [피자 나눠 먹기 (2)](Level0/피자_나눠_먹기.md) | `lcm` |
| [배열의 평균값](Level0/배열의_평균값.md) | `accumulate` |
| [k의 개수](Level0/k의_개수.md) | `to_string`, `count` |
| [중복된 문자 제거](Level0/중복된_문자_제거.md) | `string::find` |
| [2차원으로 만들기](Level0/2차원으로_만들기.md) | – |
| [모스 부호 (1)](Level0/모스_부호.md) | `stringstream`, `map` |
| [진료 순서 정하기](Level0/진료_순서_정하기.md) | `sort`(역순), `find` |
| [잘라서 배열로 저장하기](Level0/잘라서_배열로_저장하기.md) | `substr` |
| [공 던지기](Level0/공_던지기.md) | – |
| [소인수분해](Level0/소인수분해.md) | `unique`, `erase` |
| [뒤집힌 문자열](Level0/뒤집힌_문자열.md) | `reverse` |
| [직각삼각형 출력하기](Level0/직각삼각형_출력하기.md) | `string(n, ch)` |
| [삼각형의 완성조건 (1)](Level0/삼각형의_완성조건.md) | `sort` |
| [외계어 사전](Level0/외계어_사전.md) | `string::find` |
| [구슬을 나누는 경우의 수](Level0/구슬을_나누는_경우의_수.md) | – (조합 계산) |
| [배열 회전시키기](Level0/배열_회전시키기.md) | `rotate` |
| [모음 제거하기](Level0/모음_제거하기.md) | `remove_if`, `erase` |
| [문자열 정렬하기](Level0/문자열_정렬하기.md) | `string::find`, `sort` |
| [컨트롤 제트](Level0/컨트롤_제트.md) | `stringstream`, `stoi` |
| [배열 원소의 길이](Level0/배열_원소의_길이.md) | `string::length` |
| [가장 가까운 수](Level0/가장_가까운_수.md) | `sort`, `abs` |
| [대소문자 바꾸기](Level0/대소문자_바꾸기.md) | `islower`, `isupper`, `toupper`, `tolower` |
| [영어가 싫어요](Level0/영어가_싫어요.md) | `map`, `stoll` |
| [인덱스 바꾸기](Level0/인덱스_바꾸기.md) | `swap` |
| [한번만 등장한 문자](Level0/한번만_등장한_문자.md) | `count`, `sort` |
| [약수 구하기](Level0/약수_구하기.md) | – |
| [a와 b 출력하기](Level0/a와_b_출력하기.md) | – |
| [대소문자 바꿔서 출력하기](Level0/대소문자_바꿔서_출력하기.md) | `toupper`, `tolower` |
| [특수 문자 출력하기](Level0/특수_문자_출력하기.md) | – (이스케이프 시퀀스) |
| [문자열 겹쳐쓰기](Level0/문자열_겹쳐쓰기.md) | `string::replace` |
| [가장 큰 수 찾기](Level0/가장_큰_수_찾기.md) | – |
| [문자열 계산하기](Level0/문자열_계산하기.md) | `stringstream` |
| [숫자 찾기](Level0/숫자_찾기.md) | `to_string`, `string::find` |
| [자릿수 더하기](Level0/자릿수_더하기.md) | `to_string` |
| [OX퀴즈](Level0/OX퀴즈.md) | `stringstream`, `push_back` |
| [문자열 곱하기](Level0/문자열_곱하기.md) | – |
| [분수의 덧셈](Level0/분수의_덧셈.md) | `gcd` |
| [저주의 숫자 3](Level0/저주의_숫자_3.md) | `to_string`, `string::find` |
| [문자열 안에 문자열](Level0/문자열_안에_문자열.md) | `string::substr` |
| [제곱수 판별하기](Level0/제곱수_판별하기.md) | – |
| [세균 증식](Level0/세균_증식.md) | `pow` |
| [7의 개수](Level0/7의_개수.md) | `to_string`, `count` |
| [머쓱이보다 키 큰 사람](Level0/머쓱이보다_키_큰_사람.md) | – |
| [특이한 정렬](Level0/특이한_정렬.md) | `sort`, `abs` |
| [직사각형 넓이 구하기](Level0/직사각형_넓이_구하기.md) | `sort`, `abs` |
