# GROUP BY clause

-   To group/club rows with similar data/value
-   GROUP BY follows WHERE clause
-   GROUP BY preceeds ORDER BY
-   **One column is for grouping & another column is for Aggregate function**
-   Order by follows by group by we can't use order by prior to group by
-   **Syntax :**

```
SELECT col_name1, AGGREGATE FUNCTION(col_name2) from table_name GROUP BY col_name (whose value is repeating multiple times);
```

# HAVING clause

-   To apply condition with GROUP BY clause
-   Works on group of data

```
SELECT col_name1, AGGREGATE FUNCTION(col_name2) from table_name GROUP BY col_name (whose value is repeating multiple times)HAVING AGGREGATE(col_name);
```

**Table**
|FNAME| LNAME| SALARY| EMPID| JOBID| DEPTNAME| LOCATION|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|ram| sharma| 23000| 23| 56| cse| pnb|
|sram| arma| 26000| 25| 56| cse| delhi|
|sham| rma| 15000| 28| 58| civil| haryana|
|naitik| lang| 45000| 29| 59| mech| jalandhar|
|ahem| sharma| 10000| 30| 58| civil| up|

---

```
select deptname , avg(salary) from emp group by deptname having avg(salary) >15000;
```

OUTPUT:
|DEPTNAME| AVG(SALARY)|
|:-:|:-:|
|cse| 24500|
|mech| 45000|

---

```
select jobid , avg(salary) from emp group by jobid having min(salary) >15000;
```

OUTPUT:
|JOBID| AVG(SALARY)|
|:-:|:-:|
|59| 45000|
|56| 24500|

---

```
select jobid, min(salary) from emp group by jobid;
```

OUTPUT:
|JOBID| MIN(SALARY)|
|:-:|:-:|
|59| 45000
|56| 23000|
|58| 10000|

---

```
select jobid, min(salary) from emp group by jobid having min(salary) >10000;
```

OUTPUT:
|JOBID| MIN(SALARY)|
|:-:|:-:|
|59| 45000|
|56| 23000|

---

```
select jobid, min(salary) from emp group by jobid having min(salary) >10000 order by jobid;
```

OUTPUT:
|JOBID| MIN(SALARY)|
|:-:|:-:|
|56| 23000|
|59| 45000|
