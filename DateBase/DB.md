# DB

## DB
DataBase는 한 마디로 정의하면 데이터의 집합이라고 할 수 있다.  
여러 사람이 공유할 목적으로 체계화해 통합, 관리하는 데이터의 집합니다.  

DataBase의 특징
- 실시간 접근성(Real-Time Accessibility): 실시간 처리에 의한 응답이 가능해야한다.
- 계속적인 변화(Continuous Evolution): 새로운 데이터의 삽입(insert), 삭제(Delete), 갱신(Update)로 항상 최신의 데이터를 유지한다.
- 동시공용(Concurrent Sharing): 다수의 사용자가 동시에 같은 내용의 데이터를 이용할 수 있어야 한다.
- 내용에 의한 참조(Content Reference) : DataBase에 있는 데이터를 참조할 때 사용자의 요구에 따른 데이터 내용으로 데이터를 찾는다.

## DBMS
DataBase는 데이터의 집합이라고 정의한다면, 이런 DataBase를 관리하고 운영하는 소프트웨어를 DBMS(Database Management System)라고 합니다. 다양한 데이터가 저장되어 있는 DataBase는 여러 명의 사용자나 응용프로그램과 공유하고 동시에 접근이 가능해야 한다.  
### DBMS의 종류
- HDBMS(계층형) : 계층적인 형태의 DBMS 초기 DBMS의 형태 (IMS,System2000)
- NDBMS(망형): 구성과 설계가 복잡하고 데이터 종속성을 해결하지 못함 (IDS, TOTAL, IDMS)
- ODBMS(객체형) : 정보를 객체의 형태로 표현하는 DBMS (Object Store, UniSQL)
- RDBMS(관계형) : 테이블과 테이블의 관계를 기반으로 하는 가장 범용적인 DBMS이다. 데이터의 일관성을 보장한다.(Oracle, MySQL, SQL Server, MS SQL, Maria DB 등등)
- No- SQL(Not Only SQL) : 데이터 간의 관계를 설정하지 않고 유연한 테이블 스키마를 가진다. 대용량 데이터/분산 처리에 적합한 장접이 있지만 데이터 일관성이 보장되지 않는 단점이있다.(Mongo DB, Redis, Cassandra 등등)

1 ~ 3세대형식의 DBMS에서 4세대인 관계형 DBMS로 빠른 전환이 이루어 졌지만, 관계형에서 5세대인 객체지향형으로 전환은 빠르게 되지않는 편이다. 그래서 RDBMS의 형식인 DBMS가 계속 현 상태를 유지할 것이라는 전망이다.
