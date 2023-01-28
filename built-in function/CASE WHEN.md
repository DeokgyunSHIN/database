예시) 비밀먼호 앞 두자리 외에 *처리 하기 

concat 함수 (문자열을 연결하고 싶을 때 사용)

concat 함수는 어떤 DBMS냐에 따라 매개변수를 두 개만 받기도 하고 

여러개를 허용해주기도 하기 떄문에 다른르다.

![스크린샷 2023-01-28 오후 8 28 49](https://user-images.githubusercontent.com/104719555/215264186-f3d98da9-c68b-47f0-bcb9-c6b3f3991900.png)

위의 사진 SQL문을 보게 되면 

CONCAT(SUBSTRING(password,1,2,),'**') 을 볼수 있는데 

SUBSTING 은 데이터를 일부 읽어온다는 뜻을 가지고 있다.

즉, password 데이터를 1에서 2까지 만 일거오고 나머지 뒤에 문자열 ** 붙이겠다는 뜻을 가지고 있다.

![스크린샷 2023-01-28 오후 8 28 54](https://user-images.githubusercontent.com/104719555/215264440-ae3aeeb0-3528-40bc-9d8b-fc6154325034.png)

실행을 하게 되면 위의 사진처럼 나오는 걸 볼수 있다.

근데 여기서 문제점은 비밀번호가 없는데 ** 출력되는걸 볼수 있다.

여기서 비밀번호가 없는 곳은 출력이 되지 않게 하기 위해서ㅡㄴ 

CASE WHEN 을 쓰면된다.

CASE WHEN은 조건에 따라 값을 주는건데 자바로 따지면 if, else if,else 라고 생각하면된다.

기본 문법은 

```
 CASE 컬럼명 
  WHEN 조건1 THEN 값1
  WHEN 조건2 THEN 값2
 ELSE  값3
 END
```

컬럼이 조건1 일떄는 값1을 , 조건2 일때는 값2을 반환하고 조건에 맞지 않으면 

값 3을 반환하는것이다.

![스크린샷 2023-01-28 오후 8 28 17](https://user-images.githubusercontent.com/104719555/215264629-981f573d-83bb-40df-82d1-716d6f45dccc.png)

위의 사진의 SQL문을 보면 조건이 password길이가 2이상이면 concat(substring(password,1,2),'**') 이고 

조건에 해당하지 않으면 ''를 출력하라는것이다.

위의 SQL문을 실행하게된다면

![스크린샷 2023-01-28 오후 8 28 26](https://user-images.githubusercontent.com/104719555/215264702-415e690c-db95-43ae-b600-12c6b044e779.png)

위의 사진처럼 password의 길이가 2이상인 데이터만 출력이 되는 것을 볼수 있다.
