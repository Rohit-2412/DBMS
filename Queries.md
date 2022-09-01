# **NOTE**:

> -   ## **_SQL is not case sensitive_**

> -   ## **_We can insert NULL multiple times, it is treated as UNIQUE every time_**

## **DDL = Used to modify the structure of the SCHEMA**

## **DML = Used to modify the pre-existing values in the table**

## **CREATE {DDL = Data Definition Language}**

**Syntax :**

```
    CREATE TABLE table_name
    (
    col_name1 data_type(size) constraint_name,
    col_name2 data_type(size) constraint_name,
    col_name3 data_type(size) constraint_name,
    ...
    );
```

## **INSERT {DDL = Data Definition Language}**

> to insert data into table

**Syntax :**

```
INSERT INTO table_name values (value1, value2, value3,value4,...);
```

## **SELECT {DDL = Data Definition Language} { DQL = Data Query Language}**

**Syntax :**

> To view all the column of the table and it's entries

```
SELECT * FROM table_name;
```

> To view data of a particular row

```
SELECT col_name1, col_name2 from table_name;
```

**Syntax :**

> To view some particular column from table

```
SELECT * FROM table_name WHERE col_name = 'value' (CLAUSE)
```

## **DESC {DDL = Data Definition Language}**

> To view the col_name and its properties known as SCHEMA
>
> **Syntax :**

```
desc table_name;
```

## **DELETE {DML = Data Manipulation Language}**

> To delete a row from the table
>
> **Syntax :**

```
DELETE from table_name WHERE col_name = {value}
```

## **DROP {DDL = Data Definition Language}**

> To drop the table / delete everything
> **Syntax :**

```
DROP TABLE table_name;
```

## **Foreign Key Constraint**

> To set foreign key constraint

**Syntax :**

```
FOREIGN KEY col_name {in Child table} REFERENCES table_name(in Parent Table)
```

## **ALTER {DDL = Data Definition Language}**

> To modify the definition of table

-   ### To Add a column

**Syntax :**

```
ALTER TABLE table_name ADD col_name data_type(size) constraint_name;
```

-   ## To Delete a column

**Syntax :**

```
ALTER TABLE table_name DROP COLUMN col_name;
```

-   ## To Modify a column

**Syntax :**

```
ALTER TABLE table_name MODIFY col_name data_type(size);
```

-   ## To ADD PRIMARY KEY constraint to a column

```
ALTER TABLE table_name ADD PRIMARY KEY(col_name);
```

-   ## To modify the pre-existing CONSTRAINTS

```
ALTER TABLE table_name DROP PRIMARY KEY;
```

-   ## To RENAME a column

```
ALTER TABLE table_name RENAME COLUMN old_col_name TO new_col_name;
```

## RENAME {DDL = Data Definition Language}

> To rename the table

**Syntax :**

```
RENAME table_name TO new_col_name;
```

## TRUNCATE {DDL = Data Definition Language}

> To delete all the data from the table

```
TRUNCATE TABLE table_name;
```

### Difference between TRUNCATE & DROP:

> `TRUNCATE delete only the rows, SCHEMA and Structure is preserved;`

<br>

> `DROP deletes the whole table including the SCHEMA`

## UPDATE {DML = Data Definition Language}

> To update the existing rows

## To perfrom Arithmetic Operations on Table

```
SELECT [f(col_name, arithmetic_operation)] from table_name;
```

## CONCATENATION (to display value as a string in output)

` || -> Concatenation Operator`

```
SELECT col_name || 'string' || col_name from table_name WHERE condition1 OR condition2;
```

```
SELECT col_name || col_name from table_name WHERE condition1 AND condition2;
```

## DISTINCT (to get only UNIQUE values)

```
SELECT DISTINCT col_name from table_name;
```

## AS CLAUSE ()

```
SELECT col_name AS "{string1 string2}" FROM table_name;
```

```
SELECT col_name AS {string} FROM table_name; // if SINGLE WORD is there "" can be ommitted
```

