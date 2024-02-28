# Never

never 타입은 **절대로 발생하지 않는 값을 나타내는 특별한 타입**입니다.

never은 주로 함수나 표현식이 예외를 던지거나 무한루프에 빠져, 반환하지 않을 때 사용합니다.

never 타입은 모든 타입의 서브타입이라서, 모든 타입에 할당 가능하나, never 타입에게는 아무 값도 할당할 수 없습니다.

``` js
    function error(message: string): never {
        throw new Error(message); //반환 X
    }
```

``` js
    function infiniteLoop(): never {
        while (true) {
        //무한루프
        }
    }
```

보통 이러한 경우들에 주로 사용합니다.