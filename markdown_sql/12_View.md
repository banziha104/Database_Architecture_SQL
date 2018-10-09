# 뷰 사용하기

<br>

- ### 뷰 생성하기 

```sql
Create View ProductCustomer as
  select cust_name, cust_contact, prod_id
  from Customers c , Orders od, OrderItems oi
  where c.cust_id = od.cust_id and oi.order_num = od.order_num;
```

<br>

- ### qb qhrl 

```sql
select *
from productcustomer;

/*
Village Toys	John Smith	BR01
Village Toys	John Smith	BR03
Village Toys	John Smith	BNBG01
Village Toys	John Smith	BNBG02
Village Toys	John Smith	BNBG03
Fun4All	Jim Jones	BR01
Fun4All	Jim Jones	BR02
Fun4All	Jim Jones	BR03
Fun4All	Denise L. Stephens	BR03
Fun4All	Denise L. Stephens	BNBG01
Fun4All	Denise L. Stephens	BNBG02
Fun4All	Denise L. Stephens	BNBG03
Fun4All	Denise L. Stephens	RGAN01
The Toy Store	Kim Howard	RGAN01
The Toy Store	Kim Howard	BR03
The Toy Store	Kim Howard	BNBG01
The Toy Store	Kim Howard	BNBG02
The Toy Store	Kim Howard	BNBG03
*/
```

- ### 뷰 생성시 필터링