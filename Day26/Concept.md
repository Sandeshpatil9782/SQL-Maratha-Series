# Day 26 – WHERE FILTER ⚔️

## ⚔️ Concept: गाळून बघ... कोण आपलं, कोण परकं

पाणी प्यायचं असेल तर ते आधी गाळावं लागतं.

कारण प्रत्येक गोष्ट स्वीकारण्यासारखी नसते.

आयुष्यातही तसंच आहे...

प्रत्येक व्यक्ती,
प्रत्येक सल्ला,
प्रत्येक संधी,
आणि प्रत्येक नातं...

स्वीकारण्याआधी **गाळून पाहणं गरजेचं असतं.**

SQL मध्ये **WHERE** Clause आपल्याला फक्त आवश्यक Data निवडायला मदत करतो.

जे महत्त्वाचं नाही ते बाजूला राहतं.

आणि जे खरंच उपयोगाचं आहे,
तेच आपल्या समोर येतं.

---

## 🛡 Swarajya Analogy

स्वराज्यात प्रत्येकावर विश्वास ठेवला जात नव्हता.

महाराज माणसं त्यांच्या शब्दांवर नाही,
तर त्यांच्या निष्ठा आणि कृतीवर ओळखायचे.

योग्य माणसांची निवड झाली,
म्हणूनच स्वराज्य मजबूत झालं.

---

## 💻 SQL Syntax

```sql
SELECT *
FROM table_name
WHERE condition;
```

---

## 🌍 Real World SQL

**Find Active Customers**

```sql
SELECT Customer_Name,
       City
FROM Customers
WHERE Status = 'Active';
```

**Employees with Salary Above ₹50,000**

```sql
SELECT Employee_Name,
       Salary
FROM Employees
WHERE Salary > 50000;
```

---

## ⚡ Poster SQL

```sql
SELECT *
FROM Circle
WHERE Trust > 90
AND Drama = 0;
```

---

## 🎯 Why WHERE?

- फक्त आवश्यक Records मिळवण्यासाठी.
- Query Fast करण्यासाठी.
- Reports Accurate बनवण्यासाठी.
- Data Analysis मध्ये योग्य माहिती निवडण्यासाठी.

---

## 💼 Business Example

एका कंपनीला फक्त Delivered Orders पाहायच्या आहेत.

```sql
SELECT Order_ID,
       Customer_Name
FROM Orders
WHERE Order_Status = 'Delivered';
```

यामुळे फक्त आवश्यक Orders दिसतात.

---


## ⚔️ Swarajya Lesson

> **"प्रत्येकाला जवळ करू नका...
> आधी गाळून बघा, मगच विश्वास ठेवा."**

जसं SQL मध्ये **WHERE** आवश्यक Data निवडतो...

तसंच आयुष्यातही योग्य माणसं, योग्य विचार आणि योग्य संधी निवडा.

**वेळ वाया घालवू नका... योग्य गोष्टींवर लक्ष केंद्रित करा.**