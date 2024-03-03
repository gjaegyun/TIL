# Array
## some

### 배열 중 조건을 만족하는 요소가 1개 이상이라면 true 아니라면 false를 반환해주는 메서드

``` js
    const array = [1, 2, 3, 4, 5];

    const someArray = array.some((e) => {
        return e < 2;
    })

    console.log(someArray);
    // 출력 : true
```

``` js
    const array = [1, 2, 3, 4, 5];

    const someArray = array.some((e) => {
        return e < 1;
    })

    console.log(someArray);
    // 출력 : false
```