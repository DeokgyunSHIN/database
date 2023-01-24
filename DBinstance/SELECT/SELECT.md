# SELECT 

> 데이터 조회 

<img width="838" alt="스크린샷 2023-01-24 오후 5 01 54" src="https://user-images.githubusercontent.com/104719555/214242937-bda7a755-97bd-42aa-8593-f238bdeb8b23.png">

위의 사진처럼 login_member 테이블의 데이터가 있다고 가정한다.

<img width="418" alt="스크린샷 2023-01-24 오후 5 12 57" src="https://user-images.githubusercontent.com/104719555/214241851-6654fec6-d552-418f-877e-9a4f7f3827a6.png">

위의 사진 처럼 실행을 하게 되다면 

login_member 테이블의 데이터를 전부 조회를 하는 것인데 

인기있는 쇼핑몰이나 인기있는 게임사이트의 고객 유저의 정보 중에 특정 정보를 조회를 하고 싶은데 전부다 

조회를 하게 된다면 시간이 굉장히 오래 걸리게 될것이다.

이럴떄는 조건을 주어서 내가원하는 데이터만 조회를 할 수 있다는 것이다.

<img width="386" alt="스크린샷 2023-01-24 오후 5 13 25" src="https://user-images.githubusercontent.com/104719555/214242224-7ad0a839-1e5c-4c02-a9ee-f1766087567e.png">

위의 사진 처럼 실행을 하는데 뜻은 'login_member 테이블을 전부 조회를 할건데 

marketing_yn 이 true인 데이터만 조회하고 싶어'

라는 뜻을 가지고 있다.

그래서 조회를 하게 된다면 

<img width="837" alt="스크린샷 2023-01-24 오후 5 13 33" src="https://user-images.githubusercontent.com/104719555/214242665-8a1efa0d-e2d8-4af6-b8c1-b8cd0f6b2479.png">

위의 사진처럼 login_member 테이블의 데이터를 전부 조회를 하지만 marketing_yn이 true인 정보만 조회를 하는것을 볼수 있다.
