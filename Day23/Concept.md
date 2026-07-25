# Day 23 : DELETE FROM ⚔️ | SQL Swarajya Goshti

## 📜 Concept: जे उपयोगाचं नाही, ते काढून टाका

स्वराज्यात प्रत्येक गोष्ट जपली जात होती, पण जी गोष्ट राज्याच्या प्रगतीत अडथळा ठरत होती, ती योग्य वेळी हटवलीही जात होती.

तसंच Database मध्ये DELETE FROM वापरून गरज नसलेली Row काढून टाकली जाते.

जी माहिती आता उपयोगाची नाही, ती ठेवून Database मोठा आणि अव्यवस्थित करण्यापेक्षा ती हटवणं योग्य.

आयुष्यातही तसंच आहे.

लोभ, मोह, अहंकार, नकारात्मक विचार...
हे मनात साठवत बसलात तर पुढे जाता येत नाही.

जे प्रगतीत अडथळा आणतं,
ते Delete करायला शिका.

---

## ⚔️ SQL Syntax

```sql
DELETE FROM table_name
WHERE condition;
```

---

## 💻 Example

```sql
DELETE FROM Mind
WHERE Emotion IN ('Lobh', 'Moh', 'Ahankar');
```

---

## 📌 Real World Example

एका कंपनीत काम सोडून गेलेल्या कर्मचाऱ्यांची माहिती Employee टेबलमध्ये आहे.

त्यांची नोंद काढण्यासाठी:

```sql
DELETE FROM Employee
WHERE Status = 'Inactive';
```

---

## 🎯 Life Lesson

मन हलकं करायचं असेल,
तर अनावश्यक गोष्टी Delete कराव्याच लागतात.

Database असो किंवा आयुष्य...

योग्य गोष्टी ठेवा,
बाकी DELETE करा.

---

## 🚀 SQL Swarajya Mantra

DELETE करा...
पण विचार करून.

कारण एकदा Row Delete झाली,
तर ती परत आणणं नेहमीच सोपं नसतं.

⚔️ नियम. शिस्त. मुक्ती.