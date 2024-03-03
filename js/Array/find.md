# Array
## find

### 배열에서 조건을 만족하는 첫번째 요소를 반환해주는 메서드
### 조건을 만족하면 해당 요소, 찾지 못하면 undefined를 반환

``` js
    const birth = [1, 2, 0, 8];

    const oddNumber = birth.find((number) => {
        return number % 2 !== 0;
    })

    console.log(oddNumber);
    // 출력 : 1
```

``` js
    const birth = [1, 2, 0, 8];

    const bigNumber = birth.find((number) => {
        return number > 100;
    })

    console.log(bigNumber);
    // 출력 : undefined
```