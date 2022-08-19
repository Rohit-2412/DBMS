# Person Table

## DML Command: CREATE

    CREATE TABLE Person(
    P_id number(5) PRIMARY KEY,
    first_name varchar(20) UNIQUE NOT NULL,
    last_name varchar(20) NOT NULL,
    address varchar(25) NOT NULL,
    age number(2) NOT NULL
    );

## DML Command: Insert

    insert into Person values(10,'ram','sharma','punjab',20);
    insert into Person values(11,'ramesh','sharma','punjab',22);
    insert into Person values(12,'mahesh','singh','ludhiana',21);
    insert into Person values(13,'shyam','malik','orissa',30);
    insert into Person values(14,'amit','verma','bihar',50);
    insert into Person values(15,'amitabh','pandey','punjab',25);
    insert into Person values(16,'sumit','sharma','punjab',50);

## DML Command: Delete

    Delete from Person where P_id = 6;
    Delete from Person where P_id = 11;

## DDL Command: DROP

    DROP TABLE table_name; {syntax}
    DROP TABLE Person;
