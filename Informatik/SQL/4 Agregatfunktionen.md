---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:25**

---
### 3-12
#### a
```SQL
SELECT SUM(Kosten) AS Gesamtkosten FROM instandhaltung
```
#### b
```SQL
SELECT MAX(Anschaffungskosten) AS Max_Kosten FROM fahrzeug
```
#### c
```SQL
SELECT MIN(Beitrag) AS min_Beitrag FROM versicherungsvertrag
```
#### d
```
SELECT COUNT(*) AS mit FROM mitarbeiter
//oder count ID
```