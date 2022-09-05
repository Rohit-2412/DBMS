## SET Operations

-   UNION
-   UNION ALL
-   INTERSECTION
-   MINUS

## UNION

> It will combine both the tables and duplicates will be eliminated

**Syntax :**

```
SELECT * FROM table1 UNION SELECT * FROM table2;
```

## UNION ALL

> It will combine both the tables and duplicates will not be eliminated

**Syntax :**

```
SELECT * FROM table1 UNION ALL SELECT * FROM table2;
```

## INTERSECT

> It will find the common data between both the tables

**Syntax :**

```
SELECT * FROM table1 INTERSECT SELECT * FROM table2;
```

## MINUS

> It will exclude the common data between both the tables

**Syntax :**

```
SELECT * FROM table1 MINUS SELECT * FROM table2;
```
