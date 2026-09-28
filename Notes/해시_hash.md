# 해시(hash) 사용법 — unordered_set / unordered_map

특정 문제가 아니라 여러 문제에 걸쳐 쓰이는 해시 관련 정리. 관련 문제: [폰켓몬](../Level1/폰켓몬.md)

해시 함수는 어떤 값을 보고 그 값을 어디에 저장하거나 어디서 찾을지 빠르게 알려주는 함수다. C++에서는 `unordered_set`, `unordered_map`을 쓰면 내부에서 알아서 해시 함수를 만들어 처리해준다. 둘 다 평균 O(1)로 삽입/조회/삭제가 가능하다(단, 정렬은 안 됨).

## unordered_set — 값 자체만 필요할 때
중복 제거, 값이 존재하는지 확인, 서로 다른 값의 개수를 구할 때 사용한다.

```cpp
vector<int> nums = {1, 2, 2, 3, 3, 3};
unordered_set<int> s(nums.begin(), nums.end());
// s.size() == 3  (서로 다른 값의 개수)

if (s.find(3) != s.end()) {
    cout << "3이 있다";  // 존재 여부 확인
}
```

## unordered_map — 값과 그에 대응하는 값을 같이 저장할 때
숫자가 몇 번 등장했는지, 어떤 키에 어떤 값이 대응하는지 저장하고 싶을 때 사용한다.

```cpp
unordered_map<int, int> count;
for (int num : nums) count[num]++;   // 등장 횟수 세기

// 값 읽기
int c = count[1];

// 전체 순회
for (auto& p : count) {
    // p.first  = 키
    // p.second = 값
}
```

**주의**: `count[1]`처럼 `[]`로 읽기만 해도, 그 키가 없으면 자동으로 값 0인 항목이 새로 삽입되는 부작용이 있다. 삽입 없이 존재 여부만 확인하고 싶으면 `count.find(1) != count.end()`를 쓴다.

## 언제 해시를 쓸까
문제에 "중복 값을 제거하라", "서로 다른 종류의 개수를 구하라", "존재 여부를 판별하라"가 나오면 `unordered_set`. "각 값이 몇 번 등장했는지", "키에 대응하는 값을 저장하고 싶다"면 `unordered_map`. 공통적으로 "값을 빠르게 찾아야 한다"는 문제라면 해시를 떠올리면 된다.
