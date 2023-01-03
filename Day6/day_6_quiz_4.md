# 문자 반복 출력하기

## 문제

문자열 `my_string`과 정수 `n`이 매개변수로 주어질 때, `my_string`에 들어있는 각 문자를 `n`만큼 반복한 문자열을 return 하도록 solution 함수를 완성해보세요.

## 문제풀이(1차)

```javascript
  function solution(my_string, n) {
      my_string = my_string.split("");
      var answer = [];
      
      for(let i = 0; i < my_string.length; i ++) {
          for(let k = 0; k < n; k++) {
              answer.push(my_string[i])
          }
      }
      
      return answer.join("");
  }
```

`my_string`을 배열화 한뒤, 하나의 문자당 `n`번 `answer[]`에 `push`하고 다시 문자화해서 리턴하였습니다.


## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(my_string, n) {
      let answer = ""
      my_string.split("").map((str) => answer += str.repeat(n))
      
      return answer;
  }
```

다른 사람의 풀이에서 `repeat()`을 발견해서 얼른 적용해보았습니다.
`문자열.repeat(n)` 을 하면 해당 문자를 n번 반복해준다고합니다 ❗
배열화한 문자열 하나하나를 `repeat()`메소드로 반복하여 `answer`에 차곡차곡 더한 뒤 리턴해주었습니다
