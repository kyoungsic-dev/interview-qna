# 프론트엔드 면접 예상 질문과 답변 정리 👨‍💻

## 🙋‍♂️소개

프론트엔드 개발자가 되기 위해 알아야할 필수 내용들을 담고 있습니다.  
HTML, CSS, Javascript, 기타 용어 및 기술 파트로 구성되어 있으며  
해당 파트의 질문들과 답을 용어 설명과 함께 정리하고 있습니다.

### 목차

- [HTML](#HTML)
- [CSS](#CSS)
- [Javascript](#Javascript)
- [React](#React)
- [기타 용어 및 기술](#기타-용어-및-기술)
- [프로젝트 관련 예상 질문](#프로젝트-관련-예상-질문)

_written by [김경식](https://github.com/kyoungsic-dev?tab=repositories/)_

---

## ✨HTML

### 1. !Doctype이란?

> 웹 브라우저는 [쿼크모드(Quirks mode)](#-쿼크모드quirks-mode--오래된-브라우저의-행동-모방하여-렌더링)와 [표준모드(Standard mode)](#-표준모드standard-mode--w3c-표준에-따라-렌더링) 두 가지 렌더링 모드를 가지고 있다.  
> `<!DOCTYPE html>` (문서 형식선언)은 브라우저가 문서를 렌더링 할 때 쿼크모드로 바뀌지 않도록 하는 것이 목적이다. 만약 이를 선언하지 않았을 경우 웹 브라우저는 현재 버전의 엄격한 기준으로 과거 버전의 정상적으로 작성된 태그들을 문법 오류로 간주하는 오류가 생기게 된다. 브라우저는 선언된 Doctype에 따라 렌더링할 모드를 선택하게 되는데 이 과정을 Doctype sniffing 또는 Doctype switching이라고 한다. 브라우저가 출력하고자 하는 문서가 최신이라고 판단하면 표준모드로 렌더링을 하게 되고 예전 문서라고 판단 되면 쿼크모드로 렌더링을 하게 되는데 쿼크모드를 사용한다는 것은 오래된 웹페이지들이 최신 버전의 브라우저에서 렌더링 되도록 함에 목적이 있다.
>
> ###### ✔ 쿼크모드(Quirks mode) : 오래된 브라우저의 행동 모방하여 렌더링
>
> ###### ✔ 표준모드(Standard mode) : W3C 표준에 따라 렌더링

### 2. meta태그란?

> meta태그란 문서를 설명하는 태그를 일컫는다. 해당 문서가 어떤 내용을 담고 있고 문서의 핵심키워드는 무엇이며 누가 만들었는지, 문자셋은 어떤 것을 사용하는지 등의 다양한 정보를 담고 있는 태그이다.
>
> `http-equiv` `name` `content` 세가지의 속성이 있으며 설명은 아래와 같다.
>
> - `http-eqyiv` 속성은 문서에서 초기정보를 나타내는 속성으로 meta 요소에서 정의된 명령사항들을 먼저 실행한 후 페이지를 로딩한다. HTML 문서가 응답 헤더와 함께 웹 서버로부터 웹 브라우저에 전송되었을 때에만 의미를 갖는다. 기본언어(content-language), MIME 타입(content-type), 브라우저호환성설정(X-UA-Compatible), 페이지 리로드(refresh)등을 나타낼 수 있다.
> - `name` 속성값으로는 subject, title, author, keywords 등이 있다.  
>    검색엔진에게 문서의 내용을 요약해 주는 역할을 담당한다고 할 수 있다.
> - `content` meta태그의 정보를 지정해준다.

### 3. 시맨틱태그는 무엇이며 왜 사용하는가?

> HTML 문서의 구조를 설계하는 데에 있어 태그에 의미를 부여하여 문서의 구조 파악이 용이하도록 만든 태그를 말한다.
>
> #### ⚙ 시맨틱태그의 장점
>
> - **문서의 가독성이 높다**  
>   `div`가 과도하게 사용된 문서는 코드 가독성이 떨어져 작업 시 혼란을 야기시킬 수 있지만  
>   시맨틱태그는 이 문제점에서 벗어나 태그명만으로 해당 영역의 역할을 쉽게 파악할 수 있다.
>
> - **[SEO](#-seosearch-engine-optimize--웹사이트가-검색-결과에-더-잘-보이도록-최적화하는-과정) 최적화에 유리**  
>   검색 엔진이 태그의 목적에 부합하게 설계되어 있는 구조의 사이트에서  
>   더욱 빨리 정보를 파악할 수 있어 검색 결과 노출이 유리하다.
>
> - **[웹 접근성](#1-웹-표준은-무엇이며-웹-접근성은-무엇인가) 효율적**  
>   스크린리더와 같은 환경의 사용자에게 사이트 이용성을 향상시킨다.
>
> #### ⚙ 시맨틱태그의 종류
>
> - `<header>` 머리글, 제목, 헤더
> - `<nav>` 네비게이션, 목차, 리스트 등 다른 페이지로의 이동을 위한 링크 공간을 위주로 표현
> - `<aside>` 좌측과 우측 사이드 위치의 공간을 의미하며, 본문 외에 부수적인 내용을 주로 표현하는 태그
> - `<section>` 주제, 카테고리 별로 섹션을 구분하는 용도의 태그로 주로 사용. 같은 테마를 가진 여러개의 콘텐츠의 그룹화
> - `<article>` 기사, 블로그 등 텍스트 위주의 페이지를 구성할때 주로 사용
> - `<footer>` 바닥글, 문서 하단에 들어가는 정보 구분 공간을 표현하는 태그
> - `<address>` 콘텐츠 작성자나 사이트 소유자의 정보등을 부가적으로 담는 기능
> - `<hgroup>` 제목과 관련된 부제목을 묶는 태그
> - `<main>` 문서 \<body\>의 중심 주제, 주요 내용 또는 응용 프로그램의 중심 기능과 직접 관련되거나 확장되는 콘텐츠를 나타낸다.
> - `<details>` 주변 문맥에서 표시된 구절의 관련성 또는 중요성으로 인해 참조 또는 표기 목적으로 표시되거나 강조된 텍스트를 나타낸다.
> - `<figure>` 이미지, 다이어그램, 사진 등 독립적인 컨텐츠 정의 시 사용
> - `<figcaption>` \<figure\> 요소의 설명 캡션(caption) 정의
> - `<mark>` 현재 맥락에 관련이 깊거나 중요한 부분 강조
> - `<time>` 시간의 특정 지점 또는 구간, datetime과 같은 속성을 이용해 알림 같은 기능 구현
> - `<summary>` details 요소에 대한 요약, 캡션 또는 범례를 지정. summary 요소를 클릭하면 상위 details 요소의 상태가 열리고 닫힌다.
>
> ###### ✔ SEO(Search Engine Optimize) : 웹사이트가 검색 결과에 더 잘 보이도록 최적화하는 과정

### 4. 비슷한 기능을 하는 태그 간 차이는?

> - **`ul` `ol`의 차이**  
>   순서가 없는 목록(Unordered list)과 순서가 있는 목록(Ordered list)
> - **`dl` `dt` `dd` 란?**  
>   용어의 정의 목록(Description list)
> - **`strong` `b`와 `em` `i` 차이**  
>   [웹 접근성](#1-웹-표준은-무엇이며-웹-접근성은-무엇인가)으로 접근했을 때에 차이가 존재한다.  
>   단순히 굵고 기울이게(b, i)가 아닌 중요, 강조(strong, em)하는 것에 차이가 있다.

### 5. button 태그의 default type은?

> `button` 태그의 default type은 submit이다.  
> 따라서 submit 기능을 사용하지 않는 `button`이라면 type을 button으로 명시해주는 것이 좋다.  
> 가끔 `input`태그의 type을 button으로 명시하여 사용된 걸 볼 수 있는데 (`<input type="button">`)  
> 그 이유는 HTML4.0 표준부터 `<button>` 태그가 추가 되었기 때문이다.  
> 둘의 기능은 동일하지만 활용성 면에서 차이가 존재한다.  
> `<input>`은 열린 태그이기 때문에 자식 요소를 가질 수 없는 큰 단점을 가지고 있지만  
> `<button>` 태그는 자식 요소를 가질 수 있고 CSS를 활용하여 [가상 요소](#7-가상요소와-가상클래스란) 꾸며주는 것이 가능하다.

### 6. 취소선을 넣고싶을 때 어떤 태그를 사용하는가?

```html
<del>취소선 태그</del>
```

### 7. 밑줄을 넣고싶을 때 어떤 태그를 사용하는가?

```html
<ins>밑줄 태그</ins>
```

### 8. 오픈그래프란(og)?

> 오픈그래프(OG, 오픈 그래프 프로토콜)는 HTML 문서의 [meta정보](#2-meta태그란) 쉽게 표시하기 위해서  
> meta 정보에 해당하는 제목, 설명, 문서의 타입, 대표 URL 등 다양한 요소들에 대해서 사람들이 통일해서  
> 쓸 수 있도록 정의해놓은 프로토콜이며, 페이스북에 의하여 기존의 다양한 meta 데이터 표기 방법을  
> 참조하여 만들어졌다. 대부분의 콘텐츠는 URL로 공유되며 콘텐츠가 표시되는 방식을 관리하기  
> 위해 오픈 그래프 태그(OG TAG)로 웹사이트를 마크업하여 마케팅 효과를 낼 수 있다.

### 9. 모바일에서 손가락으로 확대하는것을 제어하는 방법은?

> `minimum-scale` : 줄일 수 있는 최소 크기를 지정합니다. 0\~10 사이의 값을 가집니다.  
> `maximum-scale` : 늘릴 수 있는 최대 크기를 지정합니다. 0\~10 사이의 값을 가집니다.  
> `user-scalable` : yes 또는 no 값을 가지며 사용자가 화면을 확대/축소 할 수있는지는 지정합니다.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=2.0" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=2.0" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no" />
```

### 10. XML과 XHTML의 차이는 무엇이고 XHTML을 이용한 페이지의 한계점은?

### 11. application/xhtml+xml으로 지정한 페이지에 어떠한 문제가 있는가?

### 12. 다국어가 포함된 페이지는 어떤 방식으로 제공하고 여러 방법에 관해 설명하시오.

### 13. data-속성이란 무엇이고 사용했을 때 이점은 무엇인가?

### 14. 쿠키와 세션, 로컬저장소란?

### 15. Progressive rendering이란?

### 16. HTML templating language를 사용해 본 경험이 있는가?

---

## ✨CSS

### 1. CSS 적용 우선순위

> 1.  `!important`를 붙인 속성
> 2.  태그에 inline으로 작성된 속성
> 3.  #id로 지정한 속성
> 4.  클래스, 가상 클래스로 지정한 속성
> 5.  태그 이름으로 지정한 속성
> 6.  상위 객체에 의해 상속된 속성

### 2. CSS 길이 단위 (절대 길이/상대 길이)

> #### 절대 길이
>
> | 단위 | 이름       | 다음과 동일         |
> | ---- | ---------- | ------------------- |
> | cm   | Centimeter | 1cm = 96px/2.54     |
> | mm   | Millimeter | 1mm = 1/10th of 1cm |
> | Q    | 1/4 mm     | 1Q = 1/40cm         |
> | in   | Inch       | 1in = 2.54cm = 96px |
> | pc   | Picas      | 1pc = 1/6 in        |
> | pt   | Point      | 1pt = 1/72 in       |
> | px   | Pixel      | 1px = 1/96 in       |
>
> #### 상대 길이
>
> | 단위 | 다음과 동일                               |
> | ---- | ----------------------------------------- |
> | em   | 요소의 글꼴 크기                          |
> | ex   | 요소 글꼴의 x-height.                     |
> | ch   | 요소 글꼴의 glyph "0" 의 사전 길이 (너비) |
> | rem  | 루트 요소의 글꼴 크기                     |
> | lh   | 요소의 라인 높이                          |
> | vw   | viewport 너비의 1%                        |
> | vh   | viewport 높이의 1%                        |
> | vmin | viewport wnd 작은 치수의 1%               |
> | vmax | viewport 의 큰 치수의 1%                  |

### 3. CSS로 세모는 어떻게 만드는가?

```css
div {
  width: 0;
  height: 0;
  border-bottom: 50px solid transparent;
  border-top: 50px solid transparent;
  border-left: 50px solid red;
  border-right: 50px solid transparent;
}
```

### 4. CSS Sprite란?

> CSS Sprite란 웹 사이트의 로딩 속도를 빠르게 하기 위한 최적화 기법 중의 하나로  
> 여러개의 이미지를 하나의 이미지로 합쳐서 관리하는 기술을 의미한다.
>
> #### ⚙ CSS Sprite의 장점
>
> - 리소스를 다운로드를 최소화 하여 새롭게 로딩되는 경우에도 이미지 로드 블링킹 현상이 없다.
>
> #### ⚙ CSS Sprite의 단점
>
> - 이미지 용량이 크다면 로딩시 매우 오래 걸릴 수 있다.
> - 사용하고자 하는 이미지의 position을 알아야 하며 이벤트 적용시 번거로움이 있다.

### 5. CSS flex란?

> 웹 페이지의 레이아웃을 구성할 때 사용되는 CSS속성으로 기존 `inline-block` `float` `position`과  
> 같은 속성의 문제점과 한계를 보완한 속성이다.  
> flexible box, flexbox라고도 부르는 flex는 레이아웃 배치 기능에 중점을 두어  
> 고안되었기 때문에 기존 방식보다 훨씬 수월한 레이아웃 배치 작업이 가능하다.

### 6. CSS 전처리기란?

> CSS를 프로그래밍화하여 사용하는 것으로 CSS를 사용할 때 생기는 문제점과 번거로움을 보완한다.
> Mixin, Nesting 등과 같은 기능으로 CSS 구조를 가독성있고 유지보수하기 좋게 한다.  
> LESS, SASS등과 같은 전처리기가 있으며 해당 파일을 컴파일하여 CSS포맷으로 변환한다.

### 7. 가상요소와 가상클래스란?

> - 가상요소란 실제로 존재하지 않는 가상의 요소를 만들어 CSS로 제어하는 것을 말한다.  
>   CSS2에서는 콜론(:)으로 사용할 수 있었지만 CSS3 이후로 이중콜론(::) 사용을 권장한다.  
>   대표적인 가상요소로 ::after ::before가 있다.
> - 가상클래스란 실제로 존재하는 요소에 특정 이벤트나 환경에 맞춰  
>   가상으로 클래스를 줘서 CSS로 제어하는 것을 말한다.  
>   대표적인 가상클래스로 :hover가 있다.

### 8. :root 가상 클래스란?

> 문서 트리의 root 요소를 선택한다. html문서의 root 요소는 `<html>` 요소이므로  
> :root의 명시도가 더 높다는 점을 제외하면 html 선택자와 동일하다.

### 9. 전역 CSS변수 선언하는 방법은?

```css
:root {
  --main-color: hotpink;
  --common-padding: 5px 42px;
}

div {
  color: var(--main-color);
  padding: var(--common-padding);
}
```

### 10. class와 id의 차이점은?

### 11. rest.css 를 사용하는가? 사용한다면 왜 유용한가?

### 12. `float`이 어떻게 동작하는가?

### 13. `z-index`에 대해 설명하시오.

### 14. BFC(Block Formatting Context)에 관해 설명하시오.

### 15. 클리어링(Clearing) 기술에는 어떤 것들이 있으며, 어떨 때 사용하는 것이 적절한가?

### 16. Image Replacement를 사용해야 할 때, 선호하는 기술과 언제 사용하는지를 설명하시오.

### 17. 기능이 제약된 브라우저를 위해서 어떤 방식으로 사이트를 만드는가?

### 18. 시각적으로 보이지 않고 스크린리더에서만 가능하게 하는 방법은?

### 19. 그리드 시스템(Grid system)을 사용한 적이 있다면 어떤 것을 선호하는가?

### 20. CSS Selector가 어떠한 원리로 동작하는지 설명하시오.

### 21. pseudo-elements에 관해서 설명하고 어디에서 사용되는지 설명하시오.

### 22. box model에 관해 설명하고 브라우저에서 어떻게 동작하는지 설명하시오.

### 23. `box-sizing: border-box;`은 무엇이고 사용했을때 이점은 무엇인가?

### 24. `inline`과 `inline-block`의 차이점은 무엇인가?

### 25. CSS에서 'C’는 Cascading을 의미하는데 Cascading에 관해서 설명하시오.

---

## ✨Javascript

### 1. Javascript 호이스팅(Hoisting)이란?

> 인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것을 의미한다.  
> 동기적으로 작성되지 않아도 변수와 함수는 최상위에서 먼저 실행된다.

### 2. var, let, const 차이는?

> - `var`는 변수의 선언과 초기화가 동시에 이루어진다. 별도의 값을 할당하지 않을 시 undefined가 할당 된다.  
>   변수명이 중복되어도 에러메시지가 나오지 않으며 사용하지 않는 걸 권장한다.
> - `let`은 코드 블록 내에서 선언된 변수는 코드 블록 내에서만 유효하여 코드 블록 외부에서는 참조할 수 없다.  
>   즉, [블록 레벨 스코프](#-블록-레벨-스코프--함수-if-while-등-내에서-선언된-변수는-해당-블록-내에서만-유효하며-외부에서는-참조할-수-없다)를 따르며 변수의 선언과 초기화 단계가 분리되어 진행된다.  
>   초기화 이전에 변수에 접근하면 참조 에러가 발생한다.
> - `const`와 `let`의 차이는 `const`는 값을 재할당 하는 것이 불가능하며 재선언 할 수도 없다.  
>   즉, 초기화된 값 이외에 다른 값을 할당하는 것이 불가능하다. 이는 보안에 이점이 있다.
>
> ###### ✔ 블록 레벨 스코프 : {}(함수, if, while 등) 내에서 선언된 변수는 해당 블록 내에서만 유효하며 외부에서는 참조할 수 없다.

### 3. Javascript 파일을 로드 할때 defer, async는 각각 무엇을 나타내는가?

> Javascript는 Parser blocking resource(파서 차단 리소스)이다.  
> 브라우저는 문서를 파싱해 읽다가 script를 만나면 진행하고 있던 파싱을 멈추고 script를  
> 다운로드 > 파싱 > 실행한 후에 다시 문서를 파싱한다.  
> `async`와 `defer` 없이 기본모드로 사용할 경우 script 다운로드/파싱/실행될 때까지  
> 브라우저의 문서(HTML) 파싱이 중단되어 사용자 화면 로드가 지연된다.
>
> - `async` 속성은 문서를 파싱하는 동안 script를 만나면 문서 파싱과 함께 script를 다운로드 하고  
>    다운로드가 완료되는 즉시 script를 실행한다.  
>    파일이 먼저 다운로드 되는 순서로 병렬적으로 실행되기 때문에 동기적으로 실행되어야하는  
>    여러개의 script 파일이 존재할 경우 즉, script가 의존적일 경우에 에러가 생길 수 있다.  
>   `async` 속성은 [DOM](#-domdocument-object-model--문서-객체-모델-html-문서에-접근하기-위한-일종의-인터페이스이다)을 조작하지 않고 script 의존성이 없는 코드에 적합하다.
> - `defer` 속성은 브라우저가 script를 만났을 때 다운로드와 문서 파싱을 동시에 수행하되  
>    script의 실행은 \</html\>를 만났을 때 실행된다.  
>   [DOM](#-domdocument-object-model--문서-객체-모델-html-문서에-접근하기-위한-일종의-인터페이스이다)을 조작해 HTML 의존성이 있을 때 문서가 모두 파싱된 이후에 script가 실행되어야 할 때 적합하다.
>
> ###### ✔ DOM(Document Object Model) : 문서 객체 모델. HTML 문서에 접근하기 위한 일종의 인터페이스이다.

### 4. AJAX란?

> Asynchronous Javascript And Xml(비동기식 자바스크립트와 xml)의 약자이다.  
> 브라우저가 가지고있는 XMLHttpRequest 객체를 이용해서 전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법이며 JavaScript를 사용한 비동기 통신, 클라이언트와 서버간에 XML 데이터를 주고받는 기술이다.

### 5. Javascript 이벤트 전파방지란?

```html
<div id="div_">
  DIV영역
  <p id="p_">
    P영역
    <span id="span_">SPAN영역</span>
  </p>
</div>
```

> 최상위에 있는 `div`태그를 클릭했을 때는 `div`를 클릭한 결과만 나타나지만, 가장 아래에 있는 `span`태그를 클릭할 경우 `p`와 `div`의 클릭 이벤트까지 모두 동작하게 된다. 즉, 이벤트가 전파되는 것이다. 이러한 이벤트 전파를 막기 위해 사용하는 코드는 아래와 같다.

```javascript
// 현재 이벤트의 기본 동작을 중단한다.
event.preventDefault();

// 현재 이벤트가 상위로 전파되지 않도록 중단한다.
event.stopPropagation();

// 현재 이벤트가 상위뿐 아니라 현재 레벨에 걸린 다른 이벤트도 동작하지 않도록 중단한다. (이벤트 중첩 방지)
event.stopImmediatePropagation();

// jQuery를 사용할 때는 preventDefault() stopPropagation()를 사용한 것과 같고,
// jQuery를 사용하지 않을 때는 preventDefault()와 같다
return false;
```

### 6. jQuery attr(), prop()의 차이는?

> `.attr()` 메소드와 `.prop()` 메소드의 차이점을 알기 위해서는 속성(attribute)과 프로퍼티(property)의 차이점을 알아야 한다. 속성(attribute)이란 HTML 요소의 추가적인 정보를 가지고 있는 이름과 값의 한 쌍을 의미한다.  
> \<input\>요소는 checked라는 속성(attribute)을 가지고 있으며, 그 속성값은 “checked"이다.
> 프로퍼티(property)란 속성을 객체화하였을 때의 HTML [DOM](#-domdocument-object-model--문서-객체-모델-html-문서에-접근하기-위한-일종의-인터페이스이다) 트리 내부에서의 값을 가리킨다.  
> 만약 체크박스가 체크되면 checked 프로퍼티 값은 “true"이다.
> 즉, 속성은 HTML 문서에 존재하고 값이 변하지 않으며, 프로퍼티는 HTML [DOM](#-domdocument-object-model--문서-객체-모델-html-문서에-접근하기-위한-일종의-인터페이스이다) 트리에 존재하고 그 값이 변할 수 있다. 예를 들어, 사용자가 HTML 문서에 있는 \<input\>요소를 체크하거나 자바스크립트를 이용해 값을 변경하면, 속성값은 변하지 않지만 프로퍼티의 값은 변하게 되는 것이다.

### 7. 클로저(Closure)란?

> 함수와 [렉시컬 환경](#-렉시컬-환경lexical-environment--block-function-script를-실행하기-앞서-생성되는-스코프-범위-안에-있는-변수화-함수를-프로퍼티로-저장하는-객체이다)의 조합을 말한다.  
> 함수가 생성된 당시의 외부 변수를 기억하고 생성된 이후에도 계속 접근 가능하다.
>
> ###### ✔ 렉시컬 환경(Lexical Environment) : block, function, script를 실행하기 앞서 생성되는 스코프 범위 안에 있는 변수화 함수를 프로퍼티로 저장하는 객체이다.

```javascript
function makeAdder(x) {
  return function (y) {
    return x + y;
  };
}

const add3 = makeAdder(3);
console.log(add3(2)); // 5

const add10 = makeAdder(10);
console.log(add10(5)); // 10
console.log(add3(1)); // 4
```

### 8. Arrow Function(화살표 함수)를 언제, 왜 사용하는가?

> - 화살표 함수는 함수 본연의 기능을 직관적으로 잘 표현한다.
> - 인자값이 하나라면 소괄호 생략이 가능하며 중괄호 안 코드가 `return` 뿐이라면 `return`도 생략이 가능하다.
>
> > ```javascript
> > let add2 = function (x) {
> >   return x + 2;
> > }; // 기존 방식
> >
> > let add2 = (x) => x + 2; // 화살표 함수
> > ```
>
> - 화살표 함수는 내부에서 외부의 `this` 값을 그대로 사용한다.

### 9. event delegation에 관해 설명하시오.

### 10. `this`는 Javascript에서 어떻게 작동하는지 설명허시오.

### 11. `prototype` 기반 상속은 어떻게 하는지 설명하시오.

### 12. AMD와 CommonJS는 무엇이고, 이것들에 대해 어떻게 생각하는가?

### 13. IIFE로 만들기 위해서는 어떻게 해야 하는가?

### 14. `null`과 `undefined` 그리고 `undeclared`의 차이점은?

### 15. 익명함수(anonymous functions)는 주로 어떤 상황에서 사용하는가?

### 16. 당신의 코드를 어떻게 구성하는가?

### 17. 호스트 객체(Host Objects)와 네이티브 객체(Native Objects)의 차이점은?

### 18. .call과 .apply의 차이점은 무엇인가?

### 19. Function.prototype.bind을 설명하시오.

### 20. document.write()는 언제 사용하는가?

### 21. JSON이 어떻게 동작 되는지 설명하시오.

### 22. 내장된 JavaScript 객체를 확장하는 것이 좋지 않은 이유는 무엇인가?

### 23. document load event와 DOMContentLoaded event의 차이점은 무엇인가?

### 24. ==와 ===의 차이점은 무엇인가?

### 25. JavaScript의 "동일출처정책(the same-origin policy)"에 대해서 설명하시오.

### 26. 삼항식(Ternary statement)을 사용하는 이유는 무엇이고, 그것을 표현하기 위한 연산자 단어는 무엇인가?

### 27. `use strict;`은 무엇이고, 사용했을 때 장단점에 관해서 설명하시오.

### 28. 전역 Scope를 사용했을 때 장단점은?

### 29. SPA에서 SEO에 유리하도록 만들기 위한 방법은?

### 30. `callback` 대비 `promise`의 장/단점은 무엇인가?

### 31. JavaScript의 작동방식의 장/단점은 무엇인가?

### 32. JavaScript를 디버깅할 때 사용하는 도구가 있으면 설명하시오.

### 33. mutable object와 immutable object에 관해 설명하시오.

### 34. JavaScript에서 immutable 객체의 예를 드시오.

### 35. event loop이란 무엇인가?

### 36. call stack과 task queue에 관해 설명하시오.

### 37. 함수선언식과 함수표현식의 차이는?

---

## ✨React

### 1. React의 생명 주기(Life cycle)은?

> 컴포넌트는 생성 > 업데이트 > 제거의 생명 주기를 갖고 있다.

---

## ✨기타 용어 및 기술

### 1. 웹 표준과 웹 접근성이란?

> - 웹 표준이란 다양한 브라우저 환경에서 웹 페이지를 동일하게 출력하기 위해 웹 표준화 단체인 W3C가 권고하는 웹사이트를 작성 규정이다.
> - 웹 접근성이란 장애인이나 고령자들이 웹 사이트에서 제공하는 정보를 비장애인과 동등하게 접근하고 이용할 수 있도록 작성하는 방식이다.

### 2. API란?

> API(Application Programming Interface)는 두 소프트웨어의 구성 요소가 서로 통신할 수 있게 하는 메커니즘이다.
> 예를 들어 기상청의 소프트웨어 시스템에는 일일 기상 데이터가 있고 휴대폰의 날씨 앱은 API를 통해 이 시스템과 대화하고 휴대폰에 매일 최신 날씨 정보를 표시한다.

### 3. CDN이란?

> CDN(콘텐츠 전송 네트워크)는 Content Delivery Network의 약자이다.
> 사용자 위치, 콘텐츠 원본 서버, 에지 서버 위치를 기준으로 콘텐츠를 최종 사용자에게 전송할 수 있는 분산 노드로 구성된 네트워크이다. CDN 노드는 CDN 제공업체에 의해 여러 지역에 구축되고 여러 ISP(인터넷 서비스 제공자) 네트워크에 걸쳐 배포될 수 있다. 쉽게 말해 지리적, 물리적으로 떨어져 있는 사용자에게 콘텐츠를 빠르게 제공할 수 있으며 느린 응답속도,다운로딩 타임을 극복할 수 있는 기술이다.
>
> #### ⚙ CDN의 장점
>
> - 웹 브라우저는 도메인당 동시에 다운로드할 수 있는 파일의 개수를 제한하고 있다.
>   일반적으로 동시에 네 개의 파일을 다운로드할 수 있게 하며, 5번째 파일의 다운로드는 먼저 받고 있는
>   파일 중 하나가 완료되기 전엔 시작되지 않는다.
>   그런데 CDN 파일은 다른 도메인에서 호스팅 되고 있다.
>   즉, CDN 서비스를 사용하면 브라우저가 동시에 4개의 추가 파일 다운로드를 할 수 있게 된다.
> - jQuery 같은 경우, 거의 모든 웹 사이트에서 사용된다고 볼 수 있다.
>   자신의 사이트를 방문하는 사용자는 이미 CDN 서비스를 사용하는 다른 사이트에 방문했을 가능성이 크며,
>   그렇다면 파일은 이미 브라우저에 캐시 되어 다시 다운로드할 필요가 없다.
> - 많은 상용 CDN은 대시 보드에서 설정하거나 또는 기본적으로 DDoS 공격을 완화할 수 있다.
>
> #### ⚙ CDN의 단점
>
> - 오프라인으로 작동하지 않으므로 인터넷 연결 없이는 개발할 수 없다.
>   또한 라이브 서버에 배포할 때, 수작업이 필요할 수 있다.
> - 무료 CDN을 사용하면 파일 호출에 자신의 사이트 정보도 함께 전송된다.
>   이게 싫으면 무료 CDN을 사용하면 안된다.
>   또한, JavaScript [라이브러리](#4-프레임워크플러그인라이브러리-차이)에 자신의 사이트 정보를 수집하는 코드가 삽입되어 있을 수도 있다.

### 4. 프레임워크/플러그인/라이브러리 차이는?

> - 프레임워크는 목적에 따라 효율적으로 구조를 짜놓은 개발 방식을 말한다.
>   어플리케이션 개발 시 필수적인 코드, 알고리즘, 데이터베이스 연동같은 기능들을 위해 어느정도의 뼈대(구조)를 제공해주는 것이다.
>   프레임워크의 종류에는 Spring, ReactJS가 있다.
>
> - 라이브러리는 특정 기능에 대한 도구/함수들을 모아둔 집합을 일컫는다.
>   프레임워크와 다르게 Flow에 대한 제어 권한을 사용자가 가지고 있다.
>   개발에서 라이브러리와 모듈은 같은 의미로 볼 수 있다.
>
> - 플러그인은 특정한 하나의 문제를 해결하기 위한 컴포넌트이다.
>   사람들이 자주 사용할만한 기능들을 직접 일일히 구현할 필요 없이
>   필요한 기능들만 그때마다 찾아서 사용할 수 있도록 미리 만들어 놓은 것을 말한다.
>   라이브러리 보다 작은 개념이며 플러그인의 집합을 라이브러리라고 볼 수 있다.

### 5. 크로스브라우징이란?

> 크로스브라우징은 많은 종류의 웹 브라우저에서 웹 사이트가 정상적으로 동작하도록 만드는 방법론 중 하나이다.

### 6. 반응형 웹과 적응형 웹이란?

> - 반응형 웹은 [미디어쿼리](#-미디어쿼리--화면-해상도-기기-방향-등의-조건으로-html-스타일을-전환할-수-있는-css3속성)를 사용하여 하나의 웹 사이트가 다양한 해상도의 사용자 화면에서 유연하게 출력될 수 있도록 작업된 웹 구성 방식이다.
> - 적응형 웹은 서버나 클라이언트 단에서 웹에 접근한 디바이스를 체크하여 그 디바이스에 맞는 최적화된 마크업을 호출하는 방식이다.
>
> ###### ✔ 미디어쿼리 : 화면 해상도, 기기 방향 등의 조건으로 HTML 스타일을 전환할 수 있는 CSS3속성

### 7. npm과 npx란?

> - `npm` (Node Package Manager) 는 [라이브러리](#4-프레임워크플러그인라이브러리-차이)) 설치, 업데이트, 삭제 등을 간단한 명령어로 관리할 수 있도록 도와주는 패키지 매니저이다.
> - `npx` (Node Package eXecute) 는 npm과 달리 설치, 삭제 관리가 목적이 아니라 [라이브러리](#4-프레임워크플러그인라이브러리-차이))를 실행할 수 있게 도와준다.

---

## ✨프로젝트 관련 예상 질문

- 최근에 수행했던 흥미로운 프로젝트는 무엇인가요?
- 사용하는 개발 도구에서 마음에 드는 부분은 무엇인가?
- 프론트엔드 커뮤니티에서 당신에게 영감을 준 사람이 있다면 누기인가?
- IE에서 가장 좋아하는 기능은 무엇인가?
- 어제/이번 주에 무엇을 공부하였는가?
- 코딩을 할 때 당신을 들뜨게 하거나 흥미를 끄는 것들은 무엇인 가?
- 최근에 당신이 경험한 기술적인 문제는 무엇이고 해결한 방법은?
- 웹 애플리케이션이나 사이트를 만들 때 고려해야 할 UI, Security, Performance, SEO, Maintainability에 대해서 설명하시오.
- 선호하는 개발 환경에 대해 자유롭게 이야기 하시오.
- 버전 관리 시스템은 어떤 것들을 사용해보았는가?
- 당신이 웹 페이지를 만들 때의 과정을 설명하시오.
- 점진적 향상법(progressive enhancement)과 우아한 성능저하법(graceful degradation)의 차이는?
- 웹사이트에서 assets/resources를 최적화하는 방법에 관해 설명하시오.
- 브라우저가 한 번에 1개의 도메인에서 내려받는 자원은 몇 개이고 예외에는 어떤 것들이 있는가?
- 페이지 로드 시간을 줄이는 방법은?
- 당신이 프로젝트에 합류했을 때 팀원들은 Tab을 이용하고 당신은 Space를 사용한다면 어떻게 할 것인가?
- 당신이 올해 기술적 책임자가 되었다면 무엇을 먼저 할 것인가?
- 표준의 중요성에 관하여 설명하시오.
- Flash of Unstyled Content에 관해 설명하고 FOUC를 피하기 위해선 어떻게 해야할까?
- ARIA와 screenreader에 대해 설명하고 접근성을 지원하는 웹사이트를 어떻게 만드는지에 대해도 설명하시오
- CSS 애니메이션과 JavaScript 애니메이션의 차이는?
- CORS는 무엇의 약자이고 어떤 문제에 대해서 언급하는 것인가?
- 유닛 테스트와 함수테스트의 차이점은 무엇인가?
- code style linting tool을 사용했을 때 장점은 무엇인가?
- 성능관련 이슈들을 발견하기 위해서 사용하는 방법은 무엇인가?
- 웹사이트 scrolling 성능을 향상시키기 위한 몇가지 방법에 대해 설명하시오.
- 브라우저의 layout, painting, compositing에 대해 설명하시오.
- 웹사이트의 assets을 여러 도메인으로 서빙했을 때 장점은 무엇인가?
- URL로 접속했을 때 어떤 플로우로 화면에 웹사이트가 그려지는지 네트워크 관점에서 설명하시오.
- HTTP와 HTTPS에 대해 설명해주세요.
