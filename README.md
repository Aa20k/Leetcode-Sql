1# Leetcode-Sql
**1661. Average Time of Process per Machine**
**#SQL query-**
select a1.machine_id, round(avg(a2.timestamp-a1.timestamp),3) as processing_time
from Activity a1
join Activity a2
on a1.machine_id=a2.machine_id
and a1.process_id=a2.process_id
and a1.timestamp<a2.timestamp
group by a1.machine_id

**#577. Employee Bonus**
# Write your MySQL query statement below
select e.name,b.bonus
from Employee e
left join Bonus b
on e.empId=b.empId
where b.bonus<1000
or b.bonus is null
