# Day 4: CREATE TABLE ⚔️ | SQL Swarajya Goshti

## 📜 Concept: स्वराज्याचं पहिलं खातं

राज्यात प्रवेश केला, गादीवर बसलो. पण कारभार फक्त बोलून चालत नाही. **नोंदी ठेवाव्या लागतात. खाती उघडावी लागतात.**

छत्रपती शिवाजी महाराजांनी स्वराज्य स्थापन केल्यावर पहिलं काम केलं - **जमाखर्चाची वही सुरू केली.** मावळ्यांची नोंद, किल्ल्यांचा हिशोब, शेतसाऱ्याचा ताळेबंद - प्रत्येक गोष्टीसाठी वेगळं खातं.

`CREATE DATABASE` म्हणजे वाडा बांधणे. `USE` म्हणजे वाड्यात प्रवेश करणे.  
आणि `CREATE TABLE` म्हणजे त्या वाड्यात पहिली वही, पहिलं खातं उघडणे.

वही शिवाय कारभार नाही. Table शिवाय Database नाही.

## 💻 SQL Command: `CREATE TABLE`

### **1. Syntax**
```sql
CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints,
    column3 datatype constraints,
    ...
);
