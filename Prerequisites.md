# Software Prerequisite:

1. MySQL
2. IDE(e.g., IntelliJ IDEA, Visual Studio Code)

## Databases Setup:

Step 1: Create Database name `BankApp`
```bash
-- Create a new database called 'BankApp'
CREATE DATABASE BankApp;

-- Switch to the newly created database
USE BankApp;
```

Step 2: Create Table name `customer`


```bash
--Create table
CREATE TABLE `customer` (

 ac_no int NOT NULL AUTO_INCREMENT,

 cname varchar(45) DEFAULT NULL,

 balance varchar(45) DEFAULT NULL,

 pass_code int DEFAULT NULL,

 PRIMARY KEY (ac_no),

 UNIQUE KEY cname_UNIQUE (cname)

) ;
```
## VS Code Project Setup:

Create New Project

Create A package name `BankManagement` & `BankManagement/Connection`


## File configuration

Create a `Connection` class in the `BankManagement/Connection` package

Create a `bankManagement` class in the `BankManagement` package
## JDBC configuration
### Step 1: Include JDBC Driver for MySQL
```bash
// register jdbc Driver 

String mysqlJDBCDriver = "com.mysql.cj.jdbc.Driver";

Class.forName(mysqlJDBCDriver);
```
### Step 2: Create Connection Class using MySQL username and password
```bash
// Create Connection

String url = "jdbc:mysql://localhost:3306/databaseName";

String user = "root";

String pass = "123";

con = DriverManager.getConnection(url, user, pass);
```
