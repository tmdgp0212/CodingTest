# 문자열 뒤집기

## 문제

문자열 `my_string`이 매개변수로 주어집니다. `my_string`을 거꾸로 뒤집은 문자열을 return하도록 solution 함수를 완성해주세요.

## 문제풀이(1차)

```javascript
  function solution(my_string) {
      let answer = my_string.split("").reverse();
      
      return answer.join("");
  }
```

주어진 문자열 `my_string`을 `split()`메소드를 사용해 배열화시킨 뒤 `reverse()`로 뒤집고 `join()`으로 다시 문자화 시켜주었습니다.