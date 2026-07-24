# Day 22 – UPDATE SET | SQL UPDATE Statement

## ⚔️ Concept: विचार बदलला की नशीब बदलतं

राजा फक्त किल्ले जिंकत नाही...
तो आधी स्वतःचे विचार जिंकतो.

मनात जर अजूनही भीती, शंका आणि नकारात्मकता असेल,
तर बाहेरचं जग बदललं तरी परिणाम बदलत नाही.

जेव्हा विचार बदलतो...
तेव्हा निर्णय बदलतात.

निर्णय बदलले की कृती बदलते.

कृती बदलली की आयुष्य बदलतं.

SQL मध्येही हेच घडतं.

कधी नवीन Row तयार करण्याची गरज नसते.
फक्त आधीपासून असलेली Value बदलायची असते.

यालाच म्हणतात **UPDATE**.

---

## 🛡 Swarajya Analogy

समजा एखादा मावळा सुरुवातीला घोडदळात होता.

युद्धात त्याने पराक्रम दाखवला.

महाराजांनी त्याची जबाबदारी बदलली.

तोच माणूस...
तोच Record...

फक्त त्याची माहिती बदलली.

Database मध्येही नवीन Row तयार होत नाही.

फक्त Existing Data Update होतो.

---

## 💻 SQL Syntax

```sql
UPDATE table_name
SET column_name = value
WHERE condition;
```

---

## ⚡ Poster SQL

```sql
UPDATE Mind
SET Thought = 'Positive'
WHERE Man_Thought = 'Negative';
```

---

## 📖 Real SQL Example

```sql
UPDATE Employees
SET Salary = 65000
WHERE Employee_ID = 101;
```

---

## 🎯 Why WHERE is Important?

`WHERE` नसल्यास...

```sql
UPDATE Employees
SET Salary = 65000;
```

⚠️ प्रत्येक Employee चा Salary बदलून 65000 होईल.

म्हणून UPDATE करताना **WHERE हा सर्वात महत्त्वाचा भाग आहे.**

---

## 🧠 Business Example

एका E-commerce कंपनीत Customer चा Address बदलला.

Customer तोच आहे.

Order History तीच आहे.

फक्त Address Update झाला.

त्यासाठी नवीन Record तयार केला जात नाही.

---

## ⚔️ Swarajya Lesson

> **"नवीन आयुष्य सुरू करण्यापेक्षा...
> जुने विचार बदलणे जास्त महत्त्वाचे असते."**

जसं SQL मध्ये UPDATE,
तसंच आयुष्यातही...

**विचार UPDATE करा...**
**नशीब स्वतः UPDATE होईल.**