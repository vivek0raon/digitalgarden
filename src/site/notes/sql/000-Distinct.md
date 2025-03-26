---
{"dg-publish":true,"permalink":"/sql/000-distinct/","tags":["gardenEntry"],"created":"2025-03-14T21:12:07.796+05:30","updated":"2025-03-26T16:03:53.031+05:30"}
---

Do not select duplicate element

```sql
select distinct gender
from student;
```

above query will only select female and male

but ==what if i put two rows in it?==

```sql
select distinct first_name, gender,
from student;
```

above query will also select duplicate name if the gender is different

![Pasted image 20250314212038.png](/img/user/Attachments/Pasted%20image%2020250314212038.png)

