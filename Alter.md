# ALTER

### DDL = Data Definition Language

-   To modify the definition of table

---

-   ### To Add a column

**Syntax :**

```
ALTER TABLE table_name ADD col_name data_type(size) constraint_name;
```

-   ### To Delete a column

**Syntax :**

```
ALTER TABLE table_name DROP COLUMN col_name;
```

-   ### To Modify a column

**Syntax :**

```
ALTER TABLE table_name MODIFY col_name data_type(size);
```

-   ### To ADD PRIMARY KEY constraint to a column

```
ALTER TABLE table_name ADD PRIMARY KEY(col_name);
```

-   ### To modify the pre-existing CONSTRAINTS

```
ALTER TABLE table_name DROP PRIMARY KEY;
```

-   ### To RENAME a column

```
ALTER TABLE table_name RENAME COLUMN old_col_name TO new_col_name;
```

---

# RENAME {DDL = Data Definition Language}

> To rename the table

**Syntax :**

```
RENAME table_name TO new_col_name;
```
