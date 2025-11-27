# Inline VS Block Element

- 모든 HTML 태그들은 각 태그의 용도에 따른 default display value(기본 표시 값)를 가진다.

- 이때 default display value는 **블록 레벨 요소(Block-level Elements)** 와 **인라인 레벨 요소(Inline-level Elements)** 두 가지 범주로 나뉜다.

- 예를 들면 `<div>` 태그는 **블록 레벨 요소**이고, `<span>` 태그는 **인라인 레벨 요소**이다.

    - **`<div>`**

        - `<div>` 태그는 Division. 즉, **분할**, 분배, 분류를 의미한다.

        - HTML 안에 존재하는 여러 개의 태그들을 `<div>` 라는 **큰 단위로 묶어주는 컨테이너 같은 역할**을 한다.

    - **`<span>`**

        - `<span>` 태그도 `<div>` 태그와 같이 **여러 개의 태그들을 묶어주는 주머니 역할**을 한다.

        - **특정 아이템을 꾸미는 역할**

## Block Element

- **블록 레벨 요소는 부모 요소의 전체 공간을 차지하여 블록을 만든다.**

- `<h1> ~ <h6>` , `<ol>` , `<ul>` , `<li>` , `<p>` 태그 등이 블록 요소에 속한다.

    - 화면 구성이나 레이아웃을 짤 때는 블록 레벨 요소를 사용한다.

    - 블록 레벨 요소는 **한 칸을 모두 차지하기 때문에 세로로 나열된다.**

    - **width, height, margin 속성이 적용**된다.

    - 가로, 세로 크기 조절 가능

<details>
    <summary><b>블록 레벨 요소 목록</b></summary>
    <div markdown="1">
        <ul>
            <li style="margin-bottom: 10px;"><b><code>address</code></b> - 연락처 정보</li>
            <li style="margin-bottom: 10px;"><b><code>article</code></b> - 단락 콘텐츠</li>
            <li style="margin-bottom: 10px;"><b><code>aside</code></b> - 부가 콘텐츠</li>
            <li style="margin-bottom: 10px;"><b><code>blockquote</code></b> - 긴(블록) 인용구</li>
            <li style="margin-bottom: 10px;"><b><code>details</code></b> - 상세 정보 위젯</li>
            <li style="margin-bottom: 10px;"><b><code>dialog</code></b> - 대화상자</li>
            <li style="margin-bottom: 10px;"><b><code>dd</code></b> - 설명 목록의 정의 설명</li>
            <li style="margin-bottom: 10px;"><b><code>div</code></b> - 문서의 분할</li>
            <li style="margin-bottom: 10px;"><b><code>dl</code></b> - 설명 목록</li>
            <li style="margin-bottom: 10px;"><b><code>dt</code></b> - 설명 목록의 정의</li>
            <li style="margin-bottom: 10px;"><b><code>fieldset</code></b> - 필드 집합의 라벨</li>
            <li style="margin-bottom: 10px;"><b><code>figcaption</code></b> - 그림 설명</li>
            <li style="margin-bottom: 10px;"><b><code>figure</code></b> - 미디어 콘텐츠 그룹과 설명 (<code>figcaption</code> 을 참고)</li>
            <li style="margin-bottom: 10px;"><b><code>footer</code></b> - 페이지나 구역의 푸터</li>
            <li style="margin-bottom: 10px;"><b><code>form</code></b> - 입력 폼</li>
            <li style="margin-bottom: 10px;"><b><code>h1, h2, h3, h4, h5, h6</code></b> - 1 ~ 6 단계 제목</li>
            <li style="margin-bottom: 10px;"><b><code>header</code></b> - 페이지나 구역의 헤더</li>
            <li style="margin-bottom: 10px;"><b><code>hgroup</code></b> - 헤더 정보 그룹</li>
            <li style="margin-bottom: 10px;"><b><code>hr</code></b> - 수평선 (구분선)</li>
            <li style="margin-bottom: 10px;"><b><code>li</code></b> - 목록의 항목</li>
            <li style="margin-bottom: 10px;"><b><code>main</code></b> - 문서에서 하나 뿐인 중심 콘텐츠</li>
            <li style="margin-bottom: 10px;"><b><code>nav</code></b> - 탐색 링크를 포함</li>
            <li style="margin-bottom: 10px;"><b><code>ol</code></b> - 정렬된 목록</li>
            <li style="margin-bottom: 10px;"><b><code>p</code></b> - 문단</li>
            <li style="margin-bottom: 10px;"><b><code>pre</code></b> - 미리 서식 적용한 글</li>
            <li style="margin-bottom: 10px;"><b><code>section</code></b> - 웹 페이지의 구역</li>
            <li style="margin-bottom: 10px;"><b><code>table</code></b> - 표</li>
            <li style="margin-bottom: 10px;"><b><code> ul</code></b> - 정렬되지 않은 목록</li>
        </ul>
    </div>
</details>

## Inline Element

- 인라인 레벨 요소는 콘텐츠의 흐름을 끊지 않고 (줄바꿈 X) **요소를 구성하는 태그에 할당된 공간만 차지**한다.

- `<a>` , `<em>` , `<img>` , `<span>` 태그 등이 인라인 요소에 속한다.

    - **인라인 레벨 요소는 콘텐츠 영역만큼 차지하기 때문에 가로로 나열된다.**

    - **margin-top, margin bottom 적용되지 않는다.**

        대신에 line-height 이용한다.
    
    - **width, height 속성이 적용되지 않는다.**

    - 가로, 세로 크기 조절 불가능

    - 태그가 콘텐츠의 할당된 공간만 갖고 있기 때문에 text-align과 같은 속성은 사용할 수 없다.

<details>
    <summary><b>인라인 요소들</b></summary>
    <div markdown="1">
        <ul>
            <li style="margin-bottom: 10px;"><b><code>a</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>abbr</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>audio</code></b> (컨트롤이 안 보이면)</li>
            <li style="margin-bottom: 10px;"><b><code>b</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>bdo</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>br</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>button</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>canvas</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>cite</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>code</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>data</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>datalist</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>del</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>dfn</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>em</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>embed</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>i</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>iframe</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>img</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>input</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>ins</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>kbd</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>label</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>map</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>mark</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>meter</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>noscript</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>object</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>output</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>progress</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>q</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>ruby</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>s</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>samp</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>script</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>select</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>slot</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>small</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>span</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>strong</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>sub</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>sup</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>svg</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>template</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>textarea</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>time</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>u</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>var</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>video</code></b></li>
            <li style="margin-bottom: 10px;"><b><code>wbr</code></b></li>
        </ul>
    </div>
</details>

## CSS Display 속성

- **CSS의 display 속성은 요소가 어떻게 표시되는지 설정하는 역할을 한다.**

- 위에서 언급했던 것처럼 CSS default display value가 `block` 이면 해당 태그는 블록 요소이고 `inline` 이면 인라인 요소이다.

- display 속성의 값을 변경함으로써 시각적인 표현을 변경할 수 있다.

- 즉, 블록 요소를 인라인 요소 등으로 바꿀 수 있다.

    ```
    /* 블록 요소인 div를 인라인 요소로 변경 */
    div {
        display: inline;
    }
    ```

### 속성 값

- **`none`** : 보이지 않음

- **`block`** : block 요소로 표시

- **`inline`** : inline 요소로 표시

- **`inline-block`** : block과 inline의 중간 형태로 요소는 inline인데 내부는 block처럼 표시함

- **`flex`** : layout을 만들 때 자주 사용하는 값