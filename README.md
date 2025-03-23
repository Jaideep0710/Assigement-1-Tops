# Assigement-1-Tops
Assigement 1 Tops 
 select * from worker;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         1 | Monika     | Arora     | 100000 | 2014-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2014-06-11 09:00:00 | Admin      |
|         3 | vishal     | Singhal   | 300000 | 2014-02-20 09:00:00 | HR         |
|         4 | Amitabh    | Singh     | 500000 | 2014-02-20 09:00:00 | Admin      |
|         5 | vivek      | Bhati     | 500000 | 2014-06-11 09:00:00 | Admin      |
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
|         7 | Satish     | Kumar     |  75000 | 2014-01-20 09:00:00 | Account    |
|         8 | Geetika    | Chauhan   |  90000 | 2014-04-11 09:00:00 | Admin      |
+-----------+------------+-----------+--------+---------------------+------------+

1) select * from worker order by first_name ASC;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         4 | Amitabh    | Singh     | 500000 | 2014-02-20 09:00:00 | Admin      |
|         8 | Geetika    | Chauhan   |  90000 | 2014-04-11 09:00:00 | Admin      |
|         1 | Monika     | Arora     | 100000 | 2014-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2014-06-11 09:00:00 | Admin      |
|         7 | Satish     | Kumar     |  75000 | 2014-01-20 09:00:00 | Account    |
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
|         3 | vishal     | Singhal   | 300000 | 2014-02-20 09:00:00 | HR         |
|         5 | vivek      | Bhati     | 500000 | 2014-06-11 09:00:00 | Admin      |
+-----------+------------+-----------+--------+---------------------+------------+
8 rows in set (0.05 sec)

mysql> select * from worker order by department DESC;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         1 | Monika     | Arora     | 100000 | 2014-02-20 09:00:00 | HR         |
|         3 | vishal     | Singhal   | 300000 | 2014-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2014-06-11 09:00:00 | Admin      |
|         4 | Amitabh    | Singh     | 500000 | 2014-02-20 09:00:00 | Admin      |
|         5 | vivek      | Bhati     | 500000 | 2014-06-11 09:00:00 | Admin      |
|         8 | Geetika    | Chauhan   |  90000 | 2014-04-11 09:00:00 | Admin      |
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
|         7 | Satish     | Kumar     |  75000 | 2014-01-20 09:00:00 | Account    |
+-----------+------------+-----------+--------+---------------------+------------+
8 rows in set (0.00 sec)

2) select * from worker where first_name IN ('Vipul','satish');
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
|         7 | Satish     | Kumar     |  75000 | 2014-01-20 09:00:00 | Account    |
+-----------+------------+-----------+--------+---------------------+------------+
2 rows in set (0.04 sec)

3) select * from worker where First_name like '%h' and length(first_name)=6;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         7 | Satish     | Kumar     |  75000 | 2014-01-20 09:00:00 | Account    |
+-----------+------------+-----------+--------+---------------------+------------+

4)  select * from worker where salary>100000;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         3 | vishal     | Singhal   | 300000 | 2014-02-20 09:00:00 | HR         |
|         4 | Amitabh    | Singh     | 500000 | 2014-02-20 09:00:00 | Admin      |
|         5 | vivek      | Bhati     | 500000 | 2014-06-11 09:00:00 | Admin      |
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
+-----------+------------+-----------+--------+---------------------+------------+
4 rows in set (0.00 sec)

5) select * from worker limit 6;
+-----------+------------+-----------+--------+---------------------+------------+
| worker_ID | first_name | last_name | salary | joining_date        | department |
+-----------+------------+-----------+--------+---------------------+------------+
|         1 | Monika     | Arora     | 100000 | 2014-02-20 09:00:00 | HR         |
|         2 | Niharika   | Verma     |  80000 | 2014-06-11 09:00:00 | Admin      |
|         3 | vishal     | Singhal   | 300000 | 2014-02-20 09:00:00 | HR         |
|         4 | Amitabh    | Singh     | 500000 | 2014-02-20 09:00:00 | Admin      |
|         5 | vivek      | Bhati     | 500000 | 2014-06-11 09:00:00 | Admin      |
|         6 | vipul      | Diwan     | 200000 | 2014-06-11 09:00:00 | Account    |
+-----------+------------+-----------+--------+---------------------+------------+
6 rows in set (0.00 sec)

6)  select department,count(*) from worker group by department having count(*)<5;
+------------+----------+
| department | count(*) |
+------------+----------+
| HR         |        2 |
| Admin      |        4 |
| Account    |        2 |
+------------+----------+
3 rows in set (0.00 sec)

7)  select department,count(*) as no_of_employees from worker group by department having count(*)>1;
+------------+-----------------+
| department | no_of_employees |
+------------+-----------------+
| HR         |               2 |
| Admin      |               5 |
| Account    |               2 |
+------------+-----------------+
3 rows in set (0.00 sec)

