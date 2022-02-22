# private
nothing
cd C:\Program Files\MySQL\MySQL Server 8.0\bin
mysql -u root -p
 mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+


 CREATE DATABASE bank;
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| bank               |
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
=========================================
Creating table loan info


CREATE TABLE loan_info (
loan_id int,
user_id int,
last_payment_date DATE,
payment_installation DOUBLE,
data_payable DATE
);



===========================================
insert into loan_info values(1234,5678,'2017-02-20',509,'2017-03-20');
insert into loan_info values(1243,5687,'2016-02-18',9087,'2016-03-18');
insert into loan_info values(1243,5687,'2017-02-18',8976,'2017-04-01');
insert into loan_info values(4312,8976,'2017-01-18',9087,'2017-02-18');
*********************************************



Creating table credit_card info

CREATE TABLE credit_card_info 
(
cc_number bigint,
use_id int, 
maximum_credit DOUBLE,
outstanding_balance DOUBLE,
duo_date DATE
);

===========
Inserting data into the credit_card_info table


insert into credit_card_info values(1234678753672899,1234,50000,35000,'2017-03-22'); 
insert into credit_card_info values(1234678753672900,1243,500000,500000,'2017-03-12'); 
insert into credit_card_info values(1234678753672902,1324,15000,12000,'2017-03-09'); 
insert into credit_card_info values(1234678753672908,4312,60000,60000,'2017-02-16');


/*********************************
Creating table Share_info

CREATE TABLE Share_info
(
share_id  varchar(10),
company_name varchar(20),
gmt_timestamp bigint,
share_price DOUBLE
);

=====================

insert into share_info values('S102',"MyCorp",1488412702,100);
 insert into share_info values('S102',"MyCorp",1488411802,110); 
insert into share_info values('S102',"MyCorp",1488411902,90);
 insert into share_info values('S102',"MyCorp",1488412502,80); 
insert into share_info values('S102',"MyCorp",1488411502,120);


***********************
mysql> select current_user();
+----------------+
| current_user() |
+----------------+
| root@localhost |
+----------------+
1 row in set (0.00 sec)


******************
CREATING NEW USER:
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
//to access information
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
FLUSH PRIVILEGES;
(other point : https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql)
exit;
mysql -u newuser -p
//finish
****************


