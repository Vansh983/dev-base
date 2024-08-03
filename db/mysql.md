# MySQL Commands

## Overview
- [MySQL Commands](#mysql-commands)
  - [Overview](#overview)
  - [Introduction](#introduction)
  - [Installing MySQL](#installing-mysql)
  - [Starting MySQL Service](#starting-mysql-service)
  - [Stopping MySQL Service](#stopping-mysql-service)
  - [Restarting MySQL Service](#restarting-mysql-service)
  - [Checking MySQL Status](#checking-mysql-status)
  - [Connecting to MySQL](#connecting-to-mysql)
  - [Creating a Database](#creating-a-database)
  - [Deleting a Database](#deleting-a-database)
  - [Listing Databases](#listing-databases)
  - [Creating a User](#creating-a-user)
  - [Granting Privileges to a User](#granting-privileges-to-a-user)
  - [Revoking Privileges from a User](#revoking-privileges-from-a-user)
  - [Deleting a User](#deleting-a-user)
  - [Backing Up a Database](#backing-up-a-database)
  - [Restoring a Database](#restoring-a-database)
  - [Running SQL Queries](#running-sql-queries)

## Introduction

MySQL is an open-source relational database management system. It is widely used for web databases and supports standard SQL (Structured Query Language).

## Installing MySQL

To install MySQL on macOS using Homebrew:

```sh
brew install mysql
```

## Starting MySQL Service

To start the MySQL service:

```sh
brew services start mysql
```

## Stopping MySQL Service

To stop the MySQL service:

```sh
brew services stop mysql
```

## Restarting MySQL Service

To restart the MySQL service:

```sh
brew services restart mysql
```

## Checking MySQL Status

To check the status of the MySQL service:

```sh
brew services list | grep mysql
```

## Connecting to MySQL

To connect to the MySQL database using the default `root` user:

```sh
mysql -u root -p
```

You will be prompted to enter the root password.

## Creating a Database

To create a new database:

```sql
CREATE DATABASE database_name;
```

Replace `database_name` with the name of the database you want to create.

## Deleting a Database

To delete a database:

```sql
DROP DATABASE database_name;
```

Replace `database_name` with the name of the database you want to delete.

## Listing Databases

To list all databases:

```sql
SHOW DATABASES;
```

## Creating a User

To create a new user:

```sql
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
```

Replace `username` with the name of the user you want to create and `password` with the user's password.

## Granting Privileges to a User

To grant all privileges on a database to a user:

```sql
GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost';
```

Replace `database_name` with the name of the database and `username` with the name of the user.

## Revoking Privileges from a User

To revoke all privileges on a database from a user:

```sql
REVOKE ALL PRIVILEGES ON database_name.* FROM 'username'@'localhost';
```

Replace `database_name` with the name of the database and `username` with the name of the user.

## Deleting a User

To delete a user:

```sql
DROP USER 'username'@'localhost';
```

Replace `username` with the name of the user you want to delete.

## Backing Up a Database

To back up a database:

```sh
mysqldump -u root -p database_name > backup_file.sql
```

Replace `database_name` with the name of the database you want to back up and `backup_file.sql` with the name of the backup file.

## Restoring a Database

To restore a database from a backup file:

```sh
mysql -u root -p database_name < backup_file.sql
```

Replace `database_name` with the name of the database you want to restore and `backup_file.sql` with the name of the backup file.

## Running SQL Queries

To run SQL queries directly from the command line:

```sh
mysql -u root -p -e "SQL query"
```

Replace `SQL query` with the actual SQL query you want to run.