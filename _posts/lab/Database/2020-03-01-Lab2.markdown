---
index: 4 # labs number
num: 1 # lab number
permalink: /lab/Database/Lab2 # link
category: lab # project or lab
---

#### **Development Environment**

---

This is a guide for you to get started with Google Cloud SQL. Cloud SQL is a fullymanaged database service that makes it easy to set up, maintain, manage, and administer your relational databases on Google Could Platform(GCP). Google Cloud SQL supports either MySQL or PostgreSQL for the database language, and we will use MySQL.

<br>

#### **Task**

---

1. Using SQL to create a database

   1. Create an empty database named coursys

   2. Create a table named grades

      The grades table has four columns and six rows as shown below.

      | studentid | course | mark | credit |
      | --------- | ------ | ---- | ------ |
      | 20210001  | EE477  | 90   | 3.5    |
      | 20210001  | EE412  | 85   | 4      |
      | 20210001  | EE209  | 79.5 | 5      |
      | 20210002  | EE477  | 95   | 3.5    |
      | 20210002  | EE209  | 59   | 5      |
      | 20210002  | EE412  | 70   | 4      |

      Please write an SQL query to create the grades table and insert the above data
      (six rows) into the grades table. Note that the table has to meet the following
      requirements.

      - studentid - integer
      - course - char(10)
      - mark and credit - double
      - (studentid, course) is Primary Key
      - studentid references students.id

   3. Create a table named students

      The students table has four columns and two rows as shown below.

      | id       | name | gender | age |
      | -------- | ---- | ------ | --- |
      | 20210001 | Roh  | Female | 26  |
      | 20210002 | Tae  | Male   | 23  |

      Please write an SQL query to create the students table and insert the above data
      (2 rows) into the students table. Note that the table has to meet the following
      requirements.

      - id, age - integer
      - name - varchar(30)
      - gender - char(6)
      - id is a primary key
      - name cannot be NULL

2. Using SQL to query a database

   1. Please write an SQL query to show all rows in the grades table.

   2. Please write an SQL query to show the rows whose course is “EE477” in the grades
      table.

   3. Please write an SQL query to show the rows whose mark is larger than 60 and credit
      is no smaller than 4 in the grades table.

   4. Please write an SQL query to show the rows whose course starts with “EE4” in the
      grades table.

   5. Please write an SQL query to show studentid, course and mark of all rows in the
      grades table.

   6. Please write an SQL query to show distinct course of all rows in the grades table.

   7. Please write an SQL query to show studentid, course and markpoint of all rows in
      the grades table. markpoint is defined as markpoint = mark \* credit.

   8. Please write an SQL query to find the students who have taken “EE477” and show
      their name, mark.

   9. Please write an SQL query to compute lettergrade of each row in the grades table,
      and show studentid, course and lettergrade of all rows in the grades table. lettergrade is computed as follows (use a CASE Expression):

      - If mark ≥ 90, then lettergrade = “A”
      - If 80 ≤ mark < 90, then lettergrade = “B”
      - If 70 ≤ mark < 80, then lettergrade = “C”
      - If 60 ≤ mark < 70, then lettergrade = “D”
      - If mark < 60, then lettergrade = “F”

<br>

#### **Report and Results**

---

[Github](https://github.com/Heejinee3/Database/tree/master/Lab2)
