# 2.0 Your First JS Project
## MAC에서 파일 만들기.
터미널에 다음을 복사 및 붙여넣기
> $ mkdir 파일명

## HTML파일과 JS파일 연결하기
```html
<body>
    <script src="app.js"></script> //app은 자바스크립트 파일명.
</body>
```

---

# 2.1 기본적인 데이터 타입

## Number
- **정수 (Integer)**: `1`, `2`, `3`, `4` ...
- **실수 (Float)**: `1.555`, `2.545345` ...

## String
- 문자열은 **처음부터 끝까지 문자(Text)로 구성**되어 있다.
- 큰따옴표(`" "`) 또는 작은따옴표(`' '`)로 감싸서 표현한다.

```js
"Hello," + " My name is Nico"
// 출력: Hello, My name is Nico
```

👉 문자열끼리 `+` 연산을 하면 두 문자열을 **이어 붙여(concatenate)** 출력한다.

---

# 2.2 변수

## 선언
```js
const 변수 = 데이터;
```
const는 변수 앞에 붙어 해당 변수나 값이 변경되지 않음을 나타내는 키워드이다.

## 변수 이름 짓기
단어가 여러개인 변수를 지을 때애는, 두번째 단어부터 앞글자를 대문자로. -> Camelcase

> ex) myName, veryLongVariableName

---

# 2.3 let

## 재할당
const는 한번 값을 주면 재할당 불가능.
재할당을 하고싶으면, let을 써야함.

```js
const name = "sj";
name = "ksj"; ❌

console.log(name);
```

```js
let name = "sj";
name = "ksj"; ✅

console.log(name);
```

## var
재할당, 재선언 가능.
```js
var name = "sj";
var name = "ksj"; ✅
name = "kkssjj"l ✅

console.log(name);
```
let과 const가 없었을때 쓰던 선언방식.(구버전)

> 저자는 새로운 방식(let,const)을 선호함.

---

# 2.4 booleans

## true // false
```js
let a = true; // 참
let b = false // 거짓
```

## null // undefined
```js
let a = null;
let b = undefined;
```

null -> 값이 없음을 알리기 위해 의도적으로 채운값.
undefined -> 변수선언은 됐는데, 값이 없음.

# 2.5 Array

## 선언
[]으로 감싸고, ','로 데이터 구분.
```js
const a = "a";
const b = "b";
const c = "c";
const d = "d";
const e = "e"; 
// 이런식으로 하면 귀찮고 비효율적.

const alphabet = ['a','b','c','d','e'];
```

## Array 다루기
### 특정값 꺼내기
Array 변수명 뒤에 [0],[1].. 을 붙여서 데이터를 꺼내올 수 있음.

```js
const alphabet = ['a','b','c','d','e'];

console.log(alphabet[0]);
```
### 특정값 바꾸기
변수[index] = 데이터;
```js
alphabet[0] = 'aa';
```

### 값 추가
변수.push(데이터);

```js
alphabet.push('f');
```

---

# 2.6 Objects
어쩐 객체의 값을 의미와 함께 저장하고 싶을 때 사용.

```javascript
const player = ["nico",1212,false,"little bit"];
```
이것도 나쁘지 않지만, 각 값의 의미를 알기 힘듦.

만약 object를 사용한다면.
```javascript
const player = {
    name: "nico",
    points: 1212,
    handsome: false,
    fat: "little bit"
};
```
이런식으로 데이터를 저장 가능.

## 데이터 출력
```javascript
console.log(player.name);
console.log(player["name"];
```

## 데이터 추가
```javascript
const player = {
    name : tomato,
    color : red,
    food : true
};

player.koreanName = "토마토";
console.log(player.koreanName);
```
---
# 2.7~2.8 Functions
함수는 다음과 같이 선언된다.
```javascript
function 함수명(){
    코드;
```

함수는 다음과 같이 실행된다.
```javascript
함수명();
```

다음은 예시이다.
```javascript
function sayHello1(){
    console.log("Hello!");
}

sayHello1();

function sayHello2(a){
    console.log("Hello!",a);
}

sayHello2("nico");
``` 

객체 안에도 함수를 넣을 수 있다.
```javascript
const player ={
    name: "nico",
    sayHello: function(name){
        console.log("Hello",name + "!");
    },
};

player.sayHello(player.name);
```
---
