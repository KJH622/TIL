# 기본 문법 배우기_3

## 불 값

컴퓨터는 실제로 1과 0만 안다.

1과 0은 참(true)과 거짓(false)에 대응된다.

자바스크립트에도 true와 false를 나타내는 불 값(boolean)이라는 자료형이 있다.

### 불 값 표현하기

불 값을 표현할 때는 따옴표로 감싸지 않고 `true`와 `false`를 입력한다.

```
true; // true
false; // false
```

### typeof

```
typeof true; // "boolean"
```

### 비교 연산자 사용하기

참과 거짓은 논리식의 결과값으로 주로 사용한다.

```
5 > 3; // true
5 < 3; // false

5 >= 5; // true
5 <= 4; // false
```

`==`는 '같다'는 의미이고, `!=`는 '다르다'는 의미이다.

> **NaN끼리 비교하기**
>
> 값 중에서 Nan을 비교할 때 독특한 성질을 띈다. 바로 NaN끼리 비교할 때 false 값을 가진다는 것이다.
> ```
> NaN == NaN; // false
> Nan != Nan; // true
> ```

### 불 값끼리 비교하기

true는 숫자로 변환하면 1이고, false는 숫자로 변환하면 0이다.

```
true > false; // true
true < false; // false
```

### 문자열끼리 비교하기

사전 순이라고 생각하면 된다.

a는 97이고, b는 98이고, ... 쭉 이렇게 증가한다.

```
'b' > 'a'; // true (98 > 97)
'ad' > 'ab'; // true
'ab' > 'a'; // true
```

> **문자의 번호 알아보기**
>
> 번호를 알아보려면 `charCodeAt()`을 사용한다. 
>
> ```
> 'a'.charCodeAt(); // 97
> '&'.charCodeAt(); // 65286
> ```

### 다른 자료형끼리 비교하기

다른 자료형이 모두 숫자로 형 변환된 후 비교한다.

```
'3' < 5; // true
'abc' < 5; // false
// 왜냐하면 NaN과의 비교는 false이기 때문이다.
'0' < true; // true
```

### ==와 === 차이 이해하기

`==`를 사용하면 형 변환이 되어서 비교를 하게 된다.

그러나 `===`는 자료형까지 같은지 비교하는 연산자이다.

`!=`도 마찬가지로 형 변환 되어서 비교하는 것이기 때문에 `!==`를 이용하면 자료형까지 같은지 비교할 수 있다.

```
'1' == 1; // true
1 == true; // true

'1' === 1; // false
1 === true; // false
```

## 논리 연산자

'그리고'라는 것을 표현해주는 연산자는 `&&`이다.

```
10 > 5 && 6 < 8; // true
```

'또는'은 `||` 연산자로 표현한다.

```
10 < 5 || 6 < 8; // true
10 < 5 || 6 > 8; // false
```

참을 거짓으로, 거짓을 참으로 만들어주는 연산자가 있다. `!` 연산자이다.

```
!true; // false
!false; // true
```

`!!`는 두 번 연달아 썼기 때문에 참에서 거짓으로, 다시 거짓에서 참으로 변환된다.

```
!!false; // false
!!''; // false
!!0; // false
!!NaN; // false
```

### false로 취급 (반드시 암기)

**false, ''(빈 문자열), 0, NaN, undefined, null**

위와 같은 false인 것을 제외하면 모두 true이다.

## 빈 값 사용하기

### undefined

`console.log`로 출력하면 항상 부수적으로 undefined가 식의 결괏값으로 반환된다.

```
console.log('Hello, world!');
// Hello, world!
// < undefined
```

undefined는 보통 반환할 결괏값이 없을 때 나온다. console.log 명령어는 콘솔에 무언가를 출력하지만, 그 자체로는 결괏값이 없기 때문에 undefined가 반환된다.

```
typeof undefined; // "undefined"
```

undefined는 불 값으로 형 변환했을 때 false가 나온다.

```
!!undefined; // false
```

undefined와 false는 다르다.

```
undefined == false; // false
undefined == 0; // false
undefined == ''; // false
```

### null

```
undefined == null; // true
undefined === null; // false
```

null도 불 값으로 형 변환할 때 false가 된다.

```
!!null; // false
```

null과 false는 다르다.

```
null == false; // false
null == 0; // false
null == ''; // false
```

`typeof`를 할 때 특이하다.

```
typeof null; // "object"
```

위 현상은 자바스크립트에서 유명한 버그이다. 원래는 "null"이 나와야 하지만 초창기 실수로 인해 "object"가 되었다. 그 이후로는 바꿀 수 없게 되었다.

따라서 값이 null인지 확인하기 위해서는 `=== null`을 사용해야 한다.