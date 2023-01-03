# 배열의 평균값

## 문제

정수 배열 `numbers`가 매개변수로 주어집니다. `numbers`의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.

## 문제풀이(1차)

```javascript
    function solution(numbers) {
        let addNum = 0;
        
        numbers.forEach(function(num){ addNum += num })
        
        return addNum / numbers.length
    }
```

`forEach`문 으로 배열의 각 요소를 `addNum`에 더해준 뒤 `numbers.length`로 나눠 반환해주었습니다.


## 문제풀이(2차)

```javascript
    function solution(numbers) {
        return numbers.reduce((a,b) => a + b) / numbers.length
    }
```

다른사람의 풀이를 보다보니 `reduce()`를 사용하면 로직이 상당히 짧고 간결해지길래 구글에서 속성으로 사용법을 배워 적용해보았습니다 ✍️

`reduce`함수로 배열의 각 요소를 더해준 누적값을 `numbers.length`로 나눠 반환해주었습니다.

코테를 풀려면 배열관련 함수를 최대한 많이 익혀둬야 할 것 같습니당..!

