# Head Tag

## 1. Head Tag란?

- `<head>` 태그는 **문서정보(메타데이터)** 를 담고 있다.

- **브라우저 화면에 직접적으로 보이지는 않지만 숨은 데이터를 정의하는 태그들이 들어 있다.**

```
<!DOCTYPE html>
<html lang="en">
<head>

</head>
<body>

</body>
</html>
```

- `<body>` 태그는 **문서 안의 정보**를 정의한다.

- `<head>` 태그는 **favicon, 타이틀, SNS에 전송할 때 타이틀, 설명, url, 이미지** 표현한다.

## 2. head 안에 배치할 수 있는 요소

- **`<title>`**

    - 브라우저의 **제목 표시줄이나 페이지 탭에 보이는 문서 제목**을 정의한다.

```
<title>Naver</title>
```

- **`<base>`**

    - 문서 안의 **모든 상대 URL이 사용할 기준 URL을 지정**한다.

```
<base href="/assets/images/">
```

- **`<link>`**

    - 요소는 **현재 문서와 외부 리소스의 관계**를 명시한다.

```
<!-- 파비콘 설정 -->
<link rel="shortcut icon" href="./favicon.ico" />

<!-- Style 시트 연결 -->
<link href="/style.css" rel="stylesheet">
```

- **`<style>`**

    - **스타일 규칙**을 담고 있다.

```
<style>
.title {
    color: blue;
}
</style>
```

- **`<meta>`**

    - 다른 메타 관련 요소로 **나타낼 수 없는 메타 데이터**를 나타낸다.

```
<meta property="og:image"  content="https://example.com/image.jpg">
```

- **`<script>`**

    - **데이터나 자바스크립트 코드를 웹 문서에 포함할 때 사용**한다.

```
<script src="javascript.js"></script>
```
