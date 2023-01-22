# UPDATE

SQL 문법
```
 UPDATE 테이블명 SET 컬럼1=값1, 컬럼2=값2,...;
``` 
 
 예시 

기존에 login_member 테이블을 검색을 하게 되면 

<img width="928" alt="스크린샷 2023-01-22 오후 8 26 37" src="https://user-images.githubusercontent.com/104719555/213913396-c92c921c-bc3f-4614-bd9d-028fe96dc54f.png">

위의 사진 처럼 marketing_yn 에 1이라고 적혀있다.

그 이유는 그 전에 true 라고 데이터를 넣었기 때문에 1이라고 데이터를 넣었기 때문이다.

<img width="556" alt="스크린샷 2023-01-22 오후 8 31 50" src="https://user-images.githubusercontent.com/104719555/213913526-a1190eff-4935-440f-ac4d-de422d5b6714.png">

위의 사진 처럼 명령어를 실행 한 후 다시 login_member 테이블의 데이터를 검색하게 되면 

<img width="838" alt="스크린샷 2023-01-22 오후 8 31 58" src="https://user-images.githubusercontent.com/104719555/213913677-1668dd49-97dd-4bee-8028-3dfe6dd3d019.png">

merketing_yn 에 1이 0으로 변경된 것을 볼수 있다.
