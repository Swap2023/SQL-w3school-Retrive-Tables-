# SQL-w3school-Retrive-Tables-
-- orders,salesman,nobel_win,item_mast
-- Using this command we can create database.
create database w3school;
/*
order_no (Order Number): Integer type, Primary Key.
purch_amt (Purchase Amount): Decimal type with precision 10 and scale 2.
ord_date (Order Date): Date type.
customer_id (Customer ID): Integer type.
salesman_id (Salesman ID): Integer type */

create table orders (
order_no int primary key,
purch_amt decimal(10,2),
order_date date,
customer_id int,
salesman_id int
);
-- Check created table
select * from orders;

INSERT INTO orders (order_no, purch_amt, order_date, customer_id, salesman_id) 
VALUES 
(70001, 150.5, '2012-10-05', 3005, 5002),
(70009, 270.65, '2012-09-10', 3001, 5005),
(70002, 65.26, '2012-10-05', 3002, 5001),
(70004, 110.5, '2012-08-17', 3009, 5003),
(70007, 948.5, '2012-09-10', 3005, 5002),
(70005, 2400.6, '2012-07-27', 3007, 5001),
(70008, 5760, '2012-09-10', 3002, 5001),
(70010, 1983.43, '2012-10-10', 3004, 5006),
(70003, 2480.4, '2012-10-10', 3009, 5003),
(70012, 250.45, '2012-06-27', 3008, 5002),
(70011, 75.29, '2012-08-17', 3003, 5007),
(70013, 3045.6, '2012-04-25', 3002, 5001);

select * from orders;

create table salesman(
    salesman_id INT PRIMARY KEY,
    name VARCHAR(50),
    city VARCHAR(50),
    commission DECIMAL(5,2)
);
INSERT INTO salesman (salesman_id, name, city, commission)
VALUES
(5001, 'James Hoog', 'New York', 0.15),
(5002, 'Nail Knite', 'Paris', 0.13),
(5005, 'Pit Alex', 'London', 0.11),
(5006, 'Mc Lyon', 'Paris', 0.14),
(5007, 'Paul Adam', 'Rome', 0.13),
(5003, 'Lauson Hen', 'San Jose', 0.12);
-- Check created table
select * from salesman;

CREATE TABLE nobel_win (
    Year INT,
    Subject VARCHAR(50),
    Winner VARCHAR(100),
    Country VARCHAR(50),
    Category VARCHAR(50)
);

INSERT INTO nobel_win (Year, Subject, Winner, Country, Category) VALUES
(1970, 'Physics', 'Hannes Alfven', 'Sweden', 'Scientist'),
(1970, 'Physics', 'Louis Neel', 'France', 'Scientist'),
(1970, 'Chemistry', 'Luis Federico Leloir', 'France', 'Scientist'),
(1970, 'Physiology', 'Ulf von Euler', 'Sweden', 'Scientist'),
(1970, 'Physiology', 'Bernard Katz', 'Germany', 'Scientist'),
(1970, 'Literature', 'Aleksandr Solzhenitsyn', 'Russia', 'Linguist'),
(1970, 'Economics', 'Paul Samuelson', 'USA', 'Economist'),
(1970, 'Physiology', 'Julius Axelrod', 'USA', 'Scientist'),
(1971, 'Physics', 'Dennis Gabor', 'Hungary', 'Scientist'),
(1971, 'Chemistry', 'Gerhard Herzberg', 'Germany', 'Scientist'),
(1971, 'Peace', 'Willy Brandt', 'Germany', 'Chancellor'),
(1971, 'Literature', 'Pablo Neruda', 'Chile', 'Linguist'),
(1971, 'Economics', 'Simon Kuznets', 'Russia', 'Economist'),
(1978, 'Peace', 'Anwar al-Sadat', 'Egypt', 'President'),
(1978, 'Peace', 'Menachem Begin', 'Israel', 'Prime Minister'),
(1987, 'Chemistry', 'Donald J. Cram', 'USA', 'Scientist'),
(1987, 'Chemistry', 'Jean-Marie Lehn', 'France', 'Scientist'),
(1987, 'Physiology', 'Susumu Tonegawa', 'Japan', 'Scientist'),
(1994, 'Economics', 'Reinhard Selten', 'Germany', 'Economist'),
(1994, 'Peace', 'Yitzhak Rabin', 'Israel', 'Prime Minister'),
(1987, 'Physics', 'Johannes Georg Bednorz', 'Germany', 'Scientist'),
(1987, 'Literature', 'Joseph Brodsky', 'Russia', 'Linguist'),
(1987, 'Economics', 'Robert Solow', 'USA', 'Economist'),
(1994, 'Literature', 'Kenzaburo Oe', 'Japan', 'Linguist');

select * from nobel_win;

create table  item_mast (
    PRO_ID INT PRIMARY KEY,
    PRO_NAME VARCHAR(50),
    PRO_PRICE DECIMAL(10, 2),
    PRO_COM INT
);

INSERT INTO item_mast (PRO_ID, PRO_NAME, PRO_PRICE, PRO_COM)
VALUES
    (101, 'Mother Board', 3200.00, 15),
    (102, 'Key Board', 450.00, 16),
    (103, 'ZIP drive', 250.00, 14),
    (104, 'Speaker', 550.00, 16),
    (105, 'Monitor', 5000.00, 11),
    (106, 'DVD drive', 900.00, 12),
    (107, 'CD drive', 800.00, 12),
    (108, 'Printer', 2600.00, 13),
    (109, 'Refill cartridge', 350.00, 13),
    (110, 'Mouse', 250.00, 12);
