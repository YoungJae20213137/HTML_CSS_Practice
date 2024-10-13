#  <b> Summary Points 1 </b>

<br>

## HTML 기초와 개발환경 셋팅
<br>

Brackets 에디터 : https://brackets.io/

(윈도우는 .msi 맥은 .dmg)


Visual Studio code 에디터 : https://code.visualstudio.com/


 
* (참고1) 에디터 상단 메뉴에서 '폴더열기'로 먼저 작업폴더를 오픈 후 파일을 만든다. 

* (참고2) 에디터의 번개 버튼을 누르시면 실시간 미리보기 가능

* (참고3) ctrl + s 단축키로 파일 저장, 맥북은 ctrl 대신 command.


<br>

### HTML은 어디다 쓰는 언어?

 

웹페이지를 만들고 디자인하고 싶을 때 사용한다.

세상에 존재하는 모든 웹페이지는 html 언어로 작성한다. 

 

HTML은 Hypertext Markup Language의 약자인데 Markup Language에 주목한다.

마크업 언어는 "자료의 구조를 표현하기 위한 언어".

웹페이지에 우리가 글넣고 그림넣고 박스넣고 버튼넣고 .. 자료를 입력하는데, 

그 자료들이 어디에 배치되는지 그런 것들을 기록하기 위해 존재하는 언어가 바로 HTML이라고 보면 된다.

<br>

### HTML 파일 기본 템플릿

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
 ```

HTML 문서는 .html로 끝나도록 저장하고,

모든 HTML 문서는 위의 코드를 가지고 있어야 HTML 파일로 인식한다.

<head> 내부엔 사이트 생성에 필요한 인코딩형식, 사이트제목, 필요한 CSS나 JS파일 등이 들어갈 수 있으며 

<body> 내부엔 실제 웹사이트에서 보여줄 글, 그림 등을 적으면 된다.

<br>  

<br>  

## HTML 기본 태그로 글 작성해보기
<br>

HTML은 <태그>로 작성한다.

```<p>안녕</p>```
이런 식의 태그들을 열고 닫은 후 내부에 글을 넣고 그림을 넣을 수 있다.

태그들은 종류와 용도가 매우 많이 존재한다. 

글을 작성하고 싶다면 글을 넣을 때 쓰는 태그를 사용하고,

버튼을 넣고 싶으면 버튼을 넣을 때 쓰는 태그를 사용하면 된다. 

 
<br>
 

### 기본 태그 목록 

 

```<p>글 본문</p>
<h1>글 제목</h1>
<img src="이미지 경로">
<a href="">링크</a>
<button>버튼</button>
<ul><li>리스트</li></ul>
<ol><li>리스트</li></ol>
```

① 태그를 열었으면 </태그명>으로 닫아야한다. 닫지 않아도 되는 태그도 몇개 존재한다. \<img> 이런거

② 특정 태그는 안에 href=" ", src=" " 이런 속성을 집어넣어서 추가정보를 기입가능.

href는 클릭시 이동할 링크를 기입가능하고 

src는 파일 경로를 기입가능.

 

③ 용도에 맞는 태그를 사용해야한다.

용도에 맞는 태그를 쓰는게 강제되는 사항은 아님.

```
<p>버튼</p>
```
 이렇게 만든 다음에 버튼처럼 꾸며도 전혀 문제될게 없음.

하지만 HTML은 마크업 언어기 때문에 자료의 구조를 쉽게 파악할 수 있어야하는데 그럴 때 용도에 맞는 태그 사용하는게 도움이 되고

용도에 맞는 태그를 사용하면 더욱 '웹표준'에 맞는 웹을 만들어낼 수 있다. 

 

<br> 

 

### 이미지를 눌렀을 때 다른 곳으로 이동하게(링크) 만들고 싶다면?

 
링크를 만들 수 있는 
```
<a></a>
```
 태그에 글 넣는건 해봤다. 

그럼 글 대신 그림을 집어넣을 수 있지 않을까?


```
<a href="http://naver.com">
  <img src="">
</a>
```
위처럼 하면 가능하다.

이런 식으로 HTML은 태그 안에 태그를 넣어줄 수도 있다.

<br>

## 기본적인 웹페이지 스타일링
<br>

### 간단한 스타일 넣는 법 

```
<p style="font-size : 20px; color : red"> 글자 </p>
```
거의 모든 태그는 style="" 이라는 속성을 열 수 있다.

거기 안에 스타일이름 : 스타일값; 형식으로 스타일을 넣으면 된다.

여러개를 넣고 싶다면 뒤에 쭉 나열하면 된다.

세미콜론 까먹으면 안됨.

 
<br>
 

### 자주 사용하는 글자 스타일들

 

```
font-size : 20px;
font-family : 'gulim';
color : black;
letter-spacing : -1px;
text-align : center;
font-weight : 600;
```
영어 단어를 잘 알고 계시면 무슨 뜻인지 바로바로 파악은 쉽다.

 

 <br>

 

### 이미지 정렬과 폭 조정

 

```
display : block;
margin-left : auto;
margin-right : auto;
width : 150px;
```
이미지는 width 많이 사용한다. px 혹은 % 이런 단위로 폭을 조정가능. 

이미지를 가운데 정렬하고 싶으면 display : block; margin-left : auto, margin-right : auto 를 기입해주면 된다.

 
<br>
 

 

 

### 텍스트의 일부만 스타일을 변경하고 싶을 때 

 

```
<p>안녕하세요 저는 <span style="color : red;">뛰어난</span> 개발자입니다.</p>
```

\<span>이라는 태그로 감싼 뒤에 스타일을 주면 된다. 

\<span>태그는 가끔 글자 일부를 싸매고 싶을 때 사용하는 큰 의미없는 태그다. 

\<strong>태그로 글자 일부를 싸매면 간단히 굵게 표현도 가능.

 

(참고) span 태그는 display : inline 이라는 스타일 속성을 내포하고 있으며,

display : inline을 가지고 있는 요소는 폭, 높이 등을 단독으로 결정할 수 없다.

폭, 높이를 주고싶으면 얘를 감싸고 있는 \<p>에 준다.

<br>

<br>

## CSS 파일 만들고 첨부하는 법

style 속성 안에 들어갈 코드가 매우 길어지면 

HTML이 더러워지기 때문에 이걸 다른 파일로 빼서 작성할 수 있다.

CSS 파일로 빼면 된다. 

 

 

 <br>

0. CSS를 사용하려면 CSS파일을 만든 후 HTML에 첨부해야한다.

 

우선 작업폴더에 .css로 끝나는 파일 아무거나 하나 만들고 

HTML 파일로 돌아와서 

 
```
 <link href="님들의css파일경로~~" rel="stylesheet">
