# 자바스크립트 알고리즘 문제풀이 👾

### 완료한 문제 모음

#### 위클리 퀴즈 1일차
url : https://programmers.co.kr/learn/courses/30/lessons/82612

##### 나의 풀이

```javascript
function solution(price, money, count) {
    var answer = 0;
    let total = 0
    
    for(let i = 1; i < count+1; i++){
        total += price*i;
    }
    // 금액이 부족하지 않은 경우 고려해야 함
    //answer = Math.abs(total-money);
    answer = (total-money);
    
    if(Math.sign(answer) <= 0){
        answer = 0
    }
    
    return answer;
}
```

* 개선

```javascript
function solution(price, money, count) {
    let answer = 0;

    for (let i = 1; i <= count; i++) {
        answer += price * i;
    }

    return answer > money ? answer - money : 0;
}
```

등차수열이라는 걸 알고 있음에도 그런 방식으로 풀지 못함
답을 좀 더 깔끔히 쓸 수 있음에도 안 익숙해서 못쓰겠음...