### Weather Observation Station 12

<img src="../PIc/17.png" alt="solution">


#### Topic:
Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
where LAT_N is the northern latitude and LONG_W is the western longitude.



#### Language : MS SQL
```sql
SELECT DISTINCT CITY
FROM STATION
WHERE (LEFT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U')) 
   and (RIGHT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U'))
```
