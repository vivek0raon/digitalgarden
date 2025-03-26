---
{"dg-publish":true,"permalink":"/sql/011-subqueries/","created":"2025-03-19T23:03:05.066+05:30","updated":"2025-03-26T16:14:27.079+05:30"}
---

- It can be used instead of join

```sql
select *
from employee_demo inner join employee_salary
where employee_demo.employee_id = employee_salary.employee_id and dept_id = 1;
```

```sql
select *
from employee_demo
where employee_id in (select employee_id
from employee_salary where dept_id = 1);
```

![Pasted image 20250319231510.png](/img/user/Attachments/Pasted%20image%2020250319231510.png)


- operand should contain one column
- In is operator and inside bracket is operand

### Subquery in a select statement


```sql
select first_name, salary,
(select avg(salary))
from employee_salary)
from employee_salary;
```

### Subquery in a from statemet

```sql
select gender, avg(age), max(age), min(age), count(age)
from employee_demo
group by gender;
```

![Pasted image 20250319233023.png](/img/user/Attachments/Pasted%20image%2020250319233023.png)

What if i want to find the avg of max age and avg of min age this is not possible using above form

```sql
select avg(max_age)
from (select gender, 
avg(age) as avg_age,
max(age) as max_age,
min(age) as min_age,
count(age) as count_age
from employee_demo
group by gender
) as agg_table;
```

we used in from: every derived table must have alias

