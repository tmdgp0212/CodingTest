# 배열 뒤집기

## 문제

정수가 들어 있는 배열 `num_list`가 매개변수로 주어집니다. `num_list`의 원소의 순서를 거꾸로 뒤집은 배열을 return하도록 solution 함수를 완성해주세요.

## 문제풀이(1차)

```javascript
  function solution(num_list) {
      let answer = [];
      
      for (let i = num_list.length; i > 0; i--) {
          answer.push(num_list[i-1]);
      }
      
      return answer;
  }
```

`for`문을 활용해 `num_list`의 마지막 원소부터 차례로 `answer[]`에 푸시해주었습니다.


## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(num_list) {
      return num_list.reverse();
  }
```

갠적으로 다른사람의 풀이보고 헙...하고 놀랐슴다... 딱 배열을 뒤집기 위한 함수가 마련이 되어있었더군요.. 또 이렇게 하나 배워감미다...✍️💦