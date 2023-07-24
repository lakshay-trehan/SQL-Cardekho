# SQL-Cardekho 
Create schema cars ;
USE CARS ;
1) Read Cars Data
SELECT * FROM CAR_DEKHO ;

2) Total cars
SELECT COUNT(NAME) FROM CAR_DEKHO

3) The manager asked the employee how many cars will be available in 2023 ?
SELECT * FROM CAR_DEKHO ;
SELECT COUNT(*) FROM CAR_DEKHO
WHERE YEAR = '2023' ;

4) The manager asked the employee how many cars will be availaible in 2020,2021,2022

SELECT YEAR, COUNT(*) FROM CAR_DEKHO
WHERE YEAR IN ('2020','2021','2022') 
GROUP BY YEAR ;

5) Client asked me to print the total of all cars by years . I can't see all the details 

SELECT YEAR , COUNT(*) FROM CAR_DEKHO GROUP BY YEAR
ORDER BY YEAR ASC ;

6) Client asked to car dealer agent . How many diessel cars will be there in 2020 ?
SELECT YEAR, COUNT(*) FROM CAR_DEKHO
WHERE YEAR = '2020' AND FUEL = 'DIESEL'
GROUP BY YEAR ;

7) CLIENT REQUESTED A CAR DEALER AGENT HOW MANY PETROL CARS WILL BE THERE IN 2020 ?
SELECT YEAR , COUNT(*) FROM CAR_DEKHO
WHERE YEAR = '2020' AND FUEL = 'PETROL' 
GROUP BY YEAR ;

8) The manager told  the employees to give print of all fuel cars (petrol,diesel and cng) come by all year 
SELECT YEAR , COUNT(*) FROM CAR_DEKHO WHERE FUEL IN ('PETROL') GROUP BY YEAR ;
SELECT YEAR , COUNT(*) FROM CAR_DEKHO WHERE FUEL IN ('DIESEL') GROUP BY YEAR ;
SELECT YEAR , COUNT(*) FROM CAR_DEKHO WHERE FUEL IN ('CNG') GROUP BY YEAR ;

9) Manager said there were more than 100 cars in a given year which year has more than 100 cars
SELECT YEAR,COUNT(*) FROM CAR_DEKHO GROUP BY YEAR HAVING COUNT(*) >100 ;

10) Manager said to the employee all cars count details between 2015 and 2023 we need a complete list
SELECT COUNT(*) FROM CAR_DEKHO
WHERE YEAR BETWEEN 2015 AND 2023 

11) Manager said to the employee all cars  details between 2015 and 2023 we need a complete list
SELECT * FROM CAR_DEKHO WHERE YEAR BETWEEN 2015 AND 2023 ;
