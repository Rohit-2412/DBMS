# VIEW

---

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

Student Table

| ID  |  Name   | Class | Marks | Attendance |  Address  |
| :-: | :-----: | :---: | :---: | :--------: | :-------: |
|  1  | Harshit |   9   |  86   |    52%     | Jalandhar |
|  2  |  Param  |  11   |  85   |    85%     | Mussorrie |
|  3  |  Harsh  |  10   |  88   |    42%     | Ludhiana  |
|  4  | Ramesh  |  10   |  27   |    82%     |  Roorkee  |
|  5  |   Ram   |  11   |  95   |    95%     |  Mysore   |

> If we want to work upon only those values where Attendance is less than 70%

```
CREATE OR REPLACE VIEW v AS SELECT ID, Name, Marks FROM STUDENT WHERE Attendance < '70';
```

Query: SELECT \* FROM v;

Output:

| ID  |  Name   | Marks | Attendance |
| :-: | :-----: | :---: | :--------: |
|  1  | Harshit |  86   |    52%     |
|  3  |  Harsh  |  88   |    42%     |

---
