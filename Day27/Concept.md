# Day 27 – LIMIT 1 ⚔️

## ⚔️ Concept: शंभरातून एकच निवडला...

जगात ओळखी हजारो होतात...

पण विश्वास ठेवण्यासारखी माणसं फार कमी असतात.

संकटात जे साथ सोडत नाहीत,
यशात जे मत्सर करत नाहीत,
आणि अपयशात जे खांद्याला खांदा लावून उभे राहतात...

तीच खरी माणसं.

SQL मध्ये **LIMIT** वापरून आपण आवश्यक तेवढेच Records घेतो.

कधी कधी...

हजारो Records पेक्षा एकच Record जास्त महत्त्वाचा असतो.

आयुष्यातही तसंच...

खूप मित्र असण्यापेक्षा,
एक निष्ठावान मित्र असणं अधिक मौल्यवान असतं.

---

## 🛡 Swarajya Analogy

छत्रपती संभाजी महाराजांच्या आयुष्यात अनेक लोक आले.

पण संकटाच्या काळात शेवटच्या क्षणापर्यंत
ज्यांनी साथ सोडली नाही...

ते होते **कवी कलश**.

त्यांची मैत्री ही पदावर नव्हती...
ती निष्ठेवर उभी होती.

---

## 💻 SQL Syntax

```sql
SELECT column_name
FROM table_name
LIMIT number;
```

---

## 🌍 Real World SQL

**Top 5 Highest Paid Employees**

```sql
SELECT Employee_Name,
       Salary
FROM Employees
ORDER BY Salary DESC
LIMIT 5;
```

**Latest Order**

```sql
SELECT *
FROM Orders
ORDER BY Order_Date DESC
LIMIT 1;
```

---

## ⚡ Poster SQL

```sql
SELECT Friend
FROM Life
WHERE Loyalty = '100%'
LIMIT 1;
```

---

## 🎯 Why LIMIT?

- आवश्यक तेवढाच Data मिळवण्यासाठी.
- Query Fast करण्यासाठी.
- Dashboard आणि Reports मध्ये Top Records दाखवण्यासाठी.
- Large Database मधून Sample Data पाहण्यासाठी.

---

## 💼 Business Example

एका E-commerce कंपनीला सर्वात अलीकडील Order पाहायची आहे.

```sql
SELECT Order_ID,
       Customer_Name
FROM Orders
ORDER BY Order_Date DESC
LIMIT 1;
```

यामुळे फक्त नवीन Order मिळते.

---

## ⚔️ Swarajya Lesson

> **"मित्रांची संख्या महत्त्वाची नसते...
> निष्ठा महत्त्वाची असते."**

शंभर ओळखींपेक्षा...

**एक निष्ठावान माणूस आयुष्य बदलू शकतो.**

**Quality निवडा... Quantity नाही.**