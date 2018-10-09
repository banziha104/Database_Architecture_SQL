# 고급 데이터 조작

- 제약조건 : 데이터베이스 데이터가 어떻게 삽입되고 조작될 것인가를 통제하는 규칙
- 주키 : 고유하면서 절대 변하지 않는 다는 것을 보장  
- 외래키 : 테이블에 있는 컬럼이면서 다른 테이블의 주키로 정의된 칼럼

```sql
create table Orders
(
  order_num INTEGER not null primary key,
  cust_id   char(10) not null references Customers(cust_id)
)

```

- Unique 무결성 제약 조건 : 데이터가 모두 다른 제약조건
- Check 무결성 제약 조건 : 허용 가능한 데이터의 범위나 조건을 지정하기 위한 제약 조건 

```sql
create table Orders
(
  order_num INTEGER not null primary key,
  cust_id   char(10) not null references Customers(cust_id)
  qunantitiy integer not null check(quantitiy > 0 )
)
```
