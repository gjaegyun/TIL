# callback

- callback은 사실 코드로 보는게 이해가 잘되서 코드로 설명 해보겠습니다.

``` js
    function sayHello(name, callback) {
        const words = '안녕하세요 내 이름은 ' + name + ' 입니다.';
        callback(words);  
    }

    sayHello("인파", function (name) {
        console.log(name);
    });
```

- 사실 난 이제까지 callback함수가 어떤식으로 흘러가는지 잘 몰랐던것 같아서 다시 한번 조사해본다.

- 위 코드는 sayHello함수에서 name과 callback이라는 두가지 매개변수를 받고, 호출을 할때 name은 인파, callback은 익명함수 function(name)으로 전해줬다.

- 이러면 sayHello에서 words가 name에 맞춰서 변경 될것이고, callback(words)를 불러왔을때 callback부분 익명함수에 words가 전달이 될 것이다.

- 이 흐름이 뭐냐면 처음에 name이 먼저 전달이 되고, words가 바뀐 다음에, callback으로 하나의 함수를 또 호출을 해 하나의 함수가 실행이 되는 것이다.

- 그니까 사실 sayHello안에는 2가지 함수가 존재하는것이다.

- callback(words)를 불렀을 경우에 function(name) { console.log(name) }의 값에 name에 words의 값이 담기게 되고, console.log로 words의 값이 출력이 되는 것이다!!!