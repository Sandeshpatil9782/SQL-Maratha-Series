# Day 47 – COMMIT ⚔️

## ⚔️ Concept: निर्णय पक्का करणे म्हणजे COMMIT

SQL मध्ये **TRANSACTION** मधील सर्व changes योग्य आहेत याची खात्री झाल्यावर `COMMIT` वापरला जातो.

`COMMIT` केल्यानंतर transaction मधील changes **permanently save** होतात.

म्हणजेच...

**BEGIN → प्रक्रिया सुरू करा**

**COMMIT → निर्णय पक्का करा**

---

## 🛡️ Historical Analogy

रायगडाच्या दरबारात एखादा निर्णय घेण्यापूर्वी संपूर्ण विचार केला जातो.

परिस्थिती तपासली जाते.  
योजना निश्चित केली जाते.  
सगळं योग्य आहे याची खात्री केली जाते.

पण एकदा अंतिम निर्णय घेतला की...

**शिक्कामोर्तब झालं म्हणजे झालं.  
आता माघार नाही.**

SQL मधील `COMMIT` अगदी हेच दर्शवतो.

---

## 💻 SQL Example

```sql
BEGIN TRANSACTION;

UPDATE Mavale
SET Status = 'Active'
WHERE Mavla_ID = 101;

COMMIT;