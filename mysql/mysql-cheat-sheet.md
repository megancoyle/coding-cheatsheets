# MySQL: Overview
MySQL is an open-source, free database.

## CRUD
* Stands for Create, Read, Update, Delete
* Read: use `SELECT`:
```mysql
  SELECT *
  FROM table
  WHERE column1 = 'text'
  ORDER BY column1 ASC;
```
* Create: use `INSERT`:
```mysql
  INSERT INTO table (column1, column2, column3)
  VALUES (val1, val2, val3);
```
* Update: use `UPDATE`:
```mysql
  UPDATE table
  SET column1 = 'text',
  SET column2 = 'other_text'
  WHERE id = 2;
```
* Delete: use `DELETE`:
```mysql
  DELETE FROM table
  WHERE id = 1;
```

## Databases
* Create database: `CREATE DATABASE db_name;`
* Use database to switch into it so you can start using it: `USE db_name;`
* Remove database: `DROP DATABASE db_name;`

## Logging in
* In the terminal, use `mysql -u root -p` to login in root user, then get prompted to enter your password

## Logging out
* Use `exit` to log out of MySQL

## Tables
* Show all available tables: `SHOW TABLES;`
* Create table:
```mysql
  CREATE TABLE table_name (
    column_name1 definition,
    column_name2 defintion,
    );
```
* Show what tables look like: `SHOW COLUMNS FROM table_name;`
* Remove table: `DROP TABLE table_name;`
