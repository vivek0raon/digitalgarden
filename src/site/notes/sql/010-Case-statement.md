---
{"dg-publish":true,"permalink":"/sql/010-case-statement/","created":"2025-03-19T22:44:55.546+05:30","updated":"2025-03-26T16:14:29.404+05:30"}
---

- Adding cases on a certain field


```sql
select first_name, last_name, age
case
	when age <=30 then 'Young'
	when age between 31 and 50 then 'old'
	when age >=50 then "on Death's Door"
end as Age_bracket
from employee_demo;
```

![Pasted image 20250319224928.png](/img/user/Attachments/Pasted%20image%2020250319224928.png)


#### Calculate new salary according to following

 ```
 < 50000 = 5%
 > 50000 = 7%
	finance = 10% bonus
```

```sql
select first_name, last_name, salary,
case
	when salary < 50000 then salary + (salary * 0.05)
end as new_salary
from employee_salary;
```

can also be written as

```sql
select first_name, last_name, salary,
case
	when salary < 50000 then salary * 1.05
	when salary > 50000 then salary * 1.07
	when  
end as new_salary
case
	when dept_id = 6 then salary * .10
end as bonus
from employee_salary;
```


![Pasted image 20250319230234.png](/img/user/Attachments/Pasted%20image%2020250319230234.png)
