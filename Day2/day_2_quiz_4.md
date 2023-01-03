# 배열 두배 만들기

---

## 문제

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 각 원소에 두배한 원소를 가진 배열을 return하도록 solution 함수를 완성해주세요.

---
## 문제풀이

```javascript
    function solution(numbers) {
        return numbers.map((it) => it * 2);
    }
```

`map()` 함수를 활용하여 각각의 원소를 두배로 곱해 리턴하였습니다