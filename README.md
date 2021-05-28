# javascript_curriculum

## javasscript란?

 창시자는 알자. 브렌던 아이크

 자바스크립트(영어: JavaScript)는 객체 기반의 스크립트 프로그래밍 언어이다. 
 이 언어는 웹 브라우저 내에서 주로 사용하며, 다른 응용 프로그램의 내장 객체에도 접근할 수 있는 기능을 가지고 있다.

### javascript 장점

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


### javascript-variable(변수),자료형

 variable의 앞 세 글짜를 따서 var입니다.
 말 그대로 변수란 변하는 수 입니다. 뭐가 변하냐면, 데이터가 변합니다. 데이터는 프로그래밍에서 기본이죠. 
 어떠한 정보든지 다 데이터입니다. 
 데이터를 처리하기 위해서는 데이터를 저장하는 공간이 있어야 합니다. 이 공간은 메모리에 마련됩니다. 컴퓨터를 잘 모르시는 분은 RAM이라고 생각하면 됩니다. (RAM이 커야 좋은 이유를 아시겠죠? 데이터를 저장할 공간이 늘어납니다!) 그 공간이 바로 변수라고 부릅니다.

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

