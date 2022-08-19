# Student Table

## Command to create table

    CREATE TABLE student_table(
    Regno number(12),
    name varchar(20),
    section varchar(10),
    address varchar(25),
    cgpa number(4,2),
    rollnumber number(4)
    );

## Command to see the table information

    desc student_table;

## Command to insert values

    insert into student_table values(100,'rohit','IT','delhi',8,4);
    insert into student_table values(101,'student 2','IT','uttar pradesh',8,4);

## Query to show all data

    SELECT * from student_table;
