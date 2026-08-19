# Day 48 – ROLLBACK ⚔️

## ⚔️ Concept: चूक मान्य करून निर्णय मागे घेणे म्हणजे ROLLBACK

SQL मध्ये **TRANSACTION** दरम्यान काही चुकीचे changes झाले किंवा plan अपेक्षेप्रमाणे काम करत नसेल, तर `ROLLBACK` वापरून ते changes मागे घेता येतात.

म्हणजेच...

**BEGIN → प्रक्रिया सुरू करा**

**WRONG DECISION → चूक लक्षात आली**

**ROLLBACK → बदल मागे घ्या**

---

## 🛡️ Historical Analogy

प्रतापगडाच्या जंगलात चुकीची माहिती मिळाल्यामुळे जुना युद्धाचा plan बदलण्याची वेळ आली.

जुना plan होता:

**"Open Field Meeting" ❌**

पण परिस्थिती बदलली.

नवीन plan:

**"Forest, One to One" ⚔️**

चूक लक्षात आल्यावर जुन्या plan ला चिकटून राहणे म्हणजे हट्ट.

जुना plan फाडून योग्य strategy स्वीकारणे म्हणजे **ROLLBACK**.

**अभिमान नाही, स्वराज्य मोठं.**

---

## 💻 SQL Example

```sql
BEGIN TRANSACTION Meeting;

-- Wrong information received

ROLLBACK;

-- New plan executed