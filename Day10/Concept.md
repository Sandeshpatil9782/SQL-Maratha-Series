# Day 10: CONSTRAINT - UNIQUE ⚔️ | SQL Swarajya Goshti

## 📜 Concept: नकल करू नकोस

`NOT NULL` ने सांगितलं - नाव पाहिजेच.  
`UNIQUE` सांगतं - ते नाव फक्त तुझंच पाहिजे.

रायगड एकदाच आहे. प्रतापगड एकदाच आहे.  
जर दुसऱ्या किल्ल्याला पण **"रायगड"** नाव दिलं, तर शिपाई कुठे जाणार? कोणता किल्ला जिंकायचा?

म्हणून शिवरायांनी प्रत्येक किल्ल्याला, प्रत्येक मावळ्याला वेगळी ओळख दिली.

SQL मध्ये यालाच **`UNIQUE` Constraint** म्हणतात.

**Copy-Paste ला बंदी. प्रत्येक ओळख वेगळीच!**

---

# 💻 UNIQUE Constraint

## 📖 Definition

`UNIQUE` Constraint एखाद्या Column मधील प्रत्येक Value वेगळी (Unique) असल्याची खात्री करते.

जर तीच Value पुन्हा Insert करण्याचा प्रयत्न केला, तर SQL Error देते आणि Duplicate Data स्वीकारत नाही.

---

## 📌 Rule

- एका Column मध्ये Duplicate Values चालत नाहीत.
- प्रत्येक Value Unique असावी.
- Data Integrity टिकवण्यासाठी वापरतात.
- एका Table मध्ये एकापेक्षा जास्त `UNIQUE` Constraints असू शकतात.

---

## ⚔️ Swarajya Example

प्रत्येक किल्ल्याचं नाव वेगळं.

❌ हे चुकीचं:

| Killa |
|--------|
| Raigad |
| Raigad |

कारण दोन किल्ल्यांना एकच नाव असू शकत नाही.

✅ योग्य:

| Killa |
|--------|
| Raigad |
| Pratapgad |
| Sinhagad |
| Torna |

---

## 💻 SQL Syntax

```sql
CREATE TABLE Kille (
    id INT PRIMARY KEY,
    killa_nav VARCHAR(100) UNIQUE
);
```

---

## 💻 Insert Example

### ✅ Valid

```sql
INSERT INTO Kille
VALUES
(1,'Raigad'),
(2,'Pratapgad'),
(3,'Sinhagad');
```

---

### ❌ Invalid

```sql
INSERT INTO Kille
VALUES
(4,'Raigad');
```

### Output

```text
Error:
Duplicate entry 'Raigad'
for key 'killa_nav'
```

---

# 📊 Before UNIQUE

| ID | Killa |
|----|--------|
|1|Raigad|
|2|Raigad|
|3|Raigad|

👉 Duplicate Data

---

# ✅ After UNIQUE

| ID | Killa |
|----|----------|
|1|Raigad|
|2|Pratapgad|
|3|Sinhagad|

👉 प्रत्येक Value Unique

---

# 💼 Real World Business Use Cases

### Employee Table

```sql
email VARCHAR(100) UNIQUE
```

दोन Employees चा Email एकसारखा असू शकत नाही.

---

### Banking

```sql
account_number VARCHAR(20) UNIQUE
```

प्रत्येक Account Number Unique असतो.

---

### E-Commerce

```sql
product_code VARCHAR(50) UNIQUE
```

प्रत्येक Product ला वेगळा Code असतो.

---

### College

```sql
roll_no INT UNIQUE
```

एका विद्यार्थ्याचा Roll Number दुसऱ्याला देता येत नाही.

---

## 🎯 Interview Question

**Q. Difference between PRIMARY KEY and UNIQUE?**

| PRIMARY KEY | UNIQUE |
|-------------|---------|
|Duplicate नाही|Duplicate नाही|
|NULL Allowed नाही|NULL Allowed (DBMS वर अवलंबून)|
|Table मध्ये फक्त 1|एकापेक्षा जास्त UNIQUE असू शकतात|

---

## 🚀 Why UNIQUE is Important?

- Duplicate Records टाळते.
- Data Quality सुधारते.
- Business Rules enforce करते.
- Reliable Reports तयार होतात.
- चुकीचा Data Insert होण्यापासून संरक्षण करते.

---

## 🧠 Quick Revision

- ✅ Duplicate Values Allowed? → **No**
- ✅ Data Integrity? → **Yes**
- ✅ Multiple UNIQUE Constraints? → **Yes**
- ✅ Common Use → Email, Username, Mobile Number, Product Code, Account Number

---

## ⚔️ SQL Swarajya Rule

> **"प्रत्येक किल्ला वेगळा... प्रत्येक ओळख वेगळी...**
> **म्हणूनच Swarajya मजबूत."**

**SQL मध्ये:**

> **"प्रत्येक Value Unique...**
> **म्हणून Database विश्वासार्ह."**