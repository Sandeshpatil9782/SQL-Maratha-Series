# Day 9: CONSTRAINTS (Part 1) - NOT NULL ⚔️ | SQL Swarajya Goshti

## 📜 Concept: नावाशिवाय भरती नाही

वही तयार झाली.

रकाने तयार झाले.

Data Types पण ठरले.

आता प्रश्न आहे...

**नियम कोण पाळणार?**

स्वराज्याच्या दप्तरात प्रत्येक नोंद योग्य असली पाहिजे.

समजा एखादा कारकून अशी नोंद घेऊन आला.

```
नाव : _______

गाव : उमरठे

वय : ३०
```

मुख्य कारकून लगेच विचारेल,

**"नाव कुठे आहे?"**

कारण नावाशिवाय कोणतीही नोंद स्वीकारली जात नव्हती.

त्याचप्रमाणे SQL मध्ये काही Columns कधीही रिकामे राहू शकत नाहीत.

SQL मध्ये या नियमाला **NOT NULL Constraint** म्हणतात.

> **NOT NULL = हा Column रिकामा (NULL) असू शकत नाही. प्रत्येक Row मध्ये Value असलीच पाहिजे.**

---

# 📖 What is a Constraint?

A **Constraint** is a rule applied to a column that controls what kind of data can be stored.

Constraints help to

- Maintain Data Integrity
- Prevent Invalid Data
- Improve Data Quality
- Reduce Human Errors

Think of Constraints as **security rules** for your database.

---

# 📂 Types of SQL Constraints

| Constraint | Purpose |
|------------|----------|
| NOT NULL | Value is Mandatory |
| UNIQUE | No Duplicate Values |
| PRIMARY KEY | Unique Identifier |
| FOREIGN KEY | Connects Tables |
| CHECK | Restricts Values |
| DEFAULT | Assigns Default Value |

> Today we'll learn **NOT NULL**.

---

# 🚫 What is NOT NULL?

The **NOT NULL** Constraint ensures that a column can never contain a NULL value.

Every row must have a value for that column.

---

## Syntax

```sql
column_name DATA_TYPE NOT NULL
```

Example

```sql
nav VARCHAR(100) NOT NULL
```

Meaning

```text
The "nav" column must always contain a value.

Leaving it empty is not allowed.
```

---

# 🤔 What is NULL?

Many beginners confuse **NULL** with

- Zero (0)
- Blank Space (" ")
- Empty String ('')

These are **not the same**.

NULL means

> **No Value Exists**

It represents **missing or unknown data**.

---

## Example

| Value | Is NULL? |
|--------|----------|
| 25 | ❌ |
| 0 | ❌ |
| 'Tanaji' | ❌ |
| '' (Empty String) | ❌ |
| NULL | ✅ |

---

# 🏰 Swarajya Example

Suppose every Mavala must have a name.

```sql
CREATE TABLE Mavale
(
    mavala_id INT,
    nav VARCHAR(100) NOT NULL,
    gaon VARCHAR(100),
    vay INT
);
```

---

## Valid Insert

```sql
INSERT INTO Mavale
VALUES
(
1,
'Tanaji Malusare',
'Umrathe',
35
);
```

Result

```text
✅ Record Inserted Successfully
```

---

## Invalid Insert

```sql
INSERT INTO Mavale
VALUES
(
2,
NULL,
'Raigad',
30
);
```

Result

```text
❌ Error

Column 'nav' cannot be NULL.
```

---

# 💼 Real World Example

Imagine an Employee table.

| Column | NOT NULL? | Reason |
|----------|-----------|---------|
| employee_id | ✅ | Every employee needs an ID |
| employee_name | ✅ | Name is mandatory |
| email | ✅ | Required for communication |
| joining_date | ✅ | Every employee joins on a date |
| middle_name | ❌ | Optional |

---

# 🏦 Banking Example

| Column | NOT NULL |
|----------|----------|
| account_number | ✅ |
| customer_name | ✅ |
| balance | ✅ |
| mobile_number | ✅ |
| nominee_name | ❌ |

---

# 🛒 E-Commerce Example

| Column | NOT NULL |
|----------|----------|
| product_id | ✅ |
| product_name | ✅ |
| price | ✅ |
| stock | ✅ |
| description | ❌ |

---

# 📊 Why NOT NULL is Important?

Without NOT NULL

```
Employee

ID : 101

Name : NULL

Salary : 50000
```

Who is this employee?

Impossible to identify.

NOT NULL prevents incomplete records from entering the database.

---

# 🏰 Complete Swarajya Example

```sql
CREATE DATABASE Swarajya;

USE Swarajya;

CREATE TABLE Mavale
(
    mavala_id INT,
    nav VARCHAR(100) NOT NULL,
    gaon VARCHAR(50),
    vay INT,
    bharti_dinank DATE
);

INSERT INTO Mavale
VALUES
(
1,
'Tanaji Malusare',
'Umrathe',
35,
'1648-05-12'
);

SELECT *
FROM Mavale;
```

---

# ❌ Common Beginner Mistakes

### Leaving Mandatory Columns Empty

Wrong

```sql
INSERT INTO Mavale
VALUES
(
2,
NULL,
'Raigad',
30,
'1650-10-15'
);
```

Correct

```sql
INSERT INTO Mavale
VALUES
(
2,
'Yesaji Kank',
'Raigad',
30,
'1650-10-15'
);
```

---

### Assuming NULL is Same as Empty String

Wrong

```text
NULL = ''
```

Correct

```text
NULL means No Value.

'' means Empty Text.
```

---

### Applying NOT NULL to Optional Columns

Example

```text
Middle Name

Alternate Phone

Remarks
```

These fields are often optional and may not require NOT NULL.

---

# 💡 Best Practices

✅ Apply **NOT NULL** to all mandatory fields.

✅ Use it for IDs, Names, Prices, Dates, Emails, and other essential information.

✅ Avoid using NOT NULL on optional columns.

✅ Plan mandatory fields during database design instead of adding them later.

---

# 🎯 Interview Questions

### 1. What is NOT NULL?

NOT NULL is a constraint that prevents a column from storing NULL values.

---

### 2. What is NULL?

NULL represents a missing or unknown value.

---

### 3. Is NULL the same as 0?

No.

0 is a numeric value.

NULL means no value exists.

---

### 4. Why is NOT NULL important?

It prevents incomplete records and maintains data integrity.

---

### 5. Which columns generally use NOT NULL?

Employee ID, Customer Name, Product Name, Salary, Price, Email, Joining Date, and similar mandatory fields.

---

# 📝 Quick Revision

| Constraint | Purpose |
|------------|----------|
| NOT NULL | Value is Mandatory |
| Allows NULL? | ❌ No |
| Allows Actual Values? | ✅ Yes |
| Used For | Required Columns |

---

# ⚔️ Swarajya Conclusion

**Remember this simple rule:**

📝 **Mandatory Information → NOT NULL**

❌ **No Name = No Entry**

Just as the Swarajya records never accepted an unnamed soldier, a well-designed SQL database should never allow essential information to be missing. Using **NOT NULL** ensures complete, reliable, and high-quality data in every table.