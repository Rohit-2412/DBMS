# FOREIGN KEY Constraint

## Person Table

    CREATE TABLE Person(
    P_id number(5) PRIMARY KEY,
    name varchar(20) UNIQUE NOT NULL,
    address varchar(25) NOT NULL,
    age number(2) NOT NULL
    );

    insert into Person values(1,'ram','punjab',20);
    insert into Person values(2,'ramesh','punjab',22);
    insert into Person values(3,'mahesh','ludhiana',21);

    select * from Person;

## Order table

    CREATE TABLE Order1(
    O_id int PRIMARY KEY,
    O_no int NOT NULL,
    P_id int,
    FOREIGN KEY (P_id) REFERENCES Person(P_id)
    );

> FOREIGN KEY col_name {in Child table} REFERENCES table_name(in Parent Table) [syntax]

    FOREIGN KEY (P_id) REFERENCES Person(P_id)

## Query

    insert into Order1 values(100,10,1);
    insert into Order1 values(101,11,2);
    insert into Order1 values(102,12,2);
    insert into Order1 values(103,13,3);

    insert into Order1 values(104,14,3),
    (105,15,3),
    (106,16,3);

    select * from Order1;

### - Base table = Parent table

### - Reference table = child table

-   ## _Deletion_ is not allowed in Base table

-   ## _Insertion_ of values which are not present in Base table is not allowed
