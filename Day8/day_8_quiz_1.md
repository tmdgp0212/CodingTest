# 배열자르기

## 문제

정수 배열 `numbers`와 정수 `num1`, `num2`가 매개변수로 주어질 때, `numbers`의 `num1`번 째 인덱스부터 `num2`번째 인덱스까지 자른 정수 배열을 return 하도록 solution 함수를 완성해보세요.

## 문제풀이

```javascript
  function solution(numbers, num1, num2) {
      return numbers.slice(num1,num2 + 1);
  }
```
