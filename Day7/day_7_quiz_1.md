# 특정 문자 제거하기

## 문제

문자열 `my_string`과 문자 `letter`이 매개변수로 주어집니다. `my_string`에서 `letter`를 제거한 문자열을 return하도록 solution 함수를 완성해주세요.

## 문제풀이(1차)

```javascript
  function solution(my_string, letter) {
      while (my_string.includes(letter)) {
          my_string = my_string.replace(letter,'');
      }
      return my_string
  }
```

`my_string` 에서 `letter`가 없을 때 까지 `my_string` 에서 `letter`를 ``(빈문자열)로 replace하여 return해주었습니다

## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(my_string, letter) {
      return my_string.replaceAll(letter,'');
  }
```

`replaceAll`이라는 메소드를 알게 되어 `while`문 없이 문제 해결이 가능해졌습니다