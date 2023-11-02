---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:25**

---
### 3-1
#### a
```SQL
SELECT Kennzeichen, Anschaffungskosten FROM fahrzeug
```
#### b
```SQL
SELECT * FROM fahrzeug
```
#### c
```SQL
SELECT Beginn, Ende, Zweck FROM reservierung
```
## **DISTINCT**
### 3-2
#### a
```SQL
SELECT DISTINCT Hersteller FROM fahrzeugmodell
```
#### b
```SQL
SELECT DISTINCT Zweck FROM reservierung
```
## **ORDERD BY**
### 3-3
#### a
```SQL
SELECT ID, Beitrag FROM versicherungsvertrag
ORDER BY Beitrag DESC
```
#### b
```SQL
SELECT Beginn, Ende, Zweck FROM reservierung
ORDER BY Beginn ASC, Ende ASC
```
#### c
```SQL
SELECT Anschaffungsdatum, Anschaffungskosten, Kennzeichen FROM fahrzeug
ORDER BY Anschaffungsdatum ASC, Anschaffungsdatum DESC
```
## **WHERE**
### **3-4**
#### a
```SQL
SELECT * FROM reservierung
WHERE Zweck = "Messe"
```
#### b
```SQL
SELECT * FROM instandhaltung
WHERE KmStand < 12000 ORDER BY KmStand ASC
```
#### c
```SQL
SELECT * FROM fahrzeug
WHERE Anschaffungsdatum >= "01-01-2015"
ORDER BY Anschaffungsdatum DESC, Fahrzeugmodell_ID ASC
```
---
### **3-5** 
```SQL
SELECT Bezeichnung, Kraftstoff, Verbrauch FROM fahrzeugmodell
WHERE Kraftstoff = "Diesel" AND Verbrauch <= 5
```
```SQL
SELECT * FROM Instandhaltung
WHERE Kosten <= 350 OR Kosten > 600
```
---
### **3-6**
```SQL
SELECT Kennzeichen, Anschaffungskosten FROM fahrzeug
WHERE Anschaffungskosten BETWEEN 26000 AND 30000
ORDER BY Anschaffungskosten DESC
```
---
### **3-7**
```SQL
SELECT * FROM fahrzeug
WHERE Kennzeichen IN ("HN-AB-45", "TBB-A-678", "TBB-D-9781", "WÜ-A-2435")
```
---
### **3-8**
#### a
```SQL
SELECT * FROM fahrzeug
WHERE Kennzeichen LIKE "TBB%"
```
#### b
```SQL
SELECT Bezeichnung, Kraftstoff, Verbrauch FROM fahrzeugmodell
WHERE Bezeichnung LIKE "%TDI%"
```
#### c
```SQL
SELECT * FROM fahrzeug
WHERE Kennzeichen LIKE "TBB%73%";
```
## **JOIN**
### **3-9**
#### a
```SQL
SELECT Beginn, Ende, PersNr, Nachname FROM reservierung
INNER JOIN mitarbeiter ON Mitarbeiter_ID = mitarbeiter.ID

SELECT Beginn, Ende, PersNr, Nachname FROM reservierung, mitarbeiter
Where Mitarbeiter_ID = mitarbeiter.ID
```
---
#### b
```SQL
SELECT VersNr, Kennzeichen, Kasko
FROM Versicherungsvertrag INNER JOIN Fahrzeug ON Fahrzeug_ID = Fahrzeug.ID;

SELECT VersNr, Kennzeichen, Kasko
FROM Versicherungsvertrag, Fahrzeug Fahrzeug
WHERE Fahrzeug_ID = Fahrzeug.ID;
```
---
#### c
```SQL
SELECT  Kennzeichen, Hersteller, Bezeichnung 
FROM fahrzeug INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID 
WHERE Hersteller = "VW"
ORDER BY Bezeichnung DESC

SELECT  Kennzeichen, Hersteller, Bezeichnung 
FROM fahrzeug, fahrzeugmodell
WHERE Hersteller = "VW" AND Fahrzeugmodell_ID = fahrzeugmodell.ID
ORDER BY Bezeichnung DESC
```
---
#### d
```SQL
SELECT Datum, Kosten, Kennzeichen, Anschaffungsdatum
FROM Instandhaltung INNER JOIN Fahrzeug ON Fahrzeug_ID = Fahrzeug.ID
WHERE Kosten BETWEEN 300 AND 500
ORDER BY Kosten ASC;

SELECT Datum, Kosten, Kennzeichen, Anschaffungsdatum
FROM Instandhaltung, Fahrzeug 
WHERE Fahrzeug_ID = Fahrzeug.ID AND Kosten BETWEEN 300 AND 500
ORDER BY Kosten ASC;
```