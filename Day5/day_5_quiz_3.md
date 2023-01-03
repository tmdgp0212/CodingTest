# 나이출력

## 문제

머쓱이는 40살인 선생님이 몇 년도에 태어났는지 궁금해졌습니다. 나이 `age`가 주어질 때, 2022년을 기준 출생 연도를 return 하는 solution 함수를 완성해주세요.

## 문제풀이

```javascript
  function solution(age) {
      return 2022 - age + 1;
  }
```

년도에서 나이를 빼고 + 1(태어난 연도에 1살)
