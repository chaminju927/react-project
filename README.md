# <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white"/>
## first-project : 영화 웹 서비스 만들기 (with 노마드코딩)
## 🗒 2023/06/02 : 1.1 - 2.6강
### 주요 내용 :
#### 1. 리액트 설치(script src는 React와 ReactDOM 둘다 필수)
#### 2. react.js가 element를 생성, 이때 element property에 eventListener추가 가능
#### 3. reactDOM이 생성한 element를 render()를 통해 HTML코드로 변경
#### 4. createElement() 대신 jsx사용하기 (바벨이 일반 js코드로 변환해줌) - jsx는 하나의 파일에 js와 html을 동시에 작성하여 편리, 가독성 높음
#### 5. div에 const를 넣기 위해선 const를 애로우 펑션으로 만들어 줘야 하고, 이때 컴포넌트명은 대문자로 시작해야 함.

## 🗒 2023/06/04 : 3.1 - 3.4강
### 주요 내용 :
#### 1. 리액트의 장점 ? - 페이지 내 변경된 데이터만 업데이트 해줌. 매번 html코드 전체를 로딩하지 않아도 되기에 효율적임. 코드도 간결해짐
#### 2. 리액트에서 데이터를 저장시켜 자동으로 리렌더링하는 법
#### - React.useState();를 변수에 담아 출력해보면 [data, data를 바꾸는 함수]가 나타남. 이때 data는 초기값이고, useState()의 아규먼트로 설정가능
#### 3. state를 셋팅하는 법?
#### - 직접 할당 : setState(state+1)
#### - 함수를 할당 : setState(current => current+1)

## 🗒 2023/06/13 : 3.5 - 3.7강
### 주요 내용 :
#### 1. jsx에서는 class나 for같은 js속성을 그대로 사용 불가. className, htmlFor로 사용함
#### 2. React.useState()는 array를 제공하고 첫번째 element가 현재값. 이 배열을 const []에 할당할때 [첫번째 element, 첫element를 수정해주는 modifier]
#### 3. state값으로 input을 enabled할지 disabled 할지를 결정할 수 있음.<br>디폴트 값이 false 라고 정했으므로 Hours는 disabled 되어야함 그래서 disabled={flipped === false}를 써줘서 flipped가 false라면, disabled는 true가 되도록 만들어줌
#### 4. 시간 -> 분 컨버터 : 삼항(조건)연산자(ternary operator)사용. <br>flipped ? amount : amount / 60 -> 만약 flipped 상태면 state에 있는 값을 그대로 보여주기 아니라면 60으로 나눈 변환된 값 보여주기<br>value={flipped ? amount * 60 : amount} -> 만약 flipped 상태면 60으로 곱한 변환된 값 보여주기

## 🗒 2023/06/14 : 3.8 - 4.3강
### 주요 내용 :
#### 1. setState()에 함수를 할당하는 것을 잘 활용하면 이전 state를 쉽게 바꿀수 있다.
#### 2. useState()의 두번째 인자인 modifier함수를 실행하면 해당 컴포넌트가 리렌더링 됨<br> 리렌더링 조건-> props나 state가 바꾸리 때, 부모 컴포넌트가 리렌더링 될 때!
#### 3. 속성으로 value를 가질수 있으면 onChange속성을 붙일 수 있음
