---
{"dg-publish":true,"permalink":"/sql/005-limit/","created":"2025-03-14T22:22:28.030+05:30","updated":"2025-03-26T16:14:40.347+05:30"}
---

It is used to limit the number of rows in from the select rows

```sql
select *
from employee_demo
limit 3;
```

![Pasted image 20250314222347.png](/img/user/Attachments/Pasted%20image%2020250314222347.png)

## Can be use by order by

#### Find the oldest 3 persons

```sql
select *
from emplyee_demo
order by age desc
limit 3
```

![Pasted image 20250314222541.png](/img/user/Attachments/Pasted%20image%2020250314222541.png)


***When two argument is used then it will start from first argument and take number of element assigned in second argument***


```sql
select *
from emplyee_demo
order by age desc
limit 2, 1
```

![Pasted image 20250314222805.png](/img/user/Attachments/Pasted%20image%2020250314222805.png)

