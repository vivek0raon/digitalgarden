---
{"dg-publish":true,"permalink":"/sql/004-having-clause/","created":"2025-03-14T22:10:05.401+05:30","updated":"2025-03-26T16:05:38.106+05:30"}
---

- It come just after group by 
- It is used to filter the group
- it is like where clause but for group

![Pasted image 20250314221226.png](/img/user/Attachments/Pasted%20image%2020250314221226.png)

this will give error has group has not yet formed and we have started filtering it 

Instead we will use having clause

```sql
select gender, avg(age)
from employe_demo
group by gender
having avg(age) > 40;
```


we can use combination of where and having clause like this


```sql
select occupation, avg(salary)
from employee_salary
where occupation like "%manager%"
group by occupation
having avg(salary)
```

![Pasted image 20250314222050.png](/img/user/Attachments/Pasted%20image%2020250314222050.png)