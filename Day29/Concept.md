# Day-29 SQL Swarajya Goshti – ORDER DESC
---

# 🎯 Concept

SQL मध्ये `ORDER BY` डेटा क्रमाने लावण्यासाठी वापरले जाते.

- **ASC (Ascending)** → लहान ते मोठे, खालीपासून वर, वाढत्या क्रमाने.
- **DESC (Descending)** → मोठे ते लहान, वरून खाली, घटत्या क्रमाने.

हिरकणीची गोष्ट हा फरक लक्षात ठेवण्यासाठी सर्वोत्तम उदाहरण आहे.

---

# 🏰 इतिहासाशी जोडलेला SQL

दिवसा हिरकणी दुध विकण्यासाठी **रायगडाच्या महादरवाजातून पायऱ्या चढून** गडावर आली.

संध्याकाळी दरवाजे बंद झाले.

रात्री आपल्या बाळाच्या ओढीने तिने **हिरकणी बुरुजाच्या कड्यावरून खाली उतरून** इतिहास घडवला.

---

# SQL Memory Trick

⬆️ **ASC**
> पायऱ्यांनी गड चढली.

⬇️ **DESC**
> कड्यावरून उतरली.

---

# SQL Query

```sql
SELECT Strength
FROM Mother
ORDER BY Love DESC;
```

---

# Poster Caption

**ORDER BY DESC**

पोटासाठी चढली  
मायेसाठी उतरली  
म्हणून म्हणतात हिरकणी.

**धैर्य. ममता. ⚔️👶**

---

# Interview Note

**ORDER BY ASC**
- Default sorting order.
- Small → Large
- A → Z
- Oldest → Newest

**ORDER BY DESC**
- Reverse sorting.
- Large → Small
- Z → A
- Newest → Oldest

---

# Real-World Business Example

### ASC

```sql
SELECT Product_Name, Price
FROM Products
ORDER BY Price ASC;
```

👉 सर्वात स्वस्त प्रॉडक्ट आधी दिसतील.

---

### DESC

```sql
SELECT Employee_Name, Salary
FROM Employees
ORDER BY Salary DESC;
```

👉 सर्वाधिक पगार असलेले कर्मचारी आधी दिसतील.

---

# Remember Forever

🏰 हिरकणी...

**ASC → पायऱ्यांनी गड चढली.**

**DESC → मायेसाठी कडा उतरली.**

इतिहास विसरला तरी SQL कधी विसरणार नाही.