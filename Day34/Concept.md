# Day 34 – RIGHT JOIN ⚔️

## ⚔️ Concept: ध्येय मोठं... व्यक्ती लहान

स्वतःला महत्त्व देणं चुकीचं नाही...

पण ध्येय स्वतःपेक्षा मोठं मानणं,
हीच खरी नेतृत्वाची ओळख आहे.

तुम्ही असाल...
किंवा नसाल...

ध्येय थांबता कामा नये.

SQL मध्ये **RIGHT JOIN** Right Table मधील सर्व Records कायम ठेवतो.

Left Table मधून Match झाला तर Data जोडला जातो...
Match झाला नाही तरी Right Table तसाच राहतो.

आयुष्यही हेच शिकवतं...

ध्येय कायम असतं.

आपण फक्त त्या प्रवासाचा एक भाग असतो.

---

## 🛡 Swarajya Analogy

स्वराज्य एखाद्या एका माणसावर उभं नव्हतं.

एखादा मावळा आला नाही...

तरी मोहीम थांबत नव्हती.

कारण ध्येय एका व्यक्तीपेक्षा मोठं होतं.

जो आला...

त्याचं स्वागत झालं.

पण स्वराज्याची वाटचाल कधी थांबली नाही.

---

## 💻 SQL Syntax

```sql
SELECT columns
FROM Left_Table
RIGHT JOIN Right_Table
ON Left_Table.Common_Column = Right_Table.Common_Column;
```

---

## 🌍 Real World SQL

### All Departments with Employees

```sql
SELECT e.Employee_Name,
       d.Department_Name
FROM Employees e
RIGHT JOIN Departments d
ON e.Department_ID = d.Department_ID;
```

Department मध्ये Employee नसला,
तरी Department Result मध्ये दिसेल.

---

### All Products with Sales

```sql
SELECT s.Sale_ID,
       p.Product_Name
FROM Sales s
RIGHT JOIN Products p
ON s.Product_ID = p.Product_ID;
```

Sale झाली नसली,
तरी Product दिसेल.

---

## ⚡ Poster SQL

```sql
SELECT *
FROM Soldier
RIGHT JOIN Commanders
ON Soldier.Goal = Commanders.Goal;
```

---

## 🎯 Why RIGHT JOIN?

- Right Table मधील सर्व Records मिळवण्यासाठी.
- Missing Relationships शोधण्यासाठी.
- Complete Master Data Reports तयार करण्यासाठी.
- LEFT JOIN समजल्यावर RIGHT JOIN सहज समजतो.

---

## 💼 Business Example

एका कंपनीला सर्व Departments पाहायचे आहेत.

त्या Department मध्ये Employee असो किंवा नसो,
Department Report मध्ये दिसलाच पाहिजे.

```sql
SELECT e.Employee_Name,
       d.Department_Name
FROM Employees e
RIGHT JOIN Departments d
ON e.Department_ID = d.Department_ID;
```

---
### Q1. RIGHT JOIN म्हणजे काय?

Right Table मधील सर्व Records आणि Left Table मधील Match झालेले Records परत करतो.

---

### Q2. Match नसेल तर काय दिसेल?

Left Table चे Columns **NULL** दिसतात.

---

### Q3. LEFT JOIN आणि RIGHT JOIN मध्ये फरक काय?

- **LEFT JOIN** → Left Table कायम ठेवतो.
- **RIGHT JOIN** → Right Table कायम ठेवतो.

---

## ⚔️ Swarajya Lesson

> **"ध्येय समोर असेल...
> तर मी कुठेही चालेल.
> पण स्वराज्याची वाटचाल थांबता कामा नये."**

व्यक्ती येतात...

व्यक्ती जातात...

**पण ध्येय कायम राहतं.**

ध्येयासाठी जगा...
स्वतःसाठी नाही. ⚔️