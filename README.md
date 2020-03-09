# SQL
This SQL code creates Relational Tables and performs queries within a
SQLite database.

### Introduction

For this project, there are two datasets

* Borrowings
* Repayments


The Borrowings Table have the following columns:

*   BRW_ID (PRIMARY KEY) (FOREIGN KEY)
* BRW_DisbursalDate
* BRW_Repayment_Day_Of_Month
* BRW_Interest_Rate
* BRW_Amount
* BRW_Term
* BRW_MonthlyRepaymentAmount
* BRW_State
* BRW_NotDisplayed
* BRW_LastUpdateTime

The Repayments Table have the following columns:

* REP_ID (PRIMARY KEY)
* REP_State
* REP_Amount
* REP_RepaymentDate
* REP_Borrowing
* REP_Deleted
* REP_RepaymentDate
* REP_LastUpdateTime

The SQL queries are designed to address the below requirements:

Q1. Find total number of loans disbursed between 9th Dec 2015
and 17th Oct 2017 (both dates included).

Q2. Which year / month had the most loans with state 'Withdrawn'
(list top three with highest number of disbursals).

Q3. Check for any duplicate records.

Q4. For each term, return total number of loans that have failed
repayments.

Q5. Find all loans with state 'Withdrawn' that have no repayments.

Q6. Return the latest 3 repayment dates for each loan with state
'Withdrawn', all three dates should be on a single row.


## PREREQUISITIE

1. The 'main' program is scripted in Python3. Have the correct version of
  python installed.
  Please refer link - https://docs.python.org/3/installing/index.html

2. Install a DB browser for SQLite.
   Please refer link - https://sqlitebrowser.org/. Using the browser once
   can easily create tables, insert data, edit data, or run simple SQL queries
   on the data in the database.

## INSTRUCTIONS

1. Load Terminal
2. Set current directory to the folder containing the main.py file.
3. Run script from a Terminal. Type python3 main.py
4. The results of the queries will be reported in the terminal.
5. The queries can be individually tested in any SQL environment by just
   copy-pasting the SQL commands only.
   The SQL commands can be found within curr.execute ('').
   For example:
   ```
   cur.execute('''
   SELECT REP_ID, COUNT(*)
   FROM Repayments
   Group BY REP_ID
   HAVING COUNT(*) >1
   ''')
   ```
6. The loan_db.sqlite file is created by the main.py. This doesn't have to be
   included in the directory. It will be overwritten by the Python script. 

## Author
* Jerin Philips Rajan
