# 짝수의 합

## 문제

정수 n이 주어질 때, n이하의 짝수를 모두 더한 값을 return 하도록 solution 함수를 작성해주세요.

## 문제풀이(1차)

```javascript
  function solution(n) {
      let arr = [];
      
      for(let i = 0; i <= n; i++){
          if (i % 2 === 0) {
              arr.push(i);
          }
      }
      return arr.reduce((acc,cur) => acc + cur);
  }
```

## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(n) {
      let arr = 0;
      
      for(let i = 0; i <= n; i++){
          if (i % 2 === 0) {
              arr += i
          }
      }
      return arr;
  }
```

앗차차.. 내가 너무 어렵게 생각했다... 배열을 만들 필요 없이 걍 더하믄 되는건데...😶‍🌫️