## **DESC {DDL = Data Definition Language}**

> To view the col_name and its properties known as SCHEMA

**Syntax :**

```
desc table_name;
```

## **DELETE {DML = Data Manipulation Language}**

> To delete a row from the table

**Syntax :**

```
DELETE from table_name WHERE col_name = {value}
```

## **DROP {DDL = Data Definition Language}**

> To drop the table / delete everything

**Syntax :**

```
DROP TABLE table_name;
```

## **Foreign Key Constraint**

> To set foreign key constraint

**Syntax :**

```
FOREIGN KEY col_name {in Child table} REFERENCES table_name(in Parent Table)
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

> To update the existing row's values

**Syntax :**

```
UPDATE table_name SET col_name = 'new_value' WHERE col_name = 'value';
UPDATE table_name SET col_name = 'new_value'; (All the rows will be updated)
```

## SUBQUERY

**Syntax:**

```
QUERY1 RELATIONAL_OPERATOR (QUERY2)
```

Example:

```
select deptname, avg(salary) from emp group by deptname having avg(salary) = (select min(avg(salary)) from emp group by deptname);
select deptname, min(avg(salary)) from emp group by deptname;
```
