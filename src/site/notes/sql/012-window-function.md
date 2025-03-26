---
{"dg-publish":true,"permalink":"/sql/012-window-function/","created":"2025-03-22T12:18:51.968+05:30","updated":"2025-03-26T16:05:22.689+05:30"}
---

 ```sql
 select gender, avg(salary) as avg_salary
 from employee_demographics dem
 join employee_salary as sal
 on dem.employee_id = sal.employee_id
 group by gender;
```

### Using window function

#### OVER(PARTITION BY gender) instead of group by gender

```sql
select gender, avg(salary) over(partition by gender)
from employee_demo dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
```

![Pasted image 20250322122439.png](/img/user/Attachments/Pasted%20image%2020250322122439.png)

#### But why use this

if we want to access other thing from the table it can be done using this

```sql
select dem.first_name, dem.last_name, gender, avg(salary) over(partition by gender)
from employee_demo dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
```

![Pasted image 20250322122650.png](/img/user/Attachments/Pasted%20image%2020250322122650.png)

group by will give different result

```sql
select dem.first_name, dem.last_name, gender, avg(salary)
from employee_demo dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
group by dem.first_name, dem.last_name
```

![Pasted image 20250322122843.png](/img/user/Attachments/Pasted%20image%2020250322122843.png)
### Rolling total

add value line by line

```sql
select dem.first_name, dem.last_name, gender, salary,
sum(salary) over(partition by gender order by dem.employee_id) as rolling_total
from employee_demographics dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
```


![Pasted image 20250322123602.png](/img/user/Attachments/Pasted%20image%2020250322123602.png)

```sql
select dem.employee_id, dem.first_name, dem.last_name, gender, salary, row_number()
over(partition by gender order by salary desc)
from employee_demographics dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
```

## Row_number()

![Pasted image 20250322124156.png](/img/user/Attachments/Pasted%20image%2020250322124156.png)
- it assigned the row number according to gender then order the salary in desc order

### Rank()

we it encounter the duplicate based on order by something ... it gives same rank value to both
next number will will be positionally after 5 there is 7

```sql
select dem.employee_id, dem.first_name, dem.last_name, gender, salary, row_number()
over(partition by gender order by salary desc)
from employee_demographics dem
join employee_salary sal
on dem.employee_id = sal.employee_id;
```

![Pasted image 20250322124952.png](/img/user/Attachments/Pasted%20image%2020250322124952.png)

### dense_rank()

next number will will be numerically after 5 there is 6

![Pasted image 20250322125130.png](/img/user/Attachments/Pasted%20image%2020250322125130.png)