## UPDATE {DDL = Data Definition Language}

**Syntax :**

```
UPDATE table_name SET col_name = 'new_value' WHERE col_name = 'value';
UPDATE table_name SET col_name = 'new_value'; (All the rows will be updated)
```

## COMPARISON OPERATORS

1.  `> `greater than
2.  `< `less than
3.  `>=` greater than or equal
4.  `<=` less than or equal
5.  `<>` not equal
6.  `BETWEEN AND` inclusive range

```
SELECT * FROM table_name WHERE col_name BETWEEN range1 AND range2;
```

7.  `IN` only limited values

```
SELECT * FROM table_name WHERE col_name IN (value1, value2, value3);
```

8.  `LIKE` for matching character <br>

    -   **starting with `char`**

    ```
    SELECT * FROM table_name WHERE col_name LIKE '{char}%';
    ```

    -   **ending with `char`**

    ```
    SELECT * FROM table_name WHERE col_name LIKE '%{char}';
    ```

    -   **conaining `char`**

    ```
    SELECT * FROM table_name WHERE col_name LIKE '%{char}%';
    ```

    -   **`character` at position from start**

    ```
    SELECT * FROM table_name WHERE col_name LIKE '_{char}%';
    ```

    -   **`character` at position from end**

    ```
    SELECT * FROM table_name WHERE col_name LIKE '%{char}_';
    ```

9.  `AND` both the condition should be true

```
SELECT * FROM table_name WHERE col_name1 = 'value' AND col_name2 = 'value';
```

10. `OR` either of the condition should be true

```
SELECT * FROM table_name WHERE col_name1 = 'value' OR col_name2 = 'value';
```

11. `NOT` negation

```
SELECT * FROM table_name WHERE col_name NOT IN (value1, value2, value3 ...);
```

12. `IS NULL` check if value is null

```
SELECT * FROM table_name WHERE col_name IS NULL;
```

## ORDER BY clause (default = ascending)

`Ascending`

```
SELECT * FROM table_name ORDER BY col_name ASC;
```

`Descending`

```
SELECT * FROM table_name ORDER BY col_name DESC;
```

## Aggregate Function

-   SUM
-   MIN
-   MAX
-   COUNT
-   AVG

### MIN

> To calculate the minimum value out of all data

```
SELECT MIN(col_name) from table_name;
```

### MAX

> To calculate the maximum value out of all data

```
SELECT MAX(col_name) from table_name;
```

### AVG

> To calculate the average value of all data

```
SELECT AVG(col_name) from table_name;
```

### SUM

> To calculate the sum out of all the data

```
SELECT SUM(col_name) from table_name;
```

### COUNT

> To calculate the count of all the rows

```
SELECT COUNT(col_name) from table_name;
```

> To calculate the unique count from all of the rows

```
SELECT COUNT(DISTINCT col_name) from table_name;
```

## SET Operations

-   UNION
-   UNION ALL
-   INTERSECTION
-   MINUS

## UNION

> Will combine both the tables and duplicates will be eliminated

**Syntax :**

```
SELECT * FROM table1 UNION SELECT * FROM table2;
```

## UNION ALL

> Will combine both the tables and duplicates will not be eliminated

**Syntax :**

```
SELECT * FROM table1 UNION ALL SELECT * FROM table2;
```

## INTERSECT

> Will find the common data between both the tables

**Syntax :**

```
SELECT * FROM table1 INTERSECT SELECT * FROM table2;
```

## MINUS

> Will exclude the common data between both the tables

**Syntax :**

```
SELECT * FROM table1 MINUS SELECT * FROM table2;
```

## VIEW

> To create a view from a large database / table -> like a sub table

**Syntax :**

```
CREATE OR REPLACE VIEW view_name AS SELECT col_name1,col_name2,col_name3 FROM Employee WHERE col_name = 'value';
```

> For Updation in View

```
UPDATE view_name SET col_name = 'value' WHERE col_name = 'value';
```

> For dropping view

```
DROP VIEW view_name;
```
