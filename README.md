# javascript_curriculum

## javasscript란?

 > 창시자는 알자. 브렌던 아이크

 자바스크립트(영어: JavaScript)는 객체 기반의 스크립트 프로그래밍 언어이다. 

 이 언어는 웹 브라우저 내에서 주로 사용하며, 다른 응용 프로그램의 내장 객체에도 접근할 수 있는 기능을 가지고 있다.

## javascript 장점

 1.  절차형, 객체지향형, 함수형 언어를 모두 아우를 수 있습니다.
 2.  한 언어로 여러가지 프로그래밍 기법을 배울 수 있는거죠.
 3.  웹에 정보가 제일 많습니다. 궁금할 때 도움을 줄 사람이 많습니다.
 4.  텍스트 에디터, IDE 같은 것을 설치할 필요가 없고 인터넷 브라우저만 있으면 됩니다.
 5.  결과를 바로 인터넷 브라우저 화면으로 볼 수 있어 편합니다.

 * [변수(Variable)](#javascript-variable) 
 * [객체(Object)와 배열(Array)](#jacascript-object-array)
 * [함수(Function))](#jacascript-function)
 * [연산자(Operator))](#jacascript-operator)
 * [조건문(condition))](#jacascript-condition)
 * [반복문(loop-while,for,do))](#jacascript-loop-while-for-do)


### 1. javascript-variable(변수),자료형

 variable의 앞 세 글짜를 따서 var입니다.
 말 그대로 변수란 변하는 수 입니다. 뭐가 변하냐면, 데이터가 변합니다. 데이터는 프로그래밍에서 기본이죠. 
 어떠한 정보든지 다 데이터입니다.
 데이터를 처리하기 위해서는 데이터를 저장하는 공간이 있어야 합니다. 이 공간은 메모리에 마련됩니다. 컴퓨터를 잘 모르시는 분은 RAM이라고 생각하면 됩니다. (RAM이 커야 좋은 이유를 아시겠죠? 데이터를 저장할 공간이 늘어납니다!) 
 그 공간이 바로 변수라고 부릅니다.

 데이터에는 여러 종류가 있는데요. 프로그래밍마다 또 종류가 다릅니다. 데이터를 한번 만들어 봅시다.

 ```js
 var a = ''; // 문자열
 var b = 1;  // 숫자
 var c = false; // 불린
 var d = null;  // 널
 var e = undefined; // 언디파인드
 var f = [];    // 배열 
 var g = {};    // 객체
 var h = function(){}; // 함수
 ``` 

 var a는 자바스크립트 엔진(자바스크립트 코드를 해석하는 도구)에게 "야, 이제 데이터 저장공간을 마련해! 이름은 a로 하고!"라고 말하는 겁니다. 이런 것을 변수를 선언한다라고 표현합니다.
 그리고 `var a = '';` 로 a에 ''를 대입합니다. = 으로 대입한다는 것을 표시했는데, 수학에서 말하는 같다`(equal)`라는 뜻이 아닙니다. 
 프로그래밍에서 같다는 ==이고 =는 대입(assign)한다는 뜻입니다. 
 이렇게 변수를 선언하자마자 값을 대입하는 것을 초기화한다고 표현합니다. 

 선언, 대입, 초기화같은 단어는 자주 쓰이니 기억해둡시다.

 변수의 이름을 정할 때는 a,b,c,d,... 말고도 이름을 한국어로 지어도 되고, 중국어, 일본어, 유니코드, 심지어 특수문자($와  _만 가능) 등등 상관없습니다. 하지만 세계적으로는 `영어 대소문자와 $, _만` 사용합니다.
 문장의 마지막을 보면 ;(세미콜론)으로 끝나는데 문장이 끝났다는 것을 컴퓨터에게 알리는 프로그래밍 기호입니다. 아래와 같이 만들었던 변수를 조작할 수 있습니다. 기존의 변수에 저장되어 있던 내용을 변경하는 행위입니다.

 ```js
 var a = 'String'; // a의 이름을 가진 저장공간을 만들고 문자열에 넣습니다.
 a = 'rename';    // a의 이름을 가진 저장공간에 다른 문자열을 넣습니다.
 a;               // 'rename';
 ```

 위와 같이 이름을 사용하면 됩니다. 변수의 이름으로는 a,b,c,d와 같이 의미가 없어 다른 사람이 보기에 무슨 뜻인지 알기 힘든 이름 대신 구체적인 이름을 주로 사용합니다.

 ```js
 var a = 1; // 나쁨 a대충지은 이름
 var number = 1; // 좋음 구체적인 이름
 ```
 저장공간 이름이 아무 의미 없는 a보다 number인게 더 낫겠죠? 숫자가 들어올 것을 예상할 수 있으니까요. 
 짧으면서도 구체적인 이름을 짓도록 합시다. (이게 제일 어려운 것 같습니다)

#### camelCase (카멜케이스)

 ```js
 var evenNumber = 2; // camelCase
 var evenNumberWithoutAndMinus = 4; // 나쁨
 ```
 위의 예제를 보면 even number가 아니라 evenNumber라고 썼습니다. 띄어쓰기를 하지 않는 대신에 두 번째 단어부터 첫 글자를 대문자로 쓴 것을 보실 수 있습니다. 변수 이름에는 띄어쓰기가 들어가면 안 됩니다.

 `camelCase`라고 하는데 낙타 등처럼 구불구불한 모양이라고 해서 camelCase라고 이름지어졌습니다. 자바스크립트는 camelCase로 변수명을 만드는 것이 규칙입니다.
 camelCase 외에도 PascalCase도 있고, snake_case도 있습니다. 하지만 자바스크립트는 camelCase라는 거! 잊지마세요.
 camelCase 규칙을 따르는 것은 좋지만 evenNumberWithoutAndMinus 너무 길고 한 눈에 안 들어옵니다. 너무 길지 않게, 짧으면서도 핵심을 담고 있도록 작명하는 센스가 필요합니다.

 변수 이름 중에는 안 되는 규칙들이 몇 개 있습니다. 일단 숫자로 시작하면 안 되고요. 예약어라고 자바스크립트에서 미리 쓰이는 단어들이 있습니다. for, while, do, if, catch, try, finally, else, import, export, default, break, continue, case, switch, class, function, var, let, const 등등 많습니다. 이걸 다 언제 외우느냐고요? 외울 필요 없습니다. 위에 해당하는 예약어를 쓰면 친절하게 해석기에서 Uncaught SyntaxError: unexpected token [예약어이름] 이렇게 경고창이 뜹니다. 아래 내용을 복사해보세요.

 ```js
 var for = 'a'; // Uncaught SyntaxError: unexpected token
 ```

### 1-1. 자료형

 자바스크립트 자료형에 대해 알아보겠습니다. 그냥 `자바스크립트 자료(data)의 종류(type)`라고 생각하시면 됩니다. 다른 언어를 공부하셨던 분들은 다른 언어들은 변수가 var 대신에 int라거나 float, char, double 등등으로 시작한다는 것을 아실겁니다.

 자바스크립트는 그런 것 없습니다. 그냥 var 하나입니다. var에다가 문자를 넣으면 문자 데이터가 되고, 숫자를 넣으면 숫자 데이터가 됩니다. 편하죠? 근데 이 편함이 나중에 불편함이 되기도 합니다. 이제부터 하나씩 소개하겠습니다.

#### 문자열(String)

 문자열은 데이터에 문자를 저장하는 겁니다.
 ```js
 var string = "string"; // 큰따옴표
 var string2 = 'string' // 작은 따옴표
 var string3 = "'string'" // 작은따옴표가 문자열에 들어있으면 큰따옴표로 감쌉니다.
 var string4 = '"string"' // 반대의 경우
 var string5 = '\'string\'' // 한가지 따옴표만 쓰고 싶을 때는 \로 이스케이핑
 ```
 문자열은 큰따옴표나 작은따옴표 중에 하나를 쓰면 됩니다. 상황에 맞게요. 작은따옴표가 문자열에 포함되어 있으면 큰따옴표로 감싸고요. 반대의 상황은 반대로 하면 됩니다. 그냥 한 가지 따옴표만 쓰고 싶을 경우는 \를 문자열의 따옴표 앞에 붙여 이거는 문자열 안의 따옴표라는 것을 알려주어야합니다. \를 붙이는 행위를 `이스케이핑`이라고 부릅니다.

#### 숫자(Number)

 그냥 숫자를 넣으면 됩니다. 다른 언어처럼 Int, Short, Long, Double 이런 구분이 없습니다. 그냥 아무거나 다 넣으면 됩니다.
 ```js
 var number = 1;
 var float = 5.6;
 ```

#### 불린(Boolean)

 true와 false입니다. 'true'가 아니라 따옴표 없이 true입니다. on/off나 yes/no라고 생각하셔도 됩니다.
 ```js
 var bool = true;
 var bool2 = false;
 ```

#### Undefined / Null

그 다음 Undefined와 Null이 좀 헷갈립니다. 둘 다 빈 값인데 좀 차이가 있습니다.
```js
var bool = true;
var bool2 = false;
```
undefined는 변수를 만들어 놓았는데 아무 값도 집어넣지 않았을 때 자동으로 undefined(말 그대로 정해지지 않음)가 되고요. null은 빈 값을 변수에 의도적으로 넣는겁니다.  아무 것도 안 해도 undefined가 되는데 굳이 왜 null을 넣느냐고요? null은 그냥 넣는게 아니라
```js
var b = 125;
b = null;
b: // null
```
이렇게 기존에 있는 값을 지울 때 사용합니다.