---
index: 4 # labs number
num: 2 # lab number
permalink: /lab/Database/Lab3 # link
category: lab # project or lab
---

#### **Database**

---

The database has five tables. Primary key attributes are underlined and foreign keys are
noted in superscript.

- Customer = {<u>customerID</u>, firstName, lastName, income, birthData}
- Account = {<u>accNumber</u>, type, balance, branchNumber<sup>FK-Branch</sup>}
- Owns = {<u>customer</u><sup>IDFK-Customer</sup>, <u>accNumber</u><sup>FK-Account</sup>}
- Transactions = {<u>transNumber</u>, <u>accNumber</u><sup>FK-Account</sup>, amount}
- Employee = {<u>sin</u>, firstName, lastName, salary, branchNumber<sup>FK-Branch</sup>}
- Branch = {<u>branchNumber</u>, branchName, managerSIN<sup>FK-Employee</sup>, budget}

Notes

- The customerID attribute (Customer) is a unique number that represents a customer, it is not a customer’s SIN
- The accNumber attribute (Account) represents the account number
- The balance (Account) attribute represents the total amount in an account
- The type (Account) attribute represents the type an account: chequing, saving, or business
- The Owns relation represents a many-to-many relationship (between Customer and Account)
- The transNumber attribute (Transactions) represents a transaction number, combined with account number it uniquely identify a transaction
- The branchNumber attribute (Customer) uniquely identifies a branch
- The managerSIN attribute (Customer) represents the SIN of the branch manager

<br>

#### **Task**

---

1. First name, last name, income of customers whose income is within [30,000, 80,000],
   order by income (desc), lastName, firstName.

2. SIN, branch name, salary and manager’s salary - salary (that is, the salary of the
   employee’s manager minus salary of the employee) of all employees in London or
   New York, order by ascending (manager’ salary - salary).

3. First name, last name, and income of customers whose income is at least twice the
   income of every customer whose lastName is Butler, order by last name then first
   name.

4. Customer ID, income, account numbers and branch numbers of customers with
   income greater than 70,000 who own an account at both London and Latveria
   branches, order by customer ID then account number. The result should contain all
   the account numbers of customers who meet the criteria, even if the account itself
   is not held at London or Latveria.

5. Customer ID, types, account numbers and balances of business (type BUS) and
   savings (type SAV) accounts owned by customers who own at least one business
   account or at least one savings account, order by customer ID, then type, then
   account number.

6. Branch name, account number and balance of accounts with balances greater than
   $80,000 held at the branch managed by Phillip Edwards, order by account number.

7. Customer ID of customers who have an account at the New York branch, who do
   not own an account at the London branch and who do not co-own an account with
   another customer who owns an account at the London branch, order by customer
   ID. The result should not contain duplicate customer IDs (write the query satisfying
   all three conditions).

8. SIN, first name, last name, and salary of employees who earn more than $60,000, if
   they are managers show the branch name of their branch in a fifth column (which
   should be NULL/NONE for most employees), order by branch name (desc) and
   firstName (asc). You must use an outer join in your solution (which is the easiest
   way to do it).

9. Exactly as question (8), except that your query cannot include any join operation.

10. Customer ID, first name, last name and income of customers who have income
    greater than 6000 and own accounts in ALL of the branches that Helen Morgan
    owns accounts in, order by income in decreasing order (The output includes Helen
    Morgan).

11. SIN, first name, last name and salary of the lowest paid employee (or employees) of
    the Berlin branch, order by sin.

12. Branch name, and the difference of maximum and minimum (salary gap) and average salary of the employees at each branch, order by salary gap.

13. Count of the number of employees working at the New York branch and Count of
    the number of different last names of employees working at the New York branch
    (two numbers in a single row).

14. Sum of the employee salaries (a single number) at the Berlin branch.

15. Customer ID, first name and last name of customers who own accounts from three
    different branches (only three different types of branches), order by Last Name and
    first Name.

16. Average income of customers older than 58 and average income of customers younger
    than 28, the result must have two named columns, with one row, in one result set
    (hint: look up MySQL time and date functions http://www.mysqltutorial.org/mysqltimestampdiff/ ).

17. Customer ID, first name, income, and average account balance of customers who
    have at least three accounts, and whose last names begin with S and contain an e
    (e.g. Steve), order by customer ID.

18. Account number, balance, sum of transaction amounts, and balance - transaction
    sum (sum of transaction amount) for accounts in the London branch that have at
    least 14 transactions, order by transaction sum.

19. Branch name, account type, and average transaction amount of each account type
    for each branch for branches that have at least 40 accounts of any type, order by
    branch name, then account type.

20. Account type, account number, transaction number and amount of transactions of
    accounts where the average transaction amount is greater than two-and-half times
    the (overall) average transaction amount of accounts of that type. For example,
    if the average transaction amount of all business accounts is $2,000 then return
    transactions from business accounts where the average transaction amount for that
    account is greater than $5,500. Order by account type, then account number and
    finally transaction number. Note that all transactions of qualifying accounts should
    be returned even if they are less than the average amount of the account type.

<br>

#### **Report and Results**

---

[Github](https://github.com/Heejinee3/Database/tree/master/Lab3)
