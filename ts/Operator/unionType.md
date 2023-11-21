# Union Type
- 한개 이상의 type을 선언할 때 사용을 한다.
- or 비슷한 개념으로 보면 편하다. 사용 키워드는 **|** 이다.

``` ts
function strOrNum (value: string | number) {
  if(typeof value === 'string') {
    value.toString();
  } else if(typeof value === 'number') {
    value.toLocaleString();
  } else {
    throw new TypeError('문자열 또는 숫자를 넣어주세요!');
  }
}

strOrNum('kimjaegyun');
strOrNum(1208);
```

- 이 코드는 strOfNum이라는 함수가 string이나 number을 받고 그에따른 결과가 다르게 나오며, 다르게 타입을 받았을 경우에 else문이 나오는 코드이다.

- 새롭게 알게된 부분으로는 **throw new TypeError**이다.

- throw는 js에서 예외 강제발생 키워드이다. 즉 발생시 프로그램의 흐름중단, 예외 발생을 강제로 해버린다.

- new TypeError()는 js에서 제공하는 내장객체 중 하나로 타입 관련 오류를 나타낼때 주로 쓴다.

- 즉, else문이 발동 했을때 강제로 throw new TypeError부분을 발생시켜서 코드의 흐름을 끊고 메시지를 보여주는 것이다.