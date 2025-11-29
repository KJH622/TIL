# Inline VS Block Element

모든 HTML 태그들은 각 태그의 용도에 따라서 default display value를 가진다.

Default display value는 **Block-level Elements**와 **Inline-level Elements**로 나뉜다.

- **`<div>`**

    - **분할**을 의미하고 이는 큰 단위를 묶어주는 컨테이너 같은 역할을 한다.

- **`<span>`**

    - **여러 개의 태그들을 묶어주는 주머니 역할**을 한다.

    - 즉, 특정 아이템을 꾸미는 역할이다.

## 1. Block Element

블록 레벨 요소는 부모 요소의 **전체 공간을 차지하여 블록을 만든다.**

ex) `<h1> ~ <h6>` , `<ol>` , `<ul>` , `<li>` , `<p>`

- **화면 구성이나 레이아웃을 짤 때는 블록 레벨 요소를 사용한다.**

- 블록 레벨 요소는 **한 칸을 모두 차지하기 때문에 세로로 나열된다.**

- `width`, `height`, `margin` 속성이 적용된다.

## 2. Inline Element

인라인 레벨 요소는 요소를 구성하는 태그에 **할당된 공간만 차지**한다.

ex) `<a>` , `<em>` , `<img>` , `<span>`

- 인라인 레벨 요소는 **콘텐츠 영역만큼 차지하기 때문에 가로로 나열된다.**

- `margin-top` , `margin-bottom` 적용되지 않는다.

    - 대신 `line-height` 이용 가능하다.
    
- `width`, `height` 속성이 적용되지 않는다.

![인라인 블록 요소](/Frontend/HTML/img/inline_block_elements.png)

- 빨간색 : `div` 태그 -> 세로 정렬

- 노란색 : `span` 태그 -> 가로 정렬

## 3. CSS Display 속성

CSS의 display 속성은 요소가 **화면에 어떻게 표시되는지 설정**하는 역할을 한다.

```
/* 블록 요소인 div를 인라인 요소로 변경 */
div {
    display: inline;
}
```

### 속성값

- **none** : 보이지 않음

- **block** : block 요소로 표시

- **inline** : inline 요소로 표시

- **inline-block** : block과 inline의 중간 형태로 요소는 inline인데 내부는 block처럼 표시

- **flex** : Layout을 만들 때 자주 사용하는 값