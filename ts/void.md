# void

``` ts
function something() :void {
    1 + 2 + 3
    // X return 1 + 2 + 3; <- 안됨
}
```

함수에서 void 타입은 실수로 return을 방지 해주는 것이라고 보면 편하다.

또, 아래 코드처럼 변수에는 undefined와 null만 할당한다.

``` ts
const iDontNeed : void = undefined //null
```