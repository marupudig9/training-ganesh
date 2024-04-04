## <span style="color:white">SQL:</span>

SQL is called - Structured Query Language

Common Practice to create a table name: ``` Starts with lower case and has upper case after it. eg: sqlTable ```

RDBMS is called - Relational Database Management System.
* Relational DB stores and provides access to data points that are related to one another.

---
### <u>ACID Properties:</u>

|      A      |       C       |      I      |      D       |
|:-----------:|:-------------:|:-----------:|:------------:|
 |  Atomicity  |  Consistency  |  Isolation  |  Durability  |

* These properties ensure the accuracy and integrity of the data in DB.
* Ensures that data does not corrupt as a result of failures.

#### <u>Atomicity</u>
* Atomicity provides reliability because if there is a failure in the middle of a transaction, none of the changes in the transaction will be committed.

#### <u>Consistency</u>

* The DB must remain in a consistent state after any transaction.
* Ensures that the transaction maintains data integrity constraints, leaving the data consistent.
* The data that is saved in the database must always be valid. 

#### <u>Isolation</u>

* Ensuring that the transaction will not be changed by any other concurrent transaction.
* For Eg: If a two users are purchasing two products at the same time and the first user successfully purchased the product. It will make the transaction of the other user be interrupted.

#### <u>Durability</u>

* Durability makes sure that once the transaction is committed, its changes are persisted permanently in the DB.
* Ensures that the information that is saved in the database is immutable until another update or deletion transaction affects it.

---
### <u>Different types of keys:</u>

<b><I><u>Candidate Key:</b></I></u>

* A candidate key is a column or a set of columns in a table that can uniquely identify any database record without referring to any other data.
* Each table can have one or more candidate keys, but one of these candidate keys is selected as the primary key, which is used to uniquely identify each record in the table. The other candidate keys, if any, are known as alternate keys.

<b><I><u>Primary Key:</b></I></u>

* Primary Key is a special type of candidate key in a database table that is used to uniquely identify each row in the table.
* A table can have only one Primary Key on a table
* A Primary Key should choose that those column values are non-changeable or very rare change.
* Primary key cannot have a null value in a column.
* Primary key field contain a Clustered Index.

<b><I><u>Secondary Key:</b></I></u>

* Candidate keys that are not selected are Secondary Keys.
* If Primary key has more than 2 columns. We mark one as Primary and second as Secondary key.
* Secondary key can also work as primary key, but we are not going to use it as a primary key.
* It's also called Alternate Key.

<b><I><u>Unique Key:</b></I></u>

* Same as primary key, but unique key can have Null value in a column.
* It is not selected as a Primary key.
* Unique key field contain a Non-Clustered Index.

<b><I><u>Composite Key:</b></I></u>

* Composite key is a combination of more than one attributes that can be used to uniquely identify each record.
* We can make two columns which shouldn't have duplicate values with Candidate and Primary key.

<b><I><u>Foreign Key:</b></I></u>

* Foreign key is a field in DB table that is primary key in another table.
* Foreign key is used to generate the relation b/w the tables.
* Foreign key can accept a Null and Duplicate value.
---

### <u>Normalization and Different forms of DB Normalization:</u>

Normalization is a process of organizing data in a database. In order to reduce data redundancy and improve data integrity.
<br>
It is a multi step process that puts data into tabular form, removing duplicated data from the relation tables.<br>
Normalization works in accordance with a series of so-called normal forms. <br>
1 NF, 2 NF, 3 NF...

We need Normalization to reduce below issues:
* Data Redundancy means it created duplicate value.
* Waste of Disk Space.
* Creates Maintenance problem.
* Inconsistency Dependency.

---
### <u>SQL Commands:</u>

```
To Create new table:

Note: Cannot create a table without atleast one column

create table sqlTable (

emp_id int primary key,</br>
emp_name varchar(50),</br>
emp_email varchar(100),</br>
emp_salary int,</br>

)
```
```
To Insert values into the table:

insert into sqlTable (emp_id,emp_name,emp_email,emp_salary) values </br>
('100','marupudi','abc@gmail.com','100000')
```
```
To Update value in an existing column:

update sqlTable set emp_id= '101' where emp_name= 'marupudi'
```