# Day 41 – UNION ⚔️

## ⚔️ Concept: वेगळे शस्त्र... एकच शपथ

एकाकडे तलवार आहे...

दुसऱ्याकडे धनुष्य-बाण.

काम वेगळं...

कौशल्य वेगळं...

पण ध्येय एकच असेल,
तर फरक ताकद बनतो.

SQL मध्ये **UNION** दोन किंवा अधिक `SELECT` Queries चे Results एकत्र करून **एकच Result Set** तयार करतो.

म्हणजेच...

**दोन यादी → एक Result**

आणि स्वराज्याचा धडा—

**फरक बाजूला ठेवा...**
**ताकद एकत्र आणा.**

---

## 🛡 Swarajya Analogy

एका बाजूला **तलवारधारी मावळे**...

दुसऱ्या बाजूला **धनुर्धारी मावळे**...

दोघांची युद्धपद्धत वेगळी.

पण शपथ एकच—

**स्वराज्य.**

जेव्हा दोन्ही शक्ती एकत्र आल्या,
तेव्हा तयार झाली—

**एकत्र स्वराज्य सेना.**

---

## 💻 SQL Syntax

```sql
SELECT column1, column2
FROM Table1

UNION

SELECT column1, column2
FROM Table2;
```

---

## ⚡ Important Rule

`UNION` वापरताना दोन्ही `SELECT` Queries मध्ये:

- Columns ची संख्या समान असावी.
- Corresponding Columns चे Data Types compatible असावेत.
- Column order योग्य असावा.

आणि महत्त्वाचं—

**UNION duplicate rows काढून टाकतो.**

---

## 🔥 UNION vs UNION ALL

### UNION

```sql
SELECT Name FROM Sena1
UNION
SELECT Name FROM Sena2;
```

Duplicate Names remove होतील.

### UNION ALL

```sql
SELECT Name FROM Sena1
UNION ALL
SELECT Name FROM Sena2;
```

Duplicate Records सुद्धा ठेवले जातील.

---

## 🌍 Real World Example

समजा कंपनीकडे दोन Branches आहेत:

**Pune Customers**

```sql
SELECT Customer_Name
FROM Pune_Customers;
```

**Mumbai Customers**

```sql
SELECT Customer_Name
FROM Mumbai_Customers;
```

दोन्ही Customer Lists एकत्र करायच्या असतील:

```sql
SELECT Customer_Name
FROM Pune_Customers

UNION

SELECT Customer_Name
FROM Mumbai_Customers;
```

यातून एक Combined Customer List मिळते.

---

## ⚔️ Poster SQL

```sql
SELECT Name
FROM Sena1

UNION

SELECT Name
FROM Sena2;
```

---

## 🎯 Why UNION?

- दोन समान प्रकारच्या Data Sets एकत्र करण्यासाठी.
- Multiple Branches चा Data Combine करण्यासाठी.
- Historical + Current Data Merge करण्यासाठी.
- Department-wise किंवा Region-wise Lists Consolidate करण्यासाठी.

---

## 💼 Business Use Case

एका कंपनीकडे:

- `Online_Customers`
- `Store_Customers`

असे दोन Tables आहेत.

Management ला **सर्व Customers ची एक Unique List** हवी आहे.

```sql
SELECT Customer_ID, Customer_Name
FROM Online_Customers

UNION

SELECT Customer_ID, Customer_Name
FROM Store_Customers;
```

`UNION` मुळे duplicate Customers काढून एक consolidated list मिळते.

---

### Q1. UNION म्हणजे काय?

दोन किंवा अधिक `SELECT` Queries चे Results एकत्र करून एक Result Set तयार करणारा SQL Operator.

---

### Q2. UNION आणि UNION ALL मध्ये फरक?

**UNION** → Duplicates remove करतो.

**UNION ALL** → Duplicates ठेवतो आणि सामान्यतः अधिक performant असतो कारण duplicate elimination लागत नाही.

---

### Q3. UNION साठी Columns ची संख्या समान असावी का?

होय.

दोन्ही Queries मध्ये समान संख्येचे columns असणे आवश्यक आहे.

---

## ⚔️ Swarajya Lesson

> **"शस्त्र वेगवेगळी असली...
> तरी शपथ एकच असेल,
> तर ताकद अनेक पटींनी वाढते."**

**दोन यादी...**

**एकच Result.**

**फरक बाजूला, ताकद एकत्र.** ⚔️🔥