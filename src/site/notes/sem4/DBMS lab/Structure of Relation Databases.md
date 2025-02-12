---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/structure-of-relation-databases/","created":"2025-02-12T19:37:46.128+05:30","updated":"2025-02-12T21:00:35.443+05:30"}
---

The relational database is composed of multiple tables ,each with unique name.
Tables consists of column(attribute) and rows(tuples)

### Table example
Instructor table:
columns: id, name, dept name, salary
rows: each row stores information about an instructor

### Key concepts:

Relation: Refers to a table.
Tuple: Refers to a row in a table
Attribute: Refers to a column in the table
Relation instance: specific set of rows in the table.


## Domain:

The domain of an attributes are set of permitted values of that attributes

eg: The domain of the salary attribute is all possible salary values.

Atomic domain: A domain is atomic if its elements are individual units

### Null values

Null: A special values indicating that the value is unknown or does not exist.
it causes difficulties in database and should be avoided wherever possible.


### Order of tuples:

The order in which the tuples appear is irrelevant; a relation is a set of tuples.

### Multiple-Choice Questions:

**1. What does a relational database consist of?** a) Collection of schemas b) Collection of tables c) Collection of queries d) Collection of views

**Answer:** b) Collection of tables

**2. In the context of relational databases, what does a "tuple" refer to?** a) A column b) A table c) A row d) An attribute

**Answer:** c) A row

**3. What is the domain of an attribute in a relational database?** a) The set of all possible tables b) The set of all possible column names c) The set of permitted values for that attribute d) The set of all possible rows

**Answer:** c) The set of permitted values for that attribute

**4. Which value signifies that the data is unknown or does not exist?** a) Null b) Zero c) Empty string d) Undefined

**Answer:** a) Null

**5. What is the term used for a specific instance of a relation containing a specific set of rows?** a) Relation schema b) Relation instance c) Relation domain d) Relation attribute

**Answer:** b) Relation instance

**6. In the relational model, what term is used to refer to a table?** a) Tuple b) Attribute c) Domain d) Relation

**Answer:** d) Relation

**7. What must all attributes of a relation have according to the relational model?** a) String values b) Atomic domains c) Numeric values d) Null values

**Answer:** b) Atomic domains

**8. Which table stores prerequisite relationships between courses in the example given?** a) Instructor table b) Course table c) Prereq table d) Student table

**Answer:** c) Prereq table

**9. Why should null values be avoided in a relational database?** a) They take up extra space b) They cause difficulties in accessing or updating the database c) They are not supported by all database systems d) They require special storage structures

**Answer:** b) They cause difficulties in accessing or updating the database

**10. In what order are tuples in a relation stored according to the relational model?** a) Alphabetically b) Numerically c) Randomly d) The order is irrelevant

**Answer:** d) The order is irrelevant





