# Nullish ??

- nullish 병합연산자는 값이 null or undifined일때 사용할 수 있는 편리한 연산자 기능입니다.

- nullish 병합연산자는 피연산자에서 **값이 할당**된 변수를 찾을 수 있습니다.

- 이렇게만 보면 || 연산자와 다를바 없다고 생각할 수 있지만 차이점으로는
  - ||은 첫 번째 truthy 값을 반환합니다.
  - ??은 첫 번째 정의된 값을 반환합니다.

```js
const money = 0;

console.log(money || 10000); //10000
console.log(money ?? 10000); //0
```

이렇게 된 이유는 ||은 0을 falsy한 값으로 받아들여서 10000을 출력하고, ??은 nullish한 값을 찾아내는 것이기 때문에 첫 번째 정의된 값인 0을 반환합니다.

- 연산자 순위

??의 연산자 우선순위는 5로 낮습니다.
그렇게 때문에 괄호()를 써주는 것이 좋습니다.

```js
const money = null;
const myAccount = undefined;

//best
const myMoney = (money ?? 10000) * (myAccount ?? 0);

//worst
const myMoney = money ?? 10000 * myAccount ?? 0;
```

만약 괄호()를 쓰지 않고 사용한다면 아래 worst처럼 연산이 될 수도 있습니다.
worst는 보기 편하기 위해 괄호를 써주었지만 best처럼 괄호를 사용하지 않는다면 실제로는 worst처럼 실행이 됩니다.

또, ??는 자바스크립트에서의 제약때문에 ||과 &&를 함께 사용하지 못합니다.
하지만 사용을 하고 싶다면 괄호()를 사용해야합니다.

```js
const myAccount = 1 && 2 ?? 3;
//Uncaught SyntaxError: Unexpected token '??'
```
