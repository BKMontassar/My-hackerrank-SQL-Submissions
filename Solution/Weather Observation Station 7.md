### Weather Observation Station 7


<img src="../PIc/12.png" alt="solution">


#### Topic:
Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.
where LAT_N is the northern latitude and LONG_W is the western longitude.



#### Language : MS SQL
```sql
select distinct CITY from STATION where CITY LIKE '%a' OR CITY LIKE '%e' OR CITY LIKE '%i' OR CITY LIKE '%o' OR CITY LIKE '%u'
```
