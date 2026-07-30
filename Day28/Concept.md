# Day 28 – ORDER BY ASC ⚔️

## ⚔️ Concept: शिखर गाठायचं असेल तर पहिल्या पायरीपासून सुरुवात करा

प्रत्येक मोठा प्रवास...

एका छोट्या पावलाने सुरू होतो.

कोणीही जन्मतः शिखरावर पोहोचत नाही.

पहिली पायरी...
पहिला प्रयत्न...
पहिली चूक...

यातूनच यशाची वाट तयार होते.

SQL मध्ये **ORDER BY ASC** म्हणजे माहिती लहानापासून मोठ्याकडे, पहिल्यापासून शेवटपर्यंत योग्य क्रमाने मांडणे.

आयुष्यही हाच नियम शिकवतं...

क्रम पाळा.

घाई करू नका.

प्रत्येक पायरी पार करत पुढे जा.

---

## 🛡 Swarajya Analogy

रायगड एका उडीत जिंकला गेला नव्हता.

प्रत्येक पायरी,
प्रत्येक चढाई,
प्रत्येक लढाई...

यातूनच स्वराज्य उभं राहिलं.

मोठं ध्येय गाठण्यासाठी
लहान सुरुवातीचा स्वीकार करावा लागतो.

---

## 💻 SQL Syntax

```sql
SELECT column_name
FROM table_name
ORDER BY column_name ASC;
```

---

## 🌍 Real World SQL

**Employees Sorted by Salary**

```sql
SELECT Employee_Name,
       Salary
FROM Employees
ORDER BY Salary ASC;
```

**Students Sorted by Roll Number**

```sql
SELECT Roll_No,
       Student_Name
FROM Students
ORDER BY Roll_No ASC;
```

---

## ⚡ Poster SQL

```sql
SELECT Goal
FROM Life
ORDER BY Step ASC;
```

---

## 🎯 Why ORDER BY ASC?

- Data Ascending Order मध्ये Sort करण्यासाठी.
- Reports अधिक व्यवस्थित दाखवण्यासाठी.
- Smallest ते Largest Values पाहण्यासाठी.
- Business Analysis अधिक सोपी करण्यासाठी.

---

## 💼 Business Example

एका HR Manager ला कमी Salary पासून जास्त Salary पर्यंत Employees पाहायचे आहेत.

```sql
SELECT Employee_Name,
       Salary
FROM Employees
ORDER BY Salary ASC;
```

यामुळे Salary योग्य क्रमाने दिसतात.

---

## ⚔️ Swarajya Lesson

> **"शिखर गाठण्याची घाई करू नका...
> प्रत्येक पायरी प्रामाणिकपणे चढा."**

आजची पहिली पायरी...

उद्याच्या यशाचा पाया असते.

**शिस्त पाळा... क्रम पाळा... आणि शिखर नक्की गाठा.**