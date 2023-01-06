# 양꼬치

## 문제

머쓱이네 양꼬치 가게는 10인분을 먹으면 음료수 하나를 서비스로 줍니다. 양꼬치는 1인분에 12,000원, 음료수는 2,000원입니다. 정수 `n`과 `k`가 매개변수로 주어졌을 때, 양꼬치 `n`인분과 음료수 `k`개를 먹었다면 총얼마를 지불해야 하는지 return 하도록 solution 함수를 완성해보세요.

## 문제풀이

```javascript
    function solution(n, k) {
        const lamb = n * 12000;
        const drink = (k - Math.floor(n / 10)) * 2000;
        return lamb + drink;
    }
```