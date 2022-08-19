# SQL is not case sensitive

## CREATE {DDL = Data Definition Language}

**syntax :**

    CREATE TABLE table_name
    (
    col_name1 data_type(size) constraint_name,
    col_name2 data_type(size) constraint_name,
    col_name3 data_type(size) constraint_name,
    ...
    );

## INSERT {DDL = Data Definition Language}

**syntax :**

    INSERT INTO table_name values (value1, value2, value3,value4,...);

## SELECT {DDL = Data Definition Language}

**syntax :**

    SELECT * FROM table_name;
        > To view all the column of the table and it's entries

    SELECT col_name1, col_name2 from table_name;
        > To view some particular column from table

## desc table_name;

**syntax :**

    desc table_name;
        > To view the col_name and its properties

## DELETE {DDL = Data Manipulation Language}

**syntax :**

    DELETE from table_name WHERE col_name = {value}

## DROP {DDL = Data Definition Language}

**syntax :**

    DROP TABLE table_name;

## Foreign Key Constraint

**syntax :**

    FOREIGN KEY col_name {in Child table} REFERENCES table_name(in Parent Table)
