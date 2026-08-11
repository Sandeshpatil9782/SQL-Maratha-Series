# Day 40 – SUBQUERY ⚔️

## ⚔️ Concept: आधी माहिती... मग निर्णय

युद्ध फक्त तलवारीने जिंकता येत नाही...

योग्य वेळी मिळालेली योग्य माहिती
संपूर्ण युद्धाचं चित्र बदलू शकते.

म्हणूनच...

आधी गुप्तहेर जातो.

तो शत्रूची माहिती गोळा करतो.

मगच महाराज अंतिम निर्णय घेतात.

SQL मध्ये **SUBQUERY** म्हणजे एका Query च्या आत दुसरी Query.

आधी आतली Query Result देते...

मग बाहेरची Query त्या Result वर निर्णय घेते.

आयुष्यही हेच शिकवतं...

**आधी विचार करा...**

**मग कृती करा.**

---

## 🛡 Swarajya Analogy

बहिर्जी नाईक शत्रूच्या छावणीत जाऊन माहिती घेऊन येतात.

त्यांच्या अहवालात लिहिलेलं असतं—

**"शत्रूचं सैन्य = 5000"**

हा अहवाल पाहिल्यानंतरच
छत्रपती शिवाजी महाराज युद्धाचा निर्णय घेतात.

माहितीशिवाय निर्णय नाही.

---

## 💻 SQL Syntax

```sql
SELECT column_name
FROM table_name
WHERE column_name Operator (
    SELECT column_name
    FROM another_table
);
```

---

## 🌍 Real World SQL

### Employees earning above average salary

```sql
SELECT Employee_Name,
       Salary
FROM Employees
WHERE Salary >
(
    SELECT AVG(Salary)
    FROM Employees
);
```

---

### Products priced above average

```sql
SELECT Product_Name,
       Price
FROM Products
WHERE Price >
(
    SELECT AVG(Price)
    FROM Products
);
```

---

## ⚡ Poster SQL

```sql
SELECT Plan
FROM War
WHERE EnemyCount <
(
    SELECT Count
    FROM Spy_Report
    WHERE Spy = 'Baherji'
);
```

---

## 🎯 Why SUBQUERY?

- एका Query चा Result दुसऱ्या Query मध्ये वापरण्यासाठी.
- Dynamic Filtering करण्यासाठी.
- Complex Business Logic लिहिण्यासाठी.
- Reports आणि Analytics मध्ये खूप उपयोगी.

---

## 💼 Business Example

एका कंपनीला Average Salary पेक्षा जास्त Salary असलेले Employees शोधायचे आहेत.

Average Salary आधी काढावी लागेल.

मग त्या Result च्या आधारावर Employees निवडले जातील.

```sql
SELECT Employee_Name,
       Salary
FROM Employees
WHERE Salary >
(
    SELECT AVG(Salary)
    FROM Employees
);
```

---


### Q1. SUBQUERY म्हणजे काय?

एका SQL Query च्या आत लिहिलेली दुसरी Query म्हणजे **SUBQUERY**.

---

### Q2. SUBQUERY आधी कोणती Execute होते?

आधी **Inner Query** Execute होते.

तिचा Result मिळाल्यानंतर **Outer Query** Execute होते.

---

### Q3. SUBQUERY कुठे वापरू शकतो?

- WHERE
- FROM
- SELECT
- HAVING

---

## ⚔️ Swarajya Lesson

> **"बातमी आल्याशिवाय तलवार म्यानातून बाहेर येत नाही."**

आधी माहिती...

मग निर्णय...

आणि त्यानंतरच विजय.

**विचाराशिवाय कृती करू नका...
कारण योग्य निर्णयाची सुरुवात नेहमी योग्य माहितीपासूनच होते.** ⚔️