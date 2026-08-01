# Day 30 – GROUP BY ⚔️

## ⚔️ Concept: माणसं ओळख... सगळ्यांना एकत्र ठेवू नकोस

प्रत्येक माणूस सारखा नसतो.

कोणी निष्ठावान असतो.

कोणी संधी पाहून सोबत येतो.

तर कोणी विश्वासघात करण्याची वाट पाहत असतो.

जर प्रत्येकाला सारखंच स्थान दिलं...

तर योग्य माणसाची किंमत कमी होते.

SQL मध्ये **GROUP BY** समान गुणधर्म असलेल्या Records ला एका Group मध्ये एकत्र करतो.

आयुष्यही हेच शिकवतं...

माणसांना ओळखा.

त्यांच्या कृतीनुसार त्यांना स्थान द्या.

---

## 🛡 Swarajya Analogy

स्वराज्यात प्रत्येकाची भूमिका वेगळी होती.

निष्ठावान मावळे...
संधिसाधू सरदार...
आणि गद्दार...

महाराजांनी सर्वांना एकाच नजरेने पाहिलं नाही.

ज्याची जशी निष्ठा...
तसं त्याचं स्थान.

यामुळेच स्वराज्य टिकून राहिलं.

---

## 💻 SQL Syntax

```sql
SELECT column_name,
       aggregate_function(column_name)
FROM table_name
GROUP BY column_name;
```

---

## 🌍 Real World SQL

**Employees by Department**

```sql
SELECT Department,
       COUNT(*) AS Total_Employees
FROM Employees
GROUP BY Department;
```

**Total Sales by City**

```sql
SELECT City,
       SUM(Sales_Amount) AS Total_Sales
FROM Sales
GROUP BY City;
```

---

## ⚡ Poster SQL

```sql
SELECT *
FROM People
GROUP BY Loyalty;
```

---

## 🎯 Why GROUP BY?

- समान Data एका Group मध्ये विभागण्यासाठी.
- Category-wise Reports तयार करण्यासाठी.
- COUNT(), SUM(), AVG(), MAX(), MIN() सारख्या Aggregate Functions सोबत वापरण्यासाठी.
- Business Insights मिळवण्यासाठी.

---

## 💼 Business Example

एका कंपनीला प्रत्येक Department मध्ये किती Employees आहेत हे पाहायचं आहे.

```sql
SELECT Department,
       COUNT(*) AS Employee_Count
FROM Employees
GROUP BY Department;
```

यामुळे प्रत्येक Department ची Employee संख्या वेगळी दिसते.

---

### Q1. GROUP BY कशासाठी वापरतात?

समान Values असलेल्या Records ला Group करण्यासाठी.

---

### Q2. GROUP BY सोबत कोणती Functions जास्त वापरली जातात?

- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

---

### Q3. GROUP BY शिवाय COUNT() वापरल्यास काय होईल?

संपूर्ण Table साठी एकच Result मिळेल.

GROUP BY वापरल्यास प्रत्येक Group साठी वेगळा Result मिळतो.

---

## ⚔️ Swarajya Lesson

> **"सगळ्यांना सारखं स्थान देऊ नका...
> माणसांची ओळख त्यांच्या कृतीतून करा."**

निष्ठावंतांना जवळ ठेवा...

संधिसाधूंवर लक्ष ठेवा...

आणि गद्दारांपासून अंतर ठेवा.

**योग्य माणसांचा समूहच मजबूत स्वराज्य घडवतो.**