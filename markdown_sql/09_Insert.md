# 데이터 삽입하기

<br>

- ### 완전한 행삽입

```sql
insert into Customers # into 는 생략이 가능하다. 다만 안되는 DB도 있다
values  (
         '100000006',
         'Toy Land',
         '123 Any Street',
         'New York',
         'NY',
         '11111',
         'USA',
         null,
         null )
         
         
# 명시적으로 넣기

insert into Customers (cust_id,
                       cust_name,
                       cust_address,
                       cust_city,
                       cust_state,
                       cust_zip,
                       cust_country,
                       cust_contact,
                       cust_email)
values ('100000006', 'Toy Land', '123 Any Street', 'New York', 'NY', '11111', 'USA', null, null)

```


<br> 

- ### 부분행 삽입하기

```sql

# 컬럼을 생략

insert into Customers (cust_id,
                       cust_name,
                       cust_address,
                       cust_city,
                       cust_state,
                       cust_zip,
                       cust_country)
values ('100000006', 'Toy Land', '123 Any Street', 'New York', 'NY', '11111', 'USA')


```

<br>

- ### 쿼리 결과를 삽입하기

```sql

insert into Customers (cust_id,
                       cust_name,
                       cust_address,
                       cust_city,
                       cust_state,
                       cust_zip,
                       cust_country,
                       cust_contact,
                       cust_email)
select cust_id,
       cust_name,
       cust_address,
       cust_city,
       cust_state,
       cust_zip,
       cust_country,
       cust_contact,
       cust_email
from CustNew;


```


<br>

- ### 다른테이블로 복사하기


```sql

/*두개는 동일함*/
select * 
into CustCopy
from Customers;


create table CustCopy as 
select * from Customers



```
