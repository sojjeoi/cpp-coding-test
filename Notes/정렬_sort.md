# 정렬(sort) 사용법

특정 문제가 아니라 여러 문제에 걸쳐 쓰이는 `sort` 관련 정리. 관련 문제: [특이한 정렬](../Level0/특이한_정렬.md), [직사각형 넓이 구하기](../Level0/직사각형_넓이_구하기.md)

## 오름차순 / 내림차순
- `sort(v.begin(), v.end())` → **오름차순**(기본값)
- `sort(v.rbegin(), v.rend())` → **내림차순** (reverse iterator로 뒤집어서 정렬)
- `sort(v.begin(), v.end(), greater<int>())` 또는 `sort(v.begin(), v.end(), [](int a, int b){ return a > b; })` → 내림차순을 직접 명시

## vector<vector<int>> vs vector<pair<int,int>>
같은 "값 2개를 묶은 목록"이라도 접근 방식이 다르다.

| 형태 | 원소 접근 | 특징 |
|---|---|---|
| `vector<vector<int>>` | `v[i][0]`, `v[i][1]` | 한 행에 원소가 2개보다 많아질 수도 있음(가변) |
| `vector<pair<int,int>>` | `v[i].first`, `v[i].second` | 항상 딱 2개로 고정 |

예) `{1, 2}`가 첫 원소일 때: `v[0][1] == 2` (2차원 벡터) / `v[0].second == 2` (pair 벡터)

## 커스텀 비교자로 정렬 기준 2개 걸기
1번 기준으로 정렬하고, 값이 같으면 2번 기준으로 정렬(tie-break)하는 패턴.

```cpp
// pair<int,int>: first 오름차순, 같으면 second 내림차순
sort(v.begin(), v.end(), [](pair<int,int> a, pair<int,int> b) {
    if (a.first == b.first) return a.second > b.second;
    return a.first < b.first;
});

// vector<int>: [0]번 오름차순, 같으면 [1]번 내림차순
sort(v.begin(), v.end(), [](vector<int> a, vector<int> b) {
    if (a[0] == b[0]) return a[1] > b[1];
    return a[0] < b[0];
});
```
