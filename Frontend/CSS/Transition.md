# Transition

## 1. Transition 속성

transition은 전환이라는 의미이다.

CSS에서는 속성 값이 변할 때 **더 부드럽게 전환**할 수 있도록 도와준다.

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        /* Transition */
        .box1 {
            transform: translate(10px, 10px);
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/7e471a9a-26c6-47e9-b276-590d86f9a005/image.gif)

**box1에 hover를 했을 때, `width: 200px`과 `height: 200px`이 짠! 하고 등장**

## 2. Transition 함수

- **`transition-property` : 어떤 속성에 트랜지션 효과를 줄 것인지 지정**

- **`transition-duration` : 트랜지션 효과를 몇 초 동안 실행할 것인지 지정**

- **`transition-delay` : 트랜지션 효과를 지정한 초만큼 기다렸다가 실행**

- **`transition-timing-function` : 트랜지션이 시작하면서 끝날 때의 타이밍 => 속도를 지정하는 것**

- **`transition` : 단축 속성 가능**

### Transition-duration

```
<head>
    <style>
        body {
            margin: 0px;
            padding: 0px;
            background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        /* Transition */
        .box1 {
            transform: translate(10px, 10px);
        }
        .box1 {
            transition-property: width, height;
            transition-duration: 2s;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/d99f9b9f-c6f8-4312-b762-cc3da546e3b1/image.gif)

**transition 지속 시간은 2s**

<hr>

### transition-delay

```
<head>
    <style>
        body {
            margin: 0px;
            padding: 0px;
            background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        /* Transition */
        .box1 {
            transform: translate(10px, 10px);
        }
        .box1 {
            transition-property: width, height;
            transition-duration: 2s;
            transition-delay: 1s;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/3e4a7354-b11d-4e5e-b0d1-c356d594a7c4/image.gif)

**transition 하기 전 대기하는 시간은 1s**

<hr>

### Transition-timing-function

**linear**

- 트랜지션의 시작과 끝의 속도가 일정하다.

```
<head>
    <style>
        body {
            margin: 0px;
            padding: 0px;
            background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        /* Transition */
        .box1 {
            transform: translate(10px, 10px);
        }
        .box1 {
            transition-property: width, height;
            transition-duration: 2s;
            transition-delay: 1s;
            transition-timing-function: linear;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/85f6f58f-a4fa-4845-9f1c-4fd27399cc29/image.gif)

**ease-in**

- 천천히 시작했다가 완료될 때 속도가 증가한다.

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        .box1 {
            transform: translate(10px, 10px);
        }
        /* Transition */
        .box1 {
            transition-property: width, height;
            transition-duration: 2s;
            transition-delay: 1s;
            transition-timing-function: ease-in;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/8329dd75-d4c3-4666-803b-f92ff51bf333/image.gif)

**ease-out**

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        .box1 {
            transform: translate(10px, 10px);
        }
        /* Transition */
        .box1 {
            transition-property: width, height;
            transition-duration: 2s;
            transition-delay: 1s;
            transition-timing-function: ease-out;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![transition](https://velog.velcdn.com/images/russee/post/bbfcfdc9-b5c5-4bf6-838f-3eb96423fa63/image.gif)

<hr>

### Transition (단축 속성)

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        .box1 {
            transform: translate(10px, 10px);
        }
        /* Transition */
        .box1 {
            transition: width 2s;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![](https://velog.velcdn.com/images/russee/post/bf36c2ef-75ef-45d1-b367-7677cacd5108/image.gif)

- **`transition: 2s;`로 작성하면 default 값인 `all`이 적용된다.**

- `transition: 2s;`에서 `2s`는 **transition-duration**

- `transition: 2s 1s;`에서 `1s`는 **transition-delay**

- `transition: 2s 1s ease-out;`에서 `ease-out`은 **transition-timing-function**

### 그 외

**hover할 때, 색 변화를 주고자 하면**

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        .box1 {
            transform: translate(10px, 10px);
        }
        /* Transition */
        .box1 {
            transition-property: all;
            transition-duration: 2s;
            transition-delay: 1s;
            transition-timing-function: ease-out;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![](https://velog.velcdn.com/images/russee/post/3e88fa7d-8f89-416f-95f4-fc2651cc2467/image.gif)

> `transition-property`를 하나하나 작성하지 않아도 `all` 속성 사용하면 됨.

<hr>

**hover할 때, rotate를 주고자 하면**

```
<head>
    <style>
        body {
        margin: 0px;
        padding: 0px;
        background-color: lightgrey;
        }
        .outline,
        .box {
            width: 60px;
            height: 60px;
        }
        .outline {
            border: 3px solid yellow;
            margin: 0 auto;
            margin-top: 20px;
        }
        .box {
            background-color: blue;
        }
        .box1 {
            transform: translate(10px, 10px);
        }
        /* Transition */
        .box1 {
            transition-property: all;
            transition-duration: 2s;
            transition-delay: 1s;
            transition-timing-function: ease-out;
        }
        .box1:hover {
            width: 200px;
            height: 200px;
            background-color: red;
            transform: rotate(180deg);
        }
    </style>
</head>
<body>
    <div class="outline">
        <div class="box box1"></div>
    </div>
    <div class="outline">
        <div class="box box2"></div>
    </div>
    <div class="outline">
        <div class="box box3"></div>
    </div>
    <div class="outline">
        <div class="box box4"></div>
    </div>
</body>
```

![](https://velog.velcdn.com/images/russee/post/91a86f71-d04a-41d2-874b-89f2637e3c95/image.gif)