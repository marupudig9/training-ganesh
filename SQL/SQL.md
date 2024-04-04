SQL- Structured Query Language

RDBMS- Relational Database management System.

#### <u>Different types of keys:</u>

| Candidate Key        | Primary Key | Secondary Key | Unique Key | Foreign Key | Composite Key |
|----------------------|-------------|---------------|------------|-------------|---------------|
| We need to Identify  |             |               |            |             |               | 

```
SQL Create new table command:

Note: Cannot create a table without atleast one column

create table sqlTable (

emp_id int primary key,</br>
emp_name varchar(50),</br>
emp_email varchar(100),</br>
emp_salary int,</br>

)
```
#### <u>SQL Insert values into the table command:</u>

insert into sqlTable (emp_id,emp_name,emp_email,emp_salary) values </br>
('100','marupudi','abc@gmail.com','100000')

#### <u>Update column value:</u>

update sqlTable set emp_id= '101' where emp_name= 'marupudi'