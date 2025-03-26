---
{"dg-publish":true,"permalink":"/sql/002-group-by/","created":"2025-03-14T21:40:52.468+05:30","updated":"2025-03-26T16:05:42.269+05:30"}
---

This is used to roll up all the value into this rows

```sql
select gender
from employee_demo
group by gender;
```

![Pasted image 20250314214354.png](/img/user/Attachments/Pasted%20image%2020250314214354.png)

now when we can apply aggregate function into it

- when aggregate function is applied after grouping it like avg(something) the value of this avg will only be based on group wise meaning avg of something(ex marks) on basis of group female

- when we are not using aggregate function then column which we are selecting should match with what we are grouping with example gender

**What will happen if we have two values in group by?**

- Similar distinct it consider duplicate element if the another pair is different

![Pasted image 20250314215545.png](/img/user/Attachments/Pasted%20image%2020250314215545.png)


### aggregate function

```sql
select gender,avg(age)
from employee
group by gender;
```

![Pasted image 20250314215203.png](/img/user/Attachments/Pasted%20image%2020250314215203.png)


#### Various aggregate function are

- Avg()
- Max()
- Min()
- Count()

```sql
select gender, avg(age), max(age), min(age), count(age)
from employe_demo
group by gender;
```