8) select first_name,department,salary from worker where salary IN (select max(salary) from worker group by department);
+------------+------------+--------+
| first_name | department | salary |
+------------+------------+--------+
| vishal     | HR         | 300000 |
| Amitabh    | Admin      | 500000 |
| vivek      | Admin      | 500000 |
| vipul      | Account    | 200000 |
| Raj        | Admin      | 500000 |
+------------+------------+--------+



1) select * from student;
+-----------+----------------+--------+------------+-------+---------+----------+------------+
| studentID | stdName        | Gender | percentage | class | section | Stream   | DOB        |
+-----------+----------------+--------+------------+-------+---------+----------+------------+
|         1 | Surekha Joshi  | Female |         82 |    12 | A       | Science  | 1998-08-03 |
|         2 | Maahi Agarwal  | Female |         56 |    11 | C       | Commerce | 2008-11-23 |
|         3 | sanam verma    | Male   |         59 |    11 | C       | Commerce | 2006-06-29 |
|         4 | Ronit Kumar    | Male   |         63 |    11 | C       | Commerce | 1997-11-05 |
|         5 | Dipesh Pulkit  | Male   |         78 |    11 | B       | Science  | 2003-09-14 |
|         6 | Jahanvi puri   | female |         60 |    11 | B       | commerce | 2008-07-11 |
|         7 | Sanam KUmar    | male   |         23 |    12 | F       | commerce | 1998-08-03 |
|         8 | Sahil saras    | male   |         56 |    11 | C       | commerce | 2008-07-11 |
|         9 | Akshra Agarwal | female |         72 |    12 | B       | commerce | 1996-10-01 |
|        10 | stuti Mishra   | female |         39 |    12 | F       | Science  | 2008-11-23 |
|        11 | Harsh agarwal  | male   |         42 |    11 | C       | Science  | 1998-08-03 |
|        12 | Nikunj Agarwal | male   |         49 |    12 | C       | Commerce | 1998-06-28 |
|        13 | Akriti saxena  | female |         89 |    12 | A       | Science  | 2008-11-23 |
|        14 | Tani Rastogi   | female |         82 |    12 | A       | Science  | 2008-11-23 |
+-----------+----------------+--------+------------+-------+---------+----------+------------+
14 rows in set (0.02 sec)

2)  select stdname,DOB from student;
+----------------+------------+
| stdname        | DOB        |
+----------------+------------+
| Surekha Joshi  | 1998-08-03 |
| Maahi Agarwal  | 2008-11-23 |
| sanam verma    | 2006-06-29 |
| Ronit Kumar    | 1997-11-05 |
| Dipesh Pulkit  | 2003-09-14 |
| Jahanvi puri   | 2008-07-11 |
| Sanam KUmar    | 1998-08-03 |
| Sahil saras    | 2008-07-11 |
| Akshra Agarwal | 1996-10-01 |
| stuti Mishra   | 2008-11-23 |
| Harsh agarwal  | 1998-08-03 |
| Nikunj Agarwal | 1998-06-28 |
| Akriti saxena  | 2008-11-23 |
| Tani Rastogi   | 2008-11-23 |
+----------------+------------+
14 rows in set (0.00 sec)

3)  select * from student Where percentage>=80;
+-----------+---------------+--------+------------+-------+---------+---------+------------+
| studentID | stdName       | Gender | percentage | class | section | Stream  | DOB        |
+-----------+---------------+--------+------------+-------+---------+---------+------------+
|         1 | Surekha Joshi | Female |         82 |    12 | A       | Science | 1998-08-03 |
|        13 | Akriti saxena | female |         89 |    12 | A       | Science | 2008-11-23 |
|        14 | Tani Rastogi  | female |         82 |    12 | A       | Science | 2008-11-23 |
+-----------+---------------+--------+------------+-------+---------+---------+------------+
3 rows in set (0.01 sec)

4)  select stdname,Stream,percentage from student where percentage>80;
+---------------+---------+------------+
| stdname       | Stream  | percentage |
+---------------+---------+------------+
| Surekha Joshi | Science |         82 |
| Akriti saxena | Science |         89 |
| Tani Rastogi  | Science |         82 |
+---------------+---------+------------+
3 rows in set (0.00 sec)

5) select * from student where stream ='science' AND percentage>75;
+-----------+---------------+--------+------------+-------+---------+---------+------------+
| studentID | stdName       | Gender | percentage | class | section | Stream  | DOB        |
+-----------+---------------+--------+------------+-------+---------+---------+------------+
|         1 | Surekha Joshi | Female |         82 |    12 | A       | Science | 1998-08-03 |
|         5 | Dipesh Pulkit | Male   |         78 |    11 | B       | Science | 2003-09-14 |
|        13 | Akriti saxena | female |         89 |    12 | A       | Science | 2008-11-23 |
|        14 | Tani Rastogi  | female |         82 |    12 | A       | Science | 2008-11-23 |
+-----------+---------------+--------+------------+-------+---------+---------+------------+
4 rows in set (0.00 sec) 


