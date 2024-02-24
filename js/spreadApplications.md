# spread Applications

``` js
    const friend = {
        name: "jueun"
    };

    console.log({ ...friend, newFriend: "sanghyuk"});
    /// name: "jueun" newFriend: "sanghyuk"
```

이렇게 ...붙여 풀어서 사용하는 것을 spread라고 한다.

``` js
    const userInputName = prompt("your name");

    const user = {
        userName: "jaegyun",
        ...(lastName !== "" && { lastName })
    }
```

여기서 userInputName을 사용하면 되는데 왜 굳이 spread를 사용해야 하나요? 라고 생각할 수 있다.

이유는 바로 spread 문법을 사용해서 객체를 유연하게 확장함으로써 코드의 가독성과 유지 보수성을 향상시킬 수 있기 때문이다.