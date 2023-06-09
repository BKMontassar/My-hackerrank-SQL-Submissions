### Revising the Select Query I 

<img src="../PIc/21.png" alt="solution">


#### Topic:
Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:

*Equilateral: It’s a triangle with 3 sides of equal length.
*Isosceles: It’s a triangle with 2 sides of equal length.
*Scalene: It’s a triangle with 3 sides of differing lengths.
*Not A Triangle: The given values of A, B, and C don’t form a triangle.

Sample Output

Isosceles
Equilateral
Scalene
Not A Triangle
Explanation

Values in the tuple (20,20,23) form an Isosceles triangle, because A=B.
Values in the tuple (20,20,20) form an Equilateral triangle, because A=B=C. Values in the tuple (20,21,22) form a Scalene triangle, because A!=B!=C.
Values in the tuple (13,14,30) cannot form a triangle because the combined value of sides A and B is not larger than that of side C.


#### Language : MS SQL
```sql
WITH checking_triangle as (
select A,B,C,
 Case 
    WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle'
    WHEN A = B AND B = C THEN 'Equilateral'
    WHEN A = B OR B = C OR A = C THEN 'Isosceles'
    ELSE 'Scalene'
 End as  checking 
from TRIANGLES

)


select checking  from checking_triangle

```
