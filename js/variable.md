# var, const, let

- 오늘은 기초를 복습하고자 var, const, let부터 시작하겠습니다.

- 모두 똑같이 어떤식으로 사용하는지 알겠지만

``` js
    var name = "gimjaegyun";
    const name2 = "gimjueun";
    let name3 = "banggaon";
```
- 이런식으로 선언 할 수 있다는것은 js입문자들도 아는 사실이다.
- 오늘 나는 이 var, const, let들의 차이점과 공통점에 대해 서술할 것 이다.

## 일단 var는 함수외부에서 선언되면 전역범위 내부에서 선언되면 함수범위이고, 재선언이 가능하며, 호이스팅이 있습니다.

- **호이스팅** : 변수와 함수 선언이 맨 위로 이동되는 자바스크립트 매커니즘입니다.

- **var의 문제점 : 만약 함수내에서 name이라는 변수를 썼다면 만약 전역변수 name이 선언이 되있다면 뜻밖의 출력결과나, 많은 버그를 발생시킬 수 있습니다.**

``` js
    var hello = "hey hi";

    const blabla = () => {
        var hello = "AnNyeong"
    }
    
    console.log(hello); //AnNyeong 출력
```

# 다음은 let이고, let은 블록범위입니다. 
- 블록범위란 {}안에 존재하는 것이라 생각하면 편하며, 하나의 중괄호 속에서 존재해, 중괄호 안에 있는 것은 모두 블록범위입니다.

``` js
    var hello = "hey hi";

    const blabla = () => {
        var hello = "AnNyeong"
        var name = "jaegyun";
    }
    
    console.log(name); //undifined
```

- 중괄호로 감싸진 블록에서 name을 선언했기 때문에 블록 밖인 공간에서 console을 찍으려 하니 undifined가 나왔습니다.

- var와 let은 업데이트 될 수는 있지만 차이점이 있습니다.

1. var는 범위 내에서 재선언 가능
2. let은 범위 내에서 재선언 불가능

``` js
    var name = "jaegyun";
    name = "jueun"; //가능

    let name2 = "gaon";
    name2 = "huisung"; //불가능
```
하지만

``` js
    let hello = "hey hi";

    const blabla = () => {
        let hello = "AnNyeong"
        console.log(hello); //AnNyeong
    }
    
    console.log(name); //hey hi
```
이건 된다.
- 이유는 서로 다른 범위를 가져, 다른 변수로 인식이 되기 때문이다.

- let의 호이스팅?

- var와 마찬가지로 let은 맨 위로 올라오고 var처럼 선언 이전에 쓰려하면 undifined말고 참조오류가 나올 것 입니다.

## 마지막은 const이고, const도 블록범위입니다.

- const는 재선언, 업데이트도 안됩니다.
- 오직 일정한 상수값만 가질 수 있습니다.

``` js
    const name = "jaegyun";
    name = "jueun"; // 불가능

    const name2 = "gaon";
    const name2 = "huisung"; //불가능
```
- 하지만 개체의 속성은 업데이트가 가능합니다.

``` js
    const name = {
        first: "jaegyun";
        second: "jueun";
    }

    name.second = "gaon"; //가능
```

- const의 호이스팅?
- const도 맨 위로 끌어올려지지만 초기화가 되지는 않습니다.

### 세가지 종합

- var는 전역또는 함수이고, const와 let은 블록이다.

- var는 범위 내에서 업데이트 및 재선언 가능. let은 업데이트 가능, 재선언은 불가능. const는 업데이트와 재선언 불가능

- 세가지 모두 최상위로 호이스팅, 하지만 var만 undifined로 초기화 단, 다른 변수는 초기화 X

- var와 let은 초기화하지 않은 상태에서 선언할 수 있지만, const는 선언 중에 초기화해야한다.