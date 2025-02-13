---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/multiple-choice-questions/","created":"2025-02-13T10:54:12.788+05:30","updated":"2025-02-13T11:35:25.255+05:30"}
---

1. **_______ is NOT a type of constraint in Database?**  
	**Answer:** c) ALTERNATE KEY  
	_Explanation:_ An Alternate Key is not a constraint; it is a candidate key that is not selected as the primary key.

2. **_______ command makes the updates performed by the transaction permanent in the database?**  
**Answer:** b) COMMIT  
_Explanation:_ The `COMMIT` command saves all the changes made by a transaction permanently in the database.

3. **process that ensures the system will never enter a deadlock state is called _____________ **  
**Answer:** b) deadlock prevention  
_Explanation:_ Deadlock prevention ensures that a system never enters a deadlock state by imposing certain conditions.

4. **In lock conversion, upgrading can take place in only the shrinking phase, whereas downgrading can take place in only the growing phase.**  
**Answer:** b) False  
_Explanation:_ Lock upgrading happens in the growing phase, while downgrading happens in the shrinking phase.

5. **Which of the following protocols ensures conflict serializability and safety from deadlocks?**  
**Answer:** a) Two-phase locking protocol  
_Explanation:_ The Two-Phase Locking (2PL) protocol ensures conflict serializability and prevents deadlocks using strict or rigorous variations.

 **6. When transaction Ti requests a data item currently held by Tj, Ti is allowed to wait only if it has a timestamp larger than that of Tj. Otherwise, Ti is rolled back (Tj is wounded by Ti). This is**

#### **Options:**

a) Wait-die  
b) Wait-wound  
c) **Wound-wait** ✅ _(Correct Answer)_  
d) Wait

 **Solution & Explanation:**

- **Wound-Wait** mechanism ensures older transactions (lower timestamps) do not wait for younger transactions (higher timestamps).
- If an older transaction requests a resource held by a younger transaction, it **"wounds"** the younger transaction, forcing it to rollback.

**7. Which of the following is not a transaction state?**

 **Options:**

a) Active  
b) Partially committed  
c) Failed  
d) **Compensated** ✅ _(Correct Answer)_

#### **Solution & Explanation:**

- The **valid transaction states** are:
    - **Active**: Transaction is executing.
    - **Partially committed**: It has completed execution but is not yet saved permanently.
    - **Failed**: Transaction has encountered an error and cannot continue.
    - **Aborted** (not listed but is a valid state).

**if a schedule S can be transformed into a schedule S’ by a series of swaps of non-conflicting instructions, then S and S’ are**

#### **Options:**

a) Non conflict equivalent  
b) Equal  
c) **Conflict equivalent** ✅ _(Correct Answer)_  
d) Isolation equivalent

#### **Solution & Explanation:**

- **Conflict equivalence** occurs when one schedule can be transformed into another **by swapping non-conflicting operations** without changing their result.
- **Why not the others?**
    - **Non-conflict equivalent**: Incorrect terminology.
    - **Equal**: Does not capture the idea of transformation via swaps.
    - **Isolation equivalent**: Not a standard concept in concurrency control.


**9. A relation is in 2NF if:**

#### **Options:**

a) All the values of non-key attributes are dependent fully on the candidate key.  
b) Any non-key attribute that is dependent on only part of the candidate key should be moved to another relation where the partial key is the actual full key.  
c) It must be already in 1NF.  
d) **All of the mentioned** ✅ _(Correct Answer)_

 **Solution & Explanation:**

- A relation is in **Second Normal Form (2NF)** if:
    - It is already in **First Normal Form (1NF)**.
    - It does not have **partial dependencies** (i.e., non-key attributes should not depend on just a part of a composite key).
    - All **non-key attributes must depend fully** on the candidate key.

 **11. The relation employee(ID, name, street, Credit, city, salary) is decomposed into employee1 (ID, name) and employee2 (name, street, city, salary). This type of decomposition is called**
= **Options:**

A. Lossless decomposition  
B. Lossless-join decomposition  
C. **All of the mentioned** ✅ _(Correct Answer)_  
D. None of the mentioned

**Solution & Explanation:**

- **Lossless decomposition** ensures that no data is lost when a relation is split into smaller relations.
- **Lossless-join decomposition** means that we can reconstruct the original table using joins.
- **Why not the others?**
    - **(A) & (B) individually are correct**, but option (C) **"All of the mentioned"** includes both and is the best choice.
    - **(D) None of the mentioned** is incorrect since valid decompositions exist.


**27. In E-R model, a weak entity set can be converted into a strong entity set by:**

**Options:**

a) Using generalization  
b) Using aggregation  
c) **Adding appropriate attributes** ✅ _(Correct Answer)_  
d) None of the above

**Solution & Explanation:**

- A **weak entity** does not have a primary key of its own and relies on a **strong entity** for identification.
- By **adding appropriate attributes**, we can provide the weak entity with a primary key, converting it into a **strong entity set**.


 **Q Which of the following is a top-down approach in which the entity's higher level can be divided into two lower sub-entities?**

**Options:**

a) Aggregation  
b) Generalization  
c) **Specialization** ✅ _(Correct Answer)_  
d) All of the above

**Solution & Explanation:**

- **Specialization** is a **top-down** approach where a higher-level entity is divided into **sub-entities** based on distinguishing characteristics.


**Q Higher level entity sets are designated by the term:**

**Options:**

a) Sub class  
b) **Super class** ✅ _(Correct Answer)_  
c) Parent class  
d) Root class

