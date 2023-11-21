# interface

### interface 선언해주기
``` ts
interface User {
    age : number;
    name : string;
}
```
- 대표적인 이유로는 일반적이게 object를 만들면 안에 있는 object들의 type을 지정되지 않았기 때문에 interface를 통해서 type을 지정시켜 준 후 써야한다.

### interface로 만든 변수 활용해주기
``` ts
const jaegyun: User = {
    name: "jaegyun",
    age: 17
}
```
- 여기서 jaegyun이라는 변수를 User을 통해 정의 해주고 있다.

### 함수 인자로 활용
``` ts
function getUser(user:User) {
    console.log(user);
}

getUser({name : "jaegyun", age: 17});
```
- 여기서 getUser라는 함수의 인자로 활용을 해서 함수를 호출해줄때 {}안에 name과 age를 써서 호출해준다.

### 함수 활용
``` ts
interface Add {
  (x: number, y: number): number;
}

let addFunc: Add = (a, b) => a + b;

console.log(addFunc(12, 8));
```

- 위 코드에서는 addFunc에서 Add 함수타입에서 받은 두개의 매개변수를 더하는 함수를 사용하고 있다.
- 즉, console.log안에서 addFunc를 사용해서 12와 8을 매개변수로 넣어줬을때 12 + 8인 20이 나올 것이다.

### extends interface
``` ts
interface Person {
  name: string;
  age: number;
}

interface Developer extends Person {
  job: string;
}

const jaegyun: Developer = {
  name: "jaegyun",
  age: 17,
  position: "FE"
};
```

- 여기서 extends는 말 그대로 확장의 의미를 가지며, Person보다 더 넓은 의미로 사용이 가능하다 그래서 Developer타입을 가진 jaegyun같은 경우에 name과 age, position모두 정의가 가능하다.