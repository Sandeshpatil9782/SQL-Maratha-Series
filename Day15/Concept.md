# Day 15: ALTER TABLE - ADD COLUMN ⚔️ | SQL Swarajya Goshti

## 📜 Concept: एकजुटीने वाढ

> **"सगळ्यांना मिळून घेऊन चालू..."**  
> **"एकट्याने नाही, एकजुटीने वाढू."**

स्वराज्य वाढलं तसं किल्ल्यात नवीन बुरूज, दरवाजे आणि तट जोडले गेले.

**जुना किल्ला पाडला नाही...**
**फक्त त्यात नवीन भाग जोडले.**

Database मध्येही हेच होतं.

जेव्हा नवीन माहिती साठवायची गरज निर्माण होते,
तेव्हा नवीन Table तयार न करता,
Existing Table मध्ये नवीन Column जोडला जातो.

यालाच **ALTER TABLE ... ADD COLUMN** म्हणतात.

---

# 💻 Definition

`ALTER TABLE ... ADD COLUMN` चा वापर Existing Table मध्ये नवीन Column जोडण्यासाठी केला जातो.

जुना Data तसाच राहतो.

---

# 📌 Syntax

```sql
ALTER TABLE Mavale
ADD COLUMN salary INT;
```

---

## Before

| ID | Name | Rank |
|---:|------|--------|
|1|Tanaji|Sardar|
|2|Yesaji|Sipahi|

---

## After

| ID | Name | Rank | Salary |
|---:|------|--------|--------:|
|1|Tanaji|Sardar|NULL|
|2|Yesaji|Sipahi|NULL|

---

# 💼 Real World Example

Company मध्ये आधी Employee चे फक्त नाव आणि Department Store होत होते.

नंतर Salary Track करायचा निर्णय झाला.

```sql
ALTER TABLE Employee
ADD COLUMN salary DECIMAL(10,2);
```

पूर्ण Table पुन्हा तयार करण्याची गरज पडली नाही.

---

# ✅ Key Points

- Existing Table बदलतो.
- नवीन Column जोडला जातो.
- जुना Data सुरक्षित राहतो.
- Business Requirements बदलल्यावर खूप वापरला जातो.

---

# ⚔️ SQL Swarajya Rule

> **"वाढ म्हणजे जुने मोडणे नाही..."**  
> **"वाढ म्हणजे त्यात नवीन शक्ती जोडणे."**

**SQL मध्ये:**

> **"New Requirement?"**  
> **"Add a New Column, Not a New Table."**