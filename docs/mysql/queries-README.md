# 1.SQL Query to Find the Highest Salary of Each Department
```
CREATE TABLE department(
    ID int,
    SALARY int,
    NAME Varchar(20),
    DEPT_ID Varchar(255));
```

```
INSERT INTO department VALUES (1, 34000, 'ANURAG', 'UI DEVELOPERS');
INSERT INTO department VALUES (2, 33000, 'harsh', 'BACKEND DEVELOPERS');
INSERT INTO department VALUES (3, 36000, 'SUMIT', 'BACKEND DEVELOPERS');
INSERT INTO department VALUES (4, 36000, 'RUHI', 'UI DEVELOPERS');
INSERT INTO department VALUES (5, 37000, 'KAE', 'UI DEVELOPERS');
```
# 2.SQL Query to List the Second Highest Salary By Department
Use N-1
```
select ID,SALARY,NAME,DEPT_ID from department d1
where 1 =
(select count(distinct salary) from department d2
where d2.salary > d1.salary) 
ORDER BY DEPT_ID;

```
<img width="407" alt="image" src="https://github.com/user-attachments/assets/ecfd4ae1-a818-4628-b99d-b6cfd757842a" />
<img width="568" alt="image" src="https://github.com/user-attachments/assets/4848e000-919b-4340-9f49-57ff6a3e4782" />



# 3.Search without null and blank values

```
select * from department where salary is not null and salary <> ' ';

```
# 4.For description of table
```
DESC department;
```

# 5.COUNT no of records=5
```
select count(salary) from department
```


