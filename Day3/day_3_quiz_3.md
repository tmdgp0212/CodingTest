# 최빈값 구하기

---

## 문제

최빈값은 주어진 값 중에서 가장 자주 나오는 값을 의미합니다. 정수 배열 `array`가 매개변수로 주어질 때, 최빈값을 return 하도록 solution 함수를 완성해보세요. 
최빈값이 여러 개면 -1을 return 합니다.

---
## 문제풀이

```javascript
    function solution(array) {
    
    let count = [];
    
    // 0이 1000개 담겨있는 배열 생성
    for(i = 0; i <= 1000; i++){
        count.push(0)
    }
    
    // count배열에서 숫자와 일치하는 index값의 원소에 +1씩 카운트
    array.forEach(function(arr, idx){
        count[arr] += 1;
    }) 
    
    let answer = 0;
    let bigest = 0;
    let tmp = 0;
    
    // count배열에서 가장 높은 자리의 index값을 answer배열에 담음
    count.forEach(function(arr, idx){
        if(bigest < arr) {
            answer = idx;
            bigest = arr;
        }
    });
    
    // count값이 같은 또 다른 원소가 있다면 tmp에 ++
    // (본인과도 다시한번 비교하기때문에 1은 반드시 카운팅됨)
    count.forEach(function(arr, idx){
        arr === bigest ? tmp++ : tmp
    });
    
    // tmp의 값이 1보다 크다면 중복되는 최빈값이 있다고 판단하여 -1을 return 아니라면 answer를 return
    return tmp > 1 ? -1 : answer;
}
```

1. 0만 들어있는 길이 1000의 `count`배열을 만들었고
`for`문을 활용해 `array`의 원소와 일치하는 자릿수의 `count`원소에 +1씩 더한다.
(원소가 3인경우 `count[3]`에 +1 => 3이 2개면 최종적으로 `count[3]`이 2가 됩니다)

2. `count`에서 카운트가 가장 많이 된 자리의 index값을 `answer`에 우선 담는다.
~~여기서 끝나면 좋았겠지만.. 최빈값이 가장 높은 원소가 2개 이상이면 -1을 출력해야한다...ㅜㅜ~~

3. 한번 더 `forEach`문을 돌려 카운트 값이 일치하는 원소가 한개 이상이면 `tmp`에 담아 확인했다.

4. 최종적으로 `tmp`의 값이 1 이상이면 -1을, 아니라면 최초의 `answer`값을 리턴해주었다!!!


~~여담...~~
~~다른사람들 풀이코드는 짧으면 6줄 길면 15줄쯤 쓰는것같았는데... 다른사람의 풀이를 봐도 초면인 문법이 너무나도 많았기에... 저로써는 최선을 다한 풀이랍니당...💦~~