# object Destucturing

``` js
const classRoom = {
    teacher: {
        myeongHee: "1",
        suil: "4"
    },
    friends: {
        gaon: true,
        heeSung: true,
        jueun: true
    }
}
```

이런식으로 object들이 ~안의 ~ 이렇게 되어있을때 보통이라면
classRoom안의 friends안의 gaon이런식으로 접근했을 것이다.

하지만 gaon이라고 그냥 사용할 수 있는 방법이 있다.

``` js
const {
    teacher: { suil },
    friends: { gaon }
} = classRoom;

const suil = classRoom.teacher.suil;
const gaon = classRoom.friends.gaon;

console.log(suil);
console.log(gaon);
```

이 두개는 같은 의미를 지닌 문장이다 이 두개를 보면 첫번째 구문이 더욱 간편하게 쓸 수 있을 것으로 보인다.

그리고 이 문법의 장점은 default value를 지정할 수 있다.

``` js
const {
    teacher: { suil = "3" }
} = classRoom;
```

이렇게 했을 경우 classRoom에 속해있는 teacher의 suil이라는 것이 **없을** 경우 3이라고 default value를 정해준 것이다.