# spa-practice
NodeJS ReactJS로 만드는 SPA 어플리케이션

# Tech Stack

## Client
React with typescript, mobx

## Server
Node with typescript

# Package manager

## yarn vs npm

성능, 안정성에서는 비슷비슷하나

yarn 은 yarn.lock 파일을 이용하여 모든 디바이스에서 똑같은 패키지 버전 설치를 보장하기 때문에 보안성이 좋다.

패키지 버전이 다름으로써 생기는 버그나 보안 이슈를 방지할 수 있기 때문.


# Why NodeJS?

단일 스레드 이벤트 루프 기반 (비동기 IO (Non Blocking IO))
- 하나의 스레드가 IO 요청을 해놓고 바로 다음 작업으로 넘어간다.
- IO가 끝나면 Callback 을 통해 해당 작업을 처리한다.

reference : [링크](https://junspapa-itdev.tistory.com/3)


# SPA?

단일 페이지로 구성. 배포가 간단하고 네이티브 앱과 유사한 UX 제공.

- 장점
    - 정적 리소스를 최소에 한번 다운로드한다
        - 새로운 페이지 요청 시 페이지 갱신에 필요한 데이터만 받기 때문에 트래픽 감소
        - 변경되는 부분만 렌더링 하기 때문에 새로고침 X
- 단점
    - 초기 구동 속도가 느림
        - 모든 정적 리소스를 최초 접속 시 다운로드하기 때문.
    - SEO(검색 엔진 최적화) 문제
        - 클라이언트 렌더링 방식이기 때문
        - SPA 프레임워크에서 SEO 대응 기술이 존재.

reference : [링크](https://poiemaweb.com/js-spa)

# Why React JS?

What is React?
- 컴포넌트라는 개념에 집중이 되어 있는 라이브러리
- React는 프론트엔드 라이브러리
    - 귀찮은 DOM 관리와 상태값 업데이트 관리를 최소화.
    - UI 구현에 집중하기 위한 라이브러리.

Virtual DOM
- 데이터가 바뀌었을때, Virtual DOM 을 통해서 일단 렌더링하고, 비교한 뒤 바뀐 부분만 찾아서 바꿔준다.
- Virtual DOM을 통해서, DOM 변화를 최소화. 이 횟수를 최소화 시키는 것이 매우 중요. 

reference : [링크](https://velopert.com/3612)

## 주의사항
- DRY (Don't Repeat Yourself)
    - 중복되는 코드를 최소화하여 컴포넌트를 사용하자.