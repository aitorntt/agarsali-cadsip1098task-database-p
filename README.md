# CAD-GEN-LIQUIBASE

CAD-GEN-LIQUIBASE is the generator of data of our model that will be loaded in BBDD

- [Prerequisites](#prerequisites)
- [Steps to create / update the Database](#updateBBDD)

<h2 id="updateBBDD">Prerequisites</h2>

Before executing the update of the database it will be necessary:

	- Mysql version 8.0.11 

	- mvn (Maven) in local

	- Review and update if it's necessary 'liquibase.properties' file with the 'username' and 'password' of the local database (by default these values are 'root' and 'admin').

<h2 id="updateBBDD">Steps to create / update database schema</h2>

	- Unzip the generated code 

	- Check database name, user and password to use (default values: database, root and admin)

	- Execute the following instruction in the console:

> mvn liquibase:update -Dmysql-version=8.0.11 -Dliquibase-properties=src/main/resources/liquibase.properties

	- A log will be displayed during execution, to verify that everything is OK the last message must be 'BUILD SUCCESS'.

