# 데이터 추가(넣기)

### SQL 문법

```
 INSERT INTO 테이블명(컬럼1,컬럼2,...) VALUES(값1,값2,...);
```


예시)

1. 로그인 테이블을 생성한다 .

<img width="384" alt="스크린샷 2023-01-22 오후 7 09 50" src="https://user-images.githubusercontent.com/104719555/213910479-98737db1-23a4-4185-bb15-c4d0f16120c7.png">

위의 사진 처럼 테이블을 만든후 

데이터를 넣기 위해서 

2. INSERT를 사용한다.

<img width="977" alt="스크린샷 2023-01-22 오후 7 09 39" src="https://user-images.githubusercontent.com/104719555/213910533-1a811f15-7fb1-4231-b71d-4778c45d3559.png">

위 사진 처럼 생성 후 실행을 후  ERROR 가 뜨지 않으면 정상적으로 데이터를 들어가게 된다.

 !! 간혹 가다가 
 
 <img width="1041" alt="스크린샷 2023-01-22 오후 7 14 23" src="https://user-images.githubusercontent.com/104719555/213910625-de8767b7-3c3e-48bd-a7d1-95ba2eb16b52.png">

 위의 사진처럼 컬럼명을 빼고 순서대로 적는 경우도 있지만 
 
 좋은 방법은 아니다.
 
 그 이유는 데이터베이스는 관리자 편리성 보다 더 중요한것이 데이터 저장하기 위함이기 떄문에 정확하게 지정 후 하는것이 좋다.
 
 
 3. 그 다음 데이터가 정확하게 들어갔는지 확인하기 위해서
  
<img width="876" alt="스크린샷 2023-01-22 오후 7 13 05" src="https://user-images.githubusercontent.com/104719555/213910686-33e15111-9f50-4e5b-964d-11e90edd3681.png">

SELECT * FROM login_member;

실행 하면 정상적으로 데이터가 들어간것을 볼수 있다.

