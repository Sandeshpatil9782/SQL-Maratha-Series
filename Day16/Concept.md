# Day 16: ALTER TABLE - MODIFY COLUMN ⚔️ | SQL Swarajya Goshti

## 📜 Concept: सतत सुधारणा

> **"जुनं आहे पण कमजोर नाही..."**  
> **"तरी पण अजून सुधार करू."**

स्वराज्यात किल्ले मजबूत होते.

पण वेळेनुसार त्यांचे तट अधिक भक्कम केले गेले.

जुना किल्ला बदलला नाही...

**फक्त त्याला आणखी मजबूत बनवलं.**

Database मध्येही असंच होतं.

कधी Column चा Data Type, Size किंवा Property बदलण्याची गरज पडते.

नवीन Column तयार न करता,
त्याच Column मध्ये सुधारणा केली जाते.

यालाच **ALTER TABLE ... MODIFY COLUMN** म्हणतात.

---

# 💻 Definition

`ALTER TABLE ... MODIFY COLUMN` चा वापर Existing Column चा Data Type, Size किंवा Property बदलण्यासाठी केला जातो.

Data ची Structure सुधारली जाते.

---

# 📌 Syntax

```sql
ALTER TABLE Mavale
MODIFY COLUMN salary DECIMAL(10,2);
```

---

## Before

| ID | Name | Salary |
|---:|------|--------:|
|1|Tanaji|50000|
|2|Yesaji|65000|

**Salary Data Type:** `INT`

---

## After

| ID | Name | Salary |
|---:|------|---------:|
|1|Tanaji|50000.50|
|2|Yesaji|65000.75|

**Salary Data Type:** `DECIMAL(10,2)`

---

# 💼 Real World Example

सुरुवातीला Employee Salary पूर्ण आकड्यांमध्ये Store केली जात होती.

नंतर Decimal Salary Store करण्याची गरज निर्माण झाली.

```sql
ALTER TABLE Employee
MODIFY COLUMN salary DECIMAL(10,2);
```

यामुळे नवीन गरज पूर्ण झाली, पण Table बदलावा लागला नाही.

---

# ✅ Key Points

- Existing Column Modify करतो.
- Data Type किंवा Size बदलता येतो.
- Table पुन्हा तयार करण्याची गरज नसते.
- Business Requirements नुसार Database सुधारता येतो.

---

# ⚔️ SQL Swarajya Rule

> **"सुधारणा म्हणजे जुने टाकून देणे नाही..."**  
> **"सुधारणा म्हणजे जे आहे त्याला अधिक सक्षम बनवणे."**

**SQL मध्ये:**

> **"Don't Replace the Column..."**  
> **"Improve the Column."** ⚔️