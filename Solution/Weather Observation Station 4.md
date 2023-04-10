### Weather Observation Station 4

<img src="../PIc/9.png" alt="solution">


#### Topic:
Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.
where LAT_N is the northern latitude and LONG_W is the western longitude.

For example, if there are three records in the table with CITY values ‘New York’, ‘New York’, ‘Bengalaru’, there are 2 different city names: ‘New York’ and ‘Bengalaru’. The query returns 1, because 
total number of records – number of unique city names = 3 – 2 = 1.



#### Language : MS SQL
```sql
SELECT COUNT(CITY) - COUNT(DISTINCT CITY) AS city_difference
FROM STATION;
```