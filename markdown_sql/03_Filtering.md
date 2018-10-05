# 필터링

<br>

- Where 절 사용

```sql
select prod_name, prod_price
from Products
where prod_price = 3.49


/*
Fish bean bag toy	3.49
Bird bean bag toy	3.49
Rabbit bean bag toy	3.49
*/

```

- 특정 범위의 값 확인하기 

```sql

select prod_name, prod_price
from Products
where prod_price BETWEEN 5 AND 10 

```

- 널값인지 확인하기

```sql
select cust_name
from Customers
where cust_email IS NULL

/*
Kids Place
The Toy Store
 */

```

