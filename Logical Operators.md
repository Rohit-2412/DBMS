# COMPARISON OPERATORS

---

### 1. `> `greater than

### 2. `< `less than

### 3. `>=` greater than or equal

### 4. `<=` less than or equal

### 5. `<>` not equal

### 6. `BETWEEN AND` inclusive range

---

```
SELECT * FROM table_name WHERE col_name BETWEEN range1 AND range2;
```

### 7. `IN` only limited values

```
SELECT * FROM table_name WHERE col_name IN (value1, value2, value3);
```

### 8. `LIKE` for matching character <br>

-   **starting with `char`**

```
SELECT * FROM table_name WHERE col_name LIKE '{char}%';
```

-   **ending with `char`**

```
SELECT * FROM table_name WHERE col_name LIKE '%{char}';
```

-   **containing `char`**

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
