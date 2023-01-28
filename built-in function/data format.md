# 데이터 표시 포멧(날짜 -> 문자열, 문자열 -> 날짜) (mariadb기준)


> 날짜 -> 문자열 변환: date_format
> 
> 문자열 -> 날짜 변환 : str_to_date
> 
> 날짜 변환 : date_add


### date_farmat

![스크린샷 2023-01-28 오후 9 00 07](https://user-images.githubusercontent.com/104719555/215265302-96c084fb-d8e9-40a4-b4b9-b7a68ee5411b.png)

위의 사진처럼 데이터가 들어가 있다고 가정하면 

여기서 날짜를 문자열로 표시가 가능하다 .

![스크린샷 2023-01-28 오후 9 01 19](https://user-images.githubusercontent.com/104719555/215265402-8d55b1c8-1a3c-416a-8e4e-dd4dfabb25f5.png)

위의 사진 처럼 date_format을 사용하면 가능하다 .

'%Y' 은 년도를 나타내는것이고  '%m' 는 월을 나타내는것이다.

그리고 '%d'은 일을 나타내는것이다. 

그리고 중간에 . 을 붙이는 이유는 구분을 하기 위해서이다. 

![스크린샷 2023-01-28 오후 9 05 13](https://user-images.githubusercontent.com/104719555/215265521-605e82a5-ffe3-45ba-84ac-184614aab46d.png)

실행을 하게 되면 위의 사진처럼 출력이 되는걸 볼수 있다.

<br>
<br>
<br>

### str_to_date

![스크린샷 2023-01-28 오후 9 11 16](https://user-images.githubusercontent.com/104719555/215265781-ec02d57d-394a-4332-82fe-831f4913ba0c.png)

위의 사진의 SQL문을 살펴보면 dual을 볼수 있는데 

dual은 단순한 계산, 산술연산, 함수결과등을 손쉽게 확인할수 있는 임시 테이블이라고 생각하면된다.

string을 날짜로 변환하기위해서 str_to_date 함수를 사용하면 

![스크린샷 2023-01-28 오후 9 14 21](https://user-images.githubusercontent.com/104719555/215265890-34fe6a14-0e71-4e89-990f-dcf99cfe6824.png)

위의 사진 처럼 실행되는걸 볼수 있다.

### DATE_ADD

String 에서 달월을 +1 하고 출력한다면 많이 힘들다.

그때 DATE_ADD를 해주면 쉽게 가능하다.

![스크린샷 2023-01-28 오후 9 21 27](https://user-images.githubusercontent.com/104719555/215266173-cb1008be-afe5-4f68-b988-cc51d5ed360f.png)

위의 사진을 보면 date_add의 함수를 볼수 있는데 INTERVAL 1 month 는 1달 더하는것이고

INTERVAL 1 YEAR은 1년을 더하는것이다.

위의 SQL문을 실행하게 되면 

![스크린샷 2023-01-28 오후 9 21 37](https://user-images.githubusercontent.com/104719555/215266307-acd9cc73-9a33-46b2-b0ba-9b8c881207ea.png)

1달이 더하는것을 볼수 있다.


### 종합 예제 ( 현재 날짜의 월초와 월말 구하기)

![스크린샷 2023-01-28 오후 9 35 35](https://user-images.githubusercontent.com/104719555/215266700-1c19863e-853a-4ca9-823f-16a7907ea47a.png)

1월달의 마지막날은 31일이다.

다양한 방법으로 풀수있지만 

조건을 간단하게 주어 문제를 풀었다.

2월 1일에서 1일을 빼면 1월의 마지막 날이 나오기 때문에  date_add를 두번 써서 출력을 할수 있는것을 볼수있다.

실행을 하게 되면

![스크린샷 2023-01-28 오후 9 35 39](https://user-images.githubusercontent.com/104719555/215266772-1a5f1be4-611c-4e72-afe8-979a664a934b.png)

위의 사진처럼 실행되는것을 볼수있다.