```
\<head>태그 안에 \<link>태그를 넣고

href라는 속성에 .css 파일 경로를 지정해놓으면 css 파일 이용가능. 


 
정확한 방법은 

<br>

1. CSS파일에 스타일을 집어넣고 .어쩌구 작명

```
.profile { 
  width : 200px;
  display : block;
  margin : auto;
}
```
스타일을 적고 .어쩌구 이렇게 아무렇게나 작명하고 { } 중괄호로 묶어준다.

위의 코드는 3줄의 스타일을 .profile 이렇게 하나의 단어로 묶은 것.

그 단어를 클래스라고 부른다.

 

 <br>

 

2. HTML에 클래스 명을 첨부해서 스타일을 넣을 수 있다. 
```
<img src="lion.png" class="profile">
```
class 속성을 열고 클래스명을 집어넣으면 

css 파일에서 묶어놨던 스타일들이 다 적용된다. 

 

 <br>

 

3. Brackets 에디터에선 클래스 만드는 작업을 빠르게 할 수 있다. 

class 하나 미리 작명하고 거기다가 커서 찍고 ctrl + e / command + e 누르면

\<link>로 연결해둔 css 파일이 열리기 때문에 css 파일 수정 쉽게 가능.

 

 

 

 

class 말고 다른 식으로도 스타일을 묶을 수 있는데 

```
.profile { font-size : 20px }  /*클래스*/
#special { font-size : 30px } /*아이디*/
p { font-size : 16px } /*태그*/
```
CSS selector 라고 칭하는 것들임. 

 

클래스 selector는 .클래스명{ } 이렇게 적을 수 있고 모든 class="클래스명"을 가진 요소에 스타일을 적용가능.

아이디 selector는 #아이디명 { } 이렇게 적을 수 있고 모든 id="아이디명" 속성을 가진 요소에 스타일을 적용가능.

태그 selector는 p { 스타일~~ } 이렇게 적을 수 있고 모든 \<p> 태그에 스타일을 적용가능.


 
<br>

### 셀렉터의 우선순위

 

물론 class, id를 동시에 가지는 html 요소라면

스타일이 겹칠 수 있는데, 그럴 경우 우선순위가 존재한다.

 
```
style="" (1000점)
#id (100점)
.class (10점) 
p (1점) 
```

점수가 높을 수록 더 우선적으로 적용된다. 

<br>
<br>

## 웹레이아웃의 기초: div를 이용한 네모 박스 디자인

네모 박스 디자인에 많이 사용하는 CSS 속성

 
```
.box {
  margin : 20px; 
  padding : 30px;
  border : 1px solid black;
  border-radius : 5px;
}
```
margin은 바깥 여백,

padding은 안쪽 여백,

border는 테두리 (차례로 두께, 선의 종류, 색상),

border-radius는 테두리 둥글게 처리이다. 

가운데 정렬도 많이 하는데 저번 이미지처럼 display : block; margin-left : auto; margin-right : auto 이렇게 주면 된다.

 

 

외워봤자 맨날 까먹기 때문에 필요하면 구글에서 찾아쓰는게 일반적이다. 

 

 
<br>
 

 

### margin과 padding을 원하는 방향에만 줄 수 있다.

 
```
.box {
  margin-top : 20px;
  padding-left : 30px; 
}
```
top, left, bottom, right 중 원하는 곳에만 여백을 줄 수 있다. 

(참고) margin은 음수도 가능하다. -20px 이런 식.

(참고) margin : 5px 6px 7px 8px; 이렇게 띄어쓰기를 이용해 작성하면

차례로 상 우 하 좌 마진을 5,6,7,8px 한번에 줄 수 있다. 

 

 <br>

 

 

### display : block이 내장되어있는 div박스

 
```
.box {
  display : block;
}
```
모든 div, p, h1, li 등은 display : block 속성을 주지 않아도 기본적으로 내장되어있다. 

그래서 p태그나 div태그를 그냥 사용하면 한 행을 전부 차지하게 된다. 

이게 싫다면 display 속성을 다른 것으로 부여해주면 된다.

display : inline, inline-block, flex 등 여러가지가 있다. 

 

 

 <br>

 



### 일부 스타일은 inherit 된다.

 

font-size, color, font-family, text-align 이런 속성들은

부모 태그에 쥐어주면 거기 안에 있던 태그들까지 전부 상속된다. 

영어로 inherit 된다고한다. 

안에 글자들이나 태그들이 많을 경우 전부 font-size를 작성안해도 

부모태그에 한번에 작성하고 끝낼 수 있으니 편리하다. 

다 inherit되는건 아니고 글자와 관련된 스타일들이 주로 inherit 된다.  

<br>
<br>

## 레이아웃 만들기 1: 호환성 좋은 float

html css로 사이트 레이아웃 만드는 법 :

만들고 싶은 레이아웃 디자인 위에 네모박스를 먼저 그려보고 바깥 네모부터 \<div> 써서 구현하면 된다.

어려워보이는 레이아웃도 네모박스부터 그 위에 그려보고

바깥 네모부분부터 \<div>로 하나하나 만들기 시작하면

그럼 무슨 레이아웃을 가져다주든 알아서 만들 수 있음

 

 



 

예를 들어 당근마켓 상품하나 레이아웃을 구현하고 싶으면

네모박스처럼 보이는걸 전부 네모로 표시해보고

바깥 네모 부터 하나하나 \<div>로 구현하라는 것임

물론 문자는 \<p> 이미지는 \<img> 이런거 쓰는게 좋음.

그리고 그러려면 박스를 정렬하고 배치하는 법도 알아야한다.

 

 

<br>
 

 

### 요소를 공중에 띄워 왼쪽/오른쪽 정렬하는 float 속성 

 
```
<div>
  <div class="left-box"></div>
  <div class="right-box"></div>
