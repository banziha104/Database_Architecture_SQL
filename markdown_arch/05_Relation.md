# 관계 

<br>

### 관계가 중요한 이유

- 관계는 연관이 있는 두테이블 사이의 연결을 설정한다.
- 관계는 테이블 구조를 정제하고 중복 데이터를 최소화하는 것을 돕는다
- 관계는 여러 테이블에서 동시에 데이터를 뽑아 낼 수 있는 방법이 된다

<br>

### 관계의 유형

- 1:1 관계 : 각 한개 씩 연결될떄  
- 1:다 관계 : 첫 번째 테이블의 한 레코드가 두 번째 테이블의 여러 레코드와 연결되지만, 두번쨰 레코드는 한개만 연결될떄 (소비자와 물품 DB)
- 다:다 관계 : 각 테이블이 여러개 연결될 때 (학생과 수강 신청 DB)

<br>

### 다대다 관게의 문제

- 테이블 중 하나에서 정보 추출이 어려움
- 테이블 중 하나에는 대량의 중복 데이터가 포함
- 중복 데이터가 양쪽 테이블에 존재
- 삽입 갱신 삭제하기가 어려움 

<br>

### 자가 참조 관계 

- 테이블 내에 레코들 사이에 존재하는 관계
- 자기 자신을 참조함