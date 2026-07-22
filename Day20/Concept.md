# Day 20: RENAME TABLE ⚔️ | SQL स्वराज्य गोष्टी

## 📜 Concept: नाव बदललं, ओळख नाही

> **"जुनं जाऊ द्या..."**  
> **"नवीन स्वीकारा."**

शहर तेच असतं...

लोक तेच असतात...

इतिहासही तोच असतो...

**फक्त नाव बदलतं.**

Database मध्येही असंच होतं.

कधी Table चे नाव बदलण्याची गरज पडते.

पण त्यातील Data किंवा Structure बदलत नाही.

यालाच **RENAME TABLE** म्हणतात.

---

# 💻 Definition

`RENAME TABLE` चा वापर Existing Table चे नाव बदलण्यासाठी केला जातो.

Table मधील Data आणि Structure तशीच राहते.

---

# 📌 Syntax

```sql
RENAME TABLE Aurangabad
TO Chhatrapati_Sambhajinagar;
```

---

## Before

**Table Name**

```
Aurangabad
```

---

## Execute

```sql
RENAME TABLE Aurangabad
TO Chhatrapati_Sambhajinagar;
```

---

## After

**Table Name**

```
Chhatrapati_Sambhajinagar
```

✅ Data बदलला नाही.

✅ Structure बदलली नाही.

✅ फक्त Table चे नाव बदलले.

---

# 💼 Real World Example

Company मध्ये `Customer` Table चे नाव अधिक स्पष्ट करण्यासाठी `Customers` असे ठेवायचे आहे.

```sql
RENAME TABLE Customer
TO Customers;
```

यामुळे नाव अधिक Meaningful होते.

---

# ✅ Key Points

- फक्त Table चे नाव बदलते.
- Data बदलत नाही.
- Structure बदलत नाही.
- Readability आणि Maintainability सुधारते.

---

# ⚔️ SQL स्वराज्य नियम

> **"नाव बदललं..."**  
> **"म्हणून इतिहास बदलत नाही."**

**SQL मध्ये:**

> **"Rename the Table..."**  
> **"Not the Data."** ⚔️