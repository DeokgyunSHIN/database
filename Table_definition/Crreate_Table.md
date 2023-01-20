# 테이블 생성 

> 테이터 자료형 
> 
> > 숫자 데이터 (INT)
> > 
> > 문자열(문자)데이터 (CHAR,VARCHAR)
> > 
> > Boolean 데이터(True/False) (BIT)
> > 
> > 날짜/ 시간 데이터 (DATETIME, TIMESTAMP)
> > 
> > 큰 객체 데이터 (TEXT)

예시)  (DBeaver 툴 사용)

회원 정보 테이블 생성 

회원이름 , 회원 아이디, 회원 비밀번호, 회원 나이, 회원 생년월일 , 정보 문자 전송 여부, 회원 가입일 등등이 있다.

테이블을 생성하기 위해서 일단 먼저 

use '데이터베이스명'; 을 

해준다음 테이블을 생성해주면 된다.

```
CREATE table member(
  name varchar(20),
  id varchar(50),
  pw varchar(50),
  age int,
  birth date,
  sms_send_yn bit,
  register_data datetime
 );
```

여기서 (20) 또는 (50) 이라고 적혀져 있는데 

문자열의 크기를 얼마나 할것이다. 라고 적어주는것이다.

<img width="941" alt="스크린샷 2023-01-20 오후 6 36 47" src="https://user-images.githubusercontent.com/104719555/213663638-abb8a817-87ec-4ea3-8315-cd3c6d42374f.png">

SQL 문을 적어준 다음 실행을 하게 되면 밑에 생성 된것을 알 수 있고 

DBeaver 툴에 옆에 보면 파일들이 있는데 새로고침 하면 테이블이 생성된것을 알수 있다.

<img width="318" alt="스크린샷 2023-01-20 오후 6 39 45" src="https://user-images.githubusercontent.com/104719555/213664183-c798f500-844c-4653-9742-805286c600e8.png">


그 다음 여기서 select *from '테이블명';

을 해주게 되면 테이블에 있는 데이터의 정보를 보여준다.

여기서 * 는 모든 정보를 뜻한다.

<img width="933" alt="스크린샷 2023-01-20 오후 6 43 32" src="https://user-images.githubusercontent.com/104719555/213664873-e46f6d74-322b-4841-be61-4a4343e166bf.png">

위에 사진을 보게 되면 테이블의 정보 정보가 나오게 되는데 아무런 정보가 뜨지 않는다.

그 이유는 테이블 생성만 했을 뿐 아무런 데이터를 넣지 않았기 떄문에 컬럼만 보일뿐 아무것도 보이지 않는다 .
