# 가져온 데이터 정렬하기

<br>

- ### 데이터 정렬하기

```sql


select prod_name
from Products
order by prod_name

/*
12 inch teddy bear
18 inch teddy bear
8 inch teddy bear
Bird bean bag toy
Fish bean bag toy
King doll
Queen doll
Rabbit bean bag toy
Raggedy Ann
*/

```

<br>

- ### 복수개의 칼럼 정렬하기


```sql

select prod_id,prod_name,prod_price
from Products
order by prod_price, prod_name  # prod_price가 먼저 정렬되고 그 내부에서 prod_name으로 정렬된다


/*
BNBG02	Bird bean bag toy	3.49
BNBG01	Fish bean bag toy	3.49
BNBG03	Rabbit bean bag toy	3.49
RGAN01	Raggedy Ann	4.99
BR01	8 inch teddy bear	5.99
BR02	12 inch teddy bear	8.99
RYL01	King doll	9.49
RYL02	Queen doll	9.49
BR03	18 inch teddy bear	11.99
*/

```

<br>

- ### 칼럼의 위치로 정렬하기

```sql

select prod_id,prod_price,prod_name
from Products
order by 2, 3 # 2번이 먼저 정렬되고 그 내부에서 3번이 그다음 정렬된다

/*
BNBG02	Bird bean bag toy	3.49
BNBG01	Fish bean bag toy	3.49
BNBG03	Rabbit bean bag toy	3.49
RGAN01	Raggedy Ann	4.99
BR01	8 inch teddy bear	5.99
BR02	12 inch teddy bear	8.99
RYL01	King doll	9.49
RYL02	Queen doll	9.49
BR03	18 inch teddy bear	11.99
*/

```

<br> 

- ### 정렬 순서 지정


```sql


select prod_id,prod_price,prod_name
from Products
order by prod_price DESC , prod_name # prod_price가 내림차순으로 정렬된두 prod_name 이 오름차순으로 정렬됨

/*
BR03	11.99	18 inch teddy bear
RYL01	9.49	King doll
RYL02	9.49	Queen doll
BR02	8.99	12 inch teddy bear
BR01	5.99	8 inch teddy bear
RGAN01	4.99	Raggedy Ann
BNBG02	3.49	Bird bean bag toy
BNBG01	3.49	Fish bean bag toy
BNBG03	3.49	Rabbit bean bag toy
*/

```

