# enum

enum 키워드는 일종의 default 값을 줄 수 있다

먼저 숫자형 enum으로

``` ts
    enum Name {
        jaegyun, //0
        gaon, //1
        heesung //2
    }

    const myName = Name.jaegyun; //0
```

이렇게 0, 1, 2 이런식으로 늘어나는 모습을 확인할 수 있다.

그 후 문자형 enum으로는

``` ts 
    enum Name {
        jaegyun = "재균",
        gaon = "가온",
        heesung = "희성"
    }

    const myName = Name.jaegyun; //재균
```

이렇게 된다.