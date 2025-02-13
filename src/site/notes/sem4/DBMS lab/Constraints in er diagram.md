---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/constraints-in-er-diagram/","created":"2025-02-13T00:38:10.443+05:30","updated":"2025-02-13T01:05:18.985+05:30"}
---


## Mapping cardinalities

it express the number of entities which another entity can be associated via a relationship set.

#### Types of Mapping Cardinalities

![Pasted image 20250213005948.png](/img/user/Attachments/Pasted%20image%2020250213005948.png)

- One to one: an entity in a set A is associated with at most one entity in set B and, vice versa.
- One to many: An entity in set a is associated with any number of entity in set b , but an entity in set b is only assocated with one entity in set a
- Many to one 
- many to many 

![Pasted image 20250213010013.png](/img/user/Attachments/Pasted%20image%2020250213010013.png)

*examples:*
*in university if a student can be advised by only one instructor but an instructor can advise many student then it is considered one to many*

*if a student can be advised my many instructor then many to many*

### Participation constraints

it defines whether the participation of an entity set in a relationship set is total or partial


#### Total participation: 
Every entity in the entity set E participate in at least one relationship in the relationship set R.

#### Partial participation

Only some entity in the entity set E participate in relationship in set R

*eg:  total participation: every student entity is related to instructor entity through the advisor relationship set R.*

*not every instructor advises a student so the participation of instructor in a the advisor relationship set is partial* 

#### Keys:

[[sem4/DBMS lab/keys\|keys]]

##### Types of Keys

- **Superkey**: A set of attributes that uniquely identify an entity.
    
- **Candidate Key**: A minimal superkey.
    
- **Primary Key**: A chosen candidate key for an entity set.

##### Keys in Relationship Sets

- **The primary key for a relationship set** is composed of the primary keys of the participating entity sets.
    
- For many-to-many relationships, the primary key is the union of the primary keys of the involved entity sets.
    
- For many-to-one relationships, the primary key depends on the direction (e.g., if the relationship is from student to instructor, the primary key is the student's primary key).


