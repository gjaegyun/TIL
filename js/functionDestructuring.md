# function Destructuring

``` js
function friends(myFriends) {
    console.log(myFriends.jueun)
}

friends({
    jueun: true,
    gaon: true,
    heesung: true,
    suil: false
})
```

만약 friends라는 함수를 호출하기 위해서 이렇게 썼을 경우에 friends의 jueun을 호출하기 위해서는

위 식처럼 myFriends.jueun이라고 써야 할 것이다.

이 상황이 단순하면 문제없지만 단순하지 않다면
예를 들어 suil이라는 것이 friends에 **존재하지 않거나 다른곳에 쓰일 경우**엔 문제가 생길 수 있다.

``` js

//첫번째
function friends({ jueun, gaon, heesung, suil: true}) {
    console.log(myFriends.jueun)
}

friends({
    jueun: true,
    gaon: true,
    heesung: true,
    suil: false
})

//두번째
function friends({ myFriends: true, notFriend: { suil : false } }) {
    console.log(myFriends.jueun)
}

friends({
    myFriends: {
        jueun: true,
        gaon: true,
        heesung: true
    },
    notFriend: {
        suil: false
    }
})
```

이런식으로 default value를 지정할 수 있고, 훨씬 가독성 있고 보기 좋은 코드를 완성 시킬 수 있다.