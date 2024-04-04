SQL is called - Structured Query Language

RDBMS is called - Relational Database Management System.

Common Practice to create a table name: ``` Starts with lower case and has upper case after it. eg: sqlTable ```

#### <u>Different types of keys:</u>

| Candidate Key                                                                                                                                                                                                                                                                                                                                                                                        | Primary Key                                               | Secondary Key | Unique Key                                                             | Foreign Key | Composite Key |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------|------------------------------------------------------------------------|-------------|---------------|
| * A candidate key is a column or a set of columns in a table that can uniquely identify any database record without referring to any other data. <br/> * Each table can have one or more candidate keys, but one of these candidate keys is selected as the primary key, which is used to uniquely identify each record in the table. The other candidate keys, if any, are known as alternate keys. | * Primary key cannot have a null value in a column.<br/>  |               | * Same as primary key, but unique key can have Null value in a column. |             |               | 

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