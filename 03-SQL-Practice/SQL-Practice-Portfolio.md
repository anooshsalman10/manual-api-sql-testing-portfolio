# SQL Practice Portfolio

## Overview

This document records SQL query practice using a sample SQLite database. The exercises demonstrate retrieving, filtering, sorting, joining, grouping, and aggregating data from related tables.

**Environment:** SQLite online playground  
**Database tables:** `users`, `orders`  
**Practice exercises:** 10  
**Status:** All 10 queries executed successfully

> This is a self-directed learning project using sample data. It is not professional database-testing experience or testing of a production database.

## Sample Database

### `users` table

| id | name | city |
|---:|---|---|
| 1 | Ali | Lahore |
| 2 | Sara | Karachi |
| 3 | Ahmed | Lahore |
| 4 | Zoya | Islamabad |
| 5 | Hamza | Karachi |

### `orders` table

| order_id | user_id | amount |
|---:|---:|---:|
| 101 | 1 | 1200 |
| 102 | 2 | 2500 |
| 103 | 1 | 800 |
| 104 | 3 | 1800 |
| 105 | 5 | 3000 |

The `users.id` column identifies a user. The `orders.user_id` column associates an order with a user.

## SQL Exercises

### SQL-TC-01: Retrieve all users

**Objective:** Verify that all records can be retrieved from the `users` table.

**Query:**

```sql
SELECT * FROM users;
```

**Expected result:** All five users and their `id`, `name`, and `city` values.

**Actual result:** 5 rows returned.

**Status:** PASS

---

### SQL-TC-02: Filter users by Lahore

**Objective:** Retrieve only users whose city is Lahore.

**Query:**

```sql
SELECT * FROM users
WHERE city = 'Lahore';
```

**Expected result:** Ali and Ahmed.

**Actual result:** 2 rows returned: Ali (ID 1) and Ahmed (ID 3).

**Status:** PASS

---

### SQL-TC-03: Filter users by Karachi

**Objective:** Retrieve only users whose city is Karachi.

**Query:**

```sql
SELECT * FROM users
WHERE city = 'Karachi';
```

**Expected result:** Sara and Hamza.

**Actual result:** 2 rows returned: Sara (ID 2) and Hamza (ID 5).

**Status:** PASS

---

### SQL-TC-04: Sort users alphabetically

**Objective:** Retrieve all users sorted by name in ascending alphabetical order.

**Query:**

```sql
SELECT * FROM users
ORDER BY name ASC;
```

**Expected result:** Users sorted A–Z by name.

**Actual result:** Ahmed, Ali, Hamza, Sara, Zoya; 5 rows returned.

**Status:** PASS

---

### SQL-TC-05: Filter orders above 1500

**Objective:** Retrieve orders whose amount is greater than 1500.

**Query:**

```sql
SELECT * FROM orders
WHERE amount > 1500;
```

**Expected result:** Orders 102, 104, and 105.

**Actual result:** 3 rows returned with amounts 2500, 1800, and 3000.

**Status:** PASS

---

### SQL-TC-06: Sort orders by amount descending

**Objective:** Retrieve all orders from highest amount to lowest amount.

**Query:**

```sql
SELECT * FROM orders
ORDER BY amount DESC;
```

**Expected result:** Amounts sorted from highest to lowest.

**Actual result:** 3000, 2500, 1800, 1200, 800; 5 rows returned.

**Status:** PASS

---

### SQL-TC-07: Join users and orders

**Objective:** Display each customer's name alongside each matching order amount.

**Query:**

```sql
SELECT users.name, orders.amount
FROM users
INNER JOIN orders
ON users.id = orders.user_id;
```

**Expected result:** Each order is shown with the name of the matching user.

**Actual result:** 5 rows returned. Ali appears twice because Ali has two orders.

**Status:** PASS

---

### SQL-TC-08: Join tables and filter orders

**Objective:** Display customer names and order amounts only for orders above 1500.

**Query:**

```sql
SELECT users.name, orders.amount
FROM users
INNER JOIN orders
ON users.id = orders.user_id
WHERE orders.amount > 1500;
```

**Expected result:** Sara (2500), Ahmed (1800), and Hamza (3000).

**Actual result:** 3 rows returned with the expected names and amounts.

**Status:** PASS

---

### SQL-TC-09: Count users in each city

**Objective:** Count the number of users in each city.

**Query:**

```sql
SELECT city, COUNT(*) AS total_users
FROM users
GROUP BY city;
```

**Expected result:** One row per city, showing the number of users there.

**Actual result:**

| city | total_users |
|---|---:|
| Islamabad | 1 |
| Karachi | 2 |
| Lahore | 2 |

**Status:** PASS

---

### SQL-TC-10: Calculate each customer's total order amount

**Objective:** Calculate the total value of orders for each user who has at least one order.

**Query:**

```sql
SELECT users.name, SUM(orders.amount) AS total_amount
FROM users
INNER JOIN orders
ON users.id = orders.user_id
GROUP BY users.id, users.name;
```

**Expected result:** One row per customer with matching orders, with their order amounts added together.

**Actual result:**

| name | total_amount |
|---|---:|
| Ali | 2000 |
| Sara | 2500 |
| Ahmed | 1800 |
| Hamza | 3000 |

Ali's total is 2000 (1200 + 800). Zoya is not included because she has no matching order and this query uses `INNER JOIN`.

**Status:** PASS

---

## Execution Summary

| Metric | Result |
|---|---:|
| Total exercises | 10 |
| Passed | 10 |
| Failed | 0 |

## Skills Practiced

- Selecting data from tables with `SELECT`
- Filtering rows with `WHERE`
- Sorting results with `ORDER BY ASC` and `ORDER BY DESC`
- Joining related tables with `INNER JOIN`
- Counting records with `COUNT()`
- Grouping records with `GROUP BY`
- Calculating totals with `SUM()`
- Comparing actual query results with expected results

## Notes

- The exercises use sample data created for learning purposes.
- The queries were executed in an online SQLite playground.
- Results reflect the sample database and are not claims about a live or production system.
