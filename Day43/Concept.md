# Day 43 – EXCEPT ⚔️

## ⚔️ Concept: यात होते... त्यात नाही गेले

कधी कधी दोन यादी compare कराव्या लागतात...

पहिल्या यादीत कोण होते?

आणि दुसऱ्या यादीत कोण गेले?

या दोन्हीमधला फरक शोधायचा असेल,
तर SQL मध्ये **EXCEPT** उपयोगी ठरतो.

**EXCEPT** पहिल्या Query मधील Records ठेवतो,
पण दुसऱ्या Query मध्ये असलेले Matching Records काढून टाकतो.

म्हणजेच...

**पहिल्या यादीत आहेत**
➖
**दुसऱ्या यादीत आहेत**

=
**फक्त पहिल्या यादीत उरलेले Records**

---

## 🛡 Historical Analogy

घोडखिंडीत लढणारे मावळे:

```text
Tanaji
Baji Prabhu
Shiva Kashid
Yesaji
```

विशाळगडावर पोहोचलेले:

```text
Baji Prabhu
Yesaji
```

आता शोधायचं आहे—

**घोडखिंडीत होते, पण विशाळगडावर पोहोचले नाहीत कोण?**

```sql
SELECT Name
FROM Ghod_Khind

EXCEPT

SELECT Name
FROM Vishalgad_Entry;
```

Result:

```text
Tanaji
Shiva Kashid
```

---

## 💻 SQL Syntax

```sql
SELECT column_name
FROM Table1

EXCEPT

SELECT column_name
FROM Table2;
```

**Table1 = Base Set**

**Table2 = Exclusion Set**

---

## 🌍 Real World Business Example

एका कंपनीला असे Customers शोधायचे आहेत:

**Registered Customers**
पण
**Purchased Customers मध्ये नाहीत.**

```sql
SELECT Customer_ID
FROM Customers

EXCEPT

SELECT Customer_ID
FROM Orders;
```

Result म्हणजे:

**Registered आहेत, पण अजून Purchase केलेला नाही.**

---

## 📊 Data Analytics Use Case

Marketing Team ला:

**सर्व Registered Users**
मधून
**Already Converted Users**

वगळायचे आहेत.

```sql
SELECT User_ID
FROM Registered_Users

EXCEPT

SELECT User_ID
FROM Converted_Users;
```

यामुळे Marketing Team ला **Pending Users** मिळतात.

---

## ⚔️ EXCEPT vs UNION

### UNION

```sql
A UNION B
```

➡️ दोन्ही Sets एकत्र करतो.

### EXCEPT

```sql
A EXCEPT B
```

➡️ A मधून B मधील matching records वगळतो.

---

## 🔥 Important Note

`EXCEPT` चा exact support database नुसार बदलतो.

PostgreSQL आणि SQL Server मध्ये `EXCEPT` उपलब्ध आहे.

MySQL मध्ये `EXCEPT` पारंपरिकपणे उपलब्ध नव्हता; अशा परिस्थितीत `NOT EXISTS` किंवा `LEFT JOIN ... IS NULL` वापरून equivalent logic लिहिता येतो.

### MySQL Equivalent

```sql
SELECT g.Name
FROM Ghod_Khind g
WHERE NOT EXISTS (
    SELECT 1
    FROM Vishalgad_Entry v
    WHERE v.Name = g.Name
);
```

Production SQL लिहिताना **database dialect** नेहमी तपासा.

---

## 🎯 Why EXCEPT?

- दोन Lists मधील Difference शोधण्यासाठी.
- Missing Records शोधण्यासाठी.
- Customers who haven't purchased शोधण्यासाठी.
- Incomplete Processes शोधण्यासाठी.
- Data Reconciliation करण्यासाठी.
- Source आणि Target Data Compare करण्यासाठी.

---


### Q1. EXCEPT काय करतो?

पहिल्या Query मधील Records परत करतो जे दुसऱ्या Query मध्ये अस्तित्वात नाहीत.

### Q2. EXCEPT मध्ये कोणते Records मिळतात?

**Only in the first result set, not in the second.**

### Q3. MySQL मध्ये EXCEPT नसेल तर काय वापराल?

`NOT EXISTS` किंवा योग्य परिस्थितीत `LEFT JOIN ... IS NULL`.

### Q4. EXCEPT आणि UNION मध्ये फरक?

**UNION** → Results combine करतो.

**EXCEPT** → पहिल्या Result मधून दुसऱ्यातील Matches वगळतो.

---

## ⚔️ Swarajya Lesson

> **"काही जण रणांगणात राहिले...
> काही पुढे गेले...
> पण त्यागाची किंमत कमी होत नाही."**

SQL मध्ये आपण फक्त **Difference** शोधतो.

पण इतिहासात...

**प्रत्येक त्यागाची नोंद असते.** ⚔️

### SQL Lesson

**UNION → एकत्र करा**

**UNION ALL → सगळे Records ठेवा**

**EXCEPT → फरक शोधा**

**योग्य Set Operator = योग्य Business Insight.**