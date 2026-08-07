# Day 36 – SELF JOIN

# 🪞 SQL Swarajya Goshti – SELF JOIN

## 🧠 Concept

रायगडाच्या दरबारात एक मावळा आरशासमोर उभा होता.

आरशात त्याचाच दुसरा चेहरा दिसत होता.

एक **शिष्य**...

आणि दुसरा **गुरू**...

दोघेही वेगळे नव्हते.

व्यक्ती एकच होती...

भूमिका दोन होत्या.

माणूस आयुष्यात कधी शिकवतो,
तर कधी शिकतो.

**स्वतःशी संवाद झाला कीच खरी ओळख होते.**

यालाच SQL मध्ये **SELF JOIN** म्हणतात.

---

# 💻 SQL Syntax

```sql
SELECT
    e1.Name,
    e2.Name AS Guru
FROM MavaLe e1
JOIN MavaLe e2
ON e1.GuruID = e2.ID;
```

---

# 🔍 Explanation

`SELF JOIN` म्हणजे **त्याच Table ला स्वतःशीच Join करणे.**

एका Table ला दोन वेगवेगळी नावे (Aliases) दिली जातात.

- `e1` → शिष्य
- `e2` → गुरू

दोन्ही डेटा एकाच Table मधून येतो, पण भूमिका वेगळ्या असतात.

---

# 🌍 Real World Example

एका कंपनीत प्रत्येक Employee चा Manager देखील Employee Table मध्येच असतो.

```sql
SELECT
    e1.Employee_Name,
    e2.Employee_Name AS Manager
FROM Employees e1
JOIN Employees e2
ON e1.Manager_ID = e2.Employee_ID;
```

---

# ⚔️ Swarajya Learning

स्वतःला समजून घ्यायचं असेल...

तर स्वतःशीच संवाद साधावा लागतो.

कधी आपण शिष्य असतो...

कधी आपणच कुणाचे गुरू असतो.

---

# 📌 Moral

> **एक व्यक्ती... दोन भूमिका.**
>
> **SELF JOIN शिकवतो — स्वतःशी जोडल्याशिवाय खरी ओळख होत नाही.**