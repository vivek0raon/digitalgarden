---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/keys/","created":"2025-02-12T20:17:22.095+05:30","updated":"2025-02-12T21:00:25.285+05:30"}
---

Keys in relation database

## Superkey

A set of one or more attributes in the table that uniquely identify the tuples in a relation

eg: the id attribute in the instructor relation is superkey because it uniquely distinguish one instructor from another.


## Candidate key:

A minimal superkey ie. a superkey with no extraneous attributes

example: **id** is a candidate key for the **instructor** relation. if a combination of name and deptname can also uniquely identify an instructor, then {id} and {name,deptname} are candidate keys.

**however {id, name} is not a candiate key since id alone is sufficient.**


### Primary key:

A candidate key chosen by the database designer to uniquely identify tuples within a relation.

eg: social-security numbers or enterpise-generated unique identifiers.


### Foreign key:

**An attribute in one relation that is primary key in another relation.**

eg: in deptname in instructor relation is foreign key referencing department relation

### Referential integrity constraints

Definition: requires that values in specified attributes of a tuple in the referencing relation must match values in specified attribute of at least one tuple in the referenced relation


example: Ensuring that a section exist for course in the **section** relation must be taught by at least one instructor in the **teaches** relation

### Multiple-Choice Questions:

**1. What is a superkey?** a) A set of one or more attributes that uniquely identify a tuple in a relation b) A single attribute that uniquely identifies a tuple in a relation c) A set of attributes that must contain extraneous attributes d) A subset of attributes that cannot identify a tuple in a relation

**Answer:** a) A set of one or more attributes that uniquely identify a tuple in a relation

**2. Which of the following is NOT true about a candidate key?** a) It is a minimal superkey b) It can have extraneous attributes c) It uniquely identifies tuples in a relation d) There can be multiple candidate keys in a relation

**Answer:** b) It can have extraneous attributes

**3. What is a primary key?** a) A superkey chosen by the database designer to uniquely identify tuples in a relation b) A set of attributes that contains extraneous attributes c) A combination of all attributes in a relation d) A foreign key from one relation referencing another

**Answer:** a) A superkey chosen by the database designer to uniquely identify tuples in a relation

**4. Which attribute is most suitable to be chosen as a primary key?** a) Name b) Address c) Social-security number d) Department name

**Answer:** c) Social-security number

**5. What is a foreign key?** a) A primary key in the same relation b) An attribute in one relation that is a primary key in another relation c) A minimal superkey d) A combination of attributes that uniquely identify a tuple in the same relation

**Answer:** b) An attribute in one relation that is a primary key in another relation

**6. Which of the following best describes a referential integrity constraint?** a) Ensures that all tuples in a relation are unique b) Requires values in specified attributes of a referencing relation to appear in the referenced relation c) Allows tuples in a relation to have duplicate values for key attributes d) Prevents any changes to the database schema

**Answer:** b) Requires values in specified attributes of a referencing relation to appear in the referenced relation

**7. Why should primary key attributes be chosen with care?** a) Because they should be frequently changed b) Because they can contain extraneous attributes c) Because they should never or very rarely change d) Because they should be duplicated in other relations

**Answer:** c) Because they should never or very rarely change

**8. Which of the following is an example of a candidate key?** a) {ID, name} b) {ID, deptname} c) {name, deptname} d) {ID, name, deptname}

**Answer:** c) {name, deptname}