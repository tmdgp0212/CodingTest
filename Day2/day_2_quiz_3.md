# 분수의 덧셈

---

## 문제

 첫 번째 분수의 분자와 분모를 뜻하는 `denum1`, `num1`, 두 번째 분수의 분자와 분모를 뜻하는 `denum2`, `num2`가 매개변수로 주어집니다. 두 분수를 더한 값을 기약 분수로 나타냈을 때 분자와 분모를 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

---
## 문제풀이(1차)

```javascript
	function solution(denum1, num1, denum2, num2) {
    
     //분자
    let denum = (denum1 * num2) + (denum2 * num1);
      
     //분모
    let num = num1 * num2;
    
    let tmp = 1;
    
    for (let i = 1; i < denum; i++) {
        if(denum % i === 0 && num % i === 0){
            tmp = i
        } 
    }

    return [denum / tmp, num / tmp];
    
	}
```

---

분명 초등학교때 배운 수학인데.. 
*'두 분수의...합....??을 어떻게 하더라...?? 기약분수가 뭔데...???'*

구글로 '두 분수의 합' 따위를 검색하면서 조금씩 조금씩 풀어나가다 보니 테스트케이스를 풀어내는데에는 성공을했습니다!! 

근데 막상 문제 제출을 하니 두개의 테스트 문제에서 자꾸만 실패가 나는것이아닌가요ㅛㅗ...🤔

같은 문제를 구글링을 해봐도 내 답과 같은 로직을 짠 사람들도 많이 보이는데... 나만 왜 틀리는거지..??

## 문제풀이(최종)

```javascript
	function solution(denum1, num1, denum2, num2) {
    
     //분자
    let denum = (denum1 * num2) + (denum2 * num1);
      
     //분모
    let num = num1 * num2;
    
    let tmp = 1;
    
    for (let i = 1; i <= denum; i++) {
        if(denum % i === 0 && num % i === 0){
            tmp = i
        } 
    }

    return [denum / tmp, num / tmp];
    
	}
```

---
암만봐도 틀린게 없는 내 답과 다른 사람의 답을 수십번 비교후에 드디어 답을 찾아냈지요..!!
.
.
.
정답은...
for문의 조건식이
`let i = 1; i < denum; i++` 가 아닌 `let i = 1; i <= denum; i++` 이였습니다...!! 두둥......