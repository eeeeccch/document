### 예약어
- await
- break
- case
- catch
- class
- const
- continue
- debugger
- default
- delete
- do
- else
- enum
- export
- extends
- false
- finally
- for
- function
- if
- implements
- import
- in
- instanceof
- interface
- let
- new
- null
- package
- private
- protected
- public
- return
- super
- static
- switch
- this
- throw
- true
- try
- typeof
- var
- void
- while
- with
- yield

### 네이밍 컨벤션
```js
// 카멜 케이스 (camelCase)
var FirstName;

// 스네이크 케이스 (camel_case)
var first_name;

// 파스칼 케이스 (PascalCase)
var FirstName;

// 헝가리언 케이스 (typeHungarianCase)
var strFirstName; //type + indentifier
var $elem = document.getElementById('myId') // DOM 노드
var observable$ = fromEvent(document, 'click'); RxJS 옵저버블
```

### 문(staement)
- 실행 가능한 최소의 독립적인 코드 조각

### 표현식(expression)
- 특정한 결괏값으로 계산되는 것

### 리터럴 종류
|리터럴|예시|비고|
|--|--|--|
|정수 리터럴|100||
|부동 소수점 리터럴|10.5||
|문자열 리터럴|'hello world'||
|불리언 리터럴|true<br>fasle||
|null 리터럴|null||
|undefined 리터럴|undefined|
|객체 리터럴|{ name: 'Lee', nick: 'Bug' }||
|배열 리터럴|[0,1,2]||
|함수 리터럴|function() { ... }||
|정규 표현식 리터럴|/[A-Z]+/g||

### 데이터 타입
원시 타입
|구분|데이터 타입|비고|
|--|--|--|
|원시타입|숫자|number|
|원시타입|문자열|string|
|원시타입|불리언|true or false|
|원시타입|undefined|var 키워드로 변수에 암묵적으로 할당되는 값|
|원시타입|null|값이 없다는 것을 의도적으로 명시할때 사용하는 값|
|객체타입|object|객체, 함수, 배열등등|
