# JOIN 문 

> 여러 테이블을 함께 조회하기 위함이다.
> 
> 일반적으로 사용되는 SQL문장의 상단수가 조인을 이용한다.
> 
> JOIN은 관계형 데이터베이스의 가장 큰 장점이면선 핵심 기능이다.
> 
> JOIN은 두 데이블을 연결해서 뎅티어를 검색하는 방법이다.
> 
> 연결하려는 테이블들이 적어도 하나의 컬럼을 공유하고 있어야한다.
> 
> 그리고 그 공유된 컬럼은 pk 또는 fk값으로 사용해야 한다.
> 
### JOIN은 4가지로 분류된다.

INNER JOIN.    /  FULL JOIN

LEFT JOIN.    /   RIGHT JOIN

INNER JOIN은 

$$\ A \cap \ B $$

교집합의 연산과 같으며 조인 키 컬럼 값이 양쪽 테이블 집합에서 공통적으로 존재하는 테이터만 조인해서 결과 데이터 집합으로 출력하게 된다.

예시)

기본 테이블 

member테이블 생성및 데이터 출력

``` 
 CREATE table member(
member_type varchar(10) not null comment '회원구분',
user_id varchar(50) not null comment'회원 아이디',
password varchar(50) null comment '비밀번호',
name varchar(50) null comment '이름',
primary key (member_type, user_id)
) comment '회원정보';
```
<img width="540" alt="스크린샷 2023-01-28 오후 6 09 42" src="https://user-images.githubusercontent.com/104719555/215257644-e8aedf4b-7049-48d0-b145-b9b7f248eb00.png">

member_detail 테이블 생성및 데이터 출력

```
CREATE table member_detail(
 member_type varchar(10)  not null comment '회원구분',
 user_id varchar(50) not null comment '회원 아이디',
 mobile_no varchar(12) null comment '전화번호',
 marketing_yn bit  null comment '마케팅 수신 여부',
 register_date datetime default current_timestamp() null comment '가입일',
 primary key(member_type, user_id),
 constraint fk_member_detail foreign key(member_type, user_id) references member (member_type, user_id)
) comment '회원상세정보' ;
```
<img width="784" alt="스크린샷 2023-01-28 오후 6 10 04" src="https://user-images.githubusercontent.com/104719555/215257674-71c1b150-7945-4461-a2ee-0bba8e3eeb04.png">

두 테이블간의 관계도 

<img width="320" alt="스크린샷 2023-01-28 오후 6 30 28" src="https://user-images.githubusercontent.com/104719555/215258630-56268adc-d8c5-4adf-87ec-33598a5c354c.png">


member 테이블과 member_detail테이블 두개가 있다고 가정하자 

그러면 여기서 INNER JOIN은 

```
 SELECT mb.member_type ,mb.user_id FROM member as mb join member_detail as md 
 on mb.member_type =md.member_type 
 and mb.user_id =md.user_id ;
```

를 쓰면된다.

INNER JOIN은 교집합이기 때문에 두 테이블간의 똑같은 데이터만 뽑아내는 것이다.

뜻을 해석하게 되면 

member 테이블의 별명은 mb로 하고 member_detail 테이블의 별명은 md로 설정하고 

mb 테이블 안에 컬럼명이 member_type과 md 테이블 안에 컬럼명이 member_type이 서로 데이터가 같고 

그리고 mb 테이블 안에 컬럼명이 user_id 와 md 테이블 안에 컬럼명이 user_id가 서로 테이터가 같은 것끼리 모아서 

mb.member_type , mb.user_id 뽑아달라는 뜻이다.

조금더 쉽게 설명을 한다면 두 테이블간의 member_tpye 과  user_id가 서로 같은것끼리만 출력하는것이다.

<img width="317" alt="스크린샷 2023-01-28 오후 6 28 06" src="https://user-images.githubusercontent.com/104719555/215258521-e7eb19f0-e294-4ccb-b99c-8f05c37daec2.png">

실행을 하게 된다면 위의 사진 처럼 결과값을 얻을 수 있다. 이것 INNER JOIN이다.

### LEFT JOIN

LEFT JOIN은 왼쪽에 있는거 모두 출력이다. (A와 B의 공통적인 데이터 + LEFT에 있는것만)

LEFT JOIN SQL 문 

```
  SELECT * FROM member as mb left join member_detail as md 
 on mb.member_type =md.member_type 
 and mb.user_id =md.user_id ;
```

SQL문을 보게되면 left join을 찾을수 있다.

그 단어를 기준으로 왼쪽 즉, member테이블이 기준이 되는것이다.

실행을 하게되면 

<img width="1284" alt="스크린샷 2023-01-28 오후 6 39 49" src="https://user-images.githubusercontent.com/104719555/215259126-03b3355c-0111-4797-a91d-d52a43b154d4.png">

위의 사진처럼 나오게된댜. member 테이블의 데이터는 5개 member_detail 테이블의 데이터는 3개 이다.

2개 데이터는 없기 떄문에 NULL로 출력이된다.

### RIGHT JOIN

RIGHT JOIN은 왼쪽에 있는거 모두 출력이다. (A와 B의 공통적인 테이터 + RIGHT에 있는것만)

RIGHT JOIN SQL 문 

```
  SELECT * FROM member as mb right join member_detail as md 
 on mb.member_type =md.member_type 
 and mb.user_id =md.user_id ;
```

SQL문을 보게 되면 right join의 기준으로 즉, member_detail이 기준이 된다.

실행을 하게 되면 

<img width="1283" alt="스크린샷 2023-01-28 오후 6 48 06" src="https://user-images.githubusercontent.com/104719555/215259692-132f433d-29eb-452b-b6e5-d9314f7bb4ed.png">

위의 사진 처럼 출력되는것을 알수 있다. 

member_detail 테이블의 데이터는 3개이다. 기준이 되기떄문에 3개만 나오게 되고 

member 테이블의 조건이 같지 않은 데이터는 출력 되지 않는것을 볼수 있다.

### FULL JOIN

FULL JOIN은 모든 데이터 출력이다.

```
 SELECT * FROM member as mb  join member_detail as md;
```

실행을 하게되면

<img width="1289" alt="스크린샷 2023-01-28 오후 6 51 44" src="https://user-images.githubusercontent.com/104719555/215259832-a369ce19-ebf1-4b3a-b0c3-502a029ae7b1.png">

위의 사진 처럼 총 15개의 데이터가 나오게 된다(member테이블의 테이터 5개 * member_detail테이블의 데이터 3개)=15개
