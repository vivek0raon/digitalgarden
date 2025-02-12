---
{"dg-publish":true,"permalink":"/sem4/dbms-lab/architecture-of-a-database/","created":"2025-02-12T18:58:04.800+05:30","updated":"2025-02-12T19:11:34.406+05:30"}
---

The architecture of a database system is influenced by the underlying computer system, and it can be **centralized, client-server, parallel or distributed across multiple machines**.


## Centralized and client-server system

centralized run on a single machine, whereas client-server systems have a server handling multiple clients.


## parallel architectures: 

Databases designed to use parallel processing


## Distributed Database:

Database designed to span multiple geographical separated machines



## Client and server machine

client machine: where remote users work
Server machine: where the database system runs


## Different Architecture

#### Two-tier architecture: 

Client machines invokes the database functionality at the server using odbc and jdbc


#### Three-tier Architecture

Client acts as a frontend, communicated with application server, which then interact with database systems.

![Pasted image 20250212191132.png](/img/user/Attachments/Pasted%20image%2020250212191132.png)

