# 데이터 처리 

<br>
<br>

### alias

> 별명이다. 말 그대로 부르기 쉽게 하기위함이다.
> 
> 예를 들어 테이블이 대한 별명 , 컬럼에 대한 별명 
>
> AS 키워드를 이용해서 사용한다.

예시)

<img width="365" alt="스크린샷 2023-01-24 오후 5 51 49" src="https://user-images.githubusercontent.com/104719555/214248796-22efbad7-e8a4-45c6-892e-e1011eb7a7c6.png">

위의 사진처럼 실행을 할수 있다는 것이다.

뜻은 login_member의 테이블의 별명을 lm으로 설정을 해주고 

lm.name 은 별명으로 설정해둔 lm의 별명인 login_member 안에 

name 의 컬럼명을 조회한다는 뜻을 가지고 있다.

실행을 하게되면 

<img width="395" alt="스크린샷 2023-01-24 오후 5 51 55" src="https://user-images.githubusercontent.com/104719555/214249345-d7f18199-5803-4f35-bb8d-27f57e553723.png">

결과가 나오게 된다.


또한 한글로도 쓸수 있다

예시)

<img width="405" alt="스크린샷 2023-01-27 오후 2 13 25" src="https://user-images.githubusercontent.com/104719555/215014447-2a09e2cd-3d86-4416-a7c1-560d703f8839.png">

위에 사진처럼 SQL문을 싱행하게 되면 컬럼명이 영어가 아닌 한글로 변경될 수 있다는것을 볼수있다.

<img width="355" alt="스크린샷 2023-01-27 오후 2 13 31" src="https://user-images.githubusercontent.com/104719555/215014528-c38cdd4d-547a-4e53-9e8d-be33cd627ace.png">

