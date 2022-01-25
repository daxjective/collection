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