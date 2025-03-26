---
{"dg-publish":true,"permalink":"/sql/006-aliasing/","created":"2025-03-14T22:28:54.091+05:30","updated":"2025-03-26T16:04:43.543+05:30"}
---

- It is used to change the name of column for most part alias join will be discussed later
- as keyword is used for this purpose
- as is optional

instead of doing this : 

![Pasted image 20250314223136.png](/img/user/Attachments/Pasted%20image%2020250314223136.png)

we can rename the avg(age) to avg_age


```sql
select gender, avg(age) as avg_age
from employee_demo
group by gender
having avg_age > 40;
```
