# redux-study

### Redux를 사용하는 이유 

- props drilling 방지
- state(상태) 관리 용이

### 주요 개념

외부에서 데이터 변경 막기(Immutability)

store: 전역으로 state 관리

reducer: state 수정 방법

dispathch: 컴포넌트에서 state 수정 요청

getState: 데이터 가져오기

#### state와 render의 관계

1. 리덕스의 핵심은 Store
2. Store는 정보가 저장되는 곳
3. Store 안에는 state라는 실제 정보가 저장된다.
    - state는 절대 직접 접근이 불가하다. 누군가를 통해야한다.
4. reducer
5. render는 UI를 만들어줄, 개발자가 작성할 코드 부분
6. Store에 접근 하기 전에, 일종의 창구 직원 역할하는 함수(dispatch, subscribe, getState)
7. render는 state 값을 참조해서, UI를 만든다.
8. state가 바뀔 때마다, render가 호출되게할 때, subscribe를 사용한다.

#### action과 reducer

1. submit을 눌렀을 때, 객체 하나를 전송한다. 이때 이 객체를 action이라고 한다.
2. 이 action은 dispatch에 전달된다.
3. dispatch는 2가지 일을 한다.
    - reducer를 호출해서, state 값을 바꾼다.
    - reducer에 현재의 state 값과, action을 값이 주어진다.
    - reducer의 return 하는 객체는 state의 새로운 값이 된다.
    - reducer는 state를 입력 값으로 가지고, action을 참조해서, 새로운 state 값을 만들어서, return 해주는 state를 가공해주는 가공자이다.
    - 이후, subscribe를 이용해서, render를 호출한다.
        - 새로운 state에 맞게 UI가 변한다.

![image](https://user-images.githubusercontent.com/26318691/228264527-c553c6ef-daf5-421b-9191-93f1e69b8843.png)
<b>이미지 출처(https://opentutorials.org/course/4901/24935)</b>

### 참고 자료들

[React 입문자들이 알아야할 Redux 쉽게설명 (8분컷)](https://youtu.be/QZcYz2NrDIs)

[Redux](https://opentutorials.org/module/4078)

[Redux(리덕스)란? (상태 관리 라이브러리) - 하나몬](https://hanamon.kr/redux란-리덕스-상태-관리-라이브러리/)

[Redux 시작하기 | Redux](https://ko.redux.js.org/introduction/getting-started/)
