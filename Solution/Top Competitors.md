### Top Competitors 

<img src="../PIc/1.png" alt="solution">


#### Topic:
Julia just finished conducting a coding contest, and she needs your help assembling the leaderboard! Write a query to print the respective hacker_id and name of hackers who achieved full scores for more than one challenge. Order your output in descending order by the total number of challenges in which the hacker earned a full score. If more than one hacker received full scores in same number of challenges, then sort them by ascending hacker_id.

Sample Output

90411 Joe
Explanation

Hacker 86870 got a score of 30 for challenge 71055 with a difficulty level of 2, so 86870 earned a full score for this challenge.

Hacker 90411 got a score of 30 for challenge 71055 with a difficulty level of 2, so 90411 earned a full score for this challenge.

Hacker 90411 got a score of 100 for challenge 66730 with a difficulty level of 6, so 90411 earned a full score for this challenge.

Only hacker 90411 managed to earn a full score for more than one challenge, so we print the their hacker_id and name as 2 space-separated values.

#### Language : MS SQL
```sql
select h.hacker_id ,h.name 
from submissions s
inner join hackers h
on s.hacker_id = h.hacker_id 
inner join challenges c
on s.challenge_id = c.challenge_id
inner join difficulty d 
on c.difficulty_level = d.difficulty_level
where s.score = d.score
group by h.hacker_id ,h.name
having count(s.score) >1
order by  count(*) DESC , h.hacker_id 
```
