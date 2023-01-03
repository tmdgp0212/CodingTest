# 두 수의 나눗셈

---

## 문제

정수 `num1`과 `num2`가 매개변수로 주어질 때, `num1`을 `num2`로 나눈 값에 1,000을 곱한 후 정수 부분을 return 하도록 soltuion 함수를 완성해주세요.

---

## 문제풀이

```javascript

function solution(num1, num2) {
    var answer = parseInt((num1 / num2) * 1000);
    return answer;
}

```

매개변수 `num1`과 `num2` 를 나눈 값에 1000을 곱한 뒤 `parseInt()`를 통해 정수로 반환하였습니다.

(`Math.floor`를 쓰려다 전 문제에서 `parseInt`를 본 것이 생각나 한번 써보았습니당🤔)