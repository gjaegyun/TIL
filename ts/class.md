# class

먼저, js에서의 class는

``` js
    class Friends {
        constructor (name) {
            this.name = name;
        }
    }

    const myFriend = new Friends("Jueun");
```

이런식으로 썼다면, ts에서의 class는

``` ts
    class Friends {
        name: string;
        constructor (name: string) {
            this.name = name;
        }
    }

    const myFriend = new Friends("Jueun");
```

이런식으로 자신이 사용할 변수의 타입을 미리 선언한 뒤에, 

변수 초기화를 할 때에도 () 안에 type을 선언해준다