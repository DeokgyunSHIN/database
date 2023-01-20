# 생성 

 데이터 베이스 생성 / 삭제 
 
 SQL문 
 
 CREATE DATABASE {데이터베이스인스턴스명};
 
 CREATE DATABASE {데이터베이스인스턴스명};
 
(시작하기 전에 데이터베이스는 대소문자를 구분하지 않는다.)

1. 맨처음에 내 데이터베이스를 확인 하기 떄문에 

show databases; 

SQL문을 쳐서 확인한다 .

<img width="242" alt="스크린샷 2023-01-20 오후 5 30 49" src="https://user-images.githubusercontent.com/104719555/213651026-aff5d4bd-87c6-4ed2-b989-6201b43108d7.png">


2. 확인 한 후 새로운 데이터베이스를 생성하기 위해서는  create를 사용한다.

그다음 생성하고 싶은 장소를 적은다음 원하는 이름을 적는다.

create database db1;

create -> 생성할게요 

database -> database라는 장소에 

db1 -> db1이라는 이름으로 

<img width="311" alt="스크린샷 2023-01-20 오후 5 31 02" src="https://user-images.githubusercontent.com/104719555/213651488-e4fb4b5b-c5a5-42ef-8951-a723200a1bbe.png">

여기서 생성에 성공이 되면 위에 사진 처럼 

Query OK, 1 row affected (0.001 sec) 이라고 뜨고 

만약에 실패하게되면 

ERROR 라고 뜬다.

3. 그리고 생성이 제대로 되었는지 다시 한번 

show databases;  

라고 검색을 하게 된다.

<img width="261" alt="스크린샷 2023-01-20 오후 5 31 13" src="https://user-images.githubusercontent.com/104719555/213651927-4a2258f9-4ad5-4321-a0ac-6b8a2b28782f.png">

그러면 위에 사진 처럼 db1이라고 데이터베이스에 생성하게 된다.
