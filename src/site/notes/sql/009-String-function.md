---
{"dg-publish":true,"permalink":"/sql/009-string-function/","created":"2025-03-19T22:23:26.993+05:30","updated":"2025-03-26T16:14:31.639+05:30"}
---

## Length function

- It gives the length of the string

```sql
select length('skyfall')
```

![Pasted image 20250319222512.png](/img/user/Attachments/Pasted%20image%2020250319222512.png)

#### show name with the length of the name


```sql
Select first_name, length(first_name)
from employee_demo
order by 2;
```


### Upper and lower function

for making it to upper and lower case

```sql
select upper('sky');
select lower('sky');
```

### Trim function

It trims the whitespaces

syntax:

```sql
select trim('      sky    ');
```

output:

![Pasted image 20250319223104.png](/img/user/Attachments/Pasted%20image%2020250319223104.png)
#### Ltrim
- only trim from left hand side

```sql
select ltrim('      sky    ');
```

![Pasted image 20250319223223.png](/img/user/Attachments/Pasted%20image%2020250319223223.png)
#### Rtrim
- Only trim from right hand side
```sql
select rtrim('      sky    ');
```


### Left and right function

```sql
select first_name,
left(first_name, 4),
right(first_name, 4)
from employee_demo;
```

### Substring function

```sql
select first_name
substring(first_name, 3, 2) // first position and how much
from employee_demo;
```

![Pasted image 20250319223542.png](/img/user/Attachments/Pasted%20image%2020250319223542.png)

##### Better example

finding only birth_month
![Pasted image 20250319223817.png](/img/user/Attachments/Pasted%20image%2020250319223817.png)

### Replace function

Replace the letter with different letter in a string

```sql
select first_name, replace(first_name, 'a', 'z')
from employee_demo;
```

![Pasted image 20250319224000.png](/img/user/Attachments/Pasted%20image%2020250319224000.png)

### Locate function

- It is used to find the position of the char in the string

```sql
select locate('x', "Alexander');
```

![Pasted image 20250319224112.png](/img/user/Attachments/Pasted%20image%2020250319224112.png)

### Concat function

- used for concatenate string from two different field to one 

```sql
select first_name, last_name,
concat(first_name,' ' last_name) as full_name
from employee_demo;
```


![Pasted image 20250319224436.png](/img/user/Attachments/Pasted%20image%2020250319224436.png)


