# 직각삼각형 출력하기

## 문제

"*"의 높이와 너비를 1이라고 했을 때, "*"을 이용해 직각 이등변 삼각형을 그리려고합니다. 정수 n 이 주어지면 높이와 너비가 n 인 직각 이등변 삼각형을 출력하도록 코드를 작성해보세요.

## 문제풀이

항상 문제풀이에 단순한 `solution`함수만 주어졌었는데 별안간

```javascript
  const readline = require('readline');
  const rl = readline.createInterface({
      input: process.stdin,
      output: process.stdout
  });

  let input = [];

  rl.on('line', function (line) {
      input = line.split(' ');
  }).on('close', function () {
      console.log(Number(input[0]));
  });
```

이런 녀석이 코드상에 있길래 너무 당황해버렸슴미다...
침착하게 구글링하면서 콘솔에 찍어보면서 풀어봤긴한데용...


```javascript
  const readline = require('readline');
  const rl = readline.createInterface({
      input: process.stdin,
      output: process.stdout
  });

  let input = "";

  rl.on('line', function (line) {
      
    for(let i = 1; i <= line; i++) {
        for(let k = 1; k <= i; k++) {
            input += "*";
        }
        input += "\n";    
    }
      
  }).on('close', function () {
      console.log(input);
  });
```

이게 맞는 방법인지는 모르겠어요..! 일단 정답이긴하답니다..😟(자신없음)

`for`문을 활용해 1씩 커지는 변수 `i`를 만들어
 `i`번 "*"을 찍고 "\n"로 엔터를 치는 방식을 `n`번 동안 반복하였습니다!
(저는  `n`을 `line`으로 받아왔는데 이건 맞는방법은 아닌거같아요...)