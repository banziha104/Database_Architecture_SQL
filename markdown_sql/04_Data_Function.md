# 데이터 조작 함수 사용하기

<br>

- ### 문자 조작 함수

| 이름       | 설명 |
|-----------|-----------------------------------------------|
| LEFT()    | 문자열 왼쪽에서부터 오른쪽 문자열 일부를 추출 |
| LENGTH()  | 문자열의 길이를 반환                          |
| LOWER()   | 문자열을 소문자로 반환                        |
| LTRIM()   | 왼쪽 공백 제거                                |
| RIGHT()   | 문자열 오른쪾에서부터 문자열 일부를 추출      |
| RTRIM)    | 문자열 오른쪽에 있는 공백문자 삭제            |
| SOUNDEX() | 문자열의 SOUNDEXT를 반환                      |
| UPPER()   | 문자열을 대문자로 반환                        |

```sql
select vend_name, UPPER(vend_name) as vend_name_upcase
from Vendors
order by vend_name

/*
Bear Emporium	BEAR EMPORIUM
Bears R Us	BEARS R US
Doll House Inc.	DOLL HOUSE INC.
Fun and Games	FUN AND GAMES
Furball Inc.	FURBALL INC.
Jouets et ours	JOUETS ET OURS
*/

```