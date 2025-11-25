# Emmet

## Emmet이란?

- Emmet은 HTML과 CSS의 자동완성 기능을 제공하여, 작성 시간을 아주 빠르게 단축시켜 주는 확장 기능이다.

## HTML Emmet

### HTML 표준 구조 `!`

- `! 입력 후 Tab키` : 간단하고 빠르게 HTML 기본구조를 만들어준다.

    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
  
    </body>
    </html>
    ```

### 자식노드 `>`

- `div>ul>li 입력 후 Tab키` : `>` 를 사용하여 자식 요소를 생성할 수 있다.

    ```
    <div>
        <ul>
            <li></li>
        </ul>
    </div>
    ```

### 형제노드 `+`

- `div>ul+ol+div 입력 후 Tab키` : `+` 를 사용하여 한 요소와 같은 단계에 위치한 요소를 생성할 수 있다.

    ```
    <div>
        <ul></ul>
        <ol></ol>
        <div></div>
    </div>
    ```

### 반복하기 `*`

- `div>ul>li*3 입력 후 Tab키` : `*` 를 사용하여 요소를 반복해서 생성할 수 있다.

    ```
    <div>
        <ul>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>
    ```

### 클래스 부여 `.`

- `div.title 입력 후 Tab키` : CSS 클래스를 갖을 요소를 생성할 수 있다. (기본이 div이기 때문에 생략 가능)

    ```
    <div class="title"></div>
    <span class="title"></span>
    ```

### 아이디 `#`

- `#item 입력 후 Tab키` : id를 갖는 요소를 생성할 수 있다. (기본이 div이기 때문에 생략 가능)

    ```
    <div id="item"></div>
    <span id="item"></span>
    ```

### 텍스트 입력 `{}`

- `p.container{Hello World~!} 입력 후 Tab키` : `{}` 를 사용하여 요소 안에 내용을 갖는 요소를 생성한다.

    ```
    <p class="container">Hello World~!</p>
    ```

### 자동 넘버링 부여 `$`

- `p.container{item$}*5 입력 후 Tab키` : `$` 를 사용하여 넘버링을 부여한다.

    ```
    <p class="container">item1</p>
    <p class="container">item2</p>
    <p class="container">item3</p>
    <p class="container">item4</p>
    <p class="container">item5</p>
    ```

## CSS Emmet

### width, height

- `.item{h100+w100} 입력 후 Tab키` : width, height를 지정할 수 있다.

- 기본값은 px단위이며 단위를 교체하는 것도 가능하다.

    - 기본값 -> px

    - p -> %

    - e -> em

    - x -> ex

    - r -> rem