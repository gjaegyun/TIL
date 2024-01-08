# For ... Of

``` js
    const exampleArray = ['a', 'b', 'c'];

    const repeatArray = (current, index, array) => console.log(current, index, array);
    // a, 0, ['a', 'b', 'c']
    // b, 1, ['a', 'b', 'c']
    // c, 2, ['a', 'b', 'c']

    exampleArray.forEach(repeatArray); 
```

이런식으로 forEach문에서는 이런식으로 동작한다.

하지만 For Of 같은경우에는

``` js
    const exampleArray = ['a', 'b', 'c'];

    for(const examples of exampleArray) {
        console.log(examples);
        //a
        //b
        //c
    }
```

이런식으로 exampleArray의 요소들을 example이 돌면서 쓸 수 있다고 보면 된다.

이게 forEach와 무슨 차이점이 있냐면 일단 let과 const둘중에 하나로 선언이 가능하다.

또, 내가 b를 찾았을 경우에 뭔가를 하고 싶다면 forEach같은 경우에는 중간에 뭔가를 실행시키지 못한다.