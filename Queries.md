# **NOTE**:

-   ## SQL is not case sensitive

-   ## We can insert NULL multiple times, it is treated as UNIQUE every time

## DDL = Used to modify the structure of the SCHEMA

## DML = Used to modify the pre-existing values in the table

## CREATE {DDL = Data Definition Language}

**syntax :**

```
    CREATE TABLE table_name
    (
    col_name1 data_type(size) constraint_name,
    col_name2 data_type(size) constraint_name,
    col_name3 data_type(size) constraint_name,
    ...
    );
```

## INSERT {DDL = Data Definition Language}

**syntax :**

```
INSERT INTO table_name values (value1, value2, value3,value4,...);
```

## SELECT {DDL = Data Definition Language} { DQL = Data Query Language}

**syntax :**

```
SELECT * FROM table_name;
```

> To view all the column of the table and it's entries

```
SELECT col_name1, col_name2 from table_name;
```

> To view data of a particular row

**syntax :**

```
SELECT * FROM table_name WHERE col_name = 'value' (CLAUSE)
```

> To view some particular column from table

## desc table_name; {DDL = Data Definition Language}

**syntax :**

```
desc table_name;
```

> To view the col_name and its properties

## DELETE {DDL = Data Manipulation Language}

**syntax :**

```
DELETE from table_name WHERE col_name = {value}
```

## DROP {DDL = Data Definition Language}

**syntax :**

```
DROP TABLE table_name;
```

## Foreign Key Constraint

**syntax :**

```
FOREIGN KEY col_name {in Child table} REFERENCES table_name(in Parent Table)
```

## ALTER {DDL = Data Definition Language}

-   ### To add a column

**syntax :**

```
ALTER TABLE table_name ADD col_name data_type(size) constraint_name;
```

-   ## To delete a column

**synatx :**

```
ALTER TABLE table_name DROP COLUMN col_name;
```

-   ## To modify a column

**syntax :**

```
ALTER TABLE table_name MODIFY col_name data_type(size);
```

-   ## To ADD PRIMARY KEY constraint to a column

```
ALTER TABLE table_name ADD PRIMARY KEY(col_name);
```

-   ## To modify the pre-existing CONSTRAINTS

```
ALTER TABLE table_name drop PRIMARY KEY;
```

-   ## To RENAME a column

```
ALTER TABLE table_name RENAME COLUMN old_col_name TO new_col_name;
```

## RENAME {DDL = Data Definition Language}

**syntax :**

```
RENAME table_name TO new_col_name;
```

## TRUNCATE {DML = Data Definition Language}

```
TRUNCATE TABLE table_name;
```

> Difference between TRUNCATE & DROP:
>
> > TRUNCATE delete only the rows, SCHEMA and Structure is preserved;
> > DROP deletes the whole table including the SCHEMA

## UPDATE {DML = Data Definition Language}
