### Weather Observation Station 10

<img src="../PIc/16.png" alt="solution">


#### Topic:
Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.
where LAT_N is the northern latitude and LONG_W is the western longitude.



#### Language : MS SQL
```sql
SELECT DISTINCT CITY
FROM STATION
WHERE CITY NOT LIKE '%A' 
AND CITY NOT LIKE '%E' 
AND CITY NOT LIKE '%I' 
AND CITY NOT LIKE '%O' 
AND CITY NOT LIKE '%U'

```
