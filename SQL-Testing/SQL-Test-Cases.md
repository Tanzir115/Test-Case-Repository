# SQL Test Cases Documentation

## Table of Contents
1. [Verify Data Retrieval for Valid Query](#verify-data-retrieval-for-valid-query)
2. [Verify Data Insertion](#verify-data-insertion)
3. [Verify Data Update](#verify-data-update)
4. [Verify Data Deletion](#verify-data-deletion)
5. [Verify Constraints Enforcement (Unique Constraint)](#verify-constraints-enforcement-unique-constraint)
6. [Verify Not Null Constraint](#verify-not-null-constraint)
7. [Verify Data Integrity with Foreign Key Constraints](#verify-data-integrity-with-foreign-key-constraints)
8. [Verify Index Performance](#verify-index-performance)

---

## **1. Verify Data Retrieval for Valid Query**
```
Test Case ID: TC_SQL_001 Title: Verify data retrieval with valid SQL query Description: Ensure that a valid SELECT query retrieves the correct data from the database. Preconditions: Data should exist in the relevant table. Steps to Execute:

Connect to the database.
Execute the following SQL query:
SELECT * FROM users WHERE user_id = 1;
Verify that the returned data matches the expected user information. Expected Result: The query should return the correct user details for user_id = 1. Status: Pass/Fail
```
---

## **2. Verify Data Insertion**
```
Test Case ID: TC_SQL_002 Title: Verify insertion of a new record into the users table Description: Ensure that a valid INSERT query adds a new record into the users table. Preconditions: The users table should be empty or ready for insertion. Steps to Execute:

Connect to the database.
Execute the following SQL query:
INSERT INTO users (username, password, email) 
VALUES ('new_user', 'password123', 'new_user@example.com');
Verify that the new record is added by running a SELECT query:
SELECT * FROM users WHERE username = 'new_user';
Expected Result: The new user should be added to the users table, and the data should be visible in the result set. Status: Pass/Fail

```
---

## **3. Verify Data Update**
```
Test Case ID: TC_SQL_003 Title: Verify update of user information Description: Ensure that the UPDATE query correctly modifies data in the users table. Preconditions: The user record should exist. Steps to Execute:

Connect to the database.
Execute the following SQL query:
UPDATE users SET email = 'updated_user@example.com' WHERE user_id = 1;
Verify that the email field is updated by running:
SELECT * FROM users WHERE user_id = 1;
Expected Result: The email field for user_id = 1 should be updated to 'updated_user@example.com'. Status: Pass/Fail

```
---

## **4. Verify Data Deletion**
```
Test Case ID: TC_SQL_004 Title: Verify deletion of a record from the users table Description: Ensure that a DELETE query correctly removes a record from the users table. Preconditions: A user record must exist in the users table. Steps to Execute:

Connect to the database.
Execute the following SQL query:
DELETE FROM users WHERE user_id = 1;
Verify that the record is deleted by running:
SELECT * FROM users WHERE user_id = 1;
Expected Result: No record should be returned for user_id = 1, confirming that the record has been deleted. Status: Pass/Fail

```
---

## **5. Verify Constraints Enforcement (Unique Constraint)**
```
Test Case ID: TC_SQL_005 Title: Verify enforcement of unique constraint on email Description: Ensure that a unique constraint on the email field prevents duplicate entries. Preconditions: The users table should have a unique constraint on the email column. Steps to Execute:

Connect to the database.
Attempt to insert a record with a duplicate email:
INSERT INTO users (username, password, email) 
VALUES ('duplicate_user', 'password123', 'existing_user@example.com');
Verify that the insert fails and an error is returned (unique constraint violation). Expected Result: The database should return an error due to the unique constraint violation, preventing the duplicate email entry. Status: Pass/Fail
```
---

## **6. Verify Not Null Constraint**
```
Test Case ID: TC_SQL_006 Title: Verify enforcement of NOT NULL constraint Description: Ensure that the NOT NULL constraint on the username field is enforced. Preconditions: The users table should have a NOT NULL constraint on the username column. Steps to Execute:

Connect to the database.
Attempt to insert a record with a NULL value in the username field:
INSERT INTO users (username, password, email) 
VALUES (NULL, 'password123', 'user_without_username@example.com');
Verify that the insert fails and an error is returned (NOT NULL constraint violation). Expected Result: The database should return an error, preventing the insertion of a record with a NULL username. Status: Pass/Fail
```
---

## **7. Verify Data Integrity with Foreign Key Constraints**
```
Test Case ID: TC_SQL_007 Title: Verify foreign key constraint enforcement Description: Ensure that a foreign key constraint is enforced, preventing invalid data. Preconditions: The users table should have a foreign key referencing the orders table. Steps to Execute:

Connect to the database.
Attempt to insert a record into the orders table with a non-existent user_id:
INSERT INTO orders (order_id, user_id, order_date)
VALUES (101, 999, '2025-02-27');
Verify that the insert fails due to the non-existent user_id. Expected Result: The database should return an error due to the foreign key constraint violation. Status: Pass/Fail
```
---

## **8. Verify Index Performance**
```
Test Case ID: TC_SQL_008 Title: Verify index performance for SELECT queries Description: Ensure that using an index improves the performance of SELECT queries. Preconditions: The users table should have an index on the email column. Steps to Execute:

Connect to the database.
Measure the execution time of a SELECT query without using the index:
SELECT * FROM users WHERE email = 'user@example.com';
Measure the execution time of the same query after creating an index on the email column:
CREATE INDEX idx_email ON users (email);
Re-run the query and compare the execution times. Expected Result: The query should run faster after creating the index. Status: Pass/Fail
```
---

## Bug Report Format
```
Bug ID: BUG_SQL_001 Title: INSERT query violates UNIQUE constraint Severity: High Steps to Reproduce:

Attempt to insert a record with a duplicate email.
Observe that the query should fail due to a unique constraint violation. Expected Result: The query should fail, preventing insertion of duplicate records. Actual Result: INSERT query executes successfully with duplicate data. Attachments: (Screenshots, logs, or SQL logs)
```
---

## Contribution
If you want to add more test cases, please follow the existing format and create a pull request.

## Contact
For any queries, reach out to **Tanzirul Islam** via [LinkedIn](https://LinkedIn.com/in/tanzirulshafin).

---
