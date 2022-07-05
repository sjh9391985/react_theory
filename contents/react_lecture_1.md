# React 작동원리

### react v15 이전 
    - class component 사용

### react 16 이후
    - function 사용
    - context api 사용
<hr/>

### SPA(Single Page Application) 란?

    - ES Next ~ > ES5 [Babel / 2014y 등장]
    - 10개의 jsx 파일들이 있고 한번에 다 받으면, 더 이상 서버에 가지 않음.
    - 서버에 갈 경우 ajax로 call (network 비용이 줌)
    - 대신 화면 갱신시 10개 파일이 있을 경우 다 받아야함.
    - HTML을 클라이언트에서 렌더링

### SSR(Server Side Rendering), SSG(Server Side Generation) 란?

    - A ~> B 페이지 이동시 B에 해당하는 페이지는 이동시에 가져옴 (서버에서 페이지를 내려줌)
    - HTML을 서버에서 렌더링
    - SSG: 잘 바뀌지 않는 항목들을 HTML에 박아놓음[webpack build시 DB에서 select]

### 실무 react 작동원리

    - CSR 작동방식의 Base
    - react는 react element 단위로 되어있음.
    - element 단위로 되어 있기에 JSX 컴파일시 변환
    