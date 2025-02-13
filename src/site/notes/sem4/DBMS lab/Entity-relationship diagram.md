---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/entity-relationship-diagram/","created":"2025-02-13T01:05:23.215+05:30","updated":"2025-02-13T10:52:49.822+05:30"}
---

it is used to visually express the overall logical structure of a database.

## Basic structure of the er diagram

**Rectangle:** Represent the entity and are divided into two parts.
- the first part contains the name of entity set
- The second part contains the name of all the attributes of the entity set
![Pasted image 20250213010841.png](/img/user/Attachments/Pasted%20image%2020250213010841.png)

**Diamonds:** Represent the relationship models

**Undivided Rectangles:** represents the attributes of a relationship set. Attributes that are part of the primary key are underlined

![Pasted image 20250213094312.png](/img/user/Attachments/Pasted%20image%2020250213094312.png)


**Lines:** Link entity sets to relationship sets.

**Dashed Lines**: Link attributes of a relationship set to the relationship set.

![Pasted image 20250213011524.png](/img/user/Attachments/Pasted%20image%2020250213011524.png)

**Double Lines:** Indicates total participation of an entity in a relationship set. 

**Double Diamonds:**  Represent the identifying relationship set linked to a weak entity sets
![Pasted image 20250213093939.png](/img/user/Attachments/Pasted%20image%2020250213093939.png)


### Mapping Cardinality

![Pasted image 20250213094134.png](/img/user/Attachments/Pasted%20image%2020250213094134.png)

E-R diagrams also indicate more complex constraints using minimum and maximum cardinality (e.g., `1..1` for exactly one, `0..*` for zero or more).

![Pasted image 20250213090119.png](/img/user/Attachments/Pasted%20image%2020250213090119.png)

### Roles 
We indicate roles in E-R diagrams by labeling the lines that connect diamonds to rectangles.

![Pasted image 20250213012053.png](/img/user/Attachments/Pasted%20image%2020250213012053.png)

![Pasted image 20250213090224.png](/img/user/Attachments/Pasted%20image%2020250213090224.png)
## Weak entity sets

![Pasted image 20250213094443.png](/img/user/Attachments/Pasted%20image%2020250213094443.png)


**Weak entity set:** An entity that does not a have sufficient attributes to form an primary key


- ***Example**: Consider a `section` entity, uniquely identified by `course id`, `semester`, `year`, and `sec id`.*
    
- *If `sec course` relationship set between `section` and `course` is created, it introduces redundancy since `course id` is already an attribute of `section`.*
    
- *To avoid redundancy:*
    
    - *Remove `course id` from `section` and store only `sec id`, `year`, and `semester`.*
        
    - *This makes `section` a weak entity set as it lacks enough attributes to form a unique identifier.*

### discriminator(partial key)): 
Attribute distinguishing weak entities within a set



**Strong Entity set:** An entity set that has a primary key.


### Reduction to relational schemas

1. **Representation of Strong Entity Sets with Simple Attributes**

We can represent a database that follows e-r relationship schemas by a collection of relation schemas.

for each entity set and relationship set in the database design , there is unique relation schemas

for the student entity set with attributes id, name, tot cred, the schemas is:
student(id, name, tot cred)

**Representation of Strong Entity Sets with Complex Attributes**

*instructor phone (ID, phone number)*


### Foreign-key constraints

**Relation schemas created from multivalued attributes has a foreign-key constraint referencing the entities set's relation.**

*Example:*

- *Foreign-key constraint on `instructor phone` relation:*
    
    - *Attribute `ID` references the `instructor` relation.*

The process of converting an E-R schema to relational schemas involves creating schemas for strong entity sets, handling composite and multivalued attributes, and setting up foreign-key constraints. This ensures a logical and structured representation of the database in relational form.


