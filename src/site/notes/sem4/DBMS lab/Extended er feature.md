---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/extended-er-feature/","created":"2025-02-13T09:45:09.247+05:30","updated":"2025-02-13T10:52:59.233+05:30"}
---

## Specialization

**It is the process of designing subgrouping within a entity set.**

**These subgroup has entities not shared by all the entities in the original set.**

*example:*
*consider an entity set person with attribute name, street, and city.*

*A person can be further classified as **customer** with additional attribute customer-id*
***employee** With additional attributes employee-id and salary*

`In E-R diagrams, specialization is depicted by a triangle component labeled ISA (stands for "is a"), representing superclass-subclass relationships.`

![Pasted image 20250213095302.png](/img/user/Attachments/Pasted%20image%2020250213095302.png)


## Generalization


**Generalization is bottom up design process where multiple entities sets are synthesized into a higher-level entity set based on common feature**

example:
**customer** (attributes: name, street, city, customer)
**employee** (Attributes: name, street, city, employee-id, salary)

these can be generalized into a higher-level entity set **person**

==Generalization is an inversion of specialization==



#### Summary

- **Specialization**: Differentiates entities within a set by creating distinct lower-level sets with additional attributes or relationships.
    
- **Generalization**: Combines multiple entity sets sharing common attributes into a higher-level set to emphasize similarities and simplify representation.

## Attribute inheritance


Attribute inheritance is a crucial property of the entities created by specialization and generalization. **it ensures that attributes of higher-level entities are inherited by the lower-level entities.**

### Inheritance of attributes and relationship

#### Higher-level attributes: 
Attributes of higher-level(superclass) entities are inherited by lower-level(subclass) entities.

*Example: `customer` and `employee` inherit attributes from `person`:*

- *`customer` has `name`, `street`, `city`, and `customer-id`.*
    
- *`employee` has `name`, `street`, `city`, `employee-id`, and `salary`.*
#### Inherited relationship:

Lower-level entities inherit participation in relationship sets from higher-level entities

*Example: `officer`, `teller`, and `secretary` inherit the `works-for` relationship from the `employee` entity set.*


## Aggregation:

It allows us to treat relationship as higher-level entities

this is necessary when we need to express relationship among relationship which e-r model can't do

![Pasted image 20250213103902.png](/img/user/Attachments/Pasted%20image%2020250213103902.png)

![Pasted image 20250213104007.png](/img/user/Attachments/Pasted%20image%2020250213104007.png)