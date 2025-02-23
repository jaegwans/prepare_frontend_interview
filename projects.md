## 프로젝트 관련

### 코플릭스

-   리액트 네이티브와 리액트의 차이점

    -   화면 출력시 react는 reactDom을 이용하고 rn은 AppRegistry 이용
    -   rn은 html 태그를 이용하지 않고 자체 태그를 사용
    -   기존 css가 사용되지 않고 js파일 내에서 StyleSheet사용

-   해당 프로젝트의 구조를 설명해주세요.
    -   기본 키워드를 기반으로 유투브를 통해 영상을 가져오고 백준 크롤링을 통해 코딩테스트 추천 문제를 가져옵니다. 이후 추천 이력서와 키워드 편집 페이지를 제공했습니다.
-   왜 타입스크립트를 사용했나요?
    -   런타임 이전에 타입 에러를 체크할 수 있고 이외에도 자동완성, 인터페이스 검사(특정 객체의 구성 검증), 코드 가독성 및 유지보수 향상의 장점이 있습니다.
    -   인터페이스와 타입의 차이가 뭐죠?
        -   인터페이스: 객체권장, extends,중복할당시 병합,캐싱 가능(확장시 성능 이점), 암묵적 인덱스 시그니처 불가능
        -   타입: 모든 타입,&,중복할당시 에러,캐싱 불가,암묵적 인덱스 시그니처 가능
-   해당 프로젝트의 도전 과제는 무엇이었나요?
    -   왜 로컬스토리지 사용했죠?
        -   추후 확장 가능성
-   왜 ssr을 활용했나요?
    -   어떻게 로딩 속도를 줄일 수 있을까요?
        -   렌더링 최적화. lighthouse등을 통한 분석 이후 판단
-   솔리드 원칙에 대해 설명해보세요.
    -   어떻게 컴포넌트에 단일책임원칙이 적용되었나요? 컴포넌트의 역할이란 뭔가요?
        -   컴포넌트를 최소 기능으로 분리,재사용성,유지보수, 추후 테스팅에 유리할 수 있습니다.
-   GCP 를 적용하면서 어려웠던 점이 있었나요?
    -   자동화 코드를 작성하는 것과 docker npm 문제
-   ## SEO 최적화를 어떻게 진행할 수 있었나요?
-   recoil과 react-query를 모두 적용했는데 두 상태관리 툴의 차이점을 말해보세요.
    -   recoil
        -   상태관리
        -   atom 기반
    -   react-query
        -   서버 상태관리
        -   데이터패칭, 동기화, 캐싱 등 이점
-   백준 크롤링을 어떻게 진행했나요?
    -   axios를 통한 get요청(User-Agent 설정) -> cheerio (문서 파싱 모듈) -> 데이터 제공
-   ## 랜더링 최적화를 위한 방법을 사용했나요?
    -   React.memo 사용 - 편집페이지

### 돈워리

-   왜 next.js를 선택했죠?
    -   react와 차이점이 뭔가요?
        -   ssr,최적화, 미리 준비된 라우팅 등
-   구글 솔루션 첼린지가 뭔가요?
-   상시 코드리뷰를 통해 어떤점을 얻어갈 수 있었나요?
    -   개발 생산성(중복코드 발견)
    -   상호 도움(문제 코드 조기 발견)
-   팀원간 실력 격차에 대해 어떻게 해결할 수 있을까요?
    -   하위 팀원에 대한 교육 및 향상 도모
-   로그인 로직을 어떻게 구현했나요?
    -   localstorage를 통해 accessToken 저장
-   fetch와 axios 차이
    -   fetch : 내장, 편의기능 미제공, 명시적으로 데이터 추출 필요
    -   axios : 외부, 편의기능 제공, json형태로 자동 데이터 반환
-   커스텀 훅의 사용 예시와 이점
    -   뷰와 로직을 분리함
    -   useDelay() //애니메이션 딜레이를 위한 훅

### 모이다

-   로그인 로직은 어떻게 구현했나요?
    -   왜 jwt로 구현했나요 ?
        -   서버 리소스
        -   모바일
-   seo를 성능 향상 시키기 위한 방법은 무엇이 있나요?
    -   메타 태그를 활용해 사이트의 정보 제공= 네임과 컨텐츠
    -   적절한 시멘틱 태그 활용 ,ssr, 내부구조
    -   https
-   컴포넌트 기반 스타일링의 장점은 무엇인가요?
    -   컴포넌트 기반 개발 가능, 동적 스타일링 및 가독성 유지보수
-   CORS문제가 뭐고 어떻게 해결했나요?
    -   교차 출처 자원 공유 문제로 브라우저단에서 발생합니다.
    -   호스트가 서로 다른 곳에서 요청을 보낼때 보안을 위해 차단하는 정책을 말합니다.
    -   해결을 위해 백엔드와의 소통 혹은 프론트단에서의 프록시가 있을 수 있습니다.
        -   access-Control-Allow-Origin
        -   withCredentials

### 지뢰찾기

-   props drilling이란
    하위컴포넌트로 props전달을 통해 중간 컴포넌트를 거치는 것
-   FLUX 패턴이란
    -   상태를 store에서 관리하여 상태의 대한 수정(액션)은 디스패치를 이용하여 단방향으로 뷰와 상태가 관리되는 패턴
-   dfs와 bfs 설명
    -   왜 bfs로 구현했나요?
        -   큐를 이용하여 가까이 있는 노드부터 탐색하기 때문
-   redux를 이용한 상태관리
    -   slice와 reducer 그리고 store등록
    -   dispatch(action) 사용

### 웨더코디

-   aap를 사용하지 않은이유
    -   개발 당시 비필수.
-   expo의 장점은 무엇인가요?
    -   다양한 라이브러리 제공(expo-location등)
-   bare프레임워크란 expo의 최소한의 기능만을 포함함과 동시에 네이티브 요소를 사용할 수 있음

### 안드로이드

https://sikeeoh.medium.com/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%EA%B0%9C%EB%B0%9C%EC%9E%90-%EB%A9%B4%EC%A0%91-%EC%A7%88%EB%AC%B8%EB%A6%AC%EC%8A%A4%ED%8A%B8-63e1de17453b

### ios

https://github.com/JeaSungLEE/iOSInterviewquestions

### 해커스 예상
-   개인주의적 회사 문화가 중요한가
-    최종적 삶의 목표
-    야근에 대한 생각
-    나이에 대한 생각
-    출퇴근시간
-    
