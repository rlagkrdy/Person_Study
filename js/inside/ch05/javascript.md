# 실행 컨텍스트

1.  실행 컨텍스트의 개념
2.  활성 객체
3.  스코프 체인
4.  클로저

## 실행 컨텍스트 개념

실행 가능한 코드를 형상화 하고 구분하는 추상적인 개념
이걸 콜스택과 연관하여 정의하면 실행 가능한 자바스크립트 코드 블록이 실행되는 환경

## 실행 컨텍스트 생성과정

1.  활성 객체와 변수 객체
2.  스코프 체인

실행 컨텍스트 생성되면 자바스크립트 엔진은 해당 컨텍스트에서 실행에
필요한 여러가지 정보를 담을 객체를 생성한다. 이를 활성객체라고 한다.

이 객체에 앞으로 사용하게 될 매개변수나 사용자가 정의한 변수 및 객체를 저장하고,
새로 만들어진 컨텍스트로 접근 가능하게 되어 있다.
이는 엔진 내부에서 접근할 수 있다는 것이지 사용자가 접근할 수 있다는 것은 아니다.

ExContext2();
실행 컨텍스트 생성되고
활성 객체를 생성하고
ExContext2 함수의 정의된 변수 및 객체를 저장후 실행

1.  활성 객체 생성
2.  arguments 객체 생성
3.  스코프 정보 생성 : 현재 컨텍스트의 유효 범위를 나타내는 스코프 정보를 생성하고,
    이 스코프 정보는 현재 실행 중인 실행 컨텍스트안에서 연결 리스트와 유사한 형식으로 생성된다.

4.  변수 생성 : 사용자가 정의한 변수 생성
5.  this 바인딩
6.  코드실행;

## 클로저

이미 생명 주기가 끝난 외부 함수의 변수를 참조하는 함수를 클로저라고 한다.
