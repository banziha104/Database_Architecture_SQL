# 업데이트 
 
<br>
 
- ### 특정컬럼 업데이트 하기 
 
 
```sql
update Customers
set cust_email = 'kim@thetoystore.com',
    cust_contact = 'Sam Roberts'
where cust_id = ' 100000005'
```


<br>

- ### 칼럼 값 삭제

 
```sql
update Customers
set cust_email = NULL # Null 이 허용된 경우만 가능
where cust_id = ' 100000005'
```

<br>

---

- ### 데이터 삭제

```sql

delete from Customers
where cust_id = '100000006' # where 절을 누락할 경우 모든 데이터가 삭제되는 문제가 생김

```



