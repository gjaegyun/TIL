# Array
## Array.From

### 유사 배열을 배열로 만들어주는 메서드

``` js
    console.log(Array.from('jaegyun'));
    // ["j", "a", "e", "g", "y", "u", "n"]

    console.log(Array.from([1, 2, 3], (x) => x + x));
    // [2, 4, 6]
```

위 예시처럼 첫 번째는 jaegyun을 from에 넣어서 배열을 반환해주고, 

두번째는 배열을 넣고, 순회할 함수를 넣어, 배열을 순회하여 함수의 식을 수행해, [2, 4, 6]이 나오게 됩니다.