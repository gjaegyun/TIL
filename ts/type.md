# type

- type 키워드는 interface와는 다르게 새로운 타입이 아닌 별칭을 부여하는 것이다.
- extends는 사용불가

## type 별칭 선언 봐보기

``` ts
type StrOrNum = string | number;

const str1: StrOrNum = "kimjaegyun";
const str2: StrOrNum = 1208;
```

- 여기서 StrOrNum의 별칭을 string이나 number로 부여해줬다.
- 그러므로 str: StrOfNum같은 경우에 string과 number type을 동시에 갖고 있다.

## type과 interface

- 가장 큰 차이점 **타입의 확장 가능 vs 불가능이다.**

- interface는 확장이 가능하나 type은 확장이 불가능하다.

- 이말이 뭐냐면 넓은 개념 좁은 개념으로 이해하면 안되고, interface는 type을 늘릴수 있는 것이라고 보면 편하다.