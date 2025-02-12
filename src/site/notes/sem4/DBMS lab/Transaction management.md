---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/transaction-management/","created":"2025-02-12T18:48:59.456+05:30","updated":"2025-02-12T19:10:32.344+05:30"}
---

A transaction in a database is set of operation that form a single local unit of work, crucial for maintaining database atomicity, consistency and durability.


**Atomicity**: Ensure all parts of transaction are completed successfully or none at all

**consistency**: Ensures the transaction transforms the database from one consistent state to another.

**Durability**: Ensures the result of a transaction persist even if there is system failure


The database system , specifically the recovery manger, ensures atomicity and durability by preforming failure recovery .


**Concurrency - control manager ensure that concurrent transaction do not compromise database consistency.**

