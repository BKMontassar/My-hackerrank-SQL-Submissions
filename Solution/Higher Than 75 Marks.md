### Higher Than 75 Marks

<img src="../PIc/18.png" alt="solution">


#### Topic:
Query the Name of any student in STUDENTS who scored higher than 75 Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

The Name column only contains uppercase (A-Z) and lowercase (a-z) letters.


Sample Output

Ashley
Julia
Belvet
Explanation

Only Ashley, Julia, and Belvet have Marks > 75. If you look at the last three characters of each of their names, there are no duplicates and ‘ley’ < ‘lia’ < ‘vet’.



#### Language : MS SQL
```sql
select Name from STUDENTS where Marks > 75 
order by right(Name,3) , ID asc
```
