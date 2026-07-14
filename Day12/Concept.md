# Day 12: CONSTRAINT - FOREIGN KEY ⚔️ | SQL Swarajya Goshti

## 📜 Concept: नातं जोडताना विचार करून जोडा

कारण ह्याच नात्यावर सगळं अवलंबून असतं.

`PRIMARY KEY` ने दिली ओळख.  
`FOREIGN KEY` मागतो जबाबदारी.

स्वराज्यात एक मावळा कधीच एकटा नव्हता.

तो **रायगड** चा होता.
तो **तानाजी** च्या हाताखाली होता.
तो एका मोहिमेचा भाग होता.

ते नातं तुटलं...
तर सैन्य विस्कळीत होतं.

Database मध्येही तसंच आहे.

`Mavale` Table ला `Kille` Table शी जोडावं लागतं.

पण ते नातं खोटं असेल...
तर Database चुकीचा इतिहास लिहायला लागतो.

म्हणूनच SQL मध्ये **FOREIGN KEY** वापरली जाते.

---

# 💻 FOREIGN KEY

## 📖 Definition

`FOREIGN KEY` हा असा Constraint आहे जो एका Table मधील Column ला दुसऱ्या Table च्या `PRIMARY KEY` शी जोडतो.

यामुळे दोन्ही Tables मधील Relationship सुरक्षित राहते.

Database खात्री करते की Parent Table मध्ये Record असेल, तरच Child Table मध्ये त्याचा Reference देता येईल.

---

## 📌 Rule

- FOREIGN KEY नेहमी दुसऱ्या Table च्या `PRIMARY KEY` (किंवा UNIQUE Key) ला Reference करते.
- Parent Record अस्तित्वात नसल्यास Child Record Insert करता येत नाही.
- Referential Integrity टिकवते.
- चुकीचे References तयार होऊ देत नाही.

---

## ⚔️ Swarajya Example

### 🏰 Parent Table - Kille

| killa_id | Killa |
|----------:|--------|
|1|Raigad|
|2|Pratapgad|
|3|Sinhagad|

---

### ⚔️ Child Table - Mavale

| mavla_id | Name | killa_id |
|----------:|------|----------:|
|101|Tanaji|3|
|102|Yesaji|1|
|103|Baji Prabhu|2|

प्रत्येक मावळा एखाद्या किल्ल्याशी जोडलेला आहे.

हेच नातं FOREIGN KEY जपते.

---

# 💻 SQL Syntax

## Parent Table

```sql
CREATE TABLE Kille (
    killa_id INT PRIMARY KEY,
    killa_name VARCHAR(100)
);
```

---

## Child Table

```sql
CREATE TABLE Mavale (
    mavla_id INT PRIMARY KEY,
    mavla_name VARCHAR(100),
    killa_id INT,

    FOREIGN KEY (killa_id)
    REFERENCES Kille(killa_id)
);
```

---

## ✅ Valid Insert

### Parent Table

```sql
INSERT INTO Kille
VALUES
(1,'Raigad'),
(2,'Pratapgad'),
(3,'Sinhagad');
```

---

### Child Table

```sql
INSERT INTO Mavale
VALUES
(101,'Tanaji',3),
(102,'Yesaji',1),
(103,'Baji Prabhu',2);
```

Database हे स्वीकारते.

---

## ❌ Invalid Insert

```sql
INSERT INTO Mavale
VALUES
(104,'Hambirrao',10);
```

### Output

```text
Error:
Cannot add or update a child row:
a foreign key constraint fails
```

कारण `killa_id = 10`
हा Parent Table मध्ये अस्तित्वातच नाही.

---

# 📊 Without FOREIGN KEY

### Kille

| ID | Name |
|---:|------|
|1|Raigad|
|2|Pratapgad|

---

### Mavale

| Name | Killa_ID |
|------|----------:|
|Tanaji|99|

👉 असा किल्लाच नाही...

Database चुकीचा Data साठवेल.

---

# ✅ With FOREIGN KEY

### Kille

| ID | Name |
|---:|------|
|1|Raigad|
|2|Pratapgad|
|3|Sinhagad|

---

### Mavale

| Name | Killa_ID |
|------|----------:|
|Tanaji|3|
|Yesaji|1|
|Baji|2|

👉 प्रत्येक Reference योग्य आहे.

---

# 💼 Real World Business Use Cases

### Employee → Department

```sql
department_id INT,
FOREIGN KEY (department_id)
REFERENCES Department(department_id)
```

प्रत्येक Employee वैध Department मध्येच असला पाहिजे.

---

### Students → Colleges

```sql
college_id INT,
FOREIGN KEY (college_id)
REFERENCES Colleges(college_id)
```

Student फक्त अस्तित्वात असलेल्या College शीच जोडला जाऊ शकतो.

---

# ⚙️ Why FOREIGN KEY is Important?

### 1️⃣ Maintains Relationships

Tables मधील संबंध कायम ठेवते.

---

### 2️⃣ Prevents Invalid Data

अस्तित्वात नसलेल्या Record ला Reference करता येत नाही.

---

### 3️⃣ Ensures Data Integrity

Database मधील माहिती सुसंगत आणि विश्वासार्ह राहते.

---

### 4️⃣ Reduces Human Errors

चुकीचे IDs Insert होण्यापासून संरक्षण करते.

---


# 🚀 Industry Perspective

Enterprise Databases मध्ये जवळपास प्रत्येक Transactional Table FOREIGN KEY वापरते.

Orders ↔ Customers

Employees ↔ Departments

Products ↔ Categories

Invoices ↔ Customers

Payments ↔ Orders

यामुळे Database मधील Relationships कायम सुरक्षित राहतात.

---

## 🧠 Quick Revision

- ✅ Connects Two Tables
- ✅ References PRIMARY KEY
- ✅ Prevents Invalid References
- ✅ Maintains Referential Integrity
- ✅ Parent → Child Relationship
- ✅ Multiple Rows can Reference Same Parent

---

## ⚔️ SQL Swarajya Rule

> **"मावळ्याची ओळख त्याच्या किल्ल्याशी जोडलेली...**
> **ते नातं मजबूत असेल, तरच स्वराज्य मजबूत."**

**SQL मध्ये:**

> **"FOREIGN KEY म्हणजे विश्वासाचं नातं...**
> **योग्य Reference असेल, तरच Database मजबूत."**