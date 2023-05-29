---
index: 4 # labs number
num: 3 # lab number
permalink: /lab/Database/Lab4 # link
category: lab # project or lab
---

#### **Relational Algebra**

---

In this problem, we will use a bank database that is similar to Lab3, but has more tables
and columns. Unlike Lab3, no one has the same firstName and lastName at the same
time. The database consists of 7 tables with the following schemas.

- Customer = {<u>customerID</u>, firstName, lastName, income, birthData}
- Account = {<u>accNumber</u>, type, balance, branchNumber<sup>FK-Branch</sup>}
- Owns = {<u>customerID</u><sup>FK-Customer</sup>, <u>accNumber</u><sup>FK-Account</sup>}
- Transactions = {<u>transNumber</u>, <u>accNumber</u><sup>FK-Account</sup>, amount, date}
- Employee = {<u>sin</u>, firstName, lastName, salary, startDate, branchNumber<sup>FK-Branch</sup>}
- PersonalBanker = {<u>customerID</u><sup>FK-Customer</sup>, sin<sup>FK-Employee</sup>}
- Branch = {<u>branchNumber</u>, branchName, street, numberEmployess, managerSIN<sup>FK-Employee</sup>, budget}

[Task] Write relational algebra queries.

1. You are to find the SINs, and first and last names of employees who own an account
   in the branch in which they work.

2. The customer IDs of customers who have personal bankers in either the Vancouver
   or Metrotown branches (note that the personal bankers must be distinct employees
   as an employee only works at one branch).

3. The SINs, first and last names and salaries of employees who are both personal
   bankers and managers

4. The SINs and salaries of employees who earn more than the manager of their branch.

5. The customer IDs, first names, last names and incomes of customers who have an
   account at a branch with a budget no more than $3,200,000.

6. The branch names of branches that employ at least one employee whose last name
   is Martin, and at least one employee whose last name is Jackson.

7. The customer IDs of customers who own a joint account (an account that is owned
   by more than one customer).

8. The first names, last names and birth dates of customers who own an account in
   the London branch, and the first names, last names and start dates of employees
   who work in the London branch (i.e. one query that returns one list of first and last
   names and dates of these 2 groups of people).

9. The first and last names of customers whose first name is Steve and income is less
   than $40,000.
10. The customer IDs of customers whose accounts have no transactions with amounts
    of which the absolute value is less than $3,000 (i.e. all their transactions are either
    greater than or equal to $3,000 or less than or equal to -$3,000).

<br>

#### **Entity-Relationship Model**

---

In this problem, we will design a university database that models KAIST using an E/R
diagram. The database should include information about students, departments, professors, courses, and buildings. The details are as follows.

1. The information of a student includes a student ID, a name, a department, and any
   courses they take. Here, the student ID is unique for each student. Each student
   can have multiple majors (departments).

   If a student lives in a dormitory, the student information should include the name
   of the building he or she lives in. Each student has at most one dormitory.
   Each student must be a graduate student or undergraduate student. If a student is
   in graduate school, the student information must include his or her research field.
   For undergraduate students, the research field should have a NULL value.

2. The information of a department includes a department name, the head of the
   department, professors, and buildings. The department name is unique, and each
   department has one or more buildings. Also, a building can be shared by multiple
   departments.

3. The information about a professor includes an employee ID, a name, affiliated departments, and the names of the courses the professor teaches. The employee ID
   is unique for each professor. A professor can be affiliated with one or more departments.

4. The information of a course includes a course name, a course code, and the professors
   who teach it. The code of each course is unique, and each course can be taught by
   one or more professors.

5. The information of a building contains the building’s name (e.g., IT building) and
   the building code (e.g., N1). The code of each building is unique

[Task 1] Draw an E/R diagram based on the above requirements.

When generating the diagram, try to follow the best practices covered in class. Since
there can be multiple correct solutions, briefly explain why you made any design choices.

[Task 2] Convert the E/R diagram into a schema.

Again, try to follow the best practices covered in class. Since there can be multiple
correct solutions, briefly explain why you made any design choices

<br>

#### **Normal Forms**

---

In this problem, we will use a real dataset (called Black Friday) to identify functional
dependencies (FDs) in a table and normalize its schema.

You can download the Black Friday dataset on Kaggle using [this link](https://www.kaggle.com/datasets/llopesolivei/blackfriday) (CSV file). The CSV file is one table where the first row contains the attribute names.

[Task 1] Find all the non-trivial FDs in the table based on its schema.

[Task 2] For each FD in the previous task, provide an SQL query that shows that the FD indeed holds on the table.

[Task 3] Does the table contain redundant information? Are there potential
anomalies? Briefly explain with examples.

[Task 4] Normalize the table to remove redundant information and prevent
anomalies. Write down the resulting schema and briefly explain whether the
schema is in 3NF, BCNF, and/or 4NF.

<br>

#### **Report**

---

[Github](https://github.com/Heejinee3/Database/tree/master/Lab4)

<br>

#### **Glossary**

---

[Relational Algebra](https://velog.io/@chunjakim/Relational-Algebra)

[Entity-Relationship Model](https://velog.io/@chunjakim/ER-Model-Entity-Relationship-Model)

[Normal Forms](https://velog.io/@chunjakim/Normal-Forms)
