# Array
## every

### 배열의 모든 요소가 제공된 함수의 조건을 통과하는지 아닌지 true와 false를 반환해주는 메서드

``` js
    const soonhoi = (magae /*매개입니다*/) => magae < 1208;

    const arr1 = [1, 2, 1000, 1207];
    const arr2 = [1, 2, 1000, 1208];

    console.log(arr1.every(soonhoi)); //true
    console.log(arr2.every(soonhoi)); //false
```

- 위 코드는 soonhoi라는 함수에서 매개변수를 받고, 그 매개변수를 1208보다 작는지 비교하는 함수이다.

- arr1.every(soonhoi)는 every로 arr1의 모든 요소를 soonhoi에게 매개변수로 전달하여서 true와 false를 반환한다.

- 그 중 첫번째 console.log는 arr1에 1208보다 작은 요소밖에 없어서 true, arr2는 조건을 만족하지 못해, false를 반환한다.