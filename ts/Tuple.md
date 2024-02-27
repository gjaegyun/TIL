# Tuple

Tuple은 배열의 길이가 고정 + 각 요소의 타입이 지정되 있는 배열을 말한다.

``` ts
const arr: [number, string, boolean] = [1208, "김재균", true];

arr.push("김주은"); //error
console.log(arr[5]); //error
```

아래 2줄처럼 array에 김주은이라는 요소를 추가하려 했으나 길이가 고정되있으므로 안되고,

정의되지 않은 인덱스로 접근하려 해서 console.log(arr[5]) 이 문장은 오류가 난다.