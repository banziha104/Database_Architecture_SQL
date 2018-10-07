# 데이터 요약

<br>

- ### 합계 함수

| 함수    	| 설명                    	|
|---------	|-------------------------	|
| AVG()   	| 칼럼의 평균값 반환      	|
| COUNT() 	| 칼럼에 있는 개수를 반환 	|
| MAX()   	| 칼럼의 최대값           	|
| MIN()   	| 칼럼의 최소값           	|
| SUM()   	| 칼럼의 합계             	|

<br>

```sql
select avg(prod_price) as avg_price
from Products

/*
6.823333
*/

```