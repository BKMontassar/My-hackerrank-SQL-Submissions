### New Companies

<img src="../PIc/25.png" alt="solution">


#### Topic:
Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy: 

Given the table schemas below, write a query to print the company_code, founder name, total number of lead managers, total number of senior managers, total number of managers, and total number of employees. Order your output by ascending company_code.

Note:

The tables may contain duplicate records.
The company_code is string, so the sorting should not be numeric. For example, if the company_codes are C_1, C_2, and C_10, then the ascending company_codes will be C_1, C_10, and C_2.

Sample Output

C1 Monika 1 2 1 2
C2 Samantha 1 1 2 2
Explanation

In company C1, the only lead manager is LM1. There are two senior managers, SM1 and SM2, under LM1. There is one manager, M1, under senior manager SM1. There are two employees, E1 and E2, under manager M1.

In company C2, the only lead manager is LM2. There is one senior manager, SM3, under LM2. There are two managers, M2 and M3, under senior manager SM3. There is one employee, E3, under manager M2, and another employee, E4, under manager, M3.



#### Language : MS SQL
```sql
select  C.company_code,
founder,
count(distinct L.lead_manager_code),
count( distinct S.senior_manager_code),
count(distinct M.manager_code),
count(distinct E.employee_code) 
from Company C
left join Lead_Manager L on L.company_code = C.company_code
left join Senior_Manager S on S.lead_manager_code =L.lead_manager_code
left join Manager M on M.senior_manager_code = S.senior_manager_code
left join Employee E on E.manager_code = M.manager_code
group  by  C.company_code ,founder
order by company_code
```
