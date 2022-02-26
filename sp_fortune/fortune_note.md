1. 클라이언트 - 서버

    브라우저가 naver.com 요청하는 순간,  
    네이버 서버가 자신의 원본을 복사해서 우리에게 보여준다.
    
    - 클라이언트 역할 : **서버에 요청**을 보내고 복사본을 받아와서 그 복사본을 예쁘게 보여준다.
    - 서버의 역할 : 요청이 들어오면 ***자신이 가지고 있는 원본***을 **복사**해서 요청한 이에게 보낸다.
    
     ⚙서버 동작방식⚙
    
    실제로 동작하는 <u>서버는 모두 약속들이 정해져 있다. </u>  
    이러한 약속들을 **API**라고 함
    
    ➡ naver.com을 요청하면 
    네이버 홈페이지를 보이는 것처럼 약속이 정해져있고,  
    HTML / CSS / Javascript로 이루어진 원본 파일을 복사해서 클라이언트에게 넘겨준다.
    
    ![클라이언트-서버관계](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f4770f1b-1509-4e69-b971-1cd5ceb258a6/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220125%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220125T110410Z&X-Amz-Expires=86400&X-Amz-Signature=6f4e0b36a59f763fba61322228b6ba9cdeb62a437b4514c1e837ae17db5cc2af&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
2. HTML, CSS
    - HTML : 뼈대 / 위치 / 문자  
    HTML은 head와 body로 나뉜다.
        - body : 실질적인 내용 (meta, script, link, title)
        - head :  body를 제대로 표현하기위해 필요한 것들 (페이지 속성/정보)
    - HTML로 작성한 것을 브라우저가 그려준다.

    - CSS : *HTML을 꾸미는* **세부적인 조절**
        - 특정글자를 초록색으로 바꾼다 (⭕)  
        어떤 초록색이 가장 예쁜가? (❌)  
        예쁘게 만드는 부분은 *웹 디자이너와 웹 퍼블리셔의 영역*
3. CSS 기초
    - CSS는 꾸미기 기능  
    head는 body를 온전히 잘 표현하기 위한 기능이므로
    `<style>`는 `<head>` 안에 위치한다.

    - CSS 적용할 때 기억할 두가지
        - 누구를
        - 어떻게  

    ➡ '누구를', '어떻게' 꾸며줄 것인지 항상 명시해야 한다.

    - CSS Step)

        1️⃣ div 태그에 '명찰'을 달아준다.

        (이름표를 달아주는 class와 id)

        2️⃣ 명찰을 가지고 있는 것을 꾸며준다.

    - ex.  
        `.mytitle { color: red; }`

        클래스가 mytitle인 것을(누구를)  
        글자를 빨간색으로(어떻게) 꾸며라!

        `.mytitle > h1`

        mytitle 클래스를 가진 <u>**`<div>`안에 (>) 있는</u> `<h1>`**

4. CSS 적용하기 - 배경
    - `<body>` : 화면 전체를 나타냄  
        `<body>`에 CSS 요소인 <u>`background` 속성</u>을 적용하면  
        **화면 전체에** 테마가 적용된다.
        
    - 이미지 배경화면 구성  
        어떤 이미지, 어느 위치, 반복해서 넣을 것인지를 명시해야 한다. 

        - `background-image` :  배경에 이미지 삽입  
        url('') : 어떤 이미지 파일인지 작성
        
        - `background-position` : background-image의 위치 조절  
        원하는 위치에 이미지를 배치하기 위한 속성
        
        - `background-repeat` : 배경에 이미지 반복을 설정  
        `no-repeat` 속성 값 : 이미지를 반복하지 않음
5. 폰트 입히기  
    - 폰트 다운로드 ([구글웹폰트](https://fonts.google.com/?subset=korean))  
    `<link>` 이용해서 필요한 폰트 파일들을 알아서 웹 브라우저가 다운로드 해준다.  
    `<link href="https://fonts.googleapis.com/css2?family=Yeon+Sung&display=swap rel="stylesheet">`

    - CSS 적용  
    폰트를 다운받아도 ‘누구를’ ‘어떻게’ 바꾸라는 명령이 없다면 브라우저는 알아듣지 못한다.  
        - ‘모든 태그(*)를 이 폰트(font-family)로 바꿔라’  
    `* {font-family: 'Yeon Sung', cursive;}`
6. CSS 적용하기 - 원형 배치
    - a 태그  
    href : 클릭했을 때 어디로 보낼 것인가  
    href ="#" : 그대로 있어라 (#)
        - 글자를 표현하는 태그  
        실제로 적힌 글자가 없어도 공간을 차지하려면
        1️⃣ `display : block;`  
        2️⃣ `width` 가로 설정  
        3️⃣ `height` 높이 설정

    - flex 속성  
    특정 div안에 있는 요소들을 정렬할때 사용  
    1️⃣ `display : flex;`  
    2️⃣ `flex-direction : row / column;`  
    3️⃣ `justify-content : center;`  
    - `flex-wrap: wrap;`  
    각각의 요소들이 기존의 넓이를 갖도록 한다.  
    브라우저 가로-길이 변동에 따라 줄바꿈이 된다.
1. CSS 적용하기 - 배경 이미지 삽입
    - div 중앙 배치   
    `margin: auto;` margin 값을 동일하게 가져라  
    = 버튼을 담고 있는 div 너비 이외의 나머지 영역의 왼쪽-오른쪽을 동등하게 가져라

    - 요소의 배경 이미지  
    영역에 특정 이미지를 백그라운드에 꽉 차게 넣고 싶다면  
    1️⃣ `background-image : url('');`  
    2️⃣ `background-size : cover;`  
    3️⃣ `background-position : center;`
1. hover 적용하기
    - `:hover` 특정 대상에 마우스를 올렸을 때
    ```CSS
    .rtans > a:hover {
        background-color : darkred;
    }
    ```
1. hover - 글자 나타내는 효과
    - `button`처럼 구성된 `<a>` 글자 작성이 가능하다.   
    - `<a>` 기본 배경색 `background-color:white;`  
    글자 색상 지정  `color:white`  
    마우스 올렸을 때(hover) `background-color:darkred;`   
    > 배경색 변경으로 hover 상태에서만 글자가 보이는 방식  
    
    > hover 상태가 아닌 경우,
    > 배경색과 글자색이 같아서 글자가 화면에 나타나지 않음
1. result.html 구조  
    하나의 HTML으로 12개의 다른 결과가 보여야 한다.  
    이러한 동적인 변화를 위해 자바스크립트를 활용
    - 가운데 정렬  
    margin : 상단 우측 하단 좌측 (시계방향)  
    `margin : 80px auto 50px auto;`  
    상단 80px / 하단 50px  
    좌우 auto 같은 비율로 가운데 정렬 
1. 메시지 만들기  
    - 제목(굵은 글씨) -> `<h1>`
    - 운세(덜 굵은 글씨) -> `<p>`
    > 글 색상, 정렬을 위해 명찰(class)을 통해 CSS 처리 !
    - `<br>` : 채팅방에서 치는 enter 키와 같은 줄바꿈 기능  
    - `line-height` : 줄간 간격 속성  
1. 버튼 배치하기  
    - 수평으로 배치  
    `<div>` 안에 `<button>` 두 개를 넣는다.
    - 가운데 정렬  
    `<div>` 태그 안에 있는 내용물 `<button>`들을 가운데 정렬  
    1️⃣ `display : flex;`  
    2️⃣ `justify-content : center;`  
    3️⃣ `flex-direction : row;`  
    - 버튼 꾸미기  
    `cursor: pointer;` 마우스 모양이 포인터 모양으로 표현  
    사용자 입장에서 클릭 여부를 확인할 수 있다.  
1. 모바일 버전 처리하기
- #### CSS 조건
    (1) ‘누구를’ ‘어떻게’ (2가지)  
    (2) ’특정한 경우에’ ‘누구를’ ‘어떻게’ (3가지)   
    : '스크린 사이즈가 작을 때만 특정 CSS 적용'
- #### 모바일 환경 배치 
    `@media screen and (max-width:780px) { .rtans { width: 100%; } }`  
    - `@media` : 스크린 사이즈에 조건을 거는 쿼리  
    스크린 사이즈가 780px 보다 작을 때 (특정 경우)   
    - `width :100%;` 화면 크기에 꽉 차게 맞춘다.  
    - `flex-wrap: wrap;` : 'display: flex' 인 경우에만 동작  
    'flex-wrap' 속성으로 버튼의 사이즈 `width:150px` 그대로 유지되고  
    한 줄에 못 들어가는 버튼은 아랫줄로 배치되면서 한 줄에 2-3개로 보인다.  
14. javascript
- #### javascript 작성위치
    css는 `<style>`에 작성  
    javascript는 `<script>`에 작성
- #### 동작원리 
    `function back() { alert('뒤로가기!'); }`  
    지정한 동작을 실행하도록 저장하는 함수 (function)  
    `onclick="back();"`  
    해당 버튼이 클릭(onclick)되면 back 함수를 ‘실행’하라는 명령  
- #### 실제 화면을 뒤로가게 하는 ‘뒤로가기JS’
    ```javascript
    let url = window.location.href;
    let new_url = url.split('result.html')[0] + 'index.html';
    window.location.href = new_url;```
- #### 링크를 복사하는 ’공유하기JS’ 
    ```javascript
    var t = document.createElement("textarea");
    document.body.appendChild(t);
    t.value = window.location.href;
    t.select();
    document.execCommand('copy');
    document.body.removeChild(t);
    alert('복사 완료!');
    ```
- #### 자바스크립트 적용 순서 
1. script 태그에 원하는 함수 정의 
2. onclick 옵션에 함수명 작성 
3. 함수안에 코드를 작성하면 실행 됨  