# Day 8: DATA TYPES (Part 2) ⚔️ | SQL Swarajya Goshti

## 📜 Concept: कालगणना आणि निर्णय

हिशोब झाला.

नावं झाली.

आता उरली दोन महत्त्वाच्या गोष्टी —

**वेळ** आणि **निर्णय**.

स्वराज्य चालवताना प्रत्येक गोष्ट योग्य वेळी नोंदवली जायची.

- किल्ला कधी जिंकला?
- मावळा कधी भरती झाला?
- सभा कधी झाली?
- हल्ला कोणत्या वेळी झाला?

यासोबतच काही गोष्टींचं उत्तर फक्त दोनच असायचं.

- किल्ला आपल्या ताब्यात आहे का?
- मावळा जिवंत आहे का?
- कर भरला आहे का?
- मोहीम पूर्ण झाली का?

SQL मध्ये यासाठी विशेष Data Types आहेत.

- **DATE**
- **DATETIME**
- **BOOLEAN**

> **Date Types = वेळ आणि तारीख साठवण्यासाठी**
>
> **Boolean = होय किंवा नाही साठवण्यासाठी**

---

# 📖 Why Date & Boolean Data Types?

Imagine a database without dates.

You would never know

- When an employee joined.
- When an order was placed.
- When a payment was received.
- When a project started.

Similarly, without Boolean values,

You cannot easily know

- Is customer active?
- Is payment completed?
- Is product available?
- Is employee working?

These Data Types make databases more meaningful and efficient.

---

# 📅 DATE DATA TYPE

The **DATE** Data Type stores only the calendar date.

It does **not** store time.

### Syntax

```sql

column_name DATE
```

### Format

```text
YYYY-MM-DD
```

Example

```text
2026-07-15
```

---

### Valid Examples

```text
2025-01-26

2024-12-31

1670-02-04
```

---

### Invalid Examples

```text
26-01-2025

01/01/2024

2024/12/31
```

SQL expects

```text
YYYY-MM-DD
```

---

## Swarajya Example

| Column | Example |
|----------|----------|
| janma_tarikh | 1630-02-19 |
| bharti_dinank | 1648-06-12 |
| killa_jinkla | 1670-02-04 |

---

## Real World Example

| Column | Data Type |
|----------|-----------|
| date_of_birth | DATE |
| joining_date | DATE |
| order_date | DATE |
| invoice_date | DATE |

---

# 🕒 DATETIME DATA TYPE

DATETIME stores both

- Date
- Time

### Syntax

```sql
column_name DATETIME
```

### Format

```text
YYYY-MM-DD HH:MM:SS
```

Example

```text
2026-07-15 09:45:30
```

---

### Swarajya Example

| Column | Example |
|----------|----------|
| hallachi_vel | 1670-02-04 04:30:00 |
| baithak_vel | 1674-06-06 08:00:00 |
| rajyabhishek_vel | 1674-06-06 05:15:00 |

---

### Real World Example

| Column | Data Type |
|----------|-----------|
| login_time | DATETIME |
| order_timestamp | DATETIME |
| payment_time | DATETIME |
| created_at | DATETIME |

---

# 📅 DATE vs DATETIME

| Feature | DATE | DATETIME |
|----------|------|-----------|
| Stores Date | ✅ | ✅ |
| Stores Time | ❌ | ✅ |
| Format | YYYY-MM-DD | YYYY-MM-DD HH:MM:SS |
| Best For | Birth Date, Joining Date | Login, Orders, Payments |

---

# ✅ BOOLEAN DATA TYPE

BOOLEAN stores only two values.

```text
TRUE

FALSE
```

Internally SQL stores them as

```text
1 = TRUE

0 = FALSE
```

---

### Syntax

```sql
column_name BOOLEAN
```

---

## Swarajya Example

| Column | Value |
|----------|--------|
| jivanta_ahe | TRUE |
| killa_swatacha_ahe | TRUE |
| mohim_purn | FALSE |

---

## Real World Example

| Column | Meaning |
|----------|---------|
| is_active | Employee Active? |
| payment_done | Payment Completed? |
| email_verified | Email Verified? |
| stock_available | Product Available? |

---

# TRUE vs FALSE

| Value | Meaning |
|---------|----------|
| TRUE | Yes |
| FALSE | No |
| 1 | TRUE |
| 0 | FALSE |

---

# 🏰 Complete Swarajya Example

```sql
CREATE DATABASE Swarajya;

USE Swarajya;

CREATE TABLE Mohim
(
    mohim_id INT,
    mohim_nav VARCHAR(100),
    bharti_dinank DATE,
    hallachi_vel DATETIME,
    jivanta_ahe BOOLEAN,
    killa_swatacha_ahe BOOLEAN
);
```

Insert Data

```sql
INSERT INTO Mohim
VALUES
(
1,
'Tanaji Malusare',
'1648-05-12',
'1670-02-04 04:30:00',
TRUE,
TRUE
),

(
2,
'Baji Prabhu',
'1646-08-15',
'1660-07-13 09:15:00',
FALSE,
TRUE
),

(
3,
'Yesaji Kank',
'1650-10-20',
'1671-03-18 06:45:00',
TRUE,
FALSE
);
```

View Data

```sql
SELECT *
FROM Mohim;
```

---

# 💼 Enterprise Example

Imagine an Employee table.

| Column | Data Type | Reason |
|----------|-----------|---------|
| employee_id | INT | Employee ID |
| employee_name | VARCHAR(100) | Name |
| joining_date | DATE | Date of Joining |
| last_login | DATETIME | Login Date & Time |
| is_active | BOOLEAN | Active Employee |

---

# ❌ Common Beginner Mistakes

### Wrong Date Format

```sql
'26-01-2025'
```

Correct

```sql
'2025-01-26'
```

---

### Using VARCHAR for Dates

Wrong

```sql
joining_date VARCHAR(20)
```

Correct

```sql
joining_date DATE
```

---

### Using VARCHAR for TRUE/FALSE

Wrong

```sql
payment_done VARCHAR(10)
```

Correct

```sql
payment_done BOOLEAN
```

---

### Using DATE when Time is Required

Wrong

```sql
login_time DATE
```

Correct

```sql
login_time DATETIME
```

---

# 💡 Best Practices

✅ Use **DATE** when only the calendar date is required.

✅ Use **DATETIME** when both date and time are important.

✅ Use **BOOLEAN** for Yes/No, Active/Inactive, True/False values.

✅ Never store dates as VARCHAR.

✅ Always follow the `YYYY-MM-DD` format.

---

# 🎯 Interview Questions

### 1. What is the DATE Data Type?

DATE stores only the calendar date in the format `YYYY-MM-DD`.

---

### 2. Difference between DATE and DATETIME?

- DATE stores only the date.
- DATETIME stores both date and time.

---

### 3. What is BOOLEAN?

BOOLEAN stores logical values like TRUE/FALSE or 1/0.

---

### 4. Why shouldn't dates be stored as VARCHAR?

Because SQL cannot efficiently sort, compare, or perform date calculations on text values.

---

### 5. Where is BOOLEAN commonly used?

BOOLEAN is commonly used for Active/Inactive status, Payment Completed, Email Verified, Product Availability, and similar Yes/No conditions.

---

# 📝 Quick Revision

| Data Type | Stores | Example |
|-----------|---------|----------|
| DATE | Calendar Date | 2026-07-15 |
| DATETIME | Date + Time | 2026-07-15 09:30:00 |
| BOOLEAN | TRUE/FALSE | 1, 0 |

---

# ⚔️ Swarajya Conclusion

**Remember this simple rule:**

📅 **DATE → Only Date**

🕒 **DATETIME → Date + Time**

✅ **BOOLEAN → Yes / No (TRUE / FALSE)**

Choosing the correct Date and Boolean Data Types makes databases more accurate, efficient, and easier to query. These are widely used in enterprise applications such as HR systems, banking, e-commerce, healthcare, and inventory management.