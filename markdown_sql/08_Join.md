# 조인

<br>

- ### 조인 생성 

```sql
select vend_name,prod_name,prod_price
from Vendors, Products
where Vendors.vend_id = Products.vend_id # 조인 조건이 없으면 카디전 곱연산(Vendor의 row X Product row X)을 한다. 

/*
Doll House Inc.	Fish bean bag toy	3.49
Doll House Inc.	Bird bean bag toy	3.49
Doll House Inc.	Rabbit bean bag toy	3.49
Bears R Us	8 inch teddy bear	5.99
Bears R Us	12 inch teddy bear	8.99
Bears R Us	18 inch teddy bear	11.99
Doll House Inc.	Raggedy Ann	4.99
Fun and Games	King doll	9.49
Fun and Games	Queen doll	9.49
*/


```

<br>

- ### 내부 조인 

```sql

select vend_name, prod_name, prod_price
from Vendors v inner join Products p on v.vend_id = p.vend_id


/*
Doll House Inc.	Fish bean bag toy	3.49
Doll House Inc.	Bird bean bag toy	3.49
Doll House Inc.	Rabbit bean bag toy	3.49
Bears R Us	8 inch teddy bear	5.99
Bears R Us	12 inch teddy bear	8.99
Bears R Us	18 inch teddy bear	11.99
Doll House Inc.	Raggedy Ann	4.99
Fun and Games	King doll	9.49
Fun and Games	Queen doll	9.49
*/

```

<br>

- ### 셀프조인

```sql

select c1.cust_id, c1.cust_name, c1.cust_contact
from Customers c1, Customers c2
where c1.cust_name = c2.cust_name
and c2.cust_contact = 'Jim Jones'

/*
1000000003	Fun4All	Jim Jones
1000000004	Fun4All	Denise L. Stephens
*/

```


- 외부 조인

```sql
# Left 외부 조인

select C.cust_id, o.order_num
from Customers c LEFT OUTER JOIN Orders O on c.cust_id = O.cust_id
# 외부 조인은, 실제 관련없는 행도 가져온다

/*
select C.cust_id, o.order_num
from Customers c LEFT OUTER JOIN Orders O on c.cust_id = O.cust_id
# 외부 조인은, 실제 관련없는 행도 가져온다
*/


select C.cust_id, o.order_num
from Customers c RIGHT OUTER JOIN Orders O on c.cust_id = O.cust_id

/*
1000000001	20005
1000000001	20009
1000000003	20006
1000000004	20007
1000000005	20008
*/

```

<br>

- ### 그룹 함수와 조인 함수 


```sql
select c.cust_id, COUNT(o.order_num) num_ord
From Customers c Inner join Orders O on c.cust_id = O.cust_id
group by c.cust_id


```