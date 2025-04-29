# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
![image](https://github.com/user-attachments/assets/eea273a3-bdfc-439a-a42d-50224f6d747b)



```sql
SELECT name AS Employee_Name, age AS Age
FROM employee
ORDER BY Age ASc
LIMIT 1;
```

**Output:**

![image](https://github.com/user-attachments/assets/e81b67c7-3587-42cf-8785-9ed2bca88667)


**Question 2**
---
![image](https://github.com/user-attachments/assets/5117d126-c199-4414-8ef9-e36cb1eb643b)


```sql
SELECT name,emaiL,LENGTH(email)AS min_email_length
FROM customer
ORDER BY LENGTH(email) ASC
LIMIT 1;
```

**Output:**
![image](https://github.com/user-attachments/assets/89277f4f-a9de-403a-9c84-2ecfee36c4cd)


**Question 3**
---
![image](https://github.com/user-attachments/assets/425b3b54-ceb3-4731-b049-d0f2ed612e72)


```sql
SELECT address,SUM(salary) 
FROM customer1
GROUP BY address
HAVING SUM(salary)>2000;
```

**Output:**
![image](https://github.com/user-attachments/assets/1339db0a-2850-44ef-a74a-71c8fd08d9fc)


**Question 4**
---
![image](https://github.com/user-attachments/assets/c2b0559d-9ab6-498f-824e-c5d538108710)


```sql
SELECT occupation,MIN(workhour) 
FROM employee1
GROUP BY occupation
HAVING MIN(workhour) > 8;
```

**Output:**

![image](https://github.com/user-attachments/assets/93b9491c-4619-472f-94b5-c9e4a46b4263)


**Question 5**
---


```sql
SELECT category_id,product_name,MAX(Price) AS Price
FROM products
GROUP BY category_id
HAVING MAX(Price)>15;
```

**Output:**

![image](https://github.com/user-attachments/assets/889c7f05-42c3-48df-be68-e63d8e80e843)

**Question 6**
---


```sql

```

**Output:**



**Question 7**
---


```sql

```

**Output:**



**Question 8**
---


```sql

```

**Output:**



**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
