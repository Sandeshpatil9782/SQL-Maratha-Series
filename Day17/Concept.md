# Day 17: ALTER TABLE - DROP COLUMN ⚔️ | SQL स्वराज्य गोष्टी
## 📜 Concept: निरुपयोगी गोष्टी दूर करा

> **"चांगले विचार ठेवा..."**  
> **"वाईट विचार काढून टाका."**

स्वराज्यात प्रत्येक नोंदीला महत्त्व होतं.

पण ज्या गोष्टींची गरज उरली नाही,
त्या काढून टाकल्या जायच्या.

कारण...

**अनावश्यक गोष्टी जागा घेतात.**

Database मध्येही असंच होतं.

जेव्हा एखादा Column भविष्यात उपयोगाचा राहत नाही,
तेव्हा तो Table मधून काढून टाकला जातो.

यालाच **ALTER TABLE ... DROP COLUMN** म्हणतात.

---

# 💻 Definition

`ALTER TABLE ... DROP COLUMN` चा वापर Existing Table मधून गरज नसलेला Column कायमचा काढण्यासाठी केला जातो.

---

# 📌 Syntax

```sql
ALTER TABLE Mavale
DROP COLUMN temp_id;
```

---

## Before

| ID | Name | Rank | Temp_ID |
|---:|------|--------|---------:|
|1|Tanaji|Sardar|101|
|2|Yesaji|Sipahi|102|

---

## After

| ID | Name | Rank |
|---:|------|--------|
|1|Tanaji|Sardar|
|2|Yesaji|Sipahi|

---

# 💼 Real World Example

Company मध्ये `temp_id` हा Column फक्त Migration साठी वापरला गेला होता.

काम पूर्ण झाल्यानंतर तो आवश्यक राहिला नाही.

```sql
ALTER TABLE Employee
DROP COLUMN temp_id;
```

यामुळे Table अधिक स्वच्छ आणि सोपा झाला.

---

# ✅ Key Points

- Existing Column Delete करतो.
- Column मधील Data कायमचा हटतो.
- गरज नसलेले Columns काढण्यासाठी वापरला जातो.
- Database अधिक स्वच्छ आणि Maintainable बनतो.

---

# ⚔️ SQL Swarajya Rule

> **"जे उपयोगाचं नाही..."**  
> **"ते सोडून दिलं की प्रगतीचा मार्ग मोकळा होतो."**

**SQL मध्ये:**

> **"Remove Unused Columns..."**  
> **"Keep Your Database Clean."** ⚔️