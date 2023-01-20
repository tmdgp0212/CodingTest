# 진료 순서 정하기

## 문제

외과의사 머쓱이는 응급실에 온 환자의 응급도를 기준으로 진료 순서를 정하려고 합니다. 정수 배열 `emergency`가 매개변수로 주어질 때 응급도가 높은 순서대로 진료 순서를 정한 배열을 return하도록 solution 함수를 완성해주세요.

## 문제풀이

```javascript
  function solution(emergency) {
      const originEmergency = [...emergency];
      let answer = [...originEmergency]

      emergency.sort((a,b) => b - a).forEach((curNum, curIdx) => {
          originEmergency.forEach((originNum, idx) => {
              if (curNum === originNum) {
                  answer[idx] = curIdx + 1
              }
          })
      })
      
      return answer
  }
```

1. `originEmergency`(이하 `origin...`)에 원본 배열을 담는다 (이후 원본배열이 수정 될 것이기 때문)


2. `answer`에 원본배열을 한번 더 담는다 (정답 제출용 . 원본배열과 같은 길이의 배열이 필요)

3. 원본배열은 `sort()`로 내림차순 정렬한다
3-1. 해당 숫자의 index +1  값이 해당 순자의 응급도가 됨

4. 정렬 된 원본배열과 `origin...`의 값을 하나씩 비교하여 두개의 값이 일치할 때,   
해당값이 `origin...` 에서 원래 위치해 있던 자리에 (`answer[idx]`)  
원본배열의 index +1(응급도)을 담는다 (`curIdx + 1`)