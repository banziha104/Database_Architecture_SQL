# 테이블 생성과 조작


<br>

- ### 테이블 생성

```sql
create table Products
(
  prod_id CHAR(10) NOT NULL , # Null 값 미허용
  vend_id CHAR(10) NOT NULL ,
  prod_name CHAR(10) NULL, 
  prod_desc CHAR(10) ,
  prod_price CHAR(10) DEFAULT '기본값' # 기본 값 삽입 
)
```

<br>

- ### 테이블 변경하기

```sql

ALTER TABLE Vendors
add vend_phone char(20); # 칼럼 추가


ALTER TABLE Vendors
drop column vend_phone; # 칼럼 삭제

```

- ### 테이블 삭제

```sql
drop table CustCopy 
```
