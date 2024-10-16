# <b> Summary Points 2 </b>

<br>

## HTML CSS 웹폰트 넣는 법과 안티앨리어싱
<br>

### 폰트 패밀리 설정법 
```
body {
  font-family : 'gulim', 'gothic'
}
```
- 버그없이 사용하려면 폰트의 영문명을 사용해야 함.

- 폰트명에 띄어쓰기가 있을 수 있으니 따옴표 안에 담는게 좋음.

- 폰트명을 콤마로 여러개 쓰면 제일 왼쪽에 있는 폰트부터 적용하는데, 실패하면 뒤에 있는 폰트들을 차례로 적용함.

- 웹사이트 이용자의 컴퓨터에 설치가 된 폰트들을 적용할 수 있음.

 

 

 <br>

 

 

### 사용자의 컴퓨터에 설치되지 않은 폰트를 사이트에서 이용하려면 
```
@font-face {
  font-family : '이쁜폰트';
  src : url(nanumsquare.ttf)
}
```
CSS파일 최상단에 @font-face 라는 명령어를 넣고,

url() 안에 적용할 폰트의 경로와 이름을 적어준다.

필자는 css파일과 같은 폴더에 있어서 경로는 그냥 nanumsquare.ttf 라고 적어봤음 

그럼 이제 클래스에서 font-family : '이쁜폰트' 쓰면 nanumsquare.ttf 폰트를 적용해준다.

 

 

 <br>

 

 

### 웹폰트용 woff파일 

 

웹폰트용으로 나온 woff 파일이 있다. ttf에 비해 용량이 3분의1 수준.

한글폰트 ttf 파일은 용량이 매우 크기 때문에 (한글폰트는 특히 몇천자가 들어있기 때문에)

구할 수 있다면 woff 파일을 사용하는걸 추천한다. ttf와 호환성은 거의 비슷한 수준.

어짜피 ttf나 woff 둘다 IE8 이하에선 적용되지 않는다. 자유롭게 woff를 사용하도록 하자.

나눔스퀘어 woff 버전 : https://github.com/moonspam/NanumSquare

 

<br> 

 

 

 

### IE 옛 버전에서도 호환성 좋게 폰트를 사용하려면

 
```
@font-face { 
  font-family: 'NanumSquare'; 
  font-weight: 400; 
  src: url(NanumSquareR.eot); 
  src: url(NanumSquareR.eot?#iefix) format('embedded-opentype'), 
      url(NanumSquareR.woff) format('woff'), 
      url(NanumSquareR.ttf) format('truetype'); 
}
```
eot, woff, ttf 파일들을 구한한 후 이렇게 첨부하면 된다.
 

 

 

 <br>

 

 

### 폰트를 빠르게 사용하기 위한 Google Fonts

 

구글폰트라는 사이트를 이용하면 굳이 폰트파일을 구하지 않아도 된다.

Google Fonts 사이트에서 바로 폰트파일과 CSS 정의부분을 링크할 수 있다.

https://fonts.google.com

 

저 사이트에서 원하는 폰트를 고른 다음 

HTML에 첨부하고 싶다면 \<link>로 시작되는 부분을 복붙하면 되고,

CSS에 첨부하고 싶다면 @import 로 시작되는 부분을 CSS 맨 위에 복붙하면 된다.

구글이 호스팅해주는 폰트가 미리 정의된 CSS 파일을 가져다 쓰는 것이라

내 사이트의 트래픽을 절약할 수 있다는게 장점이고

크롬브라우저는 이미 방문한 사이트는 캐싱해주기 때문에 많은 사람들이 이용할수록 더 빠르게 폰트를 이용할 수 있다. 

 

 

 <br>

 

 

### 폰트 Anti-aliasing 에 대해

 

맥으로 웹개발하면 폰트를 뭘 쓰든 이쁘게 보인다.

심지어 굴림, 돋움 같은 기본 폰트도 앤티앨리어싱이 되어서 부드럽게 나온다. 

앤티앨리어싱이 뭐냐면 그 픽셀의 각진 부분을 스무스하게 바꿔주는건데 


 

