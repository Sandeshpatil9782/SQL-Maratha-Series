# Day 32 – INNER JOIN ⚔️

## ⚔️ Concept: वेगळे आहोत... पण ध्येय एकच

एकट्याने मोठं स्वप्न पाहता येतं...

पण ते पूर्ण करण्यासाठी योग्य लोकांची साथ लागते.

शेतकरी जमीन तयार करतो.

लोहार लोखंड घडवतो.

सुतार लाकडाला आकार देतो.

तीघांचं काम वेगळं...

पण ध्येय एकच.

त्यामुळेच एक मजबूत नांगर तयार होतो.

SQL मध्ये **INNER JOIN** दोन किंवा अधिक Tables मधील जुळणारा (Matching) Data एकत्र आणतो.

जीवनातही...

ध्येय, विश्वास आणि मेहनत जुळली...

की अशक्य वाटणारं कामही शक्य होतं.

---

## 🛡 Swarajya Analogy

स्वराज्य एका व्यक्तीने उभं केलं नाही.

शेतकऱ्याने अन्न दिलं.

लोहाराने शस्त्र तयार केलं.

सुताराने युद्धसाहित्य तयार केलं.

मावळ्यांनी रणांगण जिंकलं.

प्रत्येकाची भूमिका वेगळी होती...

पण ध्येय एकच होतं—

**स्वराज्य.**

---

## 💻 SQL Syntax

```sql
SELECT columns
FROM Table1
INNER JOIN Table2
ON Table1.Common_Column = Table2.Common_Column;
```

---

## 🌍 Real World SQL

### Employee & Department

```sql
SELECT e.Employee_Name,
       d.Department_Name
FROM Employees e
INNER JOIN Departments d
ON e.Department_ID = d.Department_ID;
```

### Orders & Customers

```sql
SELECT o.Order_ID,
       c.Customer_Name
FROM Orders o
INNER JOIN Customers c
ON o.Customer_ID = c.Customer_ID;
```

---

## ⚡ Poster SQL

```sql
SELECT *
FROM Farmer
INNER JOIN Blacksmith
ON Farmer.Goal = Blacksmith.Goal;
```

---

## 🎯 Why INNER JOIN?

- दोन Tables मधील Matching Data मिळवण्यासाठी.
- Business Reports तयार करण्यासाठी.
- Customer, Orders, Products सारखा Related Data एकत्र पाहण्यासाठी.
- Real-world Databases मध्ये सर्वाधिक वापरला जाणारा JOIN.

---

## 💼 Business Example

एका कंपनीला Employee चे नाव आणि त्याचा Department एकत्र पाहायचा आहे.

Employees आणि Departments हे दोन वेगळे Tables आहेत.

```sql
SELECT e.Employee_Name,
       d.Department_Name
FROM Employees e
INNER JOIN Departments d
ON e.Department_ID = d.Department_ID;
```

यामुळे फक्त Match होणारे Employees आणि त्यांचे Departments दिसतात.

---


### Q1. INNER JOIN म्हणजे काय?

दोन किंवा अधिक Tables मधील **Matching Records** परत करणारा JOIN.

---

### Q2. Match नसलेले Records दिसतात का?

नाही.

INNER JOIN फक्त Match होणारे Records दाखवतो.

---

### Q3. INNER JOIN मध्ये ON Clause का वापरतो?

दोन Tables कोणत्या Column वर Match करायचे हे सांगण्यासाठी.

---

## ⚔️ Swarajya Lesson

> **"वेगळं काम करणारे हात...
> जेव्हा एकाच ध्येयासाठी एकत्र येतात,
> तेव्हाच इतिहास घडतो."**

एकट्याने यश मिळू शकतं...

**पण एकत्र काम केलं तर साम्राज्य उभं राहतं.**

**ध्येय Match झालं...
तर शक्ती आपोआप निर्माण होते.**