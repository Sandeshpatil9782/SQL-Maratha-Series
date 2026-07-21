# Day 19: TRUNCATE TABLE ⚔️ | SQL स्वराज्य गोष्टी

## 📜 Concept: नव्या सुरुवातीसाठी जागा करा

> **"आयुष्य तेच असतं..."**  
> **"फक्त नकारात्मक गोष्टी बाहेर काढायच्या असतात."**

स्वराज्यात किल्ला तसाच राहायचा...

पण अनावश्यक सामान, जुनी नोंद किंवा निरुपयोगी वस्तू काढून टाकल्या जायच्या.

**किल्ला पाडला जात नव्हता...**

**फक्त नव्या सुरुवातीसाठी जागा तयार केली जायची.**

Database मध्येही असंच होतं.

जेव्हा Table ची रचना (Structure) ठेवायची असते,
पण त्यातील सर्व Data हटवायचा असतो,

तेव्हा **TRUNCATE TABLE** वापरला जातो.

---

# 💻 Definition

`TRUNCATE TABLE` चा वापर Table मधील सर्व Records एकाच वेळी Delete करण्यासाठी केला जातो.

Table ची Structure कायम राहते.

---

# 📌 Syntax

```sql
TRUNCATE TABLE Nakaratmak_data;
```

---

## Before

| ID | Name |
|---:|------|
|1|Tanaji|
|2|Yesaji|
|3|Baji|

---

## Execute

```sql
TRUNCATE TABLE Nakaratmak_data;
```

---

## After

| ID | Name |
|---:|------|
| *(No Records)* | |

✅ Table रिकामा झाला.

✅ पण Table अजूनही Database मध्ये आहे.

---

# 💼 Real World Example

Monthly Report तयार करण्यापूर्वी Temporary Data रिकामा करायचा आहे.

```sql
TRUNCATE TABLE Temp_Report;
```

यामुळे जुना Data हटतो आणि नवीन Data साठी Table तयार राहतो.

---

# ✅ Key Points

- सर्व Records Delete होतात.
- Table Structure Delete होत नाही.
- `DELETE` पेक्षा जलद असतो.
- Temporary किंवा Test Data साफ करण्यासाठी वापरला जातो.

---

# ⚔️ SQL स्वराज्य नियम

> **"जुनं ओझं सोडा..."**  
> **"नव्या सुरुवातीसाठी स्वतःला तयार करा."**

**SQL मध्ये:**

> **"Remove the Data..."**  
> **"Keep the Table Ready."** ⚔️