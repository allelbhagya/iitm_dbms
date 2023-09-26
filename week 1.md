# week 1

## why databases?

a DBMS contains information about a particular enterprise

- collection of interrelated data
- set of programs to access the data
- an environment that is both convenient and efficient to use

### drawbacks of using file systems to store data

- data redundancy and inconsistency
- difficulty in accessing data
- data isolation
- integrity problems
- atomicity of updates
- concurrent access by multiple users
- security problems

### Management of data or records is a basic need for human society:

storage, retrieval, transaction, audit, archival

### history of electronic data management

- 1960: data management with punch cards / tapes and magnetic tapes
- 1970s: COBOL and CODASYL approach’

— VisiCalc - birth of spreadsheets

— magnetic disks became prevalent

- 1908s: RDBMS
- 1900s: internet data managemebnt
- 2000s: NoSQL for unstructured data mgmt
- 2010s: data science

### advantages with spreadsheets:

- durability
- scalability
- security
- ease of use
- consistency

### disadvantages

- upper limit on number of rows
- difficult to ensure consistency
- no means to check violation of constraints in face of concurrent processing
- unable to give different permissions to different people in a centralized manner
- system crash could be catastrophic

| Parameter | File Handling via Python | DBMS |
| --- | --- | --- |
| Scalability with respect to amount of data | Very difficult to handle insert, update and querying of records | In-built features to provide high scalability for a large number of records |
| Scalability with respect to changes in structure | Extremely difficult to change the structure of records as in the case of adding or removing attributes | Adding or removing attributes can be done seamlessly using simple SQL queries |
| Time of execution | seconds | milliseconds |
| Persistence | Data processed using temporary data structures have to be manually updated to the file | Data persistence is ensured via automatic, system induced mechanisms |
| Robustness | Ensuring robustness of data has to be done manually | Backup, recovery and restore need minimum manual intervention |
| Security | Difficult to implement in Python (Security at OS level) | User-specific access at database level |
| Programmer’s productivity | Most file access operations involve extensive coding to ensure persistence, robustness and security of data | Standard and simple built-in queries reduce the effort involved in coding thereby increasing a programmer’s throughput |
| Arithmetic operations | Easy to do arithmetic computations | Limited set of arithmetic operations are available |
| Costs | Low costs for hardware, software and human
resources | High costs for hardware, software and human resources |

### Levels of abstraction

- physical level - describes HOW a record is stored
- Logical level - describes data stored in database and the relationships among the data fields
- view level - application program hides the details of data types

## Schema and instance

schema 

1. Logical schema - overall logical structure of the database; analogous to type information of a variable in a program
2. physical schema - overall physical structure of the database
    
    Instance 
    
    - actual content of the database at a particular point of time; value of a variable in a program at any given point of time

### Physical data independence

ability to modify the physical schema without changing the logical schema 

- analogous to the independence of interface and implementation in object oriented systems
- apps depend on the logical schema

## data model

- relational model
- ER data model
- old models; network, hierarchical model

### relational model

- all the data is stored in tables

## DDL - data definition language

- sql commands which can be used to define the database schema
- create and modify the structure of database objects in the database
- CREATE, DROP, ALTER, TRUNCATE, COMMENT, RENAME

## DML - data manipulation language

- manipulation of data present in the database
- INSERT, UPDATE, DELETE, LOCK

## Object-Relational Data Models

- extend the relational data model by including object orientation and constructs to deal with added data types
- allow attributes of tupes/rows to have complex types
- preserve relational power
- provide compatibility with existing relational languages

## XML - eXtensible Markup language

- defined by w3c; originally intended as a document markup language not a database lang
- ability to specify new tags, create nested tag structures
- became the basis for all new generation data interchange formats

# Database Engine

- storage manager
- query processing
- transaction manager

### storage manager

- program is a module that provides the interface between the low-level data stored in the database and the application programs and queries submitted to the program
- responsible for; interaction with the os file manager, efficient storing, retrieving and updating data
- issues; storage access, file organization, indexing and hashing

### Query processing

- parsing and translation
- optimization
- evaluation
- evaluation for query- equivalent expressions; different algos for each operation
- need to estimate cost of operations; critically on statistics for intermediate results to compute

### Transaction management

- collection of operations that performs a single logical function in a database functions
- TM component ensures that the db remains in a consistent state despite system and transaction failsures
- concurrency - control manager; controls the interaction among the concurrent transactions to ensure the consistency of the db
