# 서브쿼리 

<br>

- ### 서브쿼리 사용

```sql
select cust_name, cust_contact
from Customers
where cust_id in (select cust_id
                 from Orders
                 where order_num in (select order_num
                                    from OrderItems
                                    where prod_id = 'RGAN01'))
/*
Fun4All	Denise L. Stephens
The Toy Store	Kim Howard
*/
```

<br>

- ### 계산필드로 서브쿼리 사용

```sql
select cust_name, cust_state, (
                              select COUNT(*)
                              from Orders 
                              where Orders.cust_id = Customers.cust_id) as orders
from Customers
order by cust_name


/*
Fun4All	IN	1
Fun4All	AZ	1
Kids Place	OH	0
The Toy Store	IL	1
Village Toys	MI	2
*/

```