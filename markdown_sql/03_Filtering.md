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

<br>

# 고급 데이터 필터링

<br>

- ### AND 연산자

```sql
select prod_id, prod_price, prod_name
from Products
where vend_id = 'DLL01' AND prod_price <= 4;

/*
BNBG01	3.49	Fish bean bag toy
BNBG02	3.49	Bird bean bag toy
BNBG03	3.49	Rabbit bean bag toy
*/

```

<br>

- ### OR 연산자

```sql
select prod_id, prod_price, prod_name
from Products
where vend_id = 'DLL01' OR vend_id =  'BRS01';


/*
BNBG01	3.49	Fish bean bag toy
BNBG02	3.49	Bird bean bag toy
BNBG03	3.49	Rabbit bean bag toy
BR01	5.99	8 inch teddy bear
BR02	8.99	12 inch teddy bear
BR03	11.99	18 inch teddy bear
RGAN01	4.99	Raggedy Ann
*/

```

<br>

- ### 우선순위

```sql
select prod_id, prod_price, prod_name
from Products
where (vend_id = 'DLL01' OR vend_id =  'BRS01') AND prod_price >= 10

/*
BR03	11.99	18 inch teddy bear
*/

```

<br>

- ### IN 연산자 : 조건의 범위 지정

```sql

select prod_name, prod_price
from Products
where vend_id IN ('DLL01', 'BRS01')
order by prod_name

/*
12 inch teddy bear	8.99
18 inch teddy bear	11.99
8 inch teddy bear	5.99
Bird bean bag toy	3.49
Fish bean bag toy	3.49
Rabbit bean bag toy	3.49
Raggedy Ann	4.99
*/

```


<br>

- ### NOT 연산자 : 다른연산자와 함께 써야하며, 칼럼 앞에 붙는다

```sql
select prod_name
from Products
where not  vend_id = 'DLL01' # != 이나 <>과 같다
order by prod_name 

/*
12 inch teddy bear
18 inch teddy bear
8 inch teddy bear
King doll
Queen doll
*/

```

<br>

# 와일드카드 문자를 이용한 필터링