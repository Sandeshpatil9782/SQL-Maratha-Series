# Day 11/16: CONSTRAINT Day 3 - PRIMARY KEY ⚔️ | SQL Swarajya Goshti

## 📜 Concept: निर्णय घेताना योग्यच घ्या

कारण तो पुन्हा बदलता येत नाही.

`PRIMARY KEY` म्हणजे तुमच्या Table वर मारलेला शेवटचा खिळा.

एकदा ठोकला की काढता येत नाही. काढला तर संपूर्ण रचना डळमळते.

`NOT NULL` आणि `UNIQUE` हे नियम होते.

`PRIMARY KEY` हा Database सोबतचा कायमचा करार आहे.

---

## ⚔️ Swarajya Story

शिवरायांनी प्रत्येक मावळ्याला वेगळी ओळख दिली.

समजा प्रत्येक मावळ्याला एक **Mavla ID** दिला.

| Mavla ID | Name |
|----------:|------|
| 1 | Tanaji |
| 2 | Baji Prabhu |
| 3 | Yesaji |

जर उद्या तानाजीचा ID 1 वरून 10 केला...

तर सैन्याची यादी,
मोहीम,
शस्त्रांची नोंद,
पगार,
सगळीकडे गोंधळ उडेल.

म्हणून ओळख एकदाच ठरवायची...
आणि ती कायम ठेवायची.

SQL मध्ये यालाच **PRIMARY KEY** म्हणतात.

---

# 💻 PRIMARY KEY

## 📖 Definition

`PRIMARY KEY` हा असा Constraint आहे जो Table मधील प्रत्येक Row ची **Unique आणि Permanent Identity** ठरवतो.

तो Column...

- Duplicate असू शकत नाही.
- NULL असू शकत नाही.
- प्रत्येक Row साठी एकमेव ओळख असतो.

---

## 📌 Rules

- Duplicate Values Allowed ❌
- NULL Allowed ❌
- एका Table मध्ये फक्त **एकच PRIMARY KEY**
- PRIMARY KEY वर Database आपोआप Index तयार करते.

---

## 💻 SQL Syntax

```sql
CREATE TABLE Mavale (
    mavla_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    sword VARCHAR(50)
);
```

---

# 📊 Without PRIMARY KEY

| ID | Name |
|----|------|
|1|Tanaji|
|1|Baji|
|1|Yesaji|

👉 कोणता Row कोणाचा?

---

# ✅ With PRIMARY KEY

| ID | Name |
|----|------|
|1|Tanaji|
|2|Baji|
|3|Yesaji|

👉 प्रत्येक Row ची स्वतंत्र ओळख.

---

# 💼 Real World Business Use Cases

### Employee Database

```sql
employee_id INT PRIMARY KEY
```

प्रत्येक Employee ची Unique Identity.

---

### Banking

```sql
account_id INT PRIMARY KEY
```

प्रत्येक Account ची कायमची ओळख.

---

### Hospital

```sql
patient_id INT PRIMARY KEY
```

प्रत्येक Patient साठी वेगळा ID.

---

### E-Commerce

```sql
order_id INT PRIMARY KEY
```

प्रत्येक Order ची स्वतंत्र ओळख.

---

## ⚙️ Why PRIMARY KEY is Important?

### 1️⃣ Fast Searching

PRIMARY KEY वर Database Auto Index तयार करते.

म्हणून लाखो Records मध्येही Search खूप जलद होते.

---

### 2️⃣ Relationship Maintain करते

Foreign Key दुसऱ्या Table मध्ये PRIMARY KEY ला Reference करते.

PRIMARY KEY नसल्यास योग्य Relation तयार होत नाही.

---

### 3️⃣ Duplicate Data रोखते

एकाच ID चे दोन Records तयार होऊ देत नाही.

---

### 4️⃣ Data Integrity टिकवते

प्रत्येक Row ची कायमची ओळख असल्यामुळे Database विश्वासार्ह राहतो.

---


### PRIMARY KEY आणि UNIQUE मध्ये फरक काय?

| PRIMARY KEY | UNIQUE |
|-------------|---------|
|Duplicate नाही|Duplicate नाही|
|NULL Allowed नाही|DBMS वर अवलंबून NULL Allow होऊ शकतो|
|एका Table मध्ये एकच|अनेक UNIQUE Constraints असू शकतात|
|Auto Index तयार होतो|Index DBMS वर अवलंबून|

---

# 🚀 Industry Perspective

Enterprise Applications मध्ये PRIMARY KEY हा प्रत्येक Table चा Backbone असतो.

Employee, Customer, Order, Product, Invoice, Payment, Shipment...

प्रत्येक Table ची सुरुवात एका मजबूत PRIMARY KEY पासूनच होते.

---

## 🧠 Quick Revision

- ✅ Unique Identity
- ✅ No Duplicate
- ✅ No NULL
- ✅ Auto Index
- ✅ One PRIMARY KEY per Table
- ✅ Used by Foreign Keys

---

## ⚔️ SQL Swarajya Rule

> **"राज्यात प्रत्येक मावळ्याची एकच ओळख...**
> **ती कधीच बदलत नाही."**

**SQL मध्ये:**

> **"प्रत्येक Row ची एकच Primary Identity...**
> **तीच Database चा पाया असते."**