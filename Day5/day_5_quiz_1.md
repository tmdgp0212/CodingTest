# 옷가게 할인 받기

## 문제

머쓱이네 옷가게는 <u>10만 원 이상 사면 5%, 30만 원 이상 사면 10%, 50만 원 이상 사면 20%를 할인</u>해줍니다.
구매한 옷의 가격 `price`가 주어질 때, 지불해야 할 금액을 return 하도록 solution 함수를 완성해보세요.

### 제한사항

- 10 ≤ price ≤ 1,000,000
  - price는 10원 단위로(1의 자리가 0) 주어집니다.
- 소수점 이하를 버린 정수를 return합니다.

## 문제풀이(1차)

```javascript
  function solution(price) {
    let answer = price;
    
    if(100000 <= price && price < 300000){
        answer *= 0.95;
    } else if (300000 <= price && price < 500000) {
        answer *= 0.9;
    } else if (500000 <= price) {
        answer *= 0.8;
    }
    
    return parseInt(answer);
  }
```

`if else` 문으로 `price`의 크기를 비교해 각각의 할인율을 적용해주었습니다.


## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(price) {
    let answer = price;
    
    if(500000 <= price){
        answer *= 0.8;
    }
    
    if (300000 <= price) {
        answer *= 0.9;
    }
    
    if (100000 <= price) {
        answer *= 0.95;
    }
    
    return parseInt(answer);
  }
```

큰 수 부터 걸러주고, `if else` 대신 그냥 `if`문을 쓰니 코드가 훨씬 간결하고 가독성이 높습니다..

return문에는 `parseInt` 대신 `Math.floor` 의 사용이 가능하며,
`Math.floor`는 `~~`와 같다고합니다 ❗

```javascript
  return Math.floor(answer) === ~~answer
```