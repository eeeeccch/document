- [Javascript 기초](#javascript-기초)
  - [변수](#변수variables)
  - [자료형](#자료형data-types)
  - [연산자](#연산자operators)
- [DOM 조작과 이벤트 처리](#dom-조작과-이벤트-처리)
- [객체와 배열](#객체와-배열)
- [비동기](#비동기)


## Javascript 기초
### 변수, 자료형, 연산자
> 변수, 자료형, 연산자는 프로그래밍의 기본적인 구성 요소

#### 변수(Variables)
- `var` 함수 스코프를 가지며, 재선언이 가능
- `let` 블록 스코프를 가지며, 재선언이 불가능하지만 재할당이 가능
- `const` 블록 스코프를 가지며, 재선언 및 재할당이 불가능

```javascript
var x = 10;
let y = 20;
const z = 30;
```

#### 자료형(Data Types)
> 자바스크립트의 자료형은 크게 두 가지로 나뉨

##### 원시 자료형(Primitive Data Types)
- `Number` 숫자 타입
- `String` 문자열 타입
- `Boolean` 참(`true`) 또는 거짓(`false`)
- `null` 값이 없음을 의도적으로 나타내는 타입
- `undefined` 값이 할당되지 않은 변수의 초기 상태
- `Symbol` 고유하고 변경 불가능한 값
- `BigInt` 무제한 자릿수를 제공하는 정수

##### 객체 자료형(Object Data Types)
- `Object` 키-값 쌍의 집합
- `Array` 순서가 있는 리스트
- `Function` 함수
- `Date` 날짜와 시간
- `RegExp` 정규 표현식

#### 연산자(Operators)
> 연산자는 변수나 값에 대한 산술, 할당, 비교, 논리, 문자열등의 연산을 수행

##### 산술 연산자
- `+` 더하기
- `-` 빼기
- `*` 곱하기
- `/` 나누기
- `%` 나머지
- `**` 거듭제곱

##### 할당 연산자
- `=` 할당
- `+=` 더하고 할당

##### 비교 연산자
- `==` 값이 같음
- `===` 값과 타입이 같음
- `!=` 값이 다름
- `!==` 값과 타입이 다름
- `>` 크다
- `<` 작다
- `>=` 크거나 같다
- `<=` 작거나 같다

##### 논리 연산자
- `&&` 논리 AND
- `||` 논리 OR
- `!` 논리 NOT

##### 문자열 연산자
- `+` 문자열 연결

### 조건문
> 조건문은 프로그램이 특정 조건에 따라 다른 동작을 하도록 제어하는 구조
#### if문
> `if`문은 조건이 참일 때만 코드 블록을 실행
```javascript
let x = 10;
if(x >= 10){
  console.log('true');
}
```

#### if ... else문
> `if` ... `else`문은 조건이 참일 때와 거짓일 때 각각 다른 코드 블록을 실행
```javascript
let x = 15;
if(x >= 10){
  console.log('true');
}else{
  console.log('false');
}
```

#### if ... else if ... else 문
> 여러 조건을 검사하고, 각 조건에 따라 다른 블록을 실행
```javascript
let x = 'summer';
if(x == 'spring'){
  console.log('봄');
}else if(x == 'summer'){
  console.log('여름');
}else if(x == 'autumn'){
  console.log('가을');
}else if(x == 'winter'){
  console.log('겨울');
}else{  
  console.log('unknown');
}
```

#### switch문
> `switch`문은 하나의 조건을 여러값과 비교하여, 그 값에 따라 다른 코드 블록을 실행<br>
> `case`문으로 각 조건을 설정하고 `break`문으로 각 블록의 끝을 표시<br>
> 기본적으로 어떤 조건도 만족하지 않을 때 실행될 `default` 블록을 설정할 수 있음
```javascript
let day = 3;
switch (day) {
  case 0:
    console.log('월');
    break;
  case 1:
    console.log('화);
    break;
  case 2:
    console.log('수');
    break;
  case 3:
    console.log('목');
    break;
  case 4:
    console.log('금);
    break;
  case 5:
    console.log('토');
    break;
  case 6:
    console.log('일');
    break;
  default:
    dayName = "잘못된 요일";
}
```
#### 삼항 연산자(Ternary Operator)
> 삼항 연산자는 조건문을 간단히 표현할 때 사용 `조건 ? 참일 때 값 : 거짓일 때 값`형태로 작성

### 반복문
> 반복문은 특정 코드 블록을 여러 번 실행할 때 사용 `for` `while` `do ... while`문이 있음

#### for문
`for`문은 반복 횟수가 정해져 있을 때 주로 사용 `초기화` `조건 검사` `증감 표현식`을 반복 제어
```javascript
for (let i = 0; i < 5; i++){
  console.log(i); //0, 1, 2, 3, 4 출력
}
```
- 초기화 : 반복문이 시작될 때 한번 실행(`let i = 0`)
- 조건 검사 : 각 반복이 시작될때 마다 조건을 검사, 조건이 참이면 코드를 실행하고 거짓이면 반복문을 종료(`i<5`)
- 증감 표현식 : 각 반복문이 끝날때 마다 실행(`i++`)

#### while문
`while`문은 조건이 참인 동안 코드 블록을 반속 실행(반복 횟수가 명확하지 않을때 주로 사용)
```javascript
let i = 0;

while (i < 5) {
  console.log(i); // 0, 1, 2, 3, 4 출력
  i++;
}
```
- 조건 검사 : 각 반복이 시작될 때 조건을 검사, 조건이 참이면 코드를 실행하고 거짓이면 반복문을 종료

#### do ... while문
`do ... while`문은 코드 블록을 먼저 실행한 후 조건을 검사, 따라서 최소 1회 코드 블록은 실행
```javascript
let i = 0;

do {
  console.log(i); // 0, 1, 2, 3, 4 출력
  i++;
} while (i < 5);
```

#### for ... in문
`for ... in`문은 객체의 속성을 반복할 때 사용
```javascript
const person = { name: "git", age: 24, city: "Seoul" };
for (let key in person) {
  console.log(key + ": " + person[key]);
}
// name: git
// age: 24
// city: Seoul
```

#### for ... of문
`for ... of`문은 배열이나 이터러블 객체의 요소를 반복할 때 사용
```javascript
const numbers = [1, 2, 3, 4, 5];

for (let number of numbers) {
  console.log(number); // 1, 2, 3, 4, 5 출력
}
```

#### 반복문 제어
반복문 내에서 `break`와 `continue`키워들ㄹ 사용하여 반복문을 제어할 수 있음

### 함수

## DOM 조작과 이벤트 처리
### DOM(Document Object Model) 기초
### 이벤트 처리

## 객체와 배열
### 배열과 객체
### 고차 함수

## 비동기
### 콜백 함수
### 프로미스와 async/await
