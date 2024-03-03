# Array
## splice

### 원본 배열을 수정하여 제거, 추가, 교체를 한다

사용방법으로는

- 첫번째 매개변수 (start) 변경을 시작할 인덱스입니다.

- 두번째 매개변수 (delete) 제거할 요소의 갯수입니다.

- (선택) 세번째 매개변수 (push) 추가할 요소입니다.



1. 제거
``` js
    const arr = [1, 2, 3, 4, 5];

    const remove = arr.splice(2, 2);
    // index 2(3)부터 2개 (3, 4)

    console.log(arr);
    // 출력 : [1, 2, 5]
    console.log(remove);
    // 출력 : [3, 4]
```

2. 추가
``` js
    const birth = [1, 2, 8];

    const add = arr.splice(2, 0, 0);
    // index 2번자리에 0 요소 추가

    console.log(birth);
    // 출력 : [1, 2, 0, 8];
```

3. 교체
``` js
    const birth = [1, 1, 0, 8];

    const shift = arr.splice(1, 1, 2);
    // index 1번자리를 1개 삭제시키고, 2를 추가

    console.log(birth);
    // 출력 : [1, 2, 0, 8];
```