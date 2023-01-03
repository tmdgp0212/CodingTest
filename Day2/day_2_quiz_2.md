# 숫자 비교하기

---

## 문제

정수 `num1`과 `num2`가 매개변수로 주어집니다. 두 수가 같으면 1 다르면 -1을 retrun하도록 solution 함수를 완성해주세요.

---

## 문제풀이

```javascript

function solution(num1, num2) {
    return num1 === num2 ? 1 : -1;
}

```

삼항연산자를 이용해 `num1`과 `num2`를 비교하고 true면 1 false면 2 를 리턴하도록 하였습니다