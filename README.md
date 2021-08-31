Characteristics of relational database management system (RDBMS):
- data is structured in rows and columns
- follow Codd's 12 Rules (https://www.tutorialspoint.com/dbms/dbms_codds_rules.htm)
- SQL implementation (structured query language) for accessing the database
- manages and deals with all relational databases
- stores data in form of tables, not as a file
- multi-user friendly
- "ACID" (Atomicity, Consistency, Isolation, Durability) implementation -> consistency in data structure
  - Atomicity:
    - Atomicity guarantees that each transaction is treated as a single "unit", which either succeeds completely, or fails completely:
      - if any of the statements constituting a transaction fails to complete, the entire transaction fails and the database is left unchanged.
  - Consistency:
    - Consistency ensures that a transaction can only bring the database from one valid state to another, maintaining database invariants:
      - any data written to the database must be valid according to all defined rules, including constraints, cascades, triggers, and any combination thereof.
  - Isolation:
    - Isolation ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially.
  - Durability:
    - Durability guarantees that once a transaction has been committed, it will remain committed even in the case of a system failure.
- RDBMS can be normalized
  - Database normalization is the process of structuring a database, usually a relational database, in accordance with a series of so-called normal forms in order to reduce data redundancy and improve data integrity. (https://en.wikipedia.org/wiki/Database_normalization)

Which popular SQL-RDBMS exist?
- MS SQL Server
- Oracle Database
- MySQL
- MariaDB
- SQLite

Database management system (DBMS):
- dBase
- MS Access
- LibreOffice Base
- FoxPro

Storage Engine MyISAM and InnoDB:
| InnoDB                                               | MyISAM                   |
|------------------------------------------------------|--------------------------|
| better crash recovery                                | -                        |
| didn't have FULLTEXT search engine until MySQL 5.6                              | has FULLTEXT search engine   |
| transactions, foreign keys, relationship constraints | -                        |
| row-level locking                                    | full table-level locking |
https://www.thegeekstuff.com/2014/02/myisam-innodb-memory/

InnoDB = High Resource Dependant (high Memory requirement)