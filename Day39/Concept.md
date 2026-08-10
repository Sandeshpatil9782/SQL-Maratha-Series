# Day 39 – LIKE ⚔️

## ⚔️ Concept: पूर्ण नाव माहिती नसले... तरी शोध थांबत नाही

प्रत्येक गोष्ट आपल्याला पूर्ण माहिती असतेच असं नाही.

कधी फक्त सुरुवात माहिती असते...

कधी शेवट...

तर कधी मध्येच एखादा भाग.

पण म्हणून शोध थांबत नाही.

SQL मध्ये **LIKE** Pattern Matching साठी वापरलं जातं.

पूर्ण Value माहिती नसली,
तरी काही अक्षरांच्या आधारे योग्य Records शोधता येतात.

आयुष्यही हेच शिकवतं...

**ध्येयाचा संपूर्ण रस्ता दिसत नसला...**

**तरी पहिलं पाऊल टाका.**

शोधत राहिलात...

तर योग्य दिशा नक्की सापडते.

---

## 🛡 Swarajya Analogy

रायगडाच्या दप्तरखान्यातील कारकूनाला
एका मावळ्याचं पूर्ण नाव आठवत नाही.

फक्त एवढंच आठवतं...

**"शिव..."**

तो प्रत्येक दप्तर उघडतो...

**शिवाजी**

**शिवराम**

**शिवबा**

**शिवलिंग**

जोपर्यंत योग्य नाव सापडत नाही,
तोपर्यंत शोध सुरूच राहतो.

---

## 💻 SQL Syntax

```sql
SELECT column_name
FROM table_name
WHERE column_name LIKE 'pattern';
```

---

## 🌍 Wildcard Patterns

### Starts With

```sql
SELECT *
FROM Warriors
WHERE Name LIKE 'Shiv%';
```

---

### Ends With

```sql
SELECT *
FROM Warriors
WHERE Name LIKE '%ji';
```

---

### Contains

```sql
SELECT *
FROM Warriors
WHERE Name LIKE '%iva%';
```

---

### Single Character (_)

```sql
SELECT *
FROM Warriors
WHERE Name LIKE 'Shi_';
```

---

## ⚡ Poster SQL

```sql
SELECT *
FROM Warriors
WHERE Name LIKE 'Shiv%';
```

---

## 🎯 Why LIKE?

- Partial Search करण्यासाठी.
- Search Box तयार करण्यासाठी.
- Names, Cities, Products शोधण्यासाठी.
- User Input वर आधारित Filtering करण्यासाठी.

---

## 💼 Business Example

एका E-commerce Website वर User ने Search केलं:

**"Sam"**

त्याला Sam ने सुरू होणारी