**Solution & Explanation:**

- A **superclass** is a higher-level entity in a **generalization hierarchy**, from which lower-level **subclasses** inherit attributes.


**Q For a binary many-to-many relationship, the __-____ of the participating entity sets becomes the prime attribute.**

 **Options:**

a) Intersection of primary keys  
b) Primary key of either one  
c) **Union of primary keys** ✅ _(Correct Answer)_  
d) Primary key on the many side

**Solution & Explanation:**

- In a **many-to-many relationship**, neither entity alone can serve as a primary key. Instead, the **primary key** of the relationship set is formed by the **union of the primary keys** of the participating entities.



**Q the decomposition is unable to represent certain important facts about the relation, then such a decomposition is called as?**

**Options:**

a) Lossless decomposition  
b) **Lossy decomposition** ✅ _(Correct Answer)_  
c) Insecure decomposition  
d) Secure decomposition

**Solution & Explanation:**

- A **lossy decomposition** occurs when a relation is broken into smaller relations, but some **information is lost** during retrieval, making it impossible to reconstruct the original relation correctly.

**13. State true or false: Composite attributes have non-atomic domains.**

#### **Answer:**

✅ **True**

#### **Explanation:**

- A **composite attribute** consists of multiple sub-attributes (e.g., "Full Name" can be divided into "First Name" and "Last Name")

**Q If K → R then K is said to be the ______ of R**

**Options:**

a) Candidate key  
b) Foreign key  
c) **Super key** ✅ _(Correct Answer)_  
d) Domain

**Solution & Explanation:**

- A **super key** is a set of attributes that uniquely identify a row in a table. If **K → R** (i.e., K determines R), then K must be a **super key**.

Q. **X → Y is trivial if?**

 **Options:**

a) X ⊂ Y  
b) Y ⊂ X  
c) **X ⊇ Y** ✅ _(Correct Answer)_  
d) None of the mentioned

**Solution & Explanation:**

- A **functional dependency X → Y is trivial** if Y is a **subset of X** (**X ⊇ Y**).
- Example: `{A, B} → A` is trivial because A is already in `{A, B}`.


**Q What action does ⨝ (natural join) operator perform in relational algebra?**

**Options:**

a) Output specified attributes from all rows of the input relation and remove duplicate tuples from the output  
b) Outputs pairs of rows from the two input relations that have the same value on all attributes that have the same name  
c) **Output all pairs of rows from the two input relations (regardless of whether or not they have the same values on common attributes)** ✅ _(Correct Answer)_  
d) Return rows of the input relation that satisfy the predicate

**Solution & Explanation:**

- The **natural join (⨝)** **automatically matches** common attributes from two relations and combines rows where the values are equal.

**Q Which of the following information does an SQL DDL not specify?**

 **Options:**

a) The schema for each relation  
b) The integrity constraints  
c) The operations on the tuples  
d) **The security and authorization information for each relation** ✅ _(Correct Answer)_

**Explanation:**

- SQL **DDL (Data Definition Language)** defines the **schema, tables, constraints, and structure** of the database.
- It **does not** specify **security and authorization**, which are handled by **DCL (Data Control Language)**.


**Q Which of the following commands do we use to delete a relation (R) from a database?**

**Options:**

a) **drop table R** ✅ _(Correct Answer)_  
b) drop relation R  
c) delete table R  
d) delete from R

**Explanation:**

- The **DROP TABLE** command is used to completely remove a table and all its data from the database.
- **DELETE FROM** only removes rows but retains the table.
- **DROP RELATION** and **DELETE TABLE** are incorrect as they are not valid SQL syntax.

**Q In FROM clause, instead of table name a subquery expression may also appear-**

 **Answer:**

✅ **True**

 **Explanation:**

- In SQL, **a subquery (also called an inline view)** can replace a table name in the **FROM** clause.
- Example:

**Q If we specify multiple relations in the FROM clause and do not specify any conditions in the WHERE clause, what will the result be?**

**Options:**

a) The natural join of both the relations  
b) The left outer join of both the relations  
c) A syntactical error  
d) **The Cartesian product of both the relations** ✅ _(Correct Answer)_

 **Explanation:**

- When **no condition** is provided, SQL **performs a Cartesian product** of the tables, meaning each row from the first table is paired with every row from the second table.

 **Q ________ can work on Schema Definition.**

 **Options:**

a) Application Programmer  
b) Naive User  
c) Sophisticated User  
d) **Database Administrator** ✅ _(Correct Answer)_

 **Explanation:**

- **Schema definition** involves designing the database structure, which is done by the **Database Administrator (DBA)**.


**Q Which of the following refers to the level of data abstraction that describes exactly how the data is actually stored?**

**Options:**

a) Conceptual Level  
b) **Physical Level** ✅ _(Correct Answer)_  
c) File Level  
d) Logical Level

 **Explanation:**

- The **Physical Level** describes **how data is stored on disk** (e.g., indexes, file storage, block structures).



 **Q Which of the following is a Data Model?**

 **Options:**

a) Entity-Relationship model  
b) Relational data model  
c) Object-Based data model  
d) **All of the above** ✅ _(Correct Answer)_

 **Explanation:**

- **Data models** define how data is structured and manipulated.
- **Entity-Relationship Model (ER Model)**: Represents data in terms of entities and relationships.
- **Relational Model**: Represents data as **tables with rows and columns**.
- **Object-Based Model**: Uses object-oriented concepts for database representation.