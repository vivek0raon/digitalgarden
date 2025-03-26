---
{"dg-publish":true,"permalink":"/sql/001-where-clause/","created":"2025-03-14T21:21:27.584+05:30","updated":"2025-03-26T16:14:50.081+05:30"}
---

it is used for adding condition to the query

```sql
select *
from employee_demo
where birth_rate > '1985-01-01';
```

## Operators

various operators are used for comparison in where clause

= , >, >=, != 


or we can also use these operators
- or
- or not
- and

it can also be used in combination

like this 

```sql
select *
from employee_demo
where (first_name = 'vivek' and age = 21) or age > 55;
```

## Like statement

- used for match the string
- can be done using % and _
- % - This says that anything that match i.e. %a anything that ends with a
- _ - this says exact number of character to match

#### example

 This will match any words which contain a in it:
 
```sql
select *
from employee_demo
where first_name like '%a%'
```


This should start with a and there should be exactly two character after that :

```sql
select *
from emplyee_demo
where first_name like 'a__' 
```