</div>
.left-box {
  width : 100px; 
  height : 100px;
  float : left;
}
.right-box {
  width : 100px; 
  height : 100px;
  float : left;
}
```
- 위의 코드는 박스 두개를 만들어 각각 왼쪽으로 정렬시킨다.

- 하지만 float를 쓰면 요소를 붕 띄우다보니 그 다음에 오는 HTML 요소들이 제자리를 찾지 못한다.

(참고) float 속성으로 가로정렬할 땐

영상처럼 float 박스들을 싸매는 하나의 큰 div 박스를 만들고 폭을 지정해주는게 좋다.

그래야 모바일에서 안 흘러넘침.

 

 

 

 
<br>
 

### float를 쓰고 나면 항상 clear 속성이 필요합니다.

 
```
<div>
  <div class="left-box"></div>
  <div class="right-box"></div>
  <div class="footer"></div>
</div>
.footer {
  clear : both
}
```
clear 속성을 사용하면 float 다음에 오는 박스들이 제자리를 찾게 된다.

float썼으면 까먹지 말고 항상 넣으면 된다.

안넣으면 내 의도와는 다른 레이아웃이 반겨줄 것이다. 

참고로 float : none 이것도 추가해주는게 나중에 생길 버그예방차원에서도 좋을 수 있다. 

 

 

 

 <br>

 

### 상대적인 크기 단위인 퍼센트 단위 

 
```
.box {
  width : 80%
}
```
이 경우 내 부모 태그의 width에 비해 80% 만큼 차지하게 된다.

부모태그는 나를 감싸고 있는 태그를 뜻한다. 

<br>
<br>

## 레이아웃 만들기 2: inline-block

display : inline-block 사용 법 

 

가로로 정렬할 때 float : left 이것만 쓸 수 있는 것은 아니다.

display : inline-block을 사용해보자.

 
```
<div>
  <div class="left-box"></div><div class="right-box"></div>
</div>
.left-box {
  width : 100px; 
  height : 100px;
  display : inline-block;
}
.right-box {
  width : 100px; 
  height : 100px;
  display : inline-block;
}
```
위의 코드는 박스를 만들어 왼쪽으로 정렬시키는 코드이다. 

display 속성만 inline-block으로 조정하면 가로로 배치가 가능하다.

inline- block은 "내 폭과 높이만큼 자리차지하게 해주세요~" 라는 뜻이다.

간편하지만 <태그> 사이에 스페이스바 공백이 있다면 그대로 보여주기 때문에

가로로 정렬하려면 태그 사이의 공백도 제거해줘야한다.

이런게 귀찮다 float 쓰셈 

 

 

 
<br>
 

### 공백제거 편법1. 주석처리 기호 사용하기

 
```
<div>
   <div class="left-box"></div><!--
--><div class="right-box"></div>
</div>
```
주석은 실행되지 않는 코드이다. 

(에디터에선 ctrl + ? 이걸 눌러서 주석처리가 가능하다. 맥은 command + ?)

HTML 코드는 \<!-- --> 이게 주석처리하는 코드이며

이 사이에 코드를 집어넣으면 실행되지 않는다.

하지만 그래도 더러워보인다. 

 

 

 
<br>
 

 

### 공백제거 편법2. 부모의 폰트사이즈를 0으로 만들기

 
```
<div style="font-size : 0px;">
    <div class="left-box"></div>
    <div class="right-box"></div>
</div>
```
font-size 속성은 inherit 되기 때문에 안에 있는 <div>와 그 사이에 있는 공백도 font-size가 0px이 된다.

이러면 해결인데 HTML이 깨끗해질지 모르겠지만 CSS가 더러워질 수 있다.

둘 중에 덜 더러워보이는 방법을 하나만 사용하면 된다. 

<br>
<br>

## 레이아웃 추가적인 팁

### 팁0) 뭘 만들든 레이아웃은 항상 박스부터 만들고 시작하면 된다.

 

내가 만들 디자인위에 전부 박스를 그리는 것.

 



 

그리고 이 박스들을 전부 \<div>로 구현해놓으면 된다.

그리고 안에 글넣고 그림넣고 하면 끝. 

기억해야할게 \<div>는 그냥 쓰면 display : block 때문에 위아래로 배치된다.

좌우로 나란히 배치하고 싶으면 float, 혹은 inline-block 쓰면 된다. 

 

 

 <br>

 

### 팁1) margin 속성으로 상하좌우 마진을 한꺼번에 줄 수 있다. 

 
```
.box {
  margin : 10px auto 30px auto;
}
```
margin 이나 padding 속성에 4개의 값을 동시에 집어넣을 수 있는데 4개 값은 각각 상, 우, 하, 좌측을 의미한다. 

 

 
<br>
 

 

 

### 팁2) PC 레이아웃을 만들 때 항상 container 또는 wrap 박스를 만들어놓는게 좋다. 

 
```
<div class="container">
  <div class="left"></div>
  <div class="right"></div>
