---
{"dg-publish":true,"permalink":"/sql/003-order-by/","created":"2025-03-14T21:59:30.356+05:30","updated":"2025-03-26T16:14:44.544+05:30"}
---

This is used to sort the column in ascending or descending order 
- by default it is in ASC(ascending order)
- for descending order we add DESC

```sql
select *
from employee_demo
order by first_name desc;
```

***What if we use two column in order by***

- when used two column in order by it will first sort by first element in order by statement then then by second element

eg:

```sql
select *
from employee_demo
order by gender, age;
```

First it will sorted by gender then age

![Pasted image 20250314220440.png](/img/user/Attachments/Pasted%20image%2020250314220440.png)

**Also instead of the name of column we can also give column number**

```sql
select *
from employee_demo
order by 5, 4; # 5 represent gender
```
