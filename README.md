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
