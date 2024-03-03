# Array
## filter

### 특정 조건을 만족하는 모든 요소를 합해 새 배열을 반환
### 만족하는 요소가 없을 시 빈 배열 반환

``` js
    const arr = [1, 2, 3, 4, 5];

    const filter = arr.filter((e) => {
        return e > 2;
    });

    console.log(filter);
```