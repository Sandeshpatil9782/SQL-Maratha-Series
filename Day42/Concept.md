# Day 42 – UNION ALL ⚔️

## ⚔️ Concept: योगदान मोजा, नाव नाही

एकाच मावळ्याला दोन वेगवेगळ्या जबाबदाऱ्या मिळाल्या...

**पहारा Duty** मध्ये तो आहे.

आणि **हल्ला Duty** मध्येही तो आहे.

म्हणून त्याचं नाव दोनदा दिसतं.

SQL मध्ये **UNION ALL** दोन `SELECT` Queries चे सर्व Records एकत्र करतो आणि **duplicates काढत नाही.**

म्हणजेच...

**Record आला → तो ठेवला.**

Duplicate असला तरीही ठेवला.

---

## 🛡 Swarajya Analogy

### पहारा Duty

```text
Tanaji
Baji
Shiva Kashid
```

### हल्ला Duty

```text
Baji
Shiva Kashid
Yesaji
```

`UNION ALL` केल्यावर:

```text
Tanaji
Baji
Shiva Kashid
Baji
Shiva Kashid
Yesaji
```

**Total = 6 Records**

Baji आणि Shiva Kashid दोनदा आले...

कारण त्यांनी **दोन वेगवेगळ्या Duties मध्ये योगदान दिलं.**

---

## 💻 SQL Syntax

```sql
SELECT Name
FROM Duty1

UNION ALL

SELECT Name
FROM Duty2;
```

---

## 🔥 UNION vs UNION ALL

### UNION

```sql
SELECT Name
FROM Duty1

UNION

SELECT Name
FROM Duty2;
```

Result:

```text
Tanaji
Baji
Shiva Kashid
Yesaji
```

**Total = 4**

Duplicate Names remove होतात.

---

### UNION ALL

```sql
SELECT Name
FROM Duty1

UNION ALL

SELECT Name
FROM Duty2;
```

Result:

```text
Tanaji
Baji
Shiva Kashid
Baji
Shiva Kashid
Yesaji
```

**Total = 6**

Duplicate Records कायम राहतात.

---

## 🎯 Why UNION ALL?

`UNION ALL` वापरा जेव्हा:

- प्रत्येक Record महत्त्वाचा आहे.
- Duplicate Records सुद्धा मोजायचे आहेत.
- Transaction-level data combine करायचा आहे.
- Performance महत्त्वाची आहे.
- दोन Tables मधील complete records preserve करायचे आहेत.

`UNION` सारखा duplicate elimination step नसल्यामुळे `UNION ALL` सामान्यतः अधिक performant असतो.

---

## 🌍 Real World Business Example

समजा कंपनीकडे दोन Branches ची Sales आहेत:

```sql
SELECT Customer_ID, Sale_Amount
FROM Pune_Sales

UNION ALL

SELECT Customer_ID, Sale_Amount
FROM Mumbai_Sales;
```

इथे प्रत्येक Sale Transaction महत्त्वाचा आहे.

एकाच Customer ने दोन वेगवेगळ्या Branches मधून खरेदी केली असेल,
तर त्याच्या दोन्ही Transactions ठेवायच्या आहेत.

म्हणून **UNION ALL** योग्य.

---

## 📊 Data Analytics Use Case

Monthly Sales combine करताना:

```sql
SELECT *
FROM Sales_January

UNION ALL

SELECT *
FROM Sales_February

UNION ALL

SELECT *
FROM Sales_March;
```

इथे प्रत्येक transaction preserve करणे आवश्यक आहे.

Duplicate दिसत असला तरी तो actual transaction असू शकतो.

---

### Q1. UNION ALL काय करतो?

दोन किंवा अधिक `SELECT` Queries चे सर्व Records एकत्र करतो आणि duplicates remove करत नाही.

### Q2. UNION आणि UNION ALL मध्ये मुख्य फरक?

**UNION** → duplicates remove करतो.

**UNION ALL** → duplicates ठेवतो.

### Q3. UNION ALL अधिक fast का असतो?

कारण duplicate elimination साठी अतिरिक्त processing लागत नाही.

### Q4. UNION ALL कधी वापराल?

जेव्हा प्रत्येक row महत्त्वाची आहे आणि duplicate records preserve करायचे आहेत.

---

## ⚔️ Swarajya Lesson

> **"नाव दोनदा आलं म्हणून योगदान कमी होत नाही."**

कधी पहारा...

कधी हल्ला...

जबाबदारी बदलली तरी योगदान मोजलं पाहिजे.

**प्रत्येक वार मोलाचा.** ⚔️

### SQL Lesson

**UNION → Unique Records**

**UNION ALL → All Records**

**फरक समजा... आणि योग्य Operator निवडा.**