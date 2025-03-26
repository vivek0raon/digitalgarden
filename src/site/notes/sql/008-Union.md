---
{"dg-publish":true,"permalink":"/sql/008-union/","created":"2025-03-19T20:24:24.192+05:30","updated":"2025-03-26T16:14:33.840+05:30"}
---

Used for
- Combining one select statement to another select statement

##### Bad example

```sql
select age, gender
from employee_demographics
union
select first_name, last_name
from employee_salary;
```

![Pasted image 20250319202638.png](/img/user/Attachments/Pasted%20image%2020250319202638.png)

- when using this we need to keep the data the same

```sql
select first,name, last_name
from employee_demo
union
select first_name, last_name
from employee_salary;
```

![Pasted image 20250319202906.png](/img/user/Attachments/Pasted%20image%2020250319202906.png)

- Union is by default distinct

```sql
select first_name, last_name
from employee_demo
union distinct
select first_name, last_name
from employee_salary;
```

- WE can use 'all' for also select the duplicate values

```sql
select first_name, last_name
from employee_demographic
union all
select first_name, last_name
from employee_salary
```

### Multiple Union

```sql
select first_name, last_name, 'Old Man' as Label
from employee_demo
where age > 40 and gender = 'Male'
Union
select first_name, last_name, "Old women" as
label from employee_demo
Union
select first_name, last_name , 'Highly Paid Employee' as Label
from employee_salary
where salary > 70000
Order by first_name, last_name;
```

![Pasted image 20250319222237.png](/img/user/Attachments/Pasted%20image%2020250319222237.png)

