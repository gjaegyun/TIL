# Symbol

``` js
const myName = {
    [Symbol("jaegyun")] : {
        friend: true
    },
    [Symbol("jaegyun")] : {
        friend: false
    },
}
```

이 symbol 이라는 것은 영어 번역 그 자체로 변수 자체의 상징같은 것을 의미하는데

만약 jaegyun이라는 변수가 object 외에도 존재를 한다하면 복잡해질 수 있을 것이다.

그럴 경우 사용할 수 있는 것이 이 고유의 상징을 부여해주는 symbol이다.

``` js
    const sb = Object.getOwnPropertySymbols(myName)
    sb.forEach(symbol => console.log(myName[symbol]))

    //{friend: true}
    //{friend: false}
```

이런식으로 고유의 key값을 가지듯이 나온다.