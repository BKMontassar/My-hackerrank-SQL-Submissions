### Weather Observation Station 5 

<img src="../PIc/10.png" alt="solution">


#### Topic:
Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
where LAT_N is the northern latitude and LONG_W is the western longitude.

Sample Input

For example, CITY has four entries: DEF, ABC, PQRS and WXY.

Sample Output

ABC 3
PQRS 4
Explanation

When ordered alphabetically, the CITY names are listed as ABC, DEF, PQRS, and WXY, with the respective lengths and . The longest-named city is obviously PQRS, but there are options for shortest-named city; we choose ABC, because it comes first alphabetically.

Note You can write two separate queries to get the desired output. It need not be a single query.

#### Language : MS SQL
```sql
select TOP 1 CITY , LEN(CITY) from STATion 
Order by LEN(city) DESC , CITY DESC

select TOP 1 CITY , LEN(CITY) from STATion 
Order by LEN(city) asc , CITY ASC
```
