# Array
## findIndex

### find와 비슷하게 첫번째 요소를 찾지만 요소의 **인덱스**를 찾아주는 메서드
### 조건을 만족하면 첫번째 요소의 **인덱스** 없을 경우 -1 반환

``` js
    const birth = [1, 2, 0, 8];

    const oddNumber = birth.findIndex((number) => {
        return number % 2 !== 0;
    })

    console.log(oddNumber);
    // 출력 : 0
```

``` js
    const birth = [1, 2, 0, 8];

    const bigNumber = birth.findIndex((number) => {
        return number > 100;
    })

    console.log(bigNumber);
    // 출력 : -1
```