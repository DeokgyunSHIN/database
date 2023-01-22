# 테이블 정의 

>  데이터는 관계형 데이터베이스의 기본 단위인 테이블 형태로 저장된다.
> 
>  모든 자료는 테이블에 등록되고, 테이블로부터 원하는 자료를 꺼내 온다.
>  
>  테이블은 어느 특정한 주제와 목적으로 만들어지는 일종의 집합이다.
>  
>  새로운 데이터를 입력할 때, 새로운 테이블을 생성할 필요 없이 테이터만 추가하면 된다.

| o |   |  |
|---|---|---|
| x |  x  |  x |
|  |    |   |
|  |    |   |


테이블을 보면 o이라고 되어져있는데 이것을 컬럼 또는 필드(속성) 이라고 부른다.

그리고 그 밑으로는 x 가로로 되어져 있는데 그것을 로우 또는 튜플, 레코드 라고 부른다.

좀 더 쉽게 설명하면 테이블 맨 위에 있는 줄은 컬럼 또는 필드(속성)이라고 부르고 

그 나머지 가로줄은 로우또는 레코드, 튜플 이라고 한다.

그러면 컬럼과 튜플은 무엇일까?

> 컬럼 - 필드,항목, 어떠한 의미를 지니는 정보의 한 조각으로, 데이터베이스 시스템에서 처리의 최소 단위가 되는 것이다.

> 튜플 - 각 테이블의 행은 일련의 관련 자료를 나타내며, 테이블에서 모든 로우는 동일한 구조를 가지고 있다.

이렇게 정리 하니깐 이해하기가 힘들것이다.

좀더 쉽게 설명을 하면 

학생 정보 테이블 

|이름 | 성별 | 나이 | 생일|
|:---:|:---:|:---:|:---:|
|신덕균|남자|25|0118|
|홍길동|남자|30|1212|
|가나다|여자|10|1012|

이렇게 테이블을 정리 할수 있다.

즉, 컬럼은 자기밑으로 수직으로 무슨 데이터를 의미하는지 제목이라고 볼 수 있다.

그리고 튜플은 가로줄의 데이터라고 할 수 있다.