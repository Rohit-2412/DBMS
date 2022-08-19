## **Check constraint**

## Query

    CREATE TABLE Course(
    course_id int PRIMARY KEY,
    course_name varchar(30) NOT NULL,
    course_duration number(5) Check (course_duration > 2),
    course_teacher varchar(20) NOT NULL
    );

    insert into Course values(1,'CSE',2,'abc');
    insert into Course values(2,'CSE',5,'xyz');
    insert into Course values(3,'CSE',8,'def');
    insert into Course values(4,'CSE',10,'pqr');

    select * from Course;
    select course_name from Course;
    select course_name,course_duration from Course;
