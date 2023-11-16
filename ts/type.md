## interface

간단한 예제
``` ts
interface User {
    name : string;
    age : number;
}

let user : User = {
    name : 'gimjaegyun',
    age : 17
}
```
이런식으로 코드를 작성 해야 오류가 나지 않는다.

대표적인 이유로는 일반적이게 object를 만들면 안에 있는 object들의 type을 지정되지 않았기 때문에 interface를 통해서 type을 지정시켜 준 후 써야한다.

### ?

    user object에 쓰고 싶지 않고, 변수로써 쓰고 싶을때 써도 되고 안써도 되게 하는 문법이 있다.

    ``` ts
    interface User {
        name? : string;
    }
    ```

    이런식으로 변수 뒤에 ?을 붙이면 써도 되고 안써도 된다.

### readonly

    ``` ts
    interface User {
        readonly name : string;
    }
    ```

    이렇게 변수 앞에 readonly를 쓰면 선언과 object안에 쓸 수 있지만 변경을 할 수가 없다.