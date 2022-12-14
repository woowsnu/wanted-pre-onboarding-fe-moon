
# Todo List (원티드 프리온보딩 프론트엔드 - 선발 과제)
<br/>

## 과제 요구사항

### :: 1. 로그인 / 회원가입
- `/` 경로에 로그인 / 회원가입 기능을 개발해주세요
  - 페이지 안에 이메일 입력창, 비밀번호 입력창, 제출 버튼이 포함된 형태로 구성해주세요
  - 로그인, 회원가입을 별도의 경로로 분리해도 무방합니다.

#### Assignment1

- 이메일과 비밀번호의 유효성 검사기능을 구현해주세요
  - 이메일 조건: `@` 포함
  - 비밀번호 조건: 8자 이상
  - 입력된 이메일과 비밀번호가 위 조건을 만족할 때만 버튼이 활성화 되도록 해주세요
  - 보안 상 실제 사용하고 계신 이메일과 패스워드말고 테스트용 이메일, 패스워드 사용을 권장드립니다.

#### Assignment2

- 로그인 API를 호출하고, 올바른 응답을 받았을 때 `/todo` 경로로 이동해주세요
  - 로그인 API는 로그인이 성공했을 시 Response Body에 JWT를 포함해서 응답합니다.
  - 응답받은 JWT는 로컬 스토리지에 저장해주세요

#### Assignment3

- 로그인 여부에 따른 리다이렉트 처리를 구현해주세요
  - 로컬 스토리지에 토큰이 있는 상태로 `/` 페이지에 접속한다면 `/todo` 경로로 리다이렉트 시켜주세요
  - 로컬 스토리지에 토큰이 없는 상태로 `/todo`페이지에 접속한다면 `/` 경로로 리다이렉트 시켜주세요

---

### :: 2. 투두 리스트

#### Assignment4

- `/todo`경로에 접속하면 투두 리스트의 목록을 볼 수 있도록 해주세요
- 리스트 페이지에는 투두 리스트의 내용과 완료 여부가 표시되어야 합니다.
- 리스트 페이지에는 입력창과 추가 버튼이 있고, 추가 버튼을 누르면 입력창의 내용이 새로운 투두 리스트로 추가되도록 해주세요

#### Assignment5

- 투두 리스트의 수정, 삭제 기능을 구현해주세요
  - 투두 리스트의 개별 아이템 우측에 수정버튼이 존재하고 해당 버튼을 누르면 수정모드가 활성화되고 투두 리스트의 내용을 수정할 수 있도록 해주세요
  - 수정모드에서는 개별 아이템의 우측에 제출버튼과 취소버튼이 표시되며 해당 버튼을 통해서 수정 내용을 제출하거나 수정을 취소할 수 있도록 해주세요
  - 투두 리스트의 개별 아이템 우측에 삭제버튼이 존재하고 해당 버튼을 누르면 투두 리스트가 삭제되도록 해주세요
 <br/>

## 프로젝트 실행 방법

    $ npm install
    $ npm start

-   위 순서대로 실행하면 localhost:3000 포트에 프론트엔드 서버가 실행됩니다.
-   백엔드 서버는 아래 링크에서 파일 다운로드 후 localhost:8000 포트로 실행하여 사용하였습니다.
-   https://github.com/walking-sunset/selection-task#%EB%A1%9C%EC%BB%AC-%EC%84%9C%EB%B2%84-%EA%B5%AC%EB%8F%99
  <br/>
  
## 구현화면 

<img src="https://user-images.githubusercontent.com/105709187/185537479-91d05e3b-db0f-484e-ba52-12dd4483d880.gif" />
<br/>

## 파일트리 📁

📦front  
 ┣ 📂public  
 ┃ ┗ 📜index.html  
 ┗ 📂src  
 ┃ ┣ 📂apis  
 ┃ ┃ ┣ 📜auth.js  
 ┃ ┃ ┣ 📜index.js  
 ┃ ┃ ┗ 📜todo.js  
 ┃ ┣ 📂components  
 ┃ ┃ ┣ 📂Auth  
 ┃ ┃ ┃ ┣ 📜Login.js  
 ┃ ┃ ┃ ┗ 📜Signup.js  
 ┃ ┃ ┗ 📂Todo  
 ┃ ┃ ┃ ┣ 📜AddTodo.js  
 ┃ ┃ ┃ ┣ 📜TodoItem.js  
 ┃ ┃ ┃ ┗ 📜TodoList.js  
 ┃ ┣ 📜App.js  
 ┃ ┣ 📜index.css  
 ┃ ┗ 📜index.js
<br/>
<br/>


## 느낀점

초기에 설계를 구체적으로 하지 않고 바로 api문서만 읽고나서 개발을 시작했다. 그러다보니 뒤로 갈수록 컴포넌트 간 데이터를 주고 받고 랜더링을 발생시키는 부분이 점점 꼬여서 난개발을 하게되어 많은 아쉬움이 생겼다. 초기 설계의 중요성을 다시 한번 새기게 되었다! 그리고 비동기 통신 문법은 익숙해졌으나 원리와 에러처리하는 부분에 대해 제대로 이해하지 못했던 것 같다. 이 부분에 대해 조금 더 깊게 공부를 해야겠다. 아쉬운 부분이 많아 제출 후 아래 리스트 내용대로 수정해 볼 예정이다. 혼자 공부할 때는 READ.ME를 신경써서 적지 않았었는데, 내가 했던 것들을 돌아보고, 개선 방향을 적어보는 것이 많은 도움이 되었다. 앞으로도 READ.ME와 회고에 더 신경을 써야겠다. 
<br/>
## Todo List의 Todo List ✏

[○] axios 라이브러리로 변경<br/>
[ ] 회원가입/로그인 같은 경로로 바꾸기 <br/>
[ ] 회원가입/로그인 유효성 체크로직 수정 (로그인 폼 제출 전 유효성 체크 후 다시 유효성 어긋나게 되는 경우에도 버튼 비활성화 ex)비밀번호 적었다가 다시 지웠을 때)<br/>
[ ] 회원가입/로그인 유효성 미충족시 인풋 하단에 알림 표시<br/>
[ ] 페이지 처리를 위한 pages 폴더 생성 후 App.js에서 pages 의 컴포넌트로 라우팅하게 하기<br/>
[○] 현재 useEffect로 컴포넌트에서 토큰 확인 후 리다이렉트 처리하는 부분 라우터 사용하는 방식으로 수정<br/>
[ ] 토큰확인, 로그인 체크를 context API로 변경 후 성공 시 리덕스 도전하기<br/>
[ ] 타입스크립트 적용해보기<br/>
[ ] .eslint rule, prettier 적용해보기<br/>
[ ] 페이지 배포하기<br/>
[ ] 배포된 서버에서도 잘 작동하도록 테스트 하기
