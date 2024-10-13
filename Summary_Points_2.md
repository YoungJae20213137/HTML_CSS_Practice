# <font color="green"> <b> Summary Points 2 </b> </font>

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

##

 
