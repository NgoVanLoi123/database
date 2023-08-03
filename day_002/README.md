### 1853. Convert Date Format
      
![](day1.png)

```sql
select date_format(day,'%W, %M %e, %Y') as Days from Days
``` 
![](day2.png)



### 1821. Find Customers With Positive Revenue this Year
Tạo bảng
```sql
create table Customers(
    customer_id int primary key,
    year int ,
    revenue int
    );
```
![](1821_1.png)

```sql
select Customer_id from Customers where revenue>0 and year=2021
```
![](1821_2.png)



### 2026. Low-Quality Problems
Tạo bảng
```sql
create table Problems(
    problem_id int primary key,
    likes int,
    dislikes int
    );
```
![](2026_1.png)

```sql
select problem_id from Problems where (likes/(likes+dislikes))<0.6 order by problem_id asc
```
![](2026_2.png)



### 2082. The Number of Rich Customers
Tạo bảng
```sql
create table Store(
    bill_id int primary key,
    customer_id int,
    amount int
    );
```
![](2082_1.png)

```sql
select count(DISTINCT customer_id) as rich_count  
from Store where amount>500 
```
![](2082_2.png)



### 2377. Sort the Olympic Table
Tạo bảng
```sql
create table Olympic(
    country varchar(50) primary key,
    gold_medals int,
    silver_medals int,
    bronze_medals int
    );
```
![](2377_1.png)

```sql
select *from Olympic 
ORDER BY gold_medals DESC, silver_medals DESC, bronze_medals DESC, country;
```
![](2377_2.png)
