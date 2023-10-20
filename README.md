# **코리아 IT 아카데미 앱개발**
## CSS 수업정리

### Visual Code 한글 설정
좌측 하단 마켓 플레이스(확장) 아이콘 클릭 > korean 검색
>클라이언트 : 서버에게 요청해주는 대상

### Visual Code 언어 설정 변경
```
F1 또는 Ctrl + Shift + p > Configure Display Language 입력 > 언어 선택(en, ko) > 재시작
```

### Visual Code 테마 변경
```
F1 또는 Ctrl + Shift + p >
한국어로 설정 시 : 테마 검색 > 색 테마 클릭 > 원하는 테마로 변경
영어로 설정 시 : theme 검색 > color theme 클릭 > 원하는 테마로 변경

마케플레이스(확장) 아이콘 클릭 > theme 검색 > Material Theme 설치
마켓플레이스 목록의 Material Theme 톱니바퀴 아이콘(설정) 클릭 > 색 테마 설정
```

### Visual Code에서 html파일 실행하는 방법
1. 해당 경로로 직접 들어가서 크롬브라우저로 실행한다(불편해서 못함)
2. 마켓 플레이스에서 open in browser 설치, Alt + b로 실행 <br>
  만약 크롬브라우저로 실행되지 않는다면 <br>
  해당 html파일 우클릭 > 연결 프로그램 > <br>
  다른 앱 선택 > 항상 .html을 이 앱으로 실행 체크 > Chrome 선택
4. 마켓 플레이스에서 live server 설치, Alt + l 그리고 Alt + o로 실행 <br>
  문서가 저장되면 바로 화면에 반영됨.

### Visual Code settings.json
```
{
  "editor.fontSize": 15,
  "editor.tokenColorCustomizations": {
    "comments": "#ef7a05"
  },
  "workbench.colorCustomizations": {
    "editor.selectionBackground": "#10813f",
    "editor.wordHighlightBackground": "#10813f",
    "editorCursor.foreground": "#ffffff",
    "[Material Theme Darker High Contrast]": {}
  },
  "explorer.confirmDelete": false,
  "security.workspace.trust.untrustedFiles": "open",
  "javascript.validate.enable": false,
  "json.schemas": [],
  "liveServer.settings.donotShowInfoMsg": true,
  "jupyter.askForKernelRestart": false,

  "emmet.triggerExpansionOnTab": true,
  "emmet.excludeLanguages": [],
  "emmet.showSuggestionsAsSnippets": true,
  "emmet.useInlineCompletions": true,

  "prettier.tabWidth": 2,
  "prettier.printWidth": 100,
  "prettier.semi": true,
  "prettier.singleQuote": true,

  "editor.fontLigatures": false,
  "editor.formatOnSave": true,
  "explorer.compactFolders": false,
  "open-in-browser.default": "chrome",

  "files.autoSave": "afterDelay",
  "editor.cursorWidth": 2,
  "workbench.colorTheme": "Material Theme Darker",
  "liveServer.settings.donotVerifyTags": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.fontVariations": false,
  "window.zoomLevel": 3
}
```

## CSS란
```
CSS는 Cascading(**우선순위) Style Sheets의 약자이다.
CSS는 HTML 요소들이 각종 미디어에서 어떻게 보이는 가를 정의하는 데 사용한다.
스타일을 HTML문서로부터 분리하는 것이 가능해진다.
```

### CSS를 사용하는 이유
```
HTML만으로 웹 페이지를 제작할 경우, HTML 요소의 세부 스타일을
일일이 따로 지정해주어야 하기 때문에 많은 시간이 걸리며, 완성한 후에도
스타일의 변경 및 유지보수가 매우 힘들어진다.
이 문제점을 해소하기 위해서 W3C에서 만든 스타일 시트 언어가 바로 CSS이다.
웹 페이지의 스타일을 별도의 파일로 저장할 수 있게 해줌으로써 사이트의 전체 스타일을
손쉽게 제어할 수 있게 된다. 또한 웹 사이트의 스타일을 일관성있게 유지할 수 있도록 해주며,
그에 따른 유지보수 또한 쉬워진다.
```

### CSS 문법
```
p { text-align: center; color: blue;}
  === ---------- -------  -----  -----
[선택자] 속성명   속성값 속성명 속성값
==========================
                 [선언부]
```
1. CSS의 문법은 선택자와 선언부로 구성된다.
2. 선택자는 CSS를 적용하고자 하는 HTML 요소를 가리키고 <br>
 선언부는 중괄호({})를 사용하여 전체를 둘러싼다.
3. 각 선언은 CSS 속성명과 속성값을 콜론(:)으로 연결한다.
4. CSS 선언은 언제나 마지막에 세미콜론(;)으로 끝마친다.

### CSS 선택자
1. 전체 선택자
    1. 스타일을 모든 요소에 적용할 때 사용한다.
    2. 전체 선택자는 asterisk(*) 기호를 사용한다.
```
alt + l + o -> html 실행창
```
2. HTML 태그 선택자
    1. 특정 태그가 쓰인 모든 요소에 스타일을 적용한다.
    2. 선택자 위치에 태그명을 작성하면 사용된 모든 해당 태그에 동일한 스타일이 적용된다.
3. 클래스 선택자
    1. 클래스 선택자는 특정 집단의 여러 요소를 한 번에 선택할 때 사용한다.
    2. 같은 클래스 이름을 가지고 있는 요소들을 모두 선택해주고 스타일 적용 시 <br>
        선택자에 " .클래스명 "을 작성해준다.
4. 아이디 선택자
    1. 아이디 선택자는 특정 요소를 선택할 때 사용한다. -> ***중복 안되요
    2. 스타일을 지정할 때 사용한다. 선택자 부분에 "#아이디명"을 작성한다.
```
※ 아이디와 클래스의 차이점
      class 속성 값에 여러 개의 이름을 작성할 수 있고 각 이름은 공백으로 구분한다.
      id 속성 값에는 단 한 개의 이름만 작성할 수 있다.
      class는 여러 태그에서 동일한 이름을 작성하여 묶어주는 목적이 있고,
      id는 한 개의 태그를 특정시킬 때 사용되기 때문에 중복이 없어야 한다.
      하지만 id도 중복으로 사용되었을 때 CSS 스타일은 똑같이 반영되긴 한다.
      하지만 id는 절대 중복해서 사용하지 않아야 한다. -> id, class 차이점 ->
        거의 class를 씀 ->id는 -> input tag java script를 쓸때 -> $("#userId") 클래스 ->$(id="userId") = id
      id와 class 속성이 동시에 적용된 태그가 있을 경우, id 선택자의 스타일이 적용된다.
```
5. 그룹 선택자
    1. 여러 선택자에 같은 스타일을 적용할 경우 쉼표로 구분해서 여러 선택자를 나열한 후 <br>
         스타일은 한 번만 정의한다.
6. 상속 선택자
    1. 부모 태그와 자식 태그를 구분하여 정확히 해당 태그의 소속을 작성한다.

### 캐스캐이딩(Cascading)
하나의 요소는 하나 이상의 CSS 선언에 영향을 받을 수 있다. <br>
이 때 충돌을 피하기 위해서 CSS 적용 우선순위가 필요하다.
1. 중요도 : CSS가 어디에 선언되었는지에 따라서 우선순위가 달라진다.
    1. 인라인 스타일 (HTML 태그 내부에 style 속성으로 사용) -> 안에다가 style 쓴거
    2. 내부 스타일 시트(HTML 문서의 style 태그 안에 위치) -> <style> </style> 에서 바꾸는거
    3. 외부 스타일 시트(CSS 파일을 외부에 따로 만들어서 불러오는 방법) -> css파일 따로 만들어서 쓰는거
    4. 웹 브라우저 기본 스타일
```  
우선순위는 (1) > (2) > (3) > (4) 순이다.
인라인 스타일의 우선순위가 가장 높다.
```
2. 명시도 : 명확하게 특정할 수록 우선순위가 높아진다.
```
p, .a, p.a, div p.a
!important > 아이디 선택자 > 클래스 선택자 > 태그 선택자 > 전체 선택자 > 상속받은 속성

!important를 이길 수 있는 스타일은 없지만 중요도에 따라서 같은 important일지라도 우선순위가 달라진다.		
```
3. 선언 순서 : 나중에 선언된 스타일이 우선 적용된다.

## 시멘틱 태그
- 시멘틱: "의미가 있는"
- HTML5에 도입된 시멘틱 태그는 개발자와 브라우저에게 의미있는 태그를 제공한다.

### 태그의 종류
```
<div>: non-semantic 태그, 안에 들어갈 의미를 크게 유추하기 힘들다.
<header>, <footer>, ... : semantic 태그, 특정 형태의 글이 포함될  것이라는 유추가 가능하다.
```

### 시멘틱 태그의 종류
- header: 상단, 헤더를 의미
- nav: 메뉴, 네비게이션을 의미
- section: 여러 중심 내용을 감싸는 공간을 의미
- main: 내용의 중심을 의미
- article: 글자가 많이 들어간 부분을 의미
- aside: 사이드에 위치하는 공간을 의미
- footer: 하단, 푸터를 의미

## 그리드 레이아웃을 활용한 이미지 갤러리
### 정형 그리드 레이아웃
```
가로 세로 길이가 모두 일정하게 정해져있는 형태
반복문을 통해서 자동으로 그려 줄 수 있는 형태 이기 때문에
보여주고자 하는 데이터의 갯수가 유동적으로 변화할 때 
사용하기에 적합하다(10개, 5개, 20개)
```
### 비정형 그리드 레이아웃
```
가로 세로 길이가 제각각인 형태
보통 데이터의 갯수 자체가 고정적일 때 사용하기 적합
(개별적으로 각각 다른 값들을 적용 해야 하기 때문에)
```

### 변형
- html요소의 디자인을 변형시킬 때 사용하는 속성
- 원래 나타나야하는 위치에서 오른쪽으로 조금 이동, 아래로 조금이동, <br>
  원래 크기의 1.2배로 만들어줘, ...(회전...)

### transform 
요소확대, 회전, 이동, ... 이러한 디자인 적용시키고 싶을떄 사용
```
translateX(단위) : X축으로 단위만큼 이동시킨 디자인 적용시켜줘
translateY(단위) : Y축으로 단위만큼 이동시킨 디자인 적용시켜줘
translate(a, b) : X축으로 a만큼, Y축으로 b만큼 이동시킨 디자인 적용
```

## transition
```
property duration function delay -> 순서
ex) transition : width height background-color 3s ease 0.2s
ex) transition : 2s
```
- 디자인이 변화할 때 적용시킬 속성
- 아래 있는 네개의 속성을 한번에 설정하는 단축속성

### transition-property
서서히 변화를 주고 싶은 대상이 되는 css 요소를 지정할때 사용하는 속성

### transition-duration
얼마나 서서히 변하게 할 것인지 지속시간을 설정하는 속성 <br>
단위는 s (초) 혹은 ms (밀리초) 를 사용, 기본값은 0s

### transition-timing-function
트랜지션 효과를 위한 수치함수 지정

### transition-delay
대기하는 시간을 s(초) 혹은 ms(밀리초)로 지정

### CSS 유용한 단축키
```
라이브 서버 실행(html 문서를 브라우저로 열기) : alt + l + o
복사 붙여넣기 : alt shift 위/아래화살표
코드 위아래 이동 : alt 위/아래화살표
포멧 정렬 : ctrl k f
주석 : ctrl /
전체 드래그 : ctrl a
```

### 폰트 적용
구글 웹폰트
1. html 문서 속의 <head> 태그 안쪽에다가 <link> 태그를 추가한다. <br>
    이후 css 문서에 font-family 속성을 사용하여 폰트 적용
2. css 문서 안에다가 @import 사용하여 코드를 추가하고 <br>
    이후 font-family 속성을 사용하여 폰트 적용
```
font-family : '폰트이름1' , '폰트이름2', ....
    --> 폰트이름1이 설치되어있다면 그걸로 보여준다.
    --> 설치가 안되어있다면 폰트이름2를 적용
    --> 설치가 안되어있다면 ....
```

### 애니메이션
(트랜지션의 발전된 형태) <br>
한 컷 한 컷을 정의해놓고, 연속적으로 재생해줘 라고 하면 움직이는 것처럼 보이게 된다.

### keyframe
애니메이션의 이름이 되며, 각각의 시간의 흐름에 따라 적용해야할 디자인을 정의해 놓는다.

### animation-iteration-count
몇회 재생시킬 것인가 <br>
infinite --> 무한 재생

### animation-direction
어떠한 방향으로 재생시킬 것인가
```
normal : 0 --> 100, 0-->100, 0-->100 , ...
reverse : 100--> 0 , 100->0, 100->0, ...
alternate : 0-->100, 100-->0, 0-->100, ...
alternate-reverse: 100-->0, 0-->100, 100->0, ...
```

### animation-fill-mode (기본값 : none)
```
none : 애니메이션 끝나고 애니메이션 적용 안된 상태 유지
forwards : 애니메이션 끝나고 애니메이션이 끝났을때 마지막 상태 유지
backwords : 애니메이션 딜레이 시간동안 시작상태를 유지
both : 애니메이션 딜레이 동안 시작상태 유지 + 애니메이션 끝나고 마지막상태 유지
```

### animation-play-state (기본값 : running)
- running : 애니메이션 재생 상태
- paused : 애니메이션 중지 상태
```
2배 확대 --> 0.5배축소 --> 3배확대
@keyframes 애니메이션이름 {
    10% {
        transform:scale(2);
    }

    30% {
        transform:scale(0.5);
    }

    100% {
        transform:scale(3);
    }
}

div.ball {
    width : 100px;
    height : 100px;
    border-radius:50%;
    background-color:black;
    transition:1s;
}

div.ball:hover {
    width : 100px;
    height : 100px;
    border-radius:50%;
    background-color:black;
    transition:1s;
    transform:scale(2);
}
```

### 반응형 웹사이트 제작
- 반응형 웹사이트란? 웹사이트의 화면이 달라지더라도 웹사이트 구성 요소들이 <br>
  일괄적으로 전달되도록 구현하는 방법론
- 컴퓨터, 노트북, 태블릿, 모바일을 사용하여 웹사이트에 접속 하더라도 <br>
  동일한 질의 사용자 경험을 제공해야 한다.

### 미디어 쿼리
사용자가 웹사이트를 보는 화면 조건에 알맞게 서로 다른 css를 적용시키기 위해 사용한다.

### 미디어 유형에 따른 조건
```
screen : 컴퓨터 혹은 스마트기기의 화면
tv : 영상 + 음성이 출력되는 장치
projection : 프로젝터
```

### 가로길이에 따른 조건
```
width : 웹사이트의 가로 길이에 따른 조건
max-width : 웹사이트의 최대 가로길이에 따른 조건
min-width : 웹사이트의 최소 가로길이에 따른 조건
device-width : 기기의 가로길이에 따른 조건
```

### 세로길이에 따른 조건
```
height : 웹사이트에 세로 길이에 따른 조건
max-height : 웹사이트의 최대 세로길이에 따른 조건
min-height : 웹사이트의 최소 세로길이에 따른 조건
device-height : 기기의 세로길이에 따른 조건
```

### 화면 방향에 따른 조건
- orientation : landscape --> 가로일때 적용할 디자인
- orientation : portrait --> 세로모드일때 적용할 디자인
조건 여러개를 동시에 설정하는 방법은 and 를 사용한다.
```
@media 조건1 and 조건2 and 조건3 {
    div {
        backbround-color:red;
    }

    p {
        font-size:50px;
    }
}

--> 조건1과 그리고 조건2와 그리고 조건3을 모두 만족하는 경우에 적용되는 디자인


보통은 모바일, 테블릿, 데스크탑
0~600 모바일
600~1024 태블릿
1024~ 노트북이나 데스크탑(PC)
```

### 
