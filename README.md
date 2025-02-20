# Database Design

## Question & Answer

**Q1- What Is Data ?** <br />
**A1- Data** is anything. neither it have value or not.
**Example:**
- name of your all classmates
- name of your favorite cartoon character
- your password
- your random thoughts 
- In simple anything can be data.

**Q2- What Is Database ?** <br />
**A2- Database** is something that store data, In computer science it commonly refer as the a server where we save our product (website/app/dashboard) data.

**Q3- What is an Entity ?** <br />
**A3- Entity** is anything we store data about.
**Example:**
- person
- car

**Q4- What is an Attribute ?** <br />
**A4- Attribute** are the things we store.
**Example:**
- name
- email
- color

**Q5- What is a Row ?** <br />
**A5-** A **Row** is the value (group of values) against a entity inside a table.
**Example:**
- person's name
- person's email

**Q6- What is a Column ?** <br />
**A6-** A **Column** is the value (group of values) against a attribute inside a table.
**Example:**
- name of all persons

**Q7- What is a Table ?** <br />
**A7-** A combination of rows and column to save entities.

**Q7- What is a View ?** <br />
**A7- View** is a virtual representation of a table with a selected columns.

**Q8- What is SQL - (Structured Query Language) ?** <br />
**A8- SQL - (Structured Query Language)** is a Language to communicate with SQL database:
- use to define database structure (DDL)
    - to create the table structure
- use to manipulate the data inside the database (DML)
    - to perform crud on the database
    - connection between the database

**Q9- What is Data Integrity ?** <br />
**A9- Data Integrity** is all data is correct, up to date.
- It has 3 types:
    1. Entity Integrity
        - in simple unique entity
            - every entity should have a unique identifier (mostly id/uuid)
    2. Referential Integrity
        - relations/foreign keys are referential integrity
    3. Domain Integrity
        - data type is domain integrity (int(11)/varchar(255))
            - few of data types are:
                - int = integer
                - char = string
                - null = no value
                    - nullable means this column is optional 
- Errors in database called anomaly
    - Anomaly = when database behave in unexpected way

**Q10- What is a good Database Design ?** <br />
**A10-** A **Database Design** is something which have data integrity, and no repeated data, no stale data.
In general database design break into 3 sections (schemas):
1. Conceptual
    - relation falls here
2. logical
    - table structure falls here
3. Physical
    - what database/data types/server/other stuffs falls here
--- 
We can understand them as conceptual schema is general thinking to physical is specific thinking.

**Q11- What is Relationship in a Relational Database ?** <br />
**A11-** In a **Relational Database** we have multiple types of Relationship.
1. One-To-One
    - formally written as `1:1`
    - is one entity have one attribute
        - one username
    - if anything have one-to-one relation we will add a new column in the same table
    - but sometime we save one-to-one relation in different tables
        - one person can have one driving license number
            - person will save in user table
            - driving license number will save in driving license table
    - usually between one or two tables (binary relation)
2. One-To-Many
    - formally written as `1:N`
    - here one entity have many attributes
        - one person can have multiple comments in a blog
        - one person can have multiple orders
    - if anything have one-to-many relation we will add a foreign key in the table
    - one-to-many also know as parent-child relation
        - parent is one entity and have primary key
        - child can be multiple entities and have foreign key
    - child have also refer to parent but not vice versa
    - between two tables (binary relation)
3. Many-To-Many
    - formally written as `M:N`
    - here many entity have many attributes
        - one class can have multiple students
        - but one student can have multiple classes as well
    - if anything have many-to-many relation we will add a bridge/intermediate table.
        - this table will have student_id and class_id as well.
    - usually between three or more tables but every two tables will have one-to-many relationship between primary and bridge table (binary relation)

**Q12- What is Index ?** <br />
**A12- Index** are same as in books, to find something quickly, it will point you to the data.
- **Unique Index**
    - this index will make sure that all values are unique

**Q13- What is Primary Key ?** <br />
**A13- Primary Key** is the unique identifier of the entity use to make all foreign relations.

**Q14- What is Look-Up Table ?** <br />
**A14- Look-Up Table** is a simple table consistence of **List Of Values**. <br />
- Relation
    - Look-Up tables work with One-To-Many relationship
- Example:
    - Status
    - Gender

**Q15- What are Keys ?** <br />
**A15- Keys** are unique, Never Change and Never Null.
- **SuperKey** is any number of columns that forces every row to be unique
    - **Requirement**
        - Can every row be unique
        - How any column are needed
    - **Note:** SuperKey are only for designing the database and not practical
- **Candidate Key** is minimum number of columns that forces every row to be unique

## key Points
- *One Entity - (table) should only contain relevant data*

## fun facts
- *Relational Database come from math relation not the relation between tables*

## Key words
- *tuple = use for row*
- *DBMS = Database Management System*
- *RDBMS = Relational Database Management System*
- *DDL = data definition language*
- *DML = data manipulation language*
- *Normalization = step to follow in database design*
- *key = unique identifier*

## Style Guide
- *save everything in atomic level*
### SQL
- `--` this is a single line comment = use for single line comments
- `/*
    this is a multi-line
    comment
  */` = use for multi line comments
- normally we use uppercase for build-in keywords, eg: `SELECT`, `UPDATE`, `JOIN`
- normally we use lowercase for keyword for things we name: `user`, `role`
- normally we use `kabab case` in naming conventions in sql, eg: `user_role`
