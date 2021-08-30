Characteristics of relational database management system (RDBMS):
- data is structured in rows and columns
- follow Codd's 12 Rules (https://www.tutorialspoint.com/dbms/dbms_codds_rules.htm)
- SQL implementation (structured query language) for accessing the database
- manages and deals with all relational databases
- stores data in form of tables, not as a file
- multi-user friendly
- "ACID" (Atomicity, Consistency, Isolation, Durability) implementation -> consistency in data structure
- RDBMS can be normalized

Which popular SQL-RDBMS exist?
- SQL Server
- Oracle
- MySQL
- MariaDB
- SQLite

Database management system (DBMS):
- dBase
- MS Acces
- LibreOffice Base
- FoxPro

Storage Engine MyISAM and InnoDB:
| InnoDB                                               | MyISAM                   |
|------------------------------------------------------|--------------------------|
| RDBMS                                                | DBMS                     |
| better crash recovery                                | -                        |
| did not until MySQL 5.6                              | FULLTEXT search engine   |
| transactions, foreign keys, relationship constraints | -                        |
| row-level locking                                    | full table-level locking |