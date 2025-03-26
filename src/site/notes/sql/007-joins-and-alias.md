---
{"dg-publish":true,"permalink":"/sql/007-joins-and-alias/","created":"2025-03-14T22:35:55.839+05:30","updated":"2025-03-26T16:04:50.826+05:30"}
---

When the two table have a field columns then
we can use join 

![Pasted image 20250319165152.png](/img/user/Attachments/Pasted%20image%2020250319165152.png)

![Pasted image 20250319165124.png](/img/user/Attachments/Pasted%20image%2020250319165124.png)

## Inner join 

It will return rows that is same in both columns in both tables

#### Syntax

```sql
select *
from employee_demographics
INNER JOIN employee_salary
	on employee_demographics.employee_id = employee_salary.employee_id
```

![Pasted image 20250319165850.png](/img/user/Attachments/Pasted%20image%2020250319165850.png)


### Alias

```sql
select *
from employee_demographics as dem
INNER JOIN employee_salary as sal
	on dem.employee_id = sal.employee_id
```

### Outer join

-> we have left join and right join

#### Right join

It will select everything from the right table and fill with null in left side which is  not matched in both table

![Pasted image 20250319170637.png](/img/user/Attachments/Pasted%20image%2020250319170637.png)

### Joining multiple table together

 ```sql
 select *
 from employee_demo as dem
 inner join employee_sa as sal
 on dem.employee_id = sal.employee_id
 inner join parks_departiment pd
 on sal.dept_id = pd.department_id;
```

