# function

``` ts
    function hello(name: string) {
        return `Hello, ${name || "world"}`
    }

    const result = hello();
```

- 여기서 result = hello();의 코드는 오류가 나는데 이유는, 물론 전달 받은 string이 없을때를 대비하여 || "world"를 적었지만 보다 더 명시적으로 표현해줘야 하기 때문에

- name뒤에 ?를 붙여서 string이 포함될수도 있고 안될수도 있는 상태로 만들어 name?: string이런식으로 써주면 오류가 해결된다.

- typescript는 보다 더 정확히 써줘야 한다.