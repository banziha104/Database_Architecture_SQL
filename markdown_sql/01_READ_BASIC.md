# 데이터 가져오기


- ### 단일 칼럼 가져오기

```sql

select prod_name
from Products

/*
결과 값
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


- ### 다중 칼럼 가져오기

```sql

select prod_name, prod_id, prod_price
from Products

/*
Fish bean bag toy	BNBG01	3.49
Bird bean bag toy	BNBG02	3.49
Rabbit bean bag toy	BNBG03	3.49
8 inch teddy bear	BR01	5.99
12 inch teddy bear	BR02	8.99
18 inch teddy bear	BR03	11.99
Raggedy Ann	RGAN01	4.99
King doll	RYL01	9.49
Queen doll	RYL02	9.49
*/
```


- ### 모든 칼럼가져오기

```sql
select *
from Products

/*
BNBG01	DLL01	Fish bean bag toy	3.49	Fish bean bag toy, complete with bean bag worms with which to feed it
BNBG02	DLL01	Bird bean bag toy	3.49	Bird bean bag toy, eggs are not included
BNBG03	DLL01	Rabbit bean bag toy	3.49	Rabbit bean bag toy, comes with bean bag carrots
BR01	BRS01	8 inch teddy bear	5.99	8 inch teddy bear, comes with cap and jacket
BR02	BRS01	12 inch teddy bear	8.99	12 inch teddy bear, comes with cap and jacket
BR03	BRS01	18 inch teddy bear	11.99	18 inch teddy bear, comes with cap and jacket
RGAN01	DLL01	Raggedy Ann	4.99	18 inch Raggedy Ann doll
RYL01	FNG01	King doll	9.49	12 inch king doll with royal garments and crown
RYL02	FNG01	Queen doll	9.49	12 inch queen doll with royal garments and crown

*/

```

- ### 중복행 출력 방지하기

```sql

select DISTINCT vend_id
from Products


/*
BRS01
DLL01
FNG01
*/

```