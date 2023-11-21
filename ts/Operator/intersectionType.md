# Intersection Type(교차 타입)

- 합집합과 매우 유사한 개념

- 함수 호출을 할 경우에 인자에 명시한 type을 모두 제공, **&** 키워드 사용

``` ts
interface Person {
  name: string;
  age: number;
}

interface Developer {
  name: string;
  job: string;
}

type develoPerson = Person & Developer;

let devPerson: develoPerson = {
  name: "kimjaegyun",
  age: 17,
  job: "FE"
};
```

- 여기서 교차 타입지정으로 &을 사용하여서 develoPerson을 Person과 Developer에 명시되어있는 name, age, job을 모두 작성해야한다.

- 즉, devPerson이 develoPerson이라는 타입으로 명시되어 있으니 name, age, job이 무조건 들어가야 한다는 것이다.