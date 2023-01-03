# 아이스 아메리카노

## 문제

머쓱이는 추운 날에도 아이스 아메리카노만 마십니다. 아이스 아메리카노는 한잔에 5,500원입니다. 머쓱이가 가지고 있는 돈 `money`가 매개변수로 주어질 때, 머쓱이가 최대로 마실 수 있는 아메리카노의 잔 수와 남는 돈을 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

## 문제풀이(1차)

```javascript
  function solution(money) {
    var answer = [];
    const coffee = 5500;
    
    for(let i = 0; coffee * i <= money; i++) {
        answer[0] = i
    }
    
    answer[1] = money - (coffee*answer[0])
    
    return answer;
  }
```

어.. 일단 for문으로 커피를 살 수 있는 최대치를 카운팅해서 넣고 그만큼 money에서 뺐는데..

## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(money) {
      
      const count = parseInt(money/5500)
      const changes = money - (count * 5500)
      
      return [count, changes]
  }
```

진짜 수학공부가 더 시급한가봐요 그냥 money에서 커피값을 나누면 훨씬 간단해지는걸.....저렇게 힘들게 계산했었다니요...😟💦