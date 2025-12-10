# Display

## 1. Display 속성
**`display` 속성은 HTML 요소를 어떻게 표시할지를 결정한다.**

HTML 요소마다 기본적으로 가지고 있는 display 속성 값이 다르다.

기본 값이 **`display: block` 이면 Block Level Element**이고 **`display: inline` 이면 Inline Level Element**이다.

### none

- **요소가 보이지 않게 설정한다.**

- **영역도 차지하지 않는다.**

- `visibility: hidden;`은 보이지는 않지만 영역은 차지한다.

**none인 경우**

```
<head>
    <style>
        h2 {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Display</h1>
    <h2>title</h2>
    <h3>none</h3>
</body>
```

![display](img/display_3.png)

**visibility 속성**

```
<head>
    <style>
        h2 {
            visibility: hidden;
        }
    </style>
</head>
<body>
    <h1>Display</h1>
    <h2>title</h2>
    <h3>none</h3>
</body>
```

![display](img/display_4.png)

### block

- **기본적으로 가로 영역을 모두 채운다.**

- 줄바꿈이 된 것처럼 보인다.

- **세로 정렬**로 이루어진다.

- `width`, `height` 속성을 지정할 수 있다.

- ex) `div`, `p`, `h1 ~ h6`

```
<head>
    <style>
        div {
            border: 1px solid grey;
        }
    </style>
</head>
<body>
    <div>content</div>
</body>
```

![block](img/display_1.png)

### inline

- **컨텐츠만큼 영역을 차지한다.**

- 줄바꿈이 되지 않는다.

- `width`, `height`를 지정할 수 없다.

- **가로 정렬**로 이루어진다.

- ex) `span`, `a`

```
<head>
    <style>
        span, a {
            border: 1px solid red;
        }
    </style>
</head>
<body>
    <span>Display</span>
    <a href="#">Velog</a>
</body>
```

![display](img/display_2.png)
### inline-block

- **inline처럼 컨텐츠만큼 영역을 차지하여 가로로 배치되지만 block처럼 내부 속성인 `width`, `height` 등과 같은 값을 변경할 수 있다.**

```
<head>
    <style>
        article > div,
        article > span {
            display: inline-block;
            width: 100px;
            height: 100px;
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <article>
        <div>CSS</div>
        <div>CSS</div>
        <div>CSS</div>
        <span>inline-block</span>
        <span>inline-block</span>
        <span>inline-block</span>
    </article>
</body>
```

![display](img/display_5.png)