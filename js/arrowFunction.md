# Arrow Function

```js
const nameArray = ['jaegyun', 'gaon', 'huisung'];

const addString1 = nameArray.map(function (items) {
  return items + ' is the moment';
}); //보기 안좋음

const addString2 = nameArray.map((items) => {
  return items + ' is the moment';
}); //arrow function을 사용해서 깔끔하게 보임

const addString3 = nameArray.map((items) => items + ' is the moment');
//return을 지우고 implicit return을 사용
//
```

### implicit return?

implicit return은 같은 줄에 어떤것을 적든 암시적 반환을 해준다.

하지만 () => {}이런 형식으로 arrow function을 사용한다면 **addString2처럼 return**을 꼭 사용한다.

사용하는 이유? : 코드가 더 깔끔하게 보인다
