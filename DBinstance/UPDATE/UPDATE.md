# UPDATE

SQL 문법
```
 UPDATE 테이블명 SET 컬럼1=값1, 컬럼2=값2,...;
``` 
 
 예시 

기존에 login_member 테이블을 검색을 하게 되면 

<img width="928" alt="스크린샷 2023-01-22 오후 8 26 37" src="https://user-images.githubusercontent.com/104719555/213913396-c92c921c-bc3f-4614-bd9d-028fe96dc54f.png">

위의 사진 처럼 marketing_yn 에 1이라고 적혀있다. ( 툴마다 true ,false 또는 0,1 로 표시된다고 합니다)

그 이유는 그 전에 true 라고 데이터를 넣었기 때문에 1이라고 데이터를 넣었기 때문이다.

<img width="556" alt="스크린샷 2023-01-22 오후 8 31 50" src="https://user-images.githubusercontent.com/104719555/213913526-a1190eff-4935-440f-ac4d-de422d5b6714.png">

위의 사진 처럼 명령어를 실행 한 후 다시 login_member 테이블의 데이터를 검색하게 되면 

<img width="838" alt="스크린샷 2023-01-22 오후 8 31 58" src="https://user-images.githubusercontent.com/104719555/213913677-1668dd49-97dd-4bee-8028-3dfe6dd3d019.png">

merketing_yn 에 1이 0으로 변경된 것을 볼수 있다.

<br>
<br>

### 또다른 예시 

<img width="875" alt="스크린샷 2023-01-23 오후 4 21 05" src="https://user-images.githubusercontent.com/104719555/213984956-71ebe3b5-baf6-4f97-ae48-4678e3b7539e.png">

만약에 위의 사진처럼 4개의 데이터가 있다고 생각해보자 

그러면 여기서 

UPDATE login_member set marketing_yn= FALSE;

라고 하면 컴퓨터는 다시 관리자한테 물어본다.

'조건문이 없는데 너 전부 데이터를 false로 바꾸는거 맞아? 확실해??'

라고 물어본다 여기서 하겠다고 하면 

<img width="855" alt="스크린샷 2023-01-23 오후 4 29 37" src="https://user-images.githubusercontent.com/104719555/213986230-b76e2016-b680-4456-8100-0c5365dd43f2.png">

false 로 변경되는것을 볼 수 있다.


### update는 조건이 있다.

예시)

<img width="855" alt="스크린샷 2023-01-23 오후 4 29 37" src="https://user-images.githubusercontent.com/104719555/213987073-9ee1283e-c5c0-4bd0-8f5f-db8aff1bf749.png">


만약에 login_member 테이블에 4개의 데이터가 있다고 하자 

여기서 나는 password에 데이터가 있는(NULL 이 아닌) 정보에 marketing_yn을 true 로 바꾸고 싶을 때는 조건문을 사용해야 한다.

<img width="860" alt="스크린샷 2023-01-23 오후 4 41 43" src="https://user-images.githubusercontent.com/104719555/213987978-3851034d-2056-4b5c-a148-27d11cab42d1.png">

위 사진의 뜻은 '나 login_memeber 테이블에 있는 데이터중에 marketing_yn을 true로 변경하고 싶어 근데 password의 값이 null이 아닌 로우에만" 

이라는 뜻이다

<img width="848" alt="스크린샷 2023-01-23 오후 4 44 40" src="https://user-images.githubusercontent.com/104719555/213988386-ed45a456-cc8b-4728-a185-f30cd81f23bd.png">

실행하면 위의 사진처럼 null이 아닌 로우에만 true로 바뀌는걸 볼수 있다. 

데이터 수정 / 삭제는 조심 또 조심 해야될 상황이기 떄문에 무조건 !! 조건문을 써서 데이터를 변경 또는 삭제를 하는 것이 좋다.