</div>
```
container 박스엔 항상 width를 지정해놓는게 좋다.

그래야 나중에 브라우저화면이 축소되어도 내부 div 박스들이 찌그러지지 않는다. 




 
<br>

 

 

### 팁3) Brackets 에디터에선 코드를 클릭하면 미리보기 화면에서 margin, padding을 표시해준다.

 

파란색 단색은 margin, 점선은 padding. 

왜 이 글씨가 여기 배치되어있는지 확인하고 싶을 때 매우 유용하게 쓸 수 있다. 

그래서 좀 느리고 투박해도 HTML CSS짤 때는 Brackets 에디터 못놓는 이유가 있음

<br>
<br>

## 셀렉터를 이용해 CSS 코드 양 줄이기

HTML태그에 클래스 두개 이상 붙이기

```
<div class="container text-center"> </div>
```
띄어쓰기를 하신 다음에 원하는 class를 집어넣으면 된다. 

 

 <br>

 

 

### 셀렉터 사용법 1. 공백

 
```
<ul class="navbar">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```
```
.navbar li {
  display : inline-block;
}
```
위 처럼 공백을 이용해 안에 있는 li 태그인 모든 자손을 선택할 수 있다.

- 당연히 스페이스바 다음에 tag 셀렉터 말고 class 셀렉터 id 셀렉터 자유롭게 사용가능하다. 

- .class .class .class 이런 식으로 무한히 연달아 사용가능하다. 

 

 

 
<br>
 

 

 

### 셀렉터 사용법 2. 꺾쇠괄호 > 

 
```
<ul class="navbar">
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```
```
.navbar>li {
  display : inline-block;
}
```
기호를 이용해 .li-inline 바로 밑에있는 자식만 선택할 수 있다. 

 

 

<br>

 

### 셀렉터 사용법 3. 더욱 상세히 선택하고 싶다면 

 
```
<ul class="navbar">
  <li> <span>안녕</span> </li>
  <li></li>
  <li></li>
  <li></li>
</ul>
```
```
.navbar li>span {
  color : red;
}
```
셀렉터를 그냥 연달아 사용하면 된다. 

위의 예제는

.navbar 안에 있는 모든 li, 그리고 그 안에 있는 모든 직계 자손 span 태그를 선택하고 있다. 

 

 

 

 

 

셀렉터 잘 쓰면 클래스 추가선언 없이도 내가 원하는 요소에 스타일을 쉽게 줄 수 있다. 

하지만 이렇게 4~5개 이상 연달아 붙여쓰지 않길 권장한다.

 

.container div div>p>span
이렇게 길게 쓰지 말라는 소리이다.

셀렉터를 남발하는 것 보다는 하나의 새로운 클래스를 만드는게 훨씬 더 나을 수 있다.

 

차라리 그냥 span 윗부분에 클래스를 하나 만들고 

.headline>span
이렇게 작성하면 좋다.

CSS 셀렉터부분만 읽어도 내가 어떤 요소를 스타일넣고 있는지 바로 이해가 가능하다. 

읽기만 해도 어떤 스타일을 주는지 알 수 있는 셀렉터가 좋은 셀렉터 사용법이다. 

 

그리고 셀렉터 4~5개 연달아 작성하면 나중에 파일이 커지면 쓸데없는 버그의 원인일 수 있기 때문에 

재사용가능성, 확장성을 염두에 둔다면 저렇게 쓰면 안된다. 

 

 

 <br>

 

 

### 간단한 링크 디자인 

 
```
<a href="#" class="link">링크</a>
.link {
  text-decoration : none;
}
.link:visited {
  color : black;
}
```
링크는 기본적으로 밑줄이 쳐져있는데, 이걸 제거하고싶다면 text-decoration 속성을 만져주면 된다.

그리고 링크를 방문했을 시 보라색으로 변하는데, 이걸 조작하고 싶다면 :visited 라는 pseudo-class를 셀렉터에 붙이면 되는데

그럼 방문 후(visited) 링크들의 스타일을 지정해줄 수 있다.

<br>
<br>

## 배경 이쁘게 넣는 스킬들 & margin collapse

배경관련 CSS 속성들 

 
```
.main-background {
  background-image : url(../img/shoes.jpg);
  background-size : cover;
  background-repeat : no-repeat;
  background-position : center;
  background-attachment : fixed;
}
```
background-size는 px, % 단위도 가능하고

cover는 배경으로 꽉채워라

contain은 배경이 짤리지 않게 꽉채워주라라는 뜻이다.

background-attachment는 웹사이트가 스크롤될 때 배경이 신기하게 동작하게 만들고 싶으면 써보도록 하자.
 

 
<br>
 

### 배경 두개 겹치기 신공 

 
```
.main-background {
  background-image : url(../img/shoes.jpg), url(person.jpg);
}
```
콤마로 이미지 두개를 첨부하면 된다.

투명도를 지원하는 png 이미지를 사용하면 더 재밌는 디자인을 만들 수 있다.

 
<br>
 

 

 

### 배경에 검은색 틴트 주기 

 
```
.main-background {
  background-image: linear-gradient( rgba(0,0,0,0.5), rgba(0,0,0,0.5) ), url(이미지경로~~) ;
}
```
linear-gradient 이건 색이 점진적으로 변하는 gradient를 줄 수 있는 키워드인데

여기에 투명도 0.5의 검은색을 입힌 후에 배경겹치기 스킬을 사용하면 된다다.

 

 

 <br>

 

 

### 주의해야할 margin 버그 

 
```
<div class="배경">
  <p>안에 글씨</p>
