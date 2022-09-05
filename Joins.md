# JOINS

---

-   To join two tables
-   Number of rows should be same
-   Data type should also be same

**Sample Data**

#### Table 1

| ID  |  NAME  |
| :-: | :----: |
|  4  | anusha |
|  1  | ankit  |
|  2  | ankita |
|  3  |  anu   |
|  1  | ankit  |

#### Table 2

| ID  |  ADDRESS  |
| :-: | :-------: |
|  3  | jalandhar |
|  2  |   agra    |
|  1  |   delhi   |
|  1  |   delhi   |

### Types of JOINS

**1. CARTESIAN / CROSS Join**

-   Joins each column of table2 with table1
-   Like Matrix multiplication

**Syntax :**

```
SELECT * FROM table_name1 CROSS JOIN table_name2;
```

**Output :**

| ID  |  NAME  | ID  |  ADDRESS  |
| :-: | :----: | :-: | :-------: |
|  4  | anusha |  3  | jalandhar |
|  1  | ankit  |  3  | jalandhar |
|  2  | ankita |  3  | jalandhar |
|  3  |  anu   |  3  | jalandhar |
|  1  | ankit  |  3  | jalandhar |
|  4  | anusha |  2  |   agra    |
|  1  | ankit  |  2  |   agra    |
|  2  | ankita |  2  |   agra    |
|  3  |  anu   |  2  |   agra    |
|  1  | ankit  |  2  |   agra    |

**2. INNER / EQUI Join**

-   Joins each column of table2 with table1 wherever the required column value matches with the given condition

**Syntax :**

```
SELECT * FROM table_name1 INNER JOIN table_name2 ON table_name1.col_name1 = table_name2.col_name2;
SELECT * FROM table_name1 INNER JOIN table_name2 ON {Condition};
```

**Output :**

| ID  |  NAME  | ID  |  ADDRESS  |
| :-: | :----: | :-: | :-------: |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |
|  2  | ankita |  2  |   agra    |
|  3  |  anu   |  3  | jalandhar |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |

**3. NATURAL JOIN**

-   Joins each column of table2 with table1 wherever any common column_value is found (we didn't pass any condition in this)
-   In this case we don't get the same row two times as we get in case of equi join

**Syntax :**

```
SELECT * FROM table_name1 NATURAL JOIN table_name2;
```

**Output :**

```
Query: select * from class1 natural join class2;
```

| ID  |  NAME  |  ADDRESS  |
| :-: | :----: | :-------: |
|  1  | ankit  |   delhi   |
|  1  | ankit  |   delhi   |
|  2  | ankita |   agra    |
|  3  |  anu   | jalandhar |
|  1  | ankit  |   delhi   |
|  1  | ankit  |   delhi   |

**4. LEFT OUTER JOIN**

-   All the values of first table will be displayed and corresponding matching values in table2 will be displayed if there is no matching value then NULL

**Syntax :**

```
SELECT * FROM table_name1 LEFT JOIN table_name2 ON table_name1.col_name1 = table_name2.col_name2;
SELECT * FROM table_name1 LEFT JOIN table_name2 ON {Condition};
```

**Output :**

```
Query: select * from class1 left join class2 on class1.id = class2.id;
```

| ID  |  NAME  | ID  | ADDRESS   |
| :-: | :----: | :-: | --------- |
|  3  |  anu   |  3  | jalandhar |
|  2  | ankita |  2  | agra      |
|  1  | ankit  |  1  | delhi     |
|  1  | ankit  |  1  | delhi     |
|  1  | ankit  |  1  | delhi     |
|  1  | ankit  |  1  | delhi     |
|  4  | anusha |  -  | -         |

**5. RIGHT OUTER JOIN**

-   All the values of second table will be displayed first and corresponding matching values in table1 will be displayed if there is no matching value then NULL

**Syntax :**

```
SELECT * FROM table_name1 RIGHT JOIN table_name2 ON table_name1.col_name1 = table_name2.col_name2;
SELECT * FROM table_name1 RIGHT JOIN table_name2 ON {Condition};
```

**Output :**

```
Query: select * from class1 right join class2 on class1.id = class2.id;
```

| ID  |  NAME  | ID  |  ADDRESS  |
| :-: | :----: | :-: | :-------: |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |
|  2  | ankita |  2  |   agra    |
|  3  |  anu   |  3  | jalandhar |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |

**6. FULL OUTER JOIN**

    - All the values of both the table will be displayed if there is no matching value then NULL

**Syntax :**

```
SELECT * FROM table_name1 FULL JOIN table_name2 ON table_name1.col_name1 = table_name2.col_name2;
SELECT * FROM table_name1 FULL JOIN table_name2 ON {Condition};
```

**Output :**

```
Query: select * from class1 full join class2 on class1.id = class2.id;
```

| ID  |  NAME  | ID  |  ADDRESS  |
| :-: | :----: | :-: | :-------: |
|  4  | anusha |  -  |     -     |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |
|  2  | ankita |  2  |   agra    |
|  3  |  anu   |  3  | jalandhar |
|  1  | ankit  |  1  |   delhi   |
|  1  | ankit  |  1  |   delhi   |
