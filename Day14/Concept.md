# Day 14: CONSTRAINT - DEFAULT ⚔️ | SQL Swarajya Goshti

## 📜 Concept: स्व-ओळख

**तुझी किंमत कुणाला माहित नसेल...**  
**पण तुझी ओळख स्वतःचीच असते.**

`PRIMARY KEY` = ओळख  
`FOREIGN KEY` = नातं  
`CHECK` = नियम  
`DEFAULT` = **स्वतः दिलेली ओळख**

स्वराज्यात नवीन मावळा भरती झाला...

जर त्याचा Rank अजून ठरला नसेल,
तर त्याची ओळख **"सिपाही"** अशीच नोंदवली जायची.

त्याची Duty सुरू व्हायची.
पुढे पराक्रमानुसार त्याचा Rank बदलायचा.

Database मध्येही असंच होतं.

जर आपण Value दिली नाही,
तर Database स्वतः Default Value भरते.

यालाच **DEFAULT Constraint** म्हणतात.

---

# 💻 DEFAULT Constraint

## 📖 Definition

`DEFAULT` Constraint म्हणजे Column साठी आधीच एक Value निश्चित करून ठेवणे.

INSERT करताना त्या Column ची Value दिली नाही,
तर Database आपोआप Default Value Store करते.

---

## 📌 Rule

- Value दिली नाही तर Default Value Store होते.
- Value दिली तर Default वापरला जात नाही.
- NULL आणि DEFAULT वेगळे आहेत.
- Data ला Meaningful Initial Value मिळते.

---

## 💻 SQL Syntax

```sql
CREATE TABLE Mavale (

    mavla_id INT PRIMARY KEY,

    nav VARCHAR(100),

    rank VARCHAR(20)
    DEFAULT 'Sipahi',

    status VARCHAR(20)
    DEFAULT 'Active',

    joining_date DATE
    DEFAULT CURRENT_DATE

);
```

---

## ✅ Insert Without DEFAULT Values

```sql
INSERT INTO Mavale
(mavla_id, nav)

VALUES
(1,'Tanaji');
```

### Output

| ID | Name | Rank | Status | Joining Date |
|---:|------|-------|---------|--------------|
|1|Tanaji|Sipahi|Active|Current Date|

Database ने Missing Values स्वतः भरल्या.

---

## ✅ Insert With Custom Values

```sql
INSERT INTO Mavale

VALUES
(
2,
'Yesaji',
'Sardar',
'Active',
'2025-01-15'
);
```

### Output

| ID | Name | Rank | Status | Joining Date |
|---:|------|--------|---------|--------------|
|2|Yesaji|Sardar|Active|2025-01-15|

Database Default वापरत नाही.

---

# 📊 Without DEFAULT

| Name | Rank |
|------|------|
|Tanaji|NULL|

👉 माहिती अपूर्ण राहते.

---

# ✅ With DEFAULT

| Name | Rank |
|------|---------|
|Tanaji|Sipahi|

👉 Database स्वतः योग्य Value भरते.

---

# 💼 Real World Business Use Cases

### Employee

```sql
status VARCHAR(20)
DEFAULT 'Active'
```

---

### Student Portal

```sql
admission_status VARCHAR(20)
DEFAULT 'Pending'
```

---

### User Registration

```sql
role VARCHAR(20)
DEFAULT 'User'
```

---

## ⚙️ Why DEFAULT is Important?

### 1️⃣ Reduces Manual Data Entry

प्रत्येक वेळी समान Value लिहिण्याची गरज राहत नाही.

---

### 2️⃣ Maintains Consistency

सर्व नवीन Records एकाच Default Value ने सुरू होतात.

---

### 3️⃣ Prevents Unnecessary NULL Values

रिकाम्या जागा कमी होतात.

---

### 4️⃣ Saves Time

Repeated Values आपोआप भरल्या जातात.

---


## 🚀 Industry Perspective

Enterprise Applications मध्ये DEFAULT खूप मोठ्या प्रमाणावर वापरला जातो.

- User Status
- Order Status
- Payment Status
- Employee Role
- Created Date
- Registration Date
- Active Flag

यामुळे प्रत्येक Record ला सुरुवातीपासूनच योग्य Initial Value मिळते.

---

## 🧠 Quick Revision

- ✅ Auto Value
- ✅ Used During INSERT
- ✅ Prevents NULL
- ✅ Saves Time
- ✅ Improves Consistency
- ✅ Supports Functions like CURRENT_DATE

---

## ⚔️ SQL Swarajya Rule

> **"दुसऱ्यांनी तुझी ओळख दिली नाही...**
> **तरी तुझी ओळख हरवत नाही."**

**SQL मध्ये:**

> **"Value दिली नाही...**
> **तर DEFAULT स्वतःची ओळख निर्माण करतो."**