</div>
```
div 박스 안에 p 태그를 사용했다.

p 태그에 상단 margin을 주기 위해 margin-top을 주게 되면

div와 p가 동시에 margin-top이 생기게 된다. 뭔가 이상한데,

 

 

이 현상은 margin collapse effect 라고 부르는 일종의 버그이다.

원래 박스들의 테두리가 만나면 margin이 합쳐진다. (박스가 내부에서 만나든 외부에서 만나든 상관없다.)

정확히 말하면

1. 마진을 하나로 합쳐주고

2. 혹여나 둘 다 마진이 있으면 둘 중에 더 큰 마진을 하나만 적용하게 된다.

 

그래서 두 박스의 테두리가 겹치지 않도록 해주면 보다 더 정확한 마진 노가다를 할 수 있다. 

부모 박스에 padding을 1px 이렇게 조금 주는 것으로 쉽게 해결 가능하다.

불만이 있다면 웹표준을 관리하는 www.w3.org 이라는 단체에 따지도록 하자.

<br>
<br>

## position과 좌표 레이아웃 만들기

### 좌표속성이 있다.
```
.box {
  top : 20px;
  left : 30%;
}
```
top, left, bottom, right 라는 속성을 사용하면

요소의 상하좌우 위치를 변경할 수 있다. 

하지만 이 좌표속성을 사용하려면 position 속성이 필요하다. 

position 속성은 좌표속성을 적용할 기준점이 여기에요~! 라고 지정해주는 역할이다. 

 

 
<br>
 

### position 속성은 크게 4개 값이 있습니다.
```
.box {
  position : static; /* 기준이 엄서요 (좌표적용 불가) */
  position : relative; /* 기준이 내 원래 위치요 */
  position : absolute; /* 기준이 내 부모요 */
  position : fixed; /* 기준이 브라우저 창이요 (viewport) */
}
```
여기서 원하는 기준을 선택하면 된다. 그럼 이제 좌표속성으로 좌표 값을 줄 수 있다.

position : absolute는 부모 박스를 기준으로 찰싹 달라붙은 뒤에 좌표값을 적용하게 되는데, 

정확히 말하면 부모가 아니라 부모 중에 position : relative를 가지고 있는 부모가 기준이다. 

 

 
<br>
 

 

### position : absolute 를 적용한 요소 가운데 정렬 
```
.button {
  position : absolute; 
  left : 0;
  right : 0; 
  margin-left : auto;
  margin-right : auto;
  width : 적절히
}
```
적어도 5개의 속성이 있어야 가운데 정렬이 가능하다. 

<br>
<br>

## 반응형 width & box-sizing

### 겹치는 박스 만들기

 

당연히 position 속성을 사용하면 된다.

absolute, relative, fixed 중 하나를 사용하면 된다. 

 

 

 

 

하지만 박스를 만들 때 주의점이 하나 있는데. 

원래 div 박스의 width를 주게되면 padding, border를 고려하지 않는다. 

padding 안쪽 부분만 실제 width로 설정다. 



이걸 그림을 그려보면... 파란색 저 부분만 실제 width이다.

그래서 200px의 박스를 만들어도, padding을 많이 주게 되면 실제 보여지는 박스의 폭이 padding 만큼 늘어날 수 있다.

웹사이트 대충 만드는 초보는 별 상관 없겠지만 

실제 업무에서는 사이즈 조금만 잘못되어도 다른 요소에 크게 영향을 줄 수 있다. 


 

 

 <br>
 

 

### 박스의 폭을 border까지 설정해주고 싶을 때 쓰는 속성 

 
```
.box {
  box-sizing : border-box; /*박스의 폭은 border까지 포함입니다*/
  box-sizing : content-box; /*박스의 폭은 padding 안쪽입니다*/
}
```
box-sizing이라는 속성을 주게되면 border까지를 실제 박스의 폭으로 설정해준다. 

아주 고마운 속성이다. 

빨리 모든 div 박스에 추가해보도록 하자. 

 

 

 

 <br>

 

### CSS 파일 작성시 기본으로 쓰면 좋을 속성들

 

그래서 숙련자들의 CSS 파일을 보면 일단 이런 것들을 맨 위에 정의하고 시작한다.

 
```
div {
  box-sizing : border-box;
}
body {
  margin : 0;
}
html {
  line-height : 1.15; /*기본 행간 높이*/
}
```
여기에 더해서 

모든 h, p 태그의 margin을 균일하게 설정하거나

li, a 태그에 text-decoration : none 을 주거나

나중에 배울 table 태그에 border-collapse: collapse 를 주거나 

이런 것들이 가능하다다.

이런거 미리 적고 시작하면 항상 편리하게 CSS 코드를 짤 수 있다. 

가끔 CSS Reset 이런 식으로 부르기도 한다.

 
 

 

 <br>

 

 

 

### CSS normalize

 

그리고 이런 것 뿐만 아니라 브라우저간 통일된 스타일을 주기 위해 

특정 스타일을 맨 위에 적고 CSS 코드짜기 시작하는 경우도 있다.

왜냐면 브라우저마다 \<button>의 스타일이 다르고, 가끔 line-height 이런 줄간격같은 것도 다르고 

다음 시간에 배울 \<input> 사이즈도 다르기 때문이다. 

그래서 같은 코드를 짜도 다른 브라우저에선 이상하게 보일 수 있다. 

 

 

CSS Normalize 링크 :  https://github.com/necolas/normalize.css/blob/master/normalize.css 

그래서 어떤 아저씨가 CSS normalize 라고 만든 문서가 하나 있는데

여기있는 스타일 붙여넣으면 브라우저간 다르게 보이는 문제들을 미리 해결할 수 있다. 

 

그래서 여기 있는 스타일을 그대로 나의 CSS 파일에 복붙하거나

아니면 다운받아서 \<link> 태그로 첨부하면 된다.

<br>
<br>

## form & input

### form은 form 태그로 만들어낸다.

 
```
<form>
  <input>
</form>
```
input태그는 닫지 않는다. 

 

 

 <br>

 

 

### input의 type

 
```
<input type="text">
<input type="email">
<input type="password">
<input type="radio">
<input type="file">
<input type="checkbox">
<input type="submit">
<select>
  <option>옵션1</option>