맥 OS쓰면 알아서 해주지만 윈도우는 전혀 아님. 

윈도우에서 돋움, 굴림 폰트를 매우 작게 축소하거나 아니면 매우 크게 확대했을 때 매우 각져보인다. 

돋움, 굴림 뿐만 아니라 대부분의 폰트가 저런 현상이 일어난다. 

디자인 잘하는 사람 입장에선 매우 거슬리는 문제인데

이 문제를 해결하고 싶다면 웹상의 글자를 살짝 돌려보면 된다. 

 
```
transform : rotate(0.04deg); 
```
CSS파일에다가 이걸 적용해보자. 

transform은 요소를 살짝 회전시키는 스타일이다. 

글자를 정말 매우 살짝 회전시키면 윈도우에선 안티앨리어싱 된 듯한 느낌을 준다. 부드러워짐 

<br>
<br>

## HTML CSS 코드짤 때 유용한 Emmet 그리고 부가기능들


HTML 창작 능력을 빠르게 도와줄 몇가지 부가기능이 있다.

VS code, Atom 등 다른 에디터를 사용해도

유사한 부가기능이 있을 것이니 찾아보면 된다. 

 

 <br>

 

### 0. 부가기능 설치방법 

 


 

Brackets의 경우 파일 - 확장기능 관리자를 클릭하고,

여기서 원하는 부가기능을 검색 후 설치버튼 누르면 성공. 

(참고) Brackets 부가기능 서버가 가끔 다운되어서 

https://registry.brackets.io/

여기서 직접 찾아서 다운로드해서 저기로 드래그하면 된다다.

 

VScode의 경우 제일 왼쪽 메뉴에서 Extension 버튼 누른 후에 

원하는 부가기능을 검색 후 설치버튼 누르면 성공. 

 

 <br>

 

 

### 1. Beautify 

 

코드를 예쁘게 정렬하고싶을 때 사용하는 부가기능이다.

Brackets의 경우 설치하면 우측에 마법봉이 하나 생기는데 누르면

 



 

얼마나 더럽게 코딩했든 간에 코드를 아주 예쁘게 정렬해준다. 

우클릭 해도 된다.

VScode 에디터는 설치할 필요 없이 그냥 우클릭해서 Format Document 누르면 된다.

 

 

 <br>

 

 

 

### 2. Emmet 

 

아무리 자동완성이 잘 된다고 해도 div박스 여러개 만드는 작업은 매우 귀찮은 작업이다.

그래서 셀렉터를 이용해서 HTML을 조금 쉽게 생성할 수 있는 부가기능이 있다.

일단 Emmet 이라고 검색해서 설치해보자.

VScode는 설치 안해도 요즘은 자동으로 깔려있다. 

 

 div.container>div
이렇게 입력하자마자 tab키를 한번 눌러보면

 

 
```
<div class="container">
  <div></div>
</div>
```
HTML이 생성된다.

훨씬 빠르게 레이아웃을 만들어낼 수 있다.

생각한 HTML 레이아웃을 CSS 셀렉터처럼 작성한 후에 tab키만 누르면 된다.

(> 표시는 내 바로밑의 자식요소라는 뜻이라 저렇게 생성된 것이다.)


 
 

 

 

이런 것도 가능하다.  

 

 div#header>p.title*3
이렇게 쓰고 탭키 누르면

 
```
<div id="header">
  <p class="title"></p>
  <p class="title"></p>
  <p class="title"></p>
</div>
```
p.title 이건 p태그인데 class명이 title이라는 CSS 셀렉터 문법이고

div#header 이건 div태그인데 id명이 header라는 CSS 셀렉터 문법이다.

그렇게 작성하고 tab 누르면 진짜 그렇게 html을 생성해준다.

참고로 *3 이건 3개씩 생성하라는 뜻이다. 

 

 


 

m10
CSS 작성시 m10 이렇게 입력하고 탭키 누르면

 

margin : 10px
자동생성된다. 

mt10 이건 margin-top : 10px 이고

w100% 이건 width : 100% 이다.

더 있는데 창의력만 좋으면 CSS 축약어들을 유추가능하니 직접 실험해보자.

 

 

 

이외에도

! 입력후 tab 누르기 (html 문서 시작템플릿 바로 생성)

 lorem 입력 후 tab 누르기 (임시글자 무작위 생성)

\<p> 이렇게 치는게 아니라 p 입력하고 바로 탭키 눌러서 \<p> 생성하기

이런 것들이 유용하다.

다른 문법들은 구글에 Emmet 이라고 검색하면 된다.

 

 

 <br>

 

 

Q. "저는 초보라서 div가 몇개 있을 지 먼저 생각하기 어려운데여? 안유용한듯"

 

초보면 더욱 더 사용해야한다. 빨리 연습하자.

왜냐면 초보는 

- div가 몇개 필요할지
- 여기 글은 p태그로 쓸지 h1으로 쓸지
- 클래스 명은 뭘로 할지

이런 레이아웃을 머릿속으로 생각해보는 과정이 정말 중요하다.

맨날 div 필요할 때마다 주먹구구식으로 만들지말고 

1. 샘플 디자인 위에 네모박스부터 그려보고 네모박스가 필요한 곳에 div 박스부터 딱딱 배치하고

2. 그리고 class 명도 대충 미리 채워넣고

3. 그 다음에 스타일을 입히는 방식으로 코드짜는게 좋은데

근데 Emmet 문법 연습하다보면 자연스럽게 div와 class 구조를 생각해야되니

자연스럽게 레이아웃 짜는 능력도 상승할 것이다. 

빨리 사용해보도록 하자. 

 

 
<br>
 

 

 

### 3. 테마 

 

컴퓨터의 밝은 화면은 눈건강에 좋지 않다.

어두운 테마를 설치하면 보다 오래 코딩할 수 있는데

테마란에 들어가서 어두운 테마 하나 아무거나 설치해보자.

그리고 메뉴에서 보기 - 테마를 누른 후 테마를 선택하면 된다.

Brackets에서 사용하는 테마 이름은 New One Dark,

VScode도 extension 메뉴에서 설치하면 되는데 필자가 사용하는 테마는 Atom One Dark 이다.

 

 

 
<br>
 

 

 

### 4. Power Mode 부가기능

 

코드를 입력할 때 지진이 일어난다.

스타벅스에서 HTML로 프로그래밍할 때 사용하면 주목받을 수 있다. 

 

 



 

설치랑 셋팅법은 구글 검색을 추천한다. 

VScode, Brackets 둘 다 있음.

 

 

 

 <br>

 

 

### 5. Color Hints

 



 

색상넣는 자리에 # 까지만 입력하면 내가 위에서 사용했던 색상 힌트를 보여준다.

맨날 색상코드 복사하러다니는 분들에게 매우 유용하다. 

 

 

 

 

 

실은 요즘 에디터들은 유용한 부가기능이 전부 내장되어있어서 

HTML CSS짤 땐 Emmet 정도만 있어도 충분하다. 

<br>
<br>

## head 태그에 들어갈 내용 정리
 

 
```
<!DOCTYPE HTML>
<head>
  어쩌구
</head>
<body>
  저쩌구
</body>
```
HTML 문서의 기본 템플릿은 꼭 head와 body 태그를 포함해야한다.

head태그는 사이트 내에서 눈에는 보이지 않는 중요한 정보들이 들어갈 수 있는데

head태그 내에서 쓸 수 있는 중요한 태그들을 몇개 나열해보겠다.

 

 
<br>
 

 

### 1. 각종 CSS 파일들 

 
```
<head>
  <link href="css/main.css" rel="stylesheet">
</head>
```
CSS 파일들을 첨부할 때 링크태그를 집어넣을 수 있다.

위 경로는 현 HTML 파일과 같은 위치에 있는 css폴더 안에 있는 main.css 파일을 첨부하라고 되어있는데,

1. css/main.css

2. /css/main.css

참고로 위 두개의 경로는 다른 경로이다.

1번은 현재 HTML파일과 같은 경로에 있는 css라는 폴더 내의 main.css 파일을 의미하고

2번은 현재 사이트의 메인경로 (codingapple.com)부터 시작해서 codingapple.com/css/main.css 파일을 첨부해라 라는 뜻이다.

슬래쉬 기호가 첨부터 붙어있으면 사이트 메인경로부터 시작해라~ 라는 의미이다.

멋진 말로 1번은 상대경로, 2번은 절대경로라고 한다.

 

 
<br>
 

 

### 2. 스타일 태그

 
```
<head>
  <style>
    .button {
      color : red;
    }
  </style>
</head>
```
CSS 파일을 만들기 귀찮으면 \<style> 태그를 열어서 CSS를 작성하기도 한다.

CSS 파일과 유사하게 동작한다. 

\<body> 안에 넣어도 동작하는데 html 파일안의 코드는 위에 있을 수록 먼저 읽기 때문에

\<body>태그 맨 밑 같은 곳에 두면 사이트 로딩시 스타일이 잠깐 깨질 수 있다.

그래서 넣을거면 \<head>에 넣는 사람이 많다. 

 

 

 <br>

 

 

### 3. 사이트 제목

 
```
<head>
  <title>네이버입니다</title>
</head>
```
사이트 제목을 넣을 수 있다. (브라우저 탭에 뜨는 이름)

 

 
<br>
 

 

### 4. 여러가지 meta 태그

 
```
<head>
  <meta charset="UTF-8">
  <meta name="description" content="html 잘하는 코딩애플입니다.">
  <meta name="keywords" content="HTML,CSS,JavaScript,자바스크립트,코딩">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```
1. 사이트의 인코딩 형식을 지정할 때 charset="UTF-8" 이라고 속성을 적을 수 있다.

2. 사이트의 검색 결과 화면에 뜨는 글귀를 수정하고 싶으면 이런 속성들을 추가할 수 있다. name="description" content="어쩌구"

description은 구글 검색시 파란 제목으로 뜨는 글귀,

keywords는 검색에 도움을 주는 키워드 등이다.

(이런건 온라인 마케팅 하는 사람들이 잘 안다.)

 

3. 사이트 초기 zoom 레벨이나 폭을 지정해주려면 name="viewport" 라는 속성을 부여하면 된다.

width=device-width는 모바일 기기의 실제 폭으로 렌더링 해주세요 라는 뜻이다.

요즘 스마트폰 가로 해상도가 1920px을 넘어가는 폰들이 많은데,

그럼 이것만 보고 1920px 에 해당하는 페이지를 띄워줄 수는 없을 것이다.

그래서 실제 접속시 스마트폰 기기의 실제 가로폭을 보고 렌더링하라고 명령하는 부분이라고 보면 된다.

initial-scale=1 이 부분은 접속시의 화면 줌레벨 설정이다.

그래서 반응형 웹을 만들 때 저 meta 태그를 복붙하시고 시작하면 된다.

 

 

 <br>

 

 

### 5. open graph

 
```
<head>
  <meta property="og:image" content="/이미지경로.jpg">
  <meta property="og:description" content="사이트설명">
  <meta property="og:title" content="사이트제목">
</head>
```
facebook이 만든 og 라는 메타태그가 있다.

여러분이 가끔 카톡 페북 이런 곳에 링크를 공유하면 박스가 뜨고 사이트 설명, 제목, 이미지가 뜬다.

이걸 커스터마이징하고 싶으면 저런 meta 태그를 따로 집어넣으면 된다. 

 

 

 
<br>
 

 

 

### 6. Favicon

 
```
<head>
  <link rel="icon" href="아이콘경로.ico" type="image/x-icon">
</head>
```` 
여러분의 웹사이트 제목 옆에 뜨는 아이콘을 커스터마이징하려면

이렇게 link 태그로 첨부하면 된다.

 



 

그럼 아이콘이 생긴다. 

- ico 대신 png 파일로 넣어도 되지만, ico가 호환성은 가장 좋다. 

- 요즘은 32 x 32 사이즈로 제작하면 된다. 

- 그리고 웹사이트를 바탕화면에 바로가기 추가했을 경우 뜨는 아이콘도 커스터마이징 가능하다. 

rel="apple-touch-icon-precomposed" 

이런 식으로 rel 속성을 조정하면 되는데 OS마다 요구하는 rel 속성이 달라서 필요해지면 찾아 적용하거나

favicon generator 이런거 검색해서 한번 써보면 OS별로 알아서 만들어준다. 

<br>
<br>

## 모던 웹에서 사용하는 단위정리

 
```
.box {
  width : 16px; /* 기본 px 단위 */
  width : 1.5rem; /* html태그 혹은 기본 폰트사이즈의 1.5배 */
  width : 2em; /* 내 폰트사이즈 혹은 상위요소 폰트사이즈의 2배 */
  width : 50vw; /* 브라우저(viewport) 화면 폭의 50% */
  width : 50vh; /* 브라우저(viewport) 화면 높이의 50% */
}
 ```

예전엔 rem 단위를 가끔 썼다.

모든 div의 사이즈, margin, padding, 버튼 사이즈 이런게

기본 폰트사이즈에 비례해서 움직이게 만들고 싶을 때 rem을 사용했다.

브라우저 폰트사이즈를 키운 채로 웹브라우징 하는 사람이 있어서 그랬다.

하지만 요즘은 ctrl + 마우스휠업 이렇게 줌인을 해서 쓰는 사람이 대부분이라

페이지를 폰트사이즈에 가변적으로 반응하는 사이트 만들 때 빼고는 그닥 유용한 속성은 아니다다.

 

 

가끔 typography 디자인할 때 

글자사이즈를 px 단위로 기억하기 귀찮고 힘들 때 폰트사이즈로 rem을 가끔 사용하는데, 

18px 22px 이렇게 외우는 것 보다는

1.2rem 1.4rem 이게 더 기억하기 쉽다. 가끔 헷갈려서 21px 이렇게 적는 삑사리도 안난다. 

 

 

 <br>

 

 

### 반응형 웹을 만들 때 head 태그에 들어가야할 내용

 

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
내용이 들어가있어야 모바일에서도 예쁜 레이아웃을 만들 수 있다.
 

 

 
<br>
 

 

### media query 사용하는 법 

 
```
@media screen and (max-width : 1200px) { 
  .box { 
    font-size : 40px; 
  } 
} 

@media screen and (max-width : 768px) { 
  .box { 
    font-size : 30px; 
  } 
}
```

 

CSS 파일 최하단에 사용한다.

"현재 브라우저의 폭이 1200px 이하일 경우에 안에 있는 class를 적용해주세요~" 라는 뜻이다.

여러개 원하는 만큼 사용가능하다.

그래서 위의 코드는 브라우저 폭이 1200px 이하면 .box { font-size : 40px } 이걸 적용해주고

768px 이하면 .box { font-size : 30px } 을 적용해준다. 

 

(참고) 적용은 아니고 class를 밑에 하나 더 추가해준다라고 이해하는게 정확하다.

그러면 class 안의 font-size 스타일 중복이 발생하는데

중복이 발생하면 원래 더 밑에 있는 스타일을 적용해준다다. 

 

 

 <br>

 

 

### 권장 Breakpoint 

 

media query 문법 max-width 안에 넣는 브라우저 폭을 breakpoint라고 한다. 

breakpoint는 원하는 만큼 저렇게 여러개 넣을 수 있는데 

필요할 때 마다 사이즈를 임의로 넣고 작성하는 것 보다는

많은 사람들이 사용하는 breakpoint를 쓰는게 좋다. 

 

1200px / 992px / 768px / 576px

이런 사이즈를 권장한다.

Bootstrap 라이브러리가 기본으로 권장하는 breakpoint 이며 그대로 따라하도록 하자. 

1200px부터를 태블릿사이즈로 볼지, 992px 부터를 태블릿 사이즈로 볼지는 개발자 마음이고 

768px 부터를 모바일로 볼지, 576px 부터를 모바일로 볼지도 개발자 마음이다. 

 

 

4개 저렇게 다 쓰면 스타일 관리하기가 귀찮기 때문에

1200px 

768px

이렇게 두개만 골라서 1200px 이하는 태블릿, 768px 이하는 모바일

이렇게 디자인하는게 가장 간편하다. 

<br>
<br>

## 
