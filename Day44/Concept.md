# Day 44 – INTERSECT ⚔️

## ⚔️ Concept: दोन्ही ठिकाणी नाव... म्हणजे खरी ताकद

कधी कधी दोन यादी compare कराव्या लागतात...

पहिल्या यादीत कोण आहेत?

आणि दुसऱ्या यादीत कोण आहेत?

या दोन्हीमधले **Common Records** शोधायचे असतील,
तर SQL मध्ये **INTERSECT** उपयोगी ठरतो.

**INTERSECT** दोन्ही Queries मध्ये असलेले Matching Records ठेवतो.

म्हणजेच...

**पहिल्या यादीत आहेत**  
➕  
**दुसऱ्या यादीतही आहेत**

=  
**दोन्ही यादीत Common असलेले Records**

---

## 🛡 Historical Analogy

### किल्ल्यावर चढणारे मावळे:

Tanaji
Suryaji
Yesaji
Mahadji
Shelar Mama

### लढणारे मावळे:

Tanaji
Suryaji
Baji Prabhu
Yesaji
Mahadji
---

### चढलेही आणि लढलेही असे मावळे कोण?

SELECT Name
FROM Climbers

INTERSECT

SELECT Name
FROM Fighters;

### Result:

Tanaji
Suryaji
Yesaji
Mahadji

---
### 💻 SQL Syntax

SELECT column_name
FROM Table1

INTERSECT

SELECT column_name
FROM Table2;

Table1 = First Set

Table2 = Second Set

Result = Common Records
---

### 🌍 Real World Business Example

	एका कंपनीला असे Customers शोधायचे आहेत:

Online Customers
आणि
Premium Customers

SELECT Customer_ID
FROM Online_Customers

INTERSECT

SELECT Customer_ID
FROM Premium_Customers;

	Result म्हणजे:
		Online आणि Premium दोन्ही असलेले Customers.

--- 
##3 Q1. INTERSECT काय करतो?

दोन SELECT Queries मध्ये common असलेले Records परत करतो.

### Q2. INTERSECT मध्ये कोणते Records मिळतात?

Both result sets मध्ये असलेले matching records.

### Q3. MySQL मध्ये INTERSECT उपलब्ध नसेल तर काय वापराल?

INNER JOIN किंवा EXISTS.

### Q4. INTERSECT आणि UNION मध्ये फरक?

UNION → दोन्ही Results combine करतो.

INTERSECT → दोन्ही Results मधील Common Records देतो.

---

### ⚔️ Swarajya Lesson

"फक्त चढणं पुरेसं नाही...
वेळ आली तर लढावंही लागतं."

SQL मध्ये आपण दोन्ही Lists मधला Common भाग शोधतो.

पण इतिहासात...

चढलाही आणि लढलाही, म्हणून सिंहगड. 🦁

SQL Lesson

UNION → एकत्र करा

UNION ALL → सगळे Records ठेवा

INTERSECT → Common Records शोधा

EXCEPT → फरक शोधा

योग्य Set Operator = योग्य Business Insight. ⚔️

---