</select>
<textarea></textarea>
```
10개는 더 있지만 가장 자주 쓰는 것만 모아봤다. 

나머지는 필요할 때 구글에 찾아쓰도록 하자.  

 

 
<br>
 

### input에 넣는 속성들

 
```
<input placeholder="어쩌구" value="어쩌구" name="age">
```
placeholder는 배경 글자,

value는 미리 입력된 값,

name은 서버 기능개발에 필요한 인풋의 이름을 설정 가능하다.


 

 <br>

 

### HTML의 속성으로 CSS셀렉터를 사용할 수 있다.

 
```
input[type=email] {
  color : grey
}
```
input의 type속성이 email인 요소만 찾아서 스타일을 줄 수 있다. 

폼에서 특히 유용하게 사용하다. 

 

 

 <br>

 

### 전송버튼 

 
```
<button type="submit">전송</button>
<input type="submit">
```
둘 중 하나 쓰면 된다.

그리고 물론 \<form> 태그 안에 있어야 잘 작동한다.

<br>
<br>

## form 추가 팁 & label

form 레이아웃 제작시에도 포인트는 div박스이다.

 

뭘 만들든 일단 예시 디자인 위에 박스부터 그려놓고

그걸 그대로 div 박스로 구현만 하면 쉽게 레이아웃 만들 수 있다.

div 박스부터 배치하고 그 안에 글넣고 그림넣고 input 넣고 그러면 된다.

 

 

```
<form>
  <div class="w-100">
    <input>
  </div>
  <div class="w-50">
    <input>
  </div>
  <div class="w-50">
    <input>
  </div>
  <div class="w-100">
    <textarea></textarea>
  </div>
</form>
```
가로로 꽉찬 input들은 w-100 이라는 div에 싸매고,

가로로 반반 차지할 input들은 w-50 이라는 div에 싸맸다

그리고 w-100은 width : 100%

w-50은 width : 50%; float : left 

이렇게 주었다. 

float 주면 당연히 어딘가에 clear : both 도 있어야한다.

 

 

 
<br>
 

 

\<input> 태그 디자인은

 

가로로 100% 폭을 주었고

padding 조금 주고

box-sizing : border-box

이런걸 줬다.

border-box 안해놓으면 폭이 padding을 포함해서 조금 커질 수 있기 때문이다. 

 

 
<br>
 

 

전송버튼 만들기 

 
```
<form>
  <button type="submit">전송</button>
  <input type="submit">
</form>
```
당연히 두개 중 마음에 드는걸로 만들면 된다.

 

 

 

 
<br>
 

### label 태그와 for 속성

 
```
<input type="checkbox" id="subscribe">
<label for="subscribe">누르기</label>
```
label과 for 속성을 적절히 활용하면

input대신 label을 눌러도 input을 선택할 수 있다.

(input의 id, label의 for 속성을 똑같이 맞춰주면 된다.)

 

혹은 그냥 <input> 에 제목이 필요할 때도 h, p 태그 이런거 말고 <label> 태그를 가끔 이용한다.

<br>
<br>

## 쓸데 많은 Table 레이아웃과 vertical-align 속성

vertical-align 속성을 실험해볼 이미지와 글자
```
<div> <img src="https://mdn.mozillademos.org/files/12245/frame_image.svg" width="32" height="32"> image with a default alignment.</div> 
 ```

 

 

 <br>

### 기본적인 table HTML 구성 
```
<table>
  <thead></thead>
  <tbody>
    <tr>
      <td>내용</td>
      <td>내용</td>
    </tr>
  </tbody>
</table>
```
table태그 내에 tr은 row, td는 column을 의미한다. 

내가 원하는 만큼 row, column을 넣어주면 표가 완성된다. 

tbody, thead는 그냥 헤드부분 영역구분을 위해 사용하며 td 대신 th 태그를 사용하면 기본적으로 제목처럼 굵게 처리된다.

 

 
<br>
 

 

### 테이블 셀 내에서 상하정렬할 땐 vertical-align 
```
td, th {
  vertical-align : middle;
}
```
vertical-align 속성을 이용해 테이블 내에서의 상하정렬을 할 수 있다.

top, bottom, middle 사용가능

 

 <br>

 



### inline 요소 간 상하정렬할 땐 vertical-align 
```
<p>
  <span style="font-size : 50px">Greetings</span>   <span style="font-size : 20px">안녕</span>
</p>
```
display : inline 혹은 inline-block 요소들을 나란히 배치하면 상하정렬이 이상한 경우가 있다.

특히 큰 이미지와 글,

또는 큰 글씨옆에 있는 작은 글씨

이런걸 나란히 배치했을 때 서로 높이가 맞지 않는 경우가 많은데

이럴 때 margin-top 이런거 대신 쓰는 속성이다.

위의 예제에서 ```<span>안녕</span>``` 여기에 vertical-align : top 이런거 넣어서 실험해보자.

 

top, middle, bottom 말고도 super, sub, px 단위로 사용가능하다. 

(table 안에선 top, middle, bottom만 사용가능하다.)

 

 

 <br>

 

### display : table 
```
.box {
  display : table;
  display : table-row;
  display : table-cell;
}
```
가끔 div로 이루어진 요소들을 테이블화 시키고 싶을 때가 있다.

그럴 땐 table태그로 변하길 원하는 요소에 display : table을 적어준 뒤에

tr로 변하길 원하는 요소엔 display : table-row,

td로 변하길 원하는 요소엔 display : table-cell 을 넣어주면 된다. 

하지만 그럴 일은 거의 없기 때문에 참고로만 알아두자. 

<br>
<br>

## Table 추가 팁

### nth-child 셀렉터 
```
.cart-table td:nth-child(2) {
  color: red;
}
```
여러 요소를 찾은 다음

원하는 n번째 요소만 스타일을 주고 싶으면 :nth-child(n) 이걸 뒤에 붙여주면 된다.

위의 코드는 그래서 .cart-table 안에 있는 모든 td를 찾은 다음

2번째 나오는 td에만 color를 줄 수 있다. 

테이블에서 원하는 순서의 셀에 스타일줄 때 가끔 유용하게 사용다.

 

 

 
```
.cart-table td:nth-child(even) {
  color: red;
}
```
이러면 짝수로 등장하는 td에만 스타일을 줄 수도 있고,

(odd라고 쓰면 홀수이다.)

 

 

 
```
.cart-table td:nth-child(3n+0) {
  color: red;
}
```
이러면 3의 배수로 등장하는 3,6,9,12.. 번째 등장하는 요소에만 스타일을 줄 수 있다.

3n + 1 이렇게 작성하면 (3의배수 +1) 번째 등장하는 요소에만 스타일을 줄 수 있다. 

 

 

 
<br>
 

 

### 포인트1. 테두리 색상은 밑에만 넣고 싶으면
```
td, th {
  border-bottom : 1px solid black;
}
```
border-bottom 쓰면 된다. 

 

 <br>

 

 
### 포인트2. 셀 블록마다 width를 설정해줄 수 있다.
```
<table>
  <tr>
    <td class="name">상품명</td>
    <td class="price">가격</td>
    <td>수량</td>
  </tr>
</table>
```
```
.name {
  width : 50%
}
.price {
  width : 20%
}
```
하나의 td에 width를 주어도 전체 열의 width가 변한다.

나름 편리한 점이라고 볼 수 있겠다.

 

 
<br>
 

### 포인트3. td 여러개를 합치고 싶으면
```
<td colspan="4"></td>
```
colspan에 원하는 숫자를 넣으면 그 숫자만큼 옆의 셀을 합쳐준다. 

 

 

 

 

 

 

간혹 border-collapse 속성을 table태그에 적용하면 border-radius가 안먹는 경우가 있다. 

그럴 때 사용할만한 방법들이다. 

 <br>

### table 태그에 border-radius가 안먹을 때 1. 
```
table {
  border-collapse : collapse;
  border-spacing : 0;
}

(왼쪽위에있는 td) {
  border-top-left-radius : 5px;
}
```
 <br>

### table 태그에 border-radius가 안먹을 때 2. 
```
table {
  border-collapse : collapse;
  border-radius : 7px;
  border-style : hidden;
  box-shadow : 0 0 0 1px #666;
}
```
box-shadow라는 속성을 이용해 테두리를 가짜로 만들어내는 편법이다.

box-shadow는 그림자 넣는 속성이다. 

<br>
<br>

## pseudo-class로 인터랙티브 버튼 만들기

### 상태에 따라서 스타일을 줄 수 있는 Pseudo-class 셀렉터
```
.btn:hover {
  background : chocolate; /*마우스를 올려놓을 때*/
}
.btn:focus {
  background : red; /*클릭 후 계속 포커스 상태일 때*/
}
.btn:active {
  background : brown; /*클릭 중일 때*/
}
```
pseudo-class 셀렉터를 붙이면 여러 상태에 따른 스타일을 지정해줄 수 있다.

hover, focus, active 스타일 넣을 때 순서는 꼭 이렇게 선언해야 잘 동작한한다.

1. hover

2. focus

3. active

입니다. hofa로 외우면 잘외워진다... 

이거 말고도 수많은 pseudo-class가 있기 때문에 필요하면 찾아쓰도록 하자.

 

 

 

 
```
:any-link /*방문 전, 방문 후 링크 한번에 선택할 때*/
:playing /*동영상, 음성이 재생중일 때*/
:paused /*동영상, 음성이 정지시*/
:autofill /*input의 자동채우기 스타일*/
:disabled /*disabled된 요소 스타일*/
:checked /*체크박스나 라디오버튼 체크되었을 때*/
:blank /*input이 비었을 때*/
:valid /*이메일 input 등에 이메일 형식이 맞을 경우*/
:invalid /*이메일 input 등에 이메일 형식이 맞지 않을 경우*/
:required /*필수로 입력해야할 input의 스타일*/
:nth-child(n) /*n번째 자식 선택*/
:first-child /*첫째 자식 선택*/
:last-child /*마지막 자식 선택*/
```
이거 말고도 매우 많다. 

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

 

 

 <br>

 

### input 등에도 자주 사용한다.
```
input:focus {
  border : 2px solid red;
}
```
인풋에 커서가 찍혀있을 때 인풋에 스타일을 주고 싶으면 당연히 :focus를 붙이면 된다.

 

 
<br>
 

 

### a 태그에도 자주 사용한다.
```
a:link { 
  color : red; /*방문 전 링크*/ 
} 
a:visited { 
  color : black; /*방문 후 링크*/ 
}
```
:link를 붙이면 방문 전 링크

:visited를 붙이면 방문 후 링크에 스타일을 넣을 수 있다.

모든 링크의 밑줄제거는 그냥 a태그에 text-decoration : none 붙이면 된다. 

<br>
<br>

## 코드양이 줄어드는 class 작명법 (OOCSS, BEM)

### 코드 양을 줄이는 CSS 작성법 (OOCSS)

 

똑같이 생겼는데 색만 빨강/파랑으로 다른 버튼 2개를 만들어오라고 하면 어떻게 만들 것인가?

가장 간단한 방법은 

 
```
.main-btn-red {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
  background : red;
}

.main-btn-blue {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
  background : blue;
}
```
class를 두 개 만들어서 각각 <button>에 집어넣는 것이다.

그럼 빨간 버튼 파란 버튼 완성이지만 중복된 코드가 매우 많이 발생하고 있다.

4줄이나 똑같다. 

그럼 다른 색의 버튼 10개 만들어오라고 하면 똑같은 40줄의 코드가 복붙이 된다.

 

이 경우 CSS 파일이 매우 길어지기 때문에 보기 싫다.

그리고 용량이 큰 CSS 파일은 웹사이트 로딩 속도를 저하한다.

 

 

 

 

이렇게 코드를 짜보자.
```
.main-btn {
  font-size : 20px;
  padding : 15px;
  border : none;
  cursor : pointer;
}

.bg-red {
  background : red;
}
.bg-blue {
  background : blue;
}
```
버튼의 뼈대와 살을 분리하는 것이다.

1. 버튼의 기본 스타일인 padding, font-size 이런걸 정의하는 class를 하나 만들고 

2. 버튼에 스킨 색깔놀이 하는 용도의 class를 여러개 만들어두는 것이다다.

 

 

그럼 이제 html에 사용할 때
```
<button class="main-btn bg-red">빨간버튼</button>
<button class="main-btn bg-blue">파란버튼</button>
```
이렇게 쓰면 아까랑 똑같은 버튼이 탄생한다.

 

 

 

이렇게 뼈와 살을 각각의 class로 분리하는 방법의 장점은 

1. 중복된 스타일을 재사용가능하다.

덕분에 CSS 파일용량도 줄어들고 코딩 시간도 절약된다.

 

2. 유지보수가 편리해진다.

사이트의 모든 버튼의 font-size를 약간 줄여야한다면 이 경우엔 한 곳만 건드리면 모든 버튼이 다 수정되기 때문에 편리하다다.

 

3. 코드를 빨리 짤 수 있다.

.bg-red 이렇게 색깔놀이용 class들을 전문용어로 utility class라고 부른다. 

이걸 미리 많이 만들어두면
```
.bg-red {
  background : red;
}
.bg-green {
  background : green;
}
.bg-blue {
  background : blue;
}
```
앞으로 버튼만들 때 class명을 두세개 고르기만 하면 되니까

css 파일 열지않고도 다양한 스타일을 빠르게 만들 수 있다.

(class명을 미리 외워두면)

심지어 버튼말고도 다른 UI에 색상 줄 때도 적용가능할듯 .

 

 

 
```
.font-small {
  font-size : 12px;
}
.font-medium {
  font-size : 16px;
}
.font-lg {
  font-size : 20px;
}
```
▲ 글씨 font-size 변경이 잦다면 이런 식으로 utility class 들을 많이 만들어두고

글자 스타일링할 때 가져다 쓰면 코드짜는게 매우 빨라질 수 있다.

(외워두면)

특히 width, margin, padding, text-align 이런 것들 조정하는 utility class 많이 만들어두면 편리하다. 

 

 

 

지금까지 설명한 뼈와 살을 분리하는 CSS 작성방식을 Object Oriented CSS 라고 부른른다.

어떤 아저씨가 옛날에 주장한건데 장점이 많아 실제 개발시 자주 사용한다.

이걸 잘 쓰는 라이브러리가 Bootstrap인데 나중에 알아보자. 

 

 
<br>
 

 

 

 

 

### class 작명할 때 창의력이 딸려서 어렵다면

 

이것도 방법이 하나 있다. BEM 이라는 작명법을 따르면 생각안해도 되어서 편리하다.

배우기 위해 예제를 하나 가져왔는데 예전에 했던 Profile 소개 섹션을 다시 만든다고 가정하자. 

 

 
```
<div>
  <img>
  <h4>이름</h4>
  <p>소개글</p>
  <button>빨간버튼</button>
  <button>파란버튼</button>
</div>
```
HTML은 이렇게 생겼다.

그럼 여기에 있는 모든 HTML 요소에 class명을 한번 작명해보자.

class를 6개나 작명해야하기 때문에 창의력이 딸릴 수 있는데 BEM 룰을 적용해보면 작명이 쉬워진다.

 

 
<br>
 

 

 
```
<div class="profile">
  <img class="profile">
  <h4 class="profile">이름</h4>
  <p class="profile">소개글</p>
  <button class="profile">빨간버튼</button>
  <button class="profile">파란버튼</button>
</div>
```
**1. class를 작명할 땐 우선 덩어리이름으로 시작하는게 좋다.**

덩어리를 전문용어로 컴포넌트라고 하니까 그렇게 부르겠다.

아무튼 프로필 소개하는 html 컴포넌트를 만들 것이기 때문에

거기 안에 있는 모든 class명은 일단 profile 어쩌구로 우선 작명하면 된다.

 

 
<br>
 

 
```
<div class="profile">
  <img class="profile__img">
  <h4 class="profile__h4">이름</h4>
  <p class="profile__content">소개글</p>
  <button class="profile__button">빨간버튼</button>
  <button class="profile__button">파란버튼</button>
</div>
```
**2. 태그마다 다른 class명을 부여하려면 __태그명을 뒤에 붙인다.**

그니까 profile 안에 있는 img 태그는 profile__img

그니까 profile 안에 있는 button 태그는 profile__button

이렇게 __태그이름 으로 작명하라는 것이다.

이러면 작명할 때 생각 깊게 안해도 된다.

태그 이름 쓰기 싫으면 content 이런 식으로 작명해도 됨. 

 

 <br>

 

 
```
<div class="profile">
  <img class="profile__img">
  <h4 class="profile__h4">이름</h4>
  <p class="profile__content">소개글</p>
  <button class="profile__button--red">빨간버튼</button>
  <button class="profile__button--blue">파란버튼</button>
</div>
```
**3. 같은 태그들의 디자인을 구분하려면 --**

그니까 버튼이 색깔별로 여러개가 필요하다면 

빨간 버튼은 --red

파란 버튼은 --blue 를 뒤에 붙여서 작명하라는 것이이다.

큰 버튼은 --big

작은 버튼은 --small 이렇게 맘대로 수식어를 붙이면 된다. 

 

 

BEM 룰을 쉽게 외우려면

Block__Element--Modifer 이런 식으로 기억해주시면 된다.

HTML 요소를 영어로 Element라고 하며 Modifier는 수식어라는 뜻이다. 

 

 

 

 <br>

 

근데 지금 설명한 OOCSS 클래스 작성방식, BEM 작명방식 이런건 

html css 파일이 크고 방대할 때 장점을 보이는 것이기 때문에 

요즘 React, Vue를 이용해서 웹페이지를 만들 때는 크게 유용하진 않다.

React 이런 곳에선 html 페이지 단위가 아니라 작은 UI 단위로 개발하게 되며

UI 덩어리들끼리 class명이 서로 중복되어도 상관없어서 코드를 마구 작성해도 되기 때문이다.

class명 중복을 알아서 제거해줘서 그런데 대표적으로 React 안에서 styled-components, module CSS 등의 라이브러리를 쓰면 그런게 가능하다. 

그래서 클래스명 막 넣어도 되니까 BEM 이런거 깊게 익힐 필요는 없고 여기서 설명하는 것 까지만 알아도 충분하다.

<br>
<br>
