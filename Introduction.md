#MSSQL

==RDBMS :
RELATIONAL 
DATA 
BASE
MANAGEMENT
SYSTEM== 

**ПРЕДОСТАВЯ ИНСТРУМЕНТИ ЗА РАБОТА С БАЗИ ДАННИ**
==*НЯМАМ ДИРЕКТЕН ДОСТЪП ДО ДАННИТЕ*==
**САМО МОГА ДА ОПРАВЛЯВАМ ДАННИТЕ ЧРЕЗ DBMS**

==DATA BASE ENGINE==
SQL -> Structured Query Language
-> **декларативен език**
SQL SERVER => CLIENT - SERVER MODEL
Стандартен език за изпращане на заявки към DB -> SQL
*SQL Работи с релационна DBMS*

Логически разделен на 4 части:
>**Data Definition** -> describe the structure of the data
>**Data Manipulation**-> store and retrieve data
>**Data Control** -> define who can access the data
>**Transaction Control** -> bundle operations and allow rollback

---
CLIENT -> (Query) -> ENGINE -> (Access) -> Database
---
CLIENT <- (Data) <- ENGINE <- (Data) <- Database 
---
---

https://prnt.sc/yTb4yuryaLbi
**SQL SERVER ARCHITECTURE**

Logical Storage
>Instance
>	Database
>		Schema
>			Table

Physical Storage -> това, което виждаме и с което работим
>Data files and Log files
>	Data Pages

==ENTITY==
-Ред в база данни

==Data Types in SQL Server==

NUMERIC:
>**BIT**(1-bit), **TINYINT**(8-bit), **SMALLINT**(2-bites),
>**INT**(4-bites), **BIGINT**(8-bites), 
>**FLOAT**, **REAL**, **DECIMAL** (precision, scale)

TEXTUAL:
>**CHAR**(size) -> fixed size string



