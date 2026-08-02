# Day 31 : SQL Swarajya Goshti – HAVING


---

# 🎯 Concept

`HAVING` हा SQL Clause **GROUP BY नंतर तयार झालेल्या गटांवर (groups) filter लावण्यासाठी** वापरला जातो.

- `WHERE` → रेकॉर्ड filter करतो (Grouping आधी)
- `HAVING` → Group filter करतो (Grouping नंतर)

---

# 🏰 इतिहासाशी जोडलेला SQL

रायगडावर अनेक मावळे वेगवेगळ्या कौशल्यांनुसार गटांमध्ये उभे आहेत.

- तलवारबाज
- घोडदळ
- धनुर्धारी
- गुप्तहेर

प्रथम प्रत्येक कौशल्यानुसार **गट तयार झाले (GROUP BY)**.

यानंतर महाराज प्रत्येक गट पाहतात आणि **फक्त अनुभवी व सर्वोत्तम मावळ्यांची निवड करतात**.

उद्दिष्ट स्पष्ट आहे—

> **संख्या नाही, गुणवत्ता महत्त्वाची.**

हेच SQL मधील **HAVING** आहे.

---

# SQL Memory Trick

**GROUP BY**
> आधी गट तयार करा.

**HAVING**
> मग प्रत्येक गटातून पात्र गटच निवडा.

---

# SQL Query

```sql
SELECT Skill, COUNT(*)
FROM Army
GROUP BY Skill
HAVING COUNT(*) >= 5;
```

👉 ज्या कौशल्याच्या गटात किमान 5 मावळे आहेत, तेवढेच गट दाखवा.

---

# Another Example

```sql
SELECT Department, AVG(Salary)
FROM Employees
GROUP BY Department
HAVING AVG(Salary) > 50000;
```

👉 फक्त त्या विभागांची माहिती दाखवा ज्यांचा सरासरी पगार ₹50,000 पेक्षा जास्त आहे.

---

# WHERE vs HAVING

| WHERE | HAVING |
|--------|---------|
| Grouping आधी filter | Grouping नंतर filter |
| Individual rows वर काम | Groups वर काम |
| Aggregate functions वापरत नाही | Aggregate functions वापरू शकतो |

---

### Q1. HAVING आणि WHERE मध्ये फरक काय?

**Answer:**

- `WHERE` individual rows filter करतो.
- `HAVING` grouped results filter करतो.

---

### Q2. HAVING वापरण्यासाठी GROUP BY आवश्यक आहे का?

**Answer:**

साधारणपणे हो. `HAVING` प्रामुख्याने `GROUP BY` सोबत वापरला जातो कारण तो groups वर filter लावतो.

---

# Real-World Business Use Cases

### Sales Analysis

```sql
SELECT Region, SUM(Sales)
FROM Sales
GROUP BY Region
HAVING SUM(Sales) > 100000;
```

👉 ₹1,00,000 पेक्षा जास्त विक्री असलेले प्रदेश.

---

### Customer Analysis

```sql
SELECT Customer_ID, COUNT(Order_ID)
FROM Orders
GROUP BY Customer_ID
HAVING COUNT(Order_ID) >= 10;
```

👉 10 किंवा त्यापेक्षा जास्त ऑर्डर देणारे ग्राहक.

---

# Poster Message

**HAVING**

गट केले.

पण प्रत्येक गटातून फक्त सोनं काढलं.

संख्या नको,
गुणवत्ता हवी.

**एकत्र. निवडक. ⚔️**

---

# Remember Forever

🏰 **GROUP BY** → मावळ्यांचे गट तयार झाले.

👑 **HAVING** → प्रत्येक गटातून फक्त सर्वोत्तम निवडले.

**HAVING = Filter the Groups, not the Rows.**