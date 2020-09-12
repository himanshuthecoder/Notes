# View Databases

	show databases;

# View Tables
	
	show tables;

# View Column of tables
	
	describe tablename; 

# Creating Databases

```
	create database databasename;
```
# Dropping databases

``` 
	DROP DATABASE databasename;
```

# Dropping tables

```
	DROP TABLE table_name; 
```

# Format whole table ( truncate table)

```
	TRUNCATE TABLE table_name; 
```

# Creating Tables

```
	create table tablename(
	columnname datatype contraints,
	columnname datatype contraints
	);
```

# Alter Tables

### Adding column

```
	alter table tablename add coulmname datatype contraints;
eg:-	alter table user add location varchar(255) not null;

```
### Deleting column

```
	ALTER TABLE table_name DROP COLUMN column_name;
eg:- 	ALTER TABLE Customers DROP COLUMN Email;

```
### Modify column

```
	For sql server/ms access
		ALTER TABLE table_name
		ALTER COLUMN column_name datatype; 
	
	For mysql/oracle
		ALTER TABLE table_name
		MODIFY COLUMN column_name datatype; 

	
```
	
# Contraints
SQL constraints are used to specify rules for the data in a table.
Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table. If there is any violation between the constraint and the data action, the action is aborted.
Constraints can be column level or table level. Column level constraints apply to a column, and table level constraints apply to the whole table.	
		
The following constraints are commonly used in SQL:

- NOT NULL - Ensures that a column cannot have a NULL value

```
During creation:- 
	CREATE TABLE Tablename (columnname datatype NOT NULL);

Durig Modification:-
	ALTER TABLE TableName 
	MODIFY CoulmnName datatype NOT NULL; 

```
- **UNIQUE** - Ensures that all values in a column are different

```
CREATE TABLE Tabelname (
    ColumnName datatype NOT NULL,
    UNIQUE (ColumnName)
); 

or

CREATE TABLE TableName (
    ColumnName datatype NOT NULL UNIQUE,
    );

 or
 
 ALTER TABLE TableName
 ADD UNIQUE (ColumnName);    

```

- **PRIMARY KEY** - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table

```
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
); 

or

CREATE TABLE TableName (
    ColumnName datatype NOT NULL PRIMARY KEY
    );

or

ALTER TABLE TableName
ADD PRIMARY KEY (columnname);

```

- **FOREIGN KEY** - Uniquely identifies a row/record in another table

```

CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
); 


or


ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);



```

- **CHECK** - Ensures that all values in a column satisfies a specific condition
- **DEFAULT** - Sets a default value for a column when no value is specified
- **INDEX** - Used to create and retrieve data from the database very quickly
- **AutoIncrement** -Auto-increment allows a unique number to be generated automatically when a new record is inserted into a table.

```
CREATE TABLE Persons (
    Personid int NOT NULL AUTO_INCREMENT,
   );

or

Alter table TableName
change Personid Personid int not null auto_increment;

//To give starting value to autoincrement

ALTER TABLE Persons AUTO_INCREMENT=100; 

```	


### Dropping Contraints

- Dropping Primary key
	
```
	ALTER TABLE TAbleName
	DROP PRIMARY KEY; 

```
- Dropping Unique Contraints

```
ALTER TABLE TableName
DROP INDEX UC_TableName;

```
- Dropping Foreign key Contraints

```
ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder; 

```
	





# Inserting data in table

```
		insert into tablename (column1,column2,column3...) values (value1),(value2)...(valueN);

eg:- 	insert into user (name,location,company,department) values('suraj','gurgaon','google','security'), ('arvind','delhi','apple','ui');

```
