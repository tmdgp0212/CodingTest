# 중앙값 구하기

---

## 문제

중앙값은 어떤 주어진 값들을 크기의 순서대로 정렬했을 때 가장 중앙에 위치하는 값을 의미합니다. 예를 들어 1, 2, 7, 10, 11의 중앙값은 7입니다. 
정수 배열 `array`가 매개변수로 주어질 때, 중앙값을 return 하도록 solution 함수를 완성해보세요.

---
## 문제풀이

```javascript
    function solution(array) {
    const sortedArr = array.sort((a, b) => a - b);
    var answer = sortedArr[Math.floor(sortedArr.length / 2)]
    return answer;
}
```

우선 주어진 배열을 `sort`함수로 오름차순 정렬 하였습니다.
그 다음 배열의 총 길이를 반으로 나눈 뒤 `Math.floor`로 반내림한 값 (= 중앙값)을 구해서 해당 인덱스 값의 요소를 리턴해주었습니다.

~~시행착오...~~
~~배열의 index값을 0부터 센다는 사실을 잠시 잊어 `Math.ceil`로 반올림하면서 이게 왜 틀려?? 하다가 설마 이건가 하고 floor를 넣어본게 정답이였답니다....~~