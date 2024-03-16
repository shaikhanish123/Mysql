# Mysql Query
*((1)create database
create database database name;
use database database name;

(2)create primary key with auto_increment;
>>create table Employee(id int primary key not null auto_increment,First_Name varchar(30),Last_Name varchar(30),Address varchar(30),Salary varchar(30),Department varchar(30));

(3)Add Column in table;
 >>alter table table name add column column name(30);

(4)add value in particular column;
>> update table name set columnn name  where id=1;

(5)change column name;
  >>alter table table name rename column old column name to new column name;
(6) add auto increment in existing table
 >> alter table name modify column column name auto_increment;
 (7)change column data types;
 alter table employee modify column salary int;
(8)max salary
>>select max(column name) from employee;
(8)min salary
>>select min(column name) from employee;
(9)find average salary;
>>select avg(column name) As averagesalary from employee;
(10)find distinct
>>select distinct address from employee;
find count
>>select count(last_name) from employee;
(11)find second highest salary in a table
>>SELECT MAX(SALARY) FROM employee WHERE SALARY < (SELECT MAX(SALARY) FROM employee);
(12) how to set default value in table 
>>alter table table name alter column name set default default name;
(13) find distinct value from a table
>>select  distinct State from employee where ID%2=0;
(14)Find the difference between the total number of CITY entries in the table and
 the number of distinct CITY entries in the table.
 >>SELECT COUNT(CITY)-COUNT(DISTINCT CITY)FROM STATION;
 (15) select multiple character that start with same name;
 >> select First_Name from employee where First_Name like 'a%,'e%','i%';
 (16)SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1))
 NOT IN ('a','e','i','o','u') 
 OR LOWER(SUBSTR(CITY, LENGTH(CITY),1)) NOT IN ('a','e','i','o','u'); 
(17)funtion 
(1)  find ASCII value of specific column 
>>select ASCII(column name )as column name from table name;
(2)find string length
>>select var_char(column name) as stringlength;
()find max salary when we don't know about employee;
>>select salary from company limit 1 offset 4;
(18)find second highest salary from a table;
>>select salary from company order by salary desc limit 1 offset 2;
(19)find even id no
>>select * from company where Id%2=0;
(20)find odd id no;
select * from company where Id%2!=0;
(21)insert multiple row in a single column
>>UPDATE company
SET Incoming = CASE id WHEN 1 THEN "10:30" WHEN 2 THEN "8:30" ELSE Incoming END WHERE id IN (1, 2);
(21) add column after column in table 
>>mysql> alter table company add column Holidays  varchar(30) after Outgoing;
(22)add primary key  with auto_increment in existing table ;
>>alter table table name  add primary key auto_increment(id);
>>types of Join 
(1) cross join
>>select * from table 1 name cross joint table name 2;
