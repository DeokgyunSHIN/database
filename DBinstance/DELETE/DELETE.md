# DELETE (삭제)

> 데이터 삭제 

SQL문 

```
 DELETE FROM
 테이블명 
 WHERE 조건; 
```

여기서 update문과 동일하게 조건이 있어야 한다.

특히나 데이터를 지운다는 의미는 굉장히 위험한 일이고 

특정 데이터를 지우기 위해서 DELETE를 쓰는데 조건이 없다면 

모든 데이터들이 삭제될수도 있기 떄문에 

UPDATE문과 DELETE문은 무조건(필수) 조건을 써야한다.


예시)

<img width="863" alt="스크린샷 2023-01-24 오후 4 55 47" src="https://user-images.githubusercontent.com/104719555/214239077-ed9fc082-4dc2-4b9f-8526-c633d1ae09d2.png">

login_member의 테이블에 위의 사진 처럼 데이터가 있다고 가정을하면 

1번사진 

<img width="422" alt="스크린샷 2023-01-24 오후 4 56 02" src="https://user-images.githubusercontent.com/104719555/214239162-e3b3b557-a43f-4189-9617-5edf69b7d548.png">

위의 1번 사진처럼 DELETE SQL문을 사용하게 되면 login_member 테이블의 데이터가 전부 사라지게 된다. (조심 또 조심!!)

2번 사진 

<img width="463" alt="스크린샷 2023-01-24 오후 5 01 43" src="https://user-images.githubusercontent.com/104719555/214240105-7e258122-ee7d-4d67-925c-a70cadacf361.png">

2번 사진처럼 지울 로우 데이터의 조건을 걸어서 지워줘야한다.

실행 후 정상적으로 데이터가 지워졌는지 확인하기 위해서 

select* from login_member; 실행하게 되면 

<img width="838" alt="스크린샷 2023-01-24 오후 5 01 54" src="https://user-images.githubusercontent.com/104719555/214240306-a49ed04c-97ec-4fa7-9b34-6c94d5331d3a.png">

위의 사진처럼 이메일 test1@test.com의 로우가 지워졌다는것을 볼수 있다.

