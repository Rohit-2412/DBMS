# Default Constraint

## Mobile_Phone

```
CREATE TABLE Mobile_Phone(
name varchar(20) NOT NULL,
price int NOT NULL,
imei_number varchar(16) PRIMARY KEY,
android_ver number(4,2) DEFAULT 5,
screen_size int DEFAULT 5.5
);
```

## Describing Table

```
desc Mobile_Phone;
```

**Inserting Data**

```
INSERT INTO Mobile_Phone(price,imei_number) values(15000,'1234567890001111');
INSERT INTO Mobile_Phone(name,price,imei_number) values('Samsung A33',10000,'1234567890001122');
INSERT INTO Mobile_Phone values('Samsung F32',17500,'1234567890001133',9,7);
INSERT INTO Mobile_Phone(name,price,imei_number,android_ver) values('Samsung F21',11200,'1234567890001144',10);
INSERT INTO Mobile_Phone(name,price,imei_number,screen_size) values('Samsung M90',11400,'1234567890001155',6.5);
INSERT INTO Mobile_Phone values('Samsung M21',12000,'1234567890001166',10.5,6);
INSERT INTO Mobile_Phone(name,price,imei_number,android_ver) values('Samsung M11',12000,'1234567890001177',10.5);
```

## Dropping Table

```
drop Table Mobile_Phone;
```
