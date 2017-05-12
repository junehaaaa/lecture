# Content model

## Flow Content
* 쌓이는 구조
* BODY 요소 안에 포함 가능한 모든 요소
* a abbr address area article aside audio b bdi bdo blockquote br button canvas cite code data datalist del details dfn div dl em embed fieldset figure footer form h1 h2 h3 h4 h5 h6 header hr i iframe img input ins kbd keygen label main map mark math menu meter nav noscript object ol output p picture pre progress q ruby s samp script section select small span strong sub sup svg table template textarea time u ul var video wbr

## Metadata Content
* 유저에게 보이지 않지만, 이 문서(Document)에 대한 정보를 컴퓨터(브라우저)에 제공하는 것들
* 거의 대부분이 HEAD 요소 안에서 사용됨
* base link meta noscript script style template title

## Sectioning Content
* heading 요소와 footer 요소의 scope를 나타냄.
* article aside nav section

```html
<h1>Hello World</h1>
<article>
  <h1>Hello World</h1>
  <p>Welcome to HTML World</p>
</article>
<p>Welcome to CSS World</p>
<article>
  <h1>어쩌구 저쩌구</h1>
</article>
```

## HEADING CONTENT
* 제목
* h1 h2 h3 h4 h5 h6
* 순차적 구조
* h1 > h2 > h3 > h4 > h5 > h6

## PHRASING CONTENT
* 텍스트 레벨 콘텐츠 (구 inline)
* a abbr area (if it is a descendant of a map element) audio b bdi bdo br button canvas cite code data datalist del dfn em embed i iframe img input ins kbd keygen label map mark math meter noscript object output picture progress q ruby s samp script select small span strong sub sup svg template textarea time u var video wbr text

## Embedded CONTENT
* 외부에서 긁어오는 요소
* HTML 문법이 아닌 콘텐츠를 가져올 때
* audio canvas embed iframe img math object picture svg video

```html
<svg>
  <g></g>
</svg>
```

## INTERACTIVE
* 유저랑 상호작용하는 콘텐츠
* a (if the href attribute is present) audio (if the controls attribute is present) button details embed iframe img (if the usemap attribute is present) input (if the type attribute is not in the hidden state) keygen label select textarea video (if the controls attribute is present)
* INTERACTIVE의 자식으로 INTERACTIVE를 둘 수 없음

```html
<a href="#">
  <audio src="">
</a>
```

==============

* WAI-ARIA (Web Application)
* Role (역할)

```html
<main> 요소 (Grouping) </main>
<div role="main"> 요소 (Grouping) </div>

<header></header>
<div class="header"></div>

<div class="wrap">
  <div class="header"></div>
  <div class="main" role="main"></div>
  <div class="footer"></div>
</div>

<a role="button">button</a>
<button>BUTTON</button>
```