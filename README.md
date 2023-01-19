# postgresql
postgresql basics
Output:

CREATE TABLE
INSERT 0 1
INSERT 0 1
INSERT 0 1
 user_id | first_name | second_name | date_of_joining | salary
---------+------------+-------------+-----------------+--------
       1 | vinay      | sridhar     | 2023-01-18      |   2000
       4 | SATYA      | ADARI       | 2023-01-18      |  12300
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300
(3 rows)

ALTER TABLE
 user_id | first_name | second_name | date_of_joining | salary | ctc | email_id
---------+------------+-------------+-----------------+--------+-----+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |     |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |     |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |     |
(3 rows)

ALTER TABLE
 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
(3 rows)

DELETE 0
 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
(3 rows)

 salary
--------
  17300
  12300
   2000
(3 rows)

 salary
--------
   2000
  12300
  17300
(3 rows)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
(3 rows)

 for_name | sur_name
----------+----------
 vinay    | sridhar
 SATYA    | ADARI
 SATYAA   | ADARI
(3 rows)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
(3 rows)

 user_id
---------
       5
       4
       1
(3 rows)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
(0 rows)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
(1 row)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
(1 row)

 user_id | first_name | second_name | date_of_joining | salary | email_id
---------+------------+-------------+-----------------+--------+----------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
(3 rows)

 count
-------
     3
(1 row)

INSERT 0 1
 user_id | first_name | second_name | date_of_joining | salary |         email_id        
---------+------------+-------------+-----------------+--------+--------------------------
       1 | vinay      | sridhar     | 2023-01-18      |   2000 |
       4 | SATYA      | ADARI       | 2023-01-18      |  12300 |
       5 | SATYAA     | ADARI       | 2023-01-19      |  17300 |
       2 |            | HELLO       | 2023-03-23      |  25000 | VINAYSRIDHAR98@GMAIL.COM
(4 rows)

 first_name
------------
 SATYA
 SATYAA
 
 vinay
(4 rows)

 count
-------
     1
(1 row)

        avg        
--------------------
 14150.000000000000
(1 row)














CREATE TABLE EMPLOYEE (
USER_ID int PRIMARY KEY,
FIRST_NAME varchar(50) NOT NULL,
SECOND_NAME varchar(50),
Date_of_joining date NOT NULL,
SALARY int
);
INSERT INTO EMPLOYEE
VALUES(001,'vinay','sridhar','01/18/2023',2000);
INSERT INTO EMPLOYEE
VALUES(004,'SATYA','ADARI','01/18/2023',12300);
INSERT INTO EMPLOYEE
VALUES(005,'SATYAA','ADARI','01/19/2023',17300);
SELECT * FROM EMPLOYEE;
ALTER TABLE EMPLOYEE
ADD COLUMN CTC FLOAT,
ADD COLUMN EMAIL_ID varchar;
SELECT * FROM EMPLOYEE;
ALTER TABLE EMPLOYEE DROP CTC;
SELECT * FROM EMPLOYEE;

DELETE FROM EMPLOYEE
WHERE USER_ID = 0;
SELECT * FROM EMPLOYEE;
SELECT SALARY
FROM EMPLOYEE
ORDER BY SALARY DESC;

SELECT SALARY
FROM EMPLOYEE
ORDER BY SALARY ASC;

SELECT * FROM EMPLOYEE;
SELECT FIRST_NAME AS FOR_NAME,SECOND_NAME AS SUR_NAME FROM EMPLOYEE;
SELECT * FROM EMPLOYEE;
SELECT DISTINCT USER_ID FROM EMPLOYEE;
SELECT * FROM EMPLOYEE
WHERE second_name = 'ADAR';

SELECT * FROM EMPLOYEE
WHERE Date_of_joining = '2023-01-18' AND first_name = 'vinay';

SELECT * FROM EMPLOYEE
WHERE Date_of_joining = '2023-01-10' OR SALARY = '12300';

SELECT * FROM EMPLOYEE;
SELECT COUNT (FIRST_NAME) FROM EMPLOYEE;

INSERT INTO EMPLOYEE
VALUES(002,'','HELLO','2023-03-23',25000,'VINAYSRIDHAR98@GMAIL.COM');
SELECT * FROM EMPLOYEE;
SELECT DISTINCT FIRST_NAME FROM EMPLOYEE;

SELECT COUNT (EMAIL_ID) FROM EMPLOYEE;


SELECT AVG(SALARY) FROM EMPLOYEE;


