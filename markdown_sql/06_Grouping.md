# 데이터 그룹핑

- ### 그룹 생성하기

- 규칙
    - GROUP BY 절에는 원하는 만큼의 칼럼을 써서 중첩그룹을 만들 수 있음
    - GROUP BY 절에 중첩된 그룹이 있다면, 데이터는 가장 마지막에 지정된 그룹에서 요약됨
    - GROUP BY 에 있는 칼럼은 가져오는 칼럼이거나 =, 그룹 함수는 아니면서 유효한 수식이어야 함 
    - 대부분의 SQL 실행환경에서 GROUP BY 절에 문자나 메모와 같은 가변형 길이의 데이터형은 사용할 수 없ㅇ므
    - 그룹 함수 구문을 제외하고 SELECT문에 있는 모든 칼럼은 GROUP BY 절에 존재해야함
    

```sql
select vend_id, COUNT(*) AS num_prods
from Products
group by vend_id


/*
BRS01	3
DLL01	4
FNG01	2
*/


select vend_id, avg(prod_price)
from Products
group by vend_id

/*
BRS01	8.990000
DLL01	3.865000
FNG01	9.490000
*/

```


- ### 그룹 필터링 : HAVING 사용
    
```sql
select cust_id , COUNT(*) AS orders
from Orders
group by cust_id
having count(*) >= 2 

/*
1000000001	2
*/

select vend_id, count(*) as num_prods
from Products
where prod_price >= 4 # 먼저 가격이 4 이상인 행이 온뒤
group by vend_id # 그것을 vend_id 로 그룹핑하고
having count(*) >= 2  # 2이상인 행을 가져온


/*
BRS01	3
FNG01	2
*/
```


- ### 정렬

```sql
select order_num , count(*) as items
from OrderItems
group by order_num
having count(*) >= 3
order by items,order_num # group by가 정렬해주는 것보다 order by를 통해 정렬하는 것이 더욱 정확함


/*
20006	3
20009	3
20007	5
20008	5
*/

```


- ### Select 절 순서 

> select -> from -> where -> group by -> having -> order by 