1. 관계형 데이터베이스(RDBMS)와 비관계형 데이터베이스(NoSQL)의 장단점 비교

### 관계형 데이터베이스
* 관계형 데이터베이스란 테이블(table)로 이루어져 있다.
* 테이블은 이름을 가지고 있으며, 행(row)과 열(column) 그리고 거기에 대응하는 값을 가진다. 
* 즉 관계형 데이터베이스는 위와 같이 구성된 테이블이 다른 테이블들과 관계를 맺고 모여있는 집합체로 이해할 수 있습니다.
* 장점: 데이터의 분류, 정렬, 탐색 속도가 빠름 / 오랫동안 사용된 만큼 신뢰성이 높고, 어떤 상황에서도 데이터의 무결성을 보장
* 단점: 기존에 작성된 스키마를 수정하기가 어렵다 / 데이터베이스의 부하를 분석하는 것이 어렵다 / - 빅데이터를 처리하는데 매우 비효율적임.

### 비관계형 데이터베이스
* NoSQL이라고도 부르며, Not Only SQL(SQL 뿐만이 아닌. 이라는 뜻)의 줄임말
* 거대한 Map으로서 key-value 형식을 지원함.
* 관계형 db와 달리 PK,FK JOIN등 관계를 정의하지 않음.
* 스키마에 대한 정의가 없다.
* 장점
  * 대용량 데이터 처리를 하는데 효율적임.
  * 읽기 작업보다 쓰기 작업이 더 빠르고 관계형 데이터베이스에 비해 쓰기와 읽기 성능이 빠름.
  * 데이터 모델링이 유연함.
  * 뛰어난 확장성으로 검색에 유리함.
  * 최적화된 키 값 저장 기법을 사용하여 응답속도나 처리효율 등에서 성능이 뛰어남.
  * 복잡한 데이터 구조를 표현할 수 있음.
* 단점
  * 쿼리 처리시 데이터를 파싱 후 연산을 해야해서 큰 크기의 document를 다룰 때는 성능이 저하됨.

2. 트랜잭션(transaction)이란 무엇인가요?

- 인가받지 않은 사용자로부터 데이터를 보장하기 위해 DBMS가 가져야하는 특성이자, 데이터베이스 시스템에서 하나의 논리적 기능을 정상적으로 수행학 ㅣ위한 작업의 기본 단위

3. MySQL에서 조인(join)의 역할은 무엇인가요? 다양한 join의 방식에 대해 설명해주세요.

- 조인은 두개이상의 테이블을 연결하여 데이터를 검색하는 방법
- 두 릴레이션으로부터 관련 된 튜플들을 결합하여 하나의 튜플로 만드는 가장 대표적인 데이터 연결방법
- 조인
  * inner join: 공통 존재 컬럼의 값이 같은 경우를 추출
  * outer join
      left outer join : 왼쪽 테이블의 모든 데이터와 오른쪽 테이블의 동일 데이터를 추출
      right outer join : 오른쪽 테이블의 모든 데이터와 왼쪽 테이블의 동일 데이터를 추출
      full outer join : 양쪽의 모든 데이터를 추출
  * cross join : 조인조건이 없는 모든 데이터 조합을 추출
  * self join : 자기 자신에게 별칭을 지정한 후 다시 조인

4. MySQL에서 인덱스(index)란 무엇인가요?

- 인덱스는 데이터를 빠르게 찾을 수 있는 수단으로서, 테이블에 대한 조회 속도를 높여 주는 자료구조
- 인덱스는 테이블의 특정 레코드 위치를 알려 주는 용도로 사용
- 인덱스는 자동으로 생성되지 않는다. 
