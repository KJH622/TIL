# 기본 문법 배우기_5

## 상수 만들기

let 외에도 변수를 선언하는 예약어에는 `const`와 `var`이 있다.

### const

상수(constant)의 줄임말이다.

> **변수와 상수**
>
> - 변수 : 변하는 수
>
> - 상수 : 변하지 않는 수
>
> 엄밀히 말해 `const`는 어떠한 경우는 변할 수 있는 수이기 때문에 상수는 아니다.

**<예시>**

```
let string1 = '엄청 긴 문자열이다.';
```

`string1` 변수가 나중에 실수로 수정되는 것을 방지하기 위해 `const`로 바꿔줄 수 있다.

```
const string1 = '엄청 긴 문자열이다.';
```

const로 변경하면 `string`이 수정되지 않음이 보장된다.

**즉, let은 초기화 후 다른 값으로 변경이 가능하지만, const는 상수이기 때문에 초기화 후 다른 것을 대입할 수 없다.**

**const는 반드시 초기화를 해야한다.**

### var

var(variable)의 줄임말이다.

과거에는 많이 사용하였지만 최근에는 사용하지 않는 추세이다.

변수문 : `var`로 변수를 선언한 것

```
var variable = '다시 선언할 수 있다'; // undefined
variable; // '다시 선언할 수 있다'
```

선언 시 초기화하지 않으면 값에 `undefined`가 대입된다. 

그러나 이전에 선언했던 variable 변수를 다시 선언해도 에러가 발생하지 않는다.

예약어를 변수명으로 사용할 수 있다.

```
let variable = '다시 선언할 수 없다.'; let variable = '다시 선언할 수 없다.';
// SyntaxError:

var variable = '다시 선언할 수 있다.'; var variable = '다시 선언할 수 있다.';
// undefined

var undefined = 'defined'; // undefined
```

