# 몫 구하기

---

## 문제

정수 `num1`, `num2`가 매개변수로 주어질 때, `num1`을 `num2`로 나눈 몫을 return 하도록 solution 함수를 완성해주세요.

---

## 문제풀이

```javascript

function solution(num1, num2) {
    var answer = Math.floor(num1 / num2);
    return answer;
}

```

매개변수 `num1`과 `num2` 를 나눈 값을 `Math.floor()`를 통해 정수로 반환하였습니다.

(다른 사람의 풀이를 보니 `parseInt`로도 정수변환이 가능하더랍니당🤔)