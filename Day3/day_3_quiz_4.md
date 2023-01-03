# 짝수는 싫어요

---

## 문제

정수 `n`이 매개변수로 주어질 때, `n` 이하의 홀수가 오름차순으로 담긴 배열을 return하도록 solution 함수를 완성해주세요.

---
## 문제풀이

```javascript
    function solution(n) {
    
    var answer = [];
    
    for(i = 1; i <= n; i++){
        i % 2 === 0 ? '' : answer.push(i)
    }
    
    return answer.sort((a,b) => a - b);
}
```

for문으로 n보다 작은 i의 값을 구하되, `% 2` 했을 때 나머지 값이 0인 경우(짝수)는 버리고 그렇지않은 경우(홀수) `answer`의 배열에 `push`해 주었습니다
그 다음 `sort`로 오름차순 정렬 한 뒤 리턴해주었습니다