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