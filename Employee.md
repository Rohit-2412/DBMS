    CREATE TABLE employee_table(
    emp_no number(12) PRIMARY KEY,
    Name varchar(25) NOT NULL,
    department varchar(25) NOT NULL,
    specialization varchar(50) NOT NULL,
    Address varchar(25),
    Salary number(10) NOT NULL,
    dob varchar(15) NOT NULL,
    experience number(5)
    );

    insert into employee_table values(10,'ram','CSE','artificial intelligence','punjab',10000,'1/8/2008',10);
    insert into employee_table values(11,'ramesh','CSE','artificial intelligence','punjab',1800,'1/8/2008',15);
    insert into employee_table values(12,'mohan','mec','isometric design','punjab',14000,'1/8/2008',5);
    insert into employee_table values(13,'pawan','ece','vlsi engineer','punjab',9000,'1/8/1988',2);
    insert into employee_table values(14,'param','phy','laser engineer','punjab',9000,'1/8/1985',1);
    insert into employee_table values(15,'sohaib','che','scientist','punjab',1100,'1/8/1258',20);
    insert into employee_table values(16,'malik','bio','zoologist','web developer',15000,'1/8/1995',13);
    insert into employee_table values(17,'shyam','int','networking','punjab',12000,'1/8/1485',20);

    Select * from employee_table;
    delete from employee_table where emp_no = 10;
