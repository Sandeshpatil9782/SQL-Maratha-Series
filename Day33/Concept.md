# Day 33 – LEFT JOIN ⚔️

## ⚔️ Concept: स्वतः मजबूत रहा... आणि सोबत येणाऱ्यांना जागा द्या

नेतृत्व म्हणजे...

सगळ्यांच्या मागे चालणं नाही.

आणि सगळ्यांना मागे सोडणंही नाही.

खरा नेता स्वतःच्या ध्येयावर ठाम असतो...

पण सोबत चालायला तयार असणाऱ्यांसाठी
नेहमी जागा ठेवतो.

SQL मध्ये **LEFT JOIN** डाव्या (Left) Table मधील सर्व Records ठेवतो.

उजव्या (Right) Table मधून Match झालं तर Data जोडतो...
Match नाही झालं तरी Left Table मधील Record कायम राहतो.

आयुष्यही हाच धडा शिकवतं...

**स्वतःची ओळख कधीही गमावू नका.**

पण योग्य लोक साथ द्यायला आले,
तर त्यांना नाकारूही नका.

---

## 🛡 Swarajya Analogy

स्वराज्य उभं राहत असताना...

एक ध्येय आधीच निश्चित होतं.

त्या ध्येयाभोवती अनेक मावळे,
शेतकरी,
कारागीर,
आणि सामान्य जनता जोडत गेली.

ध्येय बदललं नाही...

फक्त साथ वाढत गेली.

---

## 💻 SQL Syntax

```sql
SELECT columns
FROM Left_Table
LEFT JOIN Right_Table
ON Left_Table.Common_Column = Right_Table.Common_Column;
```

---

## 🌍 Real World SQL

### All Customers with Their Orders

```sql
SELECT c.Customer_Name,
       o.Order_ID
FROM Customers c
LEFT JOIN Orders o
ON c.Customer_ID = o.Customer_ID;
```

ज्यांनी Order दिला नाही,
ते Customers सुद्धा Result मध्ये दिसतील.

---

### Employees with Department

```sql
SELECT e.Employee_Name,
       d.Department_Name
FROM Employees e
LEFT JOIN Departments d
ON e.Department_ID = d.Department_ID;
```

Department नसला तरी Employee दिसेल.

---

## ⚡ Poster SQL

```sql
SELECT *
FROM Me
LEFT JOIN People
ON Me.Goal = People.Goal;
```

---

## 🎯 Why LEFT JOIN?

- Left Table मधील सर्व Records मिळवण्यासाठी.
- Match नसलेला Data शोधण्यासाठी.
- Missing Relationships ओळखण्यासाठी.
- Reporting आणि Business Analysis मध्ये खूप वापरला जातो.

---

## 💼 Business Example

एका कंपनीला सर्व Customers पाहायचे आहेत.

त्यांनी Order दिला असेल किंवा नसेल,
दोन्ही प्रकारचे Customers Report मध्ये हवे आहेत.

```sql
SELECT c.Customer_Name,
       o.Order_ID
FROM Customers c
LEFT JOIN Orders o
ON c.Customer_ID = o.Customer_ID;
```

---

### Q1. LEFT JOIN म्हणजे काय?

Left Table मधील सर्व Records आणि Right Table मधील Match होणारे Records परत करतो.

---

### Q2. Match नसेल तर काय दिसेल?

Right Table चे Columns **NULL** दाखवले जातात.

---

### Q3. INNER JOIN आणि LEFT JOIN मध्ये फरक काय?

- **INNER JOIN** → फक्त Match झालेले Records.
- **LEFT JOIN** → Left Table मधील सर्व Records + Match झालेले Right Records.

---

## ⚔️ Swarajya Lesson

> **"ध्येयावर ठाम रहा...
> पण योग्य लोकांना सोबत घेण्याइतकं मोठं मन ठेवा."**

एकटा माणूस प्रवास सुरू करू शकतो...

**पण एकत्र चालणारे लोकच इतिहास घडवतात.**

**मी + आपण = स्वराज्य.** ⚔️