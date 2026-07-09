# Day 7: DATA TYPES (Part 1) ⚔️ | SQL Swarajya Goshti

## 📜 Concept: शाई आणि शस्त्र

वही तयार झाली (`Table`).

रकाने तयार झाले (`Columns`).

पण प्रत्येक रकान्यात कोणत्या प्रकारचा डेटा ठेवायचा?

छत्रपती शिवाजी महाराजांच्या दप्तरात दोन प्रकारचे कारकून होते.

- **हिशोबाचे कारकून** → खजिना, कर, सैन्य, खर्च (Numbers)
- **नाव लिहिणारे कारकून** → मावळे, गावे, किल्ले (Text)

जर खजिन्यात नाव लिहिलं तर हिशोब होणार नाही.

जर नावाच्या जागी आकडा लिहिला तर इतिहास समजणार नाही.

म्हणून प्रत्येक रकान्याचा नियम असतो.

SQL मध्ये यालाच **Data Type** म्हणतात.

> **Data Type = एका Column मध्ये कोणत्या प्रकारचा डेटा ठेवायचा याचा नियम.**

---

# 📖 What is a Data Type?

A **Data Type** tells SQL what kind of value a column can store.

It helps SQL to:

- Store data correctly
- Perform calculations
- Save memory
- Improve performance
- Prevent invalid data

Without Data Types, SQL cannot determine whether a value is a number, text, date, or something else.

---

# 📂 Categories of Data Types

SQL provides several categories of Data Types.

| Category | Purpose |
|-----------|----------|
| Numeric | Numbers |
| String | Text |
| Date & Time | Dates and Time |
| Boolean | True / False |
| Binary | Images, Files |

> In this part, we'll focus only on **Numeric** and **String** Data Types.

---

# 🔢 NUMERIC DATA TYPES

Numeric Data Types store numbers.

These values can be used in mathematical operations like:

- Addition
- Subtraction
- Multiplication
- Division
- SUM()
- AVG()
- MIN()
- MAX()

---

## 1️⃣ INT (Integer)

Stores **Whole Numbers** only.

No decimal values are allowed.

### Syntax

```sql
column_name INT
```

### Example

```sql
age INT
```

### Valid Values

```text
25
100
5000
-12
```

### Invalid Values

```text
25.5
100.75
```

### Swarajya Example

| Column | Example |
|----------|----------|
| vay | 28 |
| sainik_sankhya | 4500 |
| topa | 15 |

### Real World Example

| Column | Data Type |
|----------|-----------|
| employee_id | INT |
| customer_id | INT |
| quantity | INT |
| age | INT |

---

## 2️⃣ DECIMAL

Stores decimal (exact) numbers.

Used mainly for money and financial values.

### Syntax

```sql
DECIMAL(total_digits, decimal_places)
```

Example

```sql
DECIMAL(10,2)
```

Meaning

```text
Total Digits = 10

Digits after Decimal = 2

Digits before Decimal = 8
```

### Valid Values

```text
5000.50

120.75

99999999.99
```

### Invalid Value

```text
123456789.99
```

Too many digits.

### Swarajya Example

| Column | Example |
|----------|----------|
| khajina | 2500000.50 |
| dakshina | 1500.75 |
| kar | 500.25 |

### Real World Example

| Column | Data Type |
|----------|-----------|
| salary | DECIMAL(10,2) |
| product_price | DECIMAL(10,2) |
| tax | DECIMAL(6,2) |
| balance | DECIMAL(15,2) |

---

# 🔤 STRING DATA TYPES

String Data Types store text.

Examples

- Names
- Villages
- Cities
- Emails
- Addresses
- Descriptions
- Product Names

Mathematical operations cannot be performed on String values.

---

## 3️⃣ VARCHAR

Variable Length Character.

Stores only the required number of characters.

### Syntax

```sql
VARCHAR(length)
```

Example

```sql
VARCHAR(100)
```

Maximum 100 characters allowed.

### Swarajya Example

| Column | Example |
|----------|----------|
| nav | Tanaji Malusare |
| gaon | Umrathe |
| killa | Raigad |

### Real World Example

| Column | Data Type |
|----------|-----------|
| employee_name | VARCHAR(100) |
| email | VARCHAR(150) |
| city | VARCHAR(50) |
| company_name | VARCHAR(200) |

---

## 4️⃣ CHAR

Fixed Length Character.

Always reserves the specified number of characters.

### Syntax

```sql
CHAR(10)
```

If stored value is

```text
ABC
```

SQL internally reserves

```text
ABC_______
```

Remaining spaces are padded automatically.

### Swarajya Example

| Column | Example |
|----------|----------|
| killa_code | RGD0000001 |
| sainik_code | MVL0000123 |

### Real World Example

| Column | Data Type |
|----------|-----------|
| country_code | CHAR(2) |
| gender | CHAR(1) |
| state_code | CHAR(3) |
| employee_code | CHAR(8) |

---

# ⚔️ VARCHAR vs CHAR

Suppose the value is

```text
Tanaji
```

Length = 6

### VARCHAR(100)

Stores only

```text
Tanaji
```

Memory Used

```text
6 Characters
```

---

### CHAR(100)

Stores

```text
Tanaji______________________________________
```

Memory Reserved

```text
100 Characters
```

---

## Comparison

| Feature | VARCHAR | CHAR |
|-----------|----------|------|
| Length | Variable | Fixed |
| Memory | Uses Required Space | Always Reserves Full Space |
| Storage | Efficient | Wastes Space |
| Best For | Names, Email, Address | Codes, Gender, PIN |

---

# 🏰 Complete Swarajya Example

```sql
CREATE DATABASE Swarajya;

USE Swarajya;

CREATE TABLE Mavale
(
    mavala_id INT,
    nav VARCHAR(100),
    gaon VARCHAR(50),
    vay INT,
    killa_code CHAR(10),
    khajina DECIMAL(12,2)
);

INSERT INTO Mavale
VALUES
(1,'Tanaji Malusare','Umrathe',35,'RGD0000001',25000.50),
(2,'Baji Prabhu','Hirdas Maval',32,'PNH0000002',18500.75),
(3,'Yesaji Kank','Raigad',29,'SGD0000003',12000.25);

SELECT *
FROM Mavale;
```

---

# 💼 Enterprise Example

Imagine an Employee table.

| Column | Data Type | Reason |
|----------|-----------|---------|
| employee_id | INT | Numeric ID |
| employee_name | VARCHAR(100) | Variable Length Name |
| salary | DECIMAL(10,2) | Accurate Salary |
| department_code | CHAR(5) | Fixed Code |

---

# ❌ Common Beginner Mistakes

### Wrong

```sql
age VARCHAR(10)
```

Correct

```sql
age INT
```

---

### Wrong

```sql
salary INT
```

Correct

```sql
salary DECIMAL(10,2)
```

---

### Wrong

```sql
name CHAR(100)
```

Correct

```sql
name VARCHAR(100)
```

---

# 💡 Best Practices

✅ Use **INT** for IDs, Age, Quantity, Count.

✅ Use **DECIMAL** for Salary, Price, Tax, Money.

✅ Use **VARCHAR** for Names, Email, Address, City.

✅ Use **CHAR** only for fixed-length values like Codes, Gender, Country Code.

---

# 🎯 Interview Questions

### 1. What is a Data Type?

A Data Type defines the kind of values that a column can store.

---

### 2. Difference between INT and DECIMAL?

- INT stores whole numbers.
- DECIMAL stores numbers with decimal precision.

---

### 3. Difference between VARCHAR and CHAR?

- VARCHAR stores variable-length text.
- CHAR stores fixed-length text.

---

### 4. Why is DECIMAL used for salary?

Because salary requires exact precision and should not lose decimal values.

---

### 5. Why should names use VARCHAR?

Because names have different lengths, so VARCHAR saves storage.

---

# 📝 Quick Revision

| Data Type | Stores | Example |
|-----------|---------|----------|
| INT | Whole Numbers | Age, Quantity |
| DECIMAL | Decimal Numbers | Salary, Price |
| VARCHAR | Variable Text | Name, Email |
| CHAR | Fixed Text | Employee Code |

---

# ⚔️ Swarajya Conclusion

**Remember this simple rule:**

- 🔢 **Numbers → Numeric Data Types**
- 🔤 **Text → String Data Types**

Choosing the correct Data Type improves performance, reduces storage usage, prevents errors, and is considered a fundamental SQL best practice used in real-world databases.