# Day 13: CONSTRAINT - CHECK ⚔️ | SQL Swarajya Goshti

## 📜 Concept: 2 Step Gatekeeper

 नियमाच्या बाहेर जायचं नाही.  
 नियम तोडला तर प्रवेश नाही.

`PRIMARY KEY` = ओळख दिली.  
`FOREIGN KEY` = नातं जोडलं.  
`CHECK` = **दारावर उभा राहून प्रत्येक नियम तपासतो.**

स्वराज्यात प्रत्येकाला किल्ल्यावर प्रवेश नव्हता.

किल्ल्याच्या दरवाज्यावर दोन नियम कायम होते.

✅ योग्य परवानगी असावी.
✅ राजाचे आदेश असावेत.

दोन्ही अटी पूर्ण झाल्या,
तरच दरवाजा उघडला जायचा.

SQL मध्येही Database हेच काम `CHECK` Constraint वापरून करते.

---

# 💻 CHECK Constraint

## 📖 Definition

`CHECK` Constraint एखाद्या Column मधील Value ठरवलेल्या Condition नुसारच स्वीकारते.

जर Value त्या Condition ला पूर्ण करत नसेल, तर Database Record Insert किंवा Update होऊ देत नाही.

---

## 📌 Rule

- प्रत्येक Value दिलेल्या Condition ला Match झाली पाहिजे.
- Condition False झाली तर Error येतो.
- Invalid Data Database मध्ये जाण्यापासून थांबवते.
- Data Quality सुधारते.

---

## ⚔️ Swarajya Example

किल्ल्यावर भरतीसाठी नियम.

| नाव | वय | पगार | प्रवेश |
|------|----:|------:|--------|
| Tanaji | 28 | 5000 | ✅ |
| Yesaji | 19 | 3500 | ✅ |
| Raghu | 16 | 5000 | ❌ |
| Bapu | 24 | 0 | ❌ |

Gatekeeper दोन्ही नियम तपासतो.

---

# 💻 SQL Syntax

```sql
CREATE TABLE Mavale (

    mavla_id INT PRIMARY KEY,

    nav VARCHAR(100),

    vay INT CHECK (vay >= 18),

    pagar DECIMAL(10,2)
    CHECK (pagar > 0)

);
```

---

## ✅ Valid Insert

```sql
INSERT INTO Mavale
VALUES
(1,'Tanaji',28,5000),
(2,'Yesaji',22,6500),
(3,'Baji Prabhu',30,8000);
```

Database हे Records स्वीकारेल.

---

## ❌ Invalid Insert

### Age Rule Failed

```sql
INSERT INTO Mavale
VALUES
(4,'Raghu',16,5000);
```

### Output

```text
Error:
CHECK constraint failed
```

---

### Salary Rule Failed

```sql
INSERT INTO Mavale
VALUES
(5,'Bapu',24,0);
```

### Output

```text
Error:
CHECK constraint failed
```

---

# 📊 Without CHECK

| Name | Age | Salary |
|------|----:|-------:|
| Tanaji | 15 | 5000 |
| Yesaji | 22 | 0 |

👉 चुकीचा Data Database मध्ये जाईल.

---

# ✅ With CHECK

| Name | Age | Salary |
|------|----:|-------:|
| Tanaji | 28 | 5000 |
| Yesaji | 22 | 6000 |

👉 फक्त Valid Data Store होतो.

---

# 💼 Real World Business Use Cases

### Employee

```sql
age INT CHECK (age >= 18)
```

18 वर्षांखालील Employee स्वीकारला जाणार नाही.

---

### Banking

```sql
balance DECIMAL
CHECK (balance >= 0)
```

Negative Balance रोखण्यासाठी.

---

### E-Commerce

```sql
price DECIMAL
CHECK (price > 0)
```

Product ची Price शून्य किंवा Negative असू शकत नाही.

---

### Student

```sql
marks INT
CHECK (marks BETWEEN 0 AND 100)
```

Marks फक्त 0 ते 100 दरम्यानच असतील.

---

## ⚙️ Why CHECK is Important?

### 1️⃣ Prevents Invalid Data

चुकीचा Data Database मध्ये जाऊ देत नाही.

---

### 2️⃣ Enforces Business Rules

Business चे Rules Database Level वर लागू करते.

---

### 3️⃣ Improves Data Quality

फक्त योग्य आणि विश्वासार्ह Data Store होतो.

---

### 4️⃣ Reduces Application Errors

Application वर Validation कमी करावी लागते.

---


# 🚀 Industry Perspective

Enterprise Databases मध्ये CHECK Constraints मोठ्या प्रमाणावर वापरले जातात.

- Employee Age
- Product Price
- Order Quantity
- Salary
- Discount Percentage
- Exam Marks
- Account Balance

यामुळे Invalid Data Database मध्ये जाण्यापूर्वीच थांबतो.

---

## 🧠 Quick Revision

- ✅ Validates Data
- ✅ Uses Conditions
- ✅ Prevents Invalid Values
- ✅ Enforces Business Rules
- ✅ Improves Data Quality
- ✅ Runs During INSERT & UPDATE

---

## ⚔️ SQL Swarajya Rule

> **"किल्ल्याच्या दरवाज्यावर नियम मोडणाऱ्याला प्रवेश नाही..."**

**SQL मध्ये:**

> **"CHECK म्हणजे Database चा Gatekeeper...**
> **नियम पूर्ण केले तरच Data आत येतो."**