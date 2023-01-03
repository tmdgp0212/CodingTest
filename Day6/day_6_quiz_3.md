# 짝수 홀수 개수

## 문제

정수가 담긴 리스트 `num_list`가 주어질 때, `num_list`의 원소 중 짝수와 홀수의 개수를 담은 배열을 return 하도록 solution 함수를 완성해보세요.

## 문제풀이(1차)

```javascript
  function solution(num_list) {
      var answer = [0,0]

      num_list.map((num) => num % 2 === 0 ? answer[0] += 1 : answer[1] += 1);

      return answer;
  }
```

주어진 `num_list`의 각 원소가 짝수이면 `answer[0]`에 홀수이면 `answer[1]`에 1씩 더해서 리턴해주었습니다.