# Day 35 – FULL OUTER JOIN ⚔️

## ⚔️ Concept: कोणीही बाहेर नाही... सगळे आपलेच

स्वराज्य उभं राहतं...

जेव्हा प्रत्येकाला आपली जागा मिळते.

कोणी शेतात राबतो...

कोणी शस्त्र घडवतो...

कोणी रणांगणात लढतो...

तर कोणी राज्यकारभार सांभाळतो.

प्रत्येकाची भूमिका वेगळी...

पण प्रत्येकाचं योगदान तितकंच महत्त्वाचं.

SQL मध्ये **FULL OUTER JOIN** दोन्ही Tables मधील सर्व Records परत करतो.

Match झालेले Records एकत्र येतात...

आणि Match न झालेले Records सुद्धा Result मध्ये दिसतात.

आयुष्यही हेच शिकवतं...

**प्रत्येक माणसाची किंमत असते.**

कोणी आज तुमच्यासोबत असेल...

कोणी उद्या येईल...

पण योग्य मनाने स्वीकारलं,
तर प्रत्येक जण स्वराज्याचा भाग बनू शकतो.

---

## 🛡 Swarajya Analogy

स्वराज्य फक्त राजांनी उभं केलं नाही.

शेतकरी...

लोहार...

सुतार...

मावळे...

सरदार...

स्त्रिया...

आणि सामान्य जनता...

सगळ्यांनी मिळून स्वराज्य घडवलं.

कोणीही कमी नव्हता.

प्रत्येक जण आवश्यक होता.

---

## 💻 SQL Syntax

```sql
SELECT columns
FROM Table1
FULL OUTER JOIN Table2
ON Table1.Common_Column = Table2.Common_Column;
```

---

## 🌍 Real World SQL

### Employees & Projects

```sql
SELECT e.Employee_Name,
       p.Project_Name
FROM Employees e
FULL OUTER JOIN Projects p
ON e.Project_ID = p.Project_ID;
```

यामुळे Project नसलेले Employees आणि Employee नसलेले Projects दोन्ही दिसतात.

---

### Customers & Orders

```sql
SELECT c.Customer_Name,
       o.Order_ID
FROM Customers c
FULL OUTER JOIN Orders o
ON c.Customer_ID = o.Customer_ID;
```

Order नसलेले Customers आणि Customer नसलेले Orders दोन्ही Result मध्ये दिसतात.

---

## ⚡ Poster SQL

```sql
SELECT *
FROM People
FULL OUTER JOIN Leaders
ON People.Goal = Leaders.Goal;
```

---

## 🎯 Why FULL OUTER JOIN?

- दोन्ही Tables मधील सर्व Records मिळवण्यासाठी.
- Match आणि Non-Match दोन्ही Records पाहण्यासाठी.
- Missing Data Analysis करण्यासाठी.
- Complete Business Reports तयार करण्यासाठी.

---

## 💼 Business Example

एका कंपनीला सर्व Customers आणि सर्व Orders पाहायचे आहेत.

Order असो किंवा नसो...

Customer असो किंवा नसो...

दोन्ही माहिती Report मध्ये हवी आहे.

```sql
SELECT c.Customer_Name,
       o.Order_ID
FROM Customers c
FULL OUTER JOIN Orders o
ON c.Customer_ID = o.Customer_ID;
```

---


### Q1. FULL OUTER JOIN म्हणजे काय?

दोन्ही Tables मधील सर्व Records परत करतो. Match झालेले Records एकत्र येतात आणि Match नसलेल्या Records साठी दुसऱ्या Table चे Columns `NULL` दाखवले जातात.

---

### Q2. FULL OUTER JOIN मध्ये `NULL` का येतात?

कारण एका Table मध्ये Record असतो पण दुसऱ्या Table मध्ये त्याचा Match नसतो.

---

### Q3. INNER JOIN, LEFT JOIN, RIGHT JOIN आणि FULL OUTER JOIN मध्ये मुख्य फरक काय?

- **INNER JOIN** → फक्त Match झालेले Records.
- **LEFT JOIN** → Left Table मधील सर्व + Match झालेले Right Records.
- **RIGHT JOIN** → Right Table मधील सर्व + Match झालेले Left Records.
- **FULL OUTER JOIN** → दोन्ही Tables मधील सर्व Records.

---

## ⚔️ Swarajya Lesson

> **"स्वराज्य एका व्यक्तीचं नसतं...
> ते प्रत्येकाच्या योगदानातून घडतं."**

**मी पण आहे...**

**ते पण आहेत...**

**आणि आपण सगळे मिळूनच स्वराज्य आहोत.** ⚔️