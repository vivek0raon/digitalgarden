---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/database-design-and-e-r-model/","created":"2025-02-12T23:09:22.843+05:30","updated":"2025-02-13T10:53:16.494+05:30"}
---

purpose: developed to facilitates database design by representing the overall logical structure of a database.


### components of e-r model

#### Entity set
collection of similar entities 

#### Relation sets

collections between entities

#### Attributes
properties or characteristics of entities


## Entity set

An entity is an object distinguishable from other object, having a set of properties that uniquely identify it.

eg: each person in a university is an entity with properties such as person id.

**collection of entities of same type sharing the same properties is known as entity set**

each entity has a value of each atributes


## Relation set

**A relationship is an association among multiple entities**

**The relationship set is a collection of relationships of the same type**

#### Degree of relationship sets

**Binary relation set**: involves two entity sets
**Involves three entity sets**



### Descriptive attributes

Attributes that provides additional information about a relationship

eg: the **advisor** relationship set can have a descriptive attributes **date** to specify when an instructor became a student's advisor


## Attributes

Attributes in e-r model are descriptive properties associated with entities in an entity set. Each attributes has a set of permitted values knows as its domain.

eg: domain of semester might be {fall, Winter, Spring, Summer}

### Types of Attributes


![Pasted image 20250213094358.png](/img/user/Attachments/Pasted%20image%2020250213094358.png)

#### Simple and composite attributes

![Pasted image 20250213003150.png](/img/user/Attachments/Pasted%20image%2020250213003150.png)

Simple Attributes: indivisible attributes

Composite attributes: can be divided into subparts

eg: An attributes name can be divided into first name, middle initial and last name.
an attributes address can be divided into street, city, state, and postal code

- Hierarchy: Composite attributes may have a hierarchical structure. for example street can be further divided into street number, street name, and apartment number

#### Single-valued and multivalued attributes

**Single-valued attributes:** Have a single value for a particular entity.

*example: student id for a student entity*

**Multivalued attributes**: Have a set of value for a specific entity.

*example: An instructor may have multiple phone number or dependents.*
*multivalued attributes are denoted with brances. such as {phone number}*

#### Derived Attributes

Values can be derived from other related attributes or entities

*eg: age can be derived from date of birth*

- **base attribute**: The stored attribute used to derive the value



#### Null values

When an entity doesn't have a values for an attribute

not 









