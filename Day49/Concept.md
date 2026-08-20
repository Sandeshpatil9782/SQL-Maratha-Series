# Day 49 – SAVEPOINT ⚔️

## ⚔️ Concept: मोठ्या Transaction मध्ये छोटे checkpoints म्हणजे SAVEPOINT

SQL मध्ये **SAVEPOINT** वापरून transaction च्या आत एक specific checkpoint तयार करता येतो.

पूर्ण transaction `ROLLBACK` करण्याऐवजी, आपण एखाद्या specific SAVEPOINT पर्यंतच changes मागे घेऊ शकतो.

म्हणजेच...

**BEGIN → Transaction सुरू करा**

**SAVEPOINT → एक checkpoint तयार करा**

**ROLLBACK TO SAVEPOINT → त्या checkpointपर्यंत मागे जा**

**COMMIT → शेवटी योग्य changes कायम करा**

---

## 🏰 Historical Analogy

सह्याद्रीतून मोठा प्रवास करताना प्रत्येक किल्ला एक checkpoint समजा.

**PANHALA → SAVEPOINT 1**

पहिला टप्पा पूर्ण.

**GHODKHIND → SAVEPOINT 2**

मोठा संघर्ष झाला, पण पुढचा मार्ग सुरू ठेवला.

**VISHALGAD → SAVEPOINT 3**

अंतिम सुरक्षित ठिकाण.

मोठं ध्येय एकाच उडीने गाठायचं नसतं.

**पायरी पायरीने पुढे जायचं.**

एखाद्या टप्प्यावर चूक झाली तर संपूर्ण प्रवास सुरुवातीपासून सुरू करण्याची गरज नाही.

जिथे SAVEPOINT तयार केला आहे, तिथून पुढे जाता येतं.

---

## 💻 SQL Example

```sql
START TRANSACTION;

UPDATE Mavale
SET Status = 'Ready'
WHERE Mavla_ID = 101;

SAVEPOINT Panhala;

UPDATE Mavale
SET Location = 'Ghodkhind'
WHERE Mavla_ID = 101;

SAVEPOINT Ghodkhind;

UPDATE Mavale
SET Location = 'Vishalgad'
WHERE Mavla_ID = 101;

SAVEPOINT Vishalgad;

COMMIT;