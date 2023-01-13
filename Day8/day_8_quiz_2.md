# 외계행성의 나이

## 문제

우주여행을 하던 머쓱이는 엔진 고장으로 PROGRAMMERS-962 행성에 불시착하게 됐습니다. 입국심사에서 나이를 말해야 하는데, PROGRAMMERS-962 행성에서는 나이를 알파벳으로 말하고 있습니다. a는 0, b는 1, c는 2, ..., j는 9입니다. 예를 들어 23살은 cd, 51살은 fb로 표현합니다. 나이 `age`가 매개변수로 주어질 때 PROGRAMMER-962식 나이를 return하도록 solution 함수를 완성해주세요.

## 문제풀이(1차)

```javascript
  function solution(age) {
      var answer = String(age).split('').map(num => {
          switch (num) {
              case '0' : 
                  return age = 'a'
              case '1' :
                  return age = 'b'
              case '2' :
                  return age = 'c'
              case '3' :
                  return age = 'd'
              case '4' :
                  return age = 'e'
              case '5' :
                  return age = 'f'
              case '6' :
                  return age = 'g'
              case '7' :
                  return age = 'h'
              case '8' :
                  return age = 'i'
              case '9' :
                  return age = 'j'
          }
      });
      return answer.join("");
  }
```

분명 다른 방법이 있을거같긴 했지만... 생각나는 방식은 가장 단순한 노가다방식뿐이였다...
일단 당장을 모르겠으니 생각대로 풀어서 제출..!

## 문제풀이(2차) :: 다른사람의 풀이를 참고함

```javascript
  function solution(age) {
      const alphabet = 'abcdefghijk'

      const answer = age.toString().split('').map(num => {
        return alphabet.slice(~~num, ~~num + 1)
      })
      
      return answer.join('')
  }
```

인덱스 값을 생각했으면 이런 노가다를 할 필요가 없던 것이였던것이였습니다...😩
하지만 로직은 조금 더 복잡해서 생각 할 시간이 많이 필요했당...

알파벳을 문자열로 묶어 변수에 할당해 준 뒤,
`age`를 문자화하고 한글자씩 배열에 나누어담았다.
`map`함수 내에서 한자릿씩, 해당 인덱스값에 해당하는 알파벳을 잘라서 썻다!