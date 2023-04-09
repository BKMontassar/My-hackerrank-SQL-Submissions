### Revising the Select Query I 

<img src="./PIc/1.png"  >

#### Topic:
Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.
The CITY table is described as follows:



#### Language : MS SQL
```sql
select * from CITY where CITY.POPULATION > 100000 and CITY.COUNTRYCODE ='USA'
```
