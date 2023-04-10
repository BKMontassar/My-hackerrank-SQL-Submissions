### Symmetric Pairs

<img src="../PIc/1.png" alt="solution">


#### Topic:
You are given a table, Functions, containing two columns: X and Y.
Two pairs (X1, Y1) and (X2, Y2) are said to be symmetric pairs if X1 = Y2 and X2 = Y1.

Write a query to output all such symmetric pairs in ascending order by the value of X. List the rows such that X1 ≤ Y1.

Sample Output

20 20
20 21
22 23



#### Language : MS SQL
```sql

with found_pairs as (
select X ,Y,
ROW_NUMBER()  over(Order by F.X ,F.Y asc ) as rank_P
from Functions F 
)
select distinct  FP.X,FP.Y 
from found_pairs FP join found_pairs FP2 on FP.X = FP2.Y 
and FP2.X = FP.Y
and FP.rank_P <> FP2.rank_P
where FP.X <= FP.Y
Order by X asc


```
