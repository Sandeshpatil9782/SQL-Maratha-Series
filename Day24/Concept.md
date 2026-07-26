# Day 24 – COMMENT ON ⚔️

## ⚔️ Concept: इतरांच्या बोलण्याला महत्व देऊ नका

प्रत्येक यशस्वी व्यक्तीबद्दल लोक बोलतात.

कोणी टीका करतो.
कोणी हसतो.
कोणी कमी लेखतो.

पण इतिहास नेहमी त्यांचाच लिहिला जातो,
जे स्वतःच्या ध्येयावर लक्ष ठेवतात.

SQL मध्ये **COMMENT ON** वापरून आपण एखाद्या Table, Column किंवा Object बद्दल माहिती लिहितो.

Comment हा Data बदलत नाही.

तो फक्त संदर्भ (Context) देतो.

तसंच आयुष्यात...

लोकांच्या Comments तुमचं आयुष्य बदलत नाहीत.

तुमचे निर्णय आणि कृतीच तुमचं भविष्य घडवतात.

---

## 🛡 Swarajya Analogy

महाराजांवर अनेकांनी टीका केली.

अनेकांनी त्यांना थांबवण्याचा प्रयत्न केला.

पण त्यांनी प्रत्येक Comment ला उत्तर देण्यात वेळ घालवला नाही.

त्यांनी फक्त Swarajya उभं केलं.

काम इतकं मोठं करा,
की लोकांचे Comment आपोआप शांत होतील.

---

## 💻 SQL Syntax

```sql
COMMENT ON TABLE table_name
IS 'Description';
```

---

## 🌍 Real World SQL

**Table Description**

```sql
COMMENT ON TABLE Employees
IS 'Stores employee master records.';
```

**Column Description**

```sql
COMMENT ON COLUMN Employees.Salary
IS 'Monthly salary in INR.';
```

---

## ⚡ Poster SQL

```sql
COMMENT ON Life
IS 'Focus on your Karma, Ignore the Noise';
```

---

## 🎯 Why COMMENT ON?

- Documentation सुधारते.
- Team ला Database समजायला सोपं जातं.
- Column किंवा Table चा Purpose स्पष्ट होतो.
- Production Projects मध्ये Best Practice मानली जाते.

---

## ⚔️ Swarajya Lesson

> **"लोक काय बोलतात यापेक्षा...
> तुम्ही काय निर्माण करता हे जास्त महत्त्वाचं असतं."**

Comment ऐकून थांबू नका.

**काम करा...
इतिहास स्वतः तुमच्यावर Comment करेल.**