## **Select**
- SELECT Kennzeichen, Anschaffungskosten FROM fahrzeug

- SELECT * FROM fahrzeug

- SELECT Beginn, Ende, Zweck FROM reservierung


## **DISTINCT**
- SELECT DISTINCT Hersteller FROM fahrzeugmodell

- SELECT DISTINCT Zweck FROM reservierung

## **ORDERD BY**
- SELECT ID, Beitrag FROM versicherungsvertrag
ORDER BY Beitrag DESC

- SELECT Beginn, Ende, Zweck FROM reservierung
ORDER BY Beginn ASC, Ende ASC

- SELECT Anschaffungsdatum, Anschaffungskosten, Kennzeichen FROM fahrzeug
ORDER BY Anschaffungsdatum ASC, Anschaffungsdatum DESC

## **WHERE**
### 3-4
- SELECT * FROM reservierung
WHERE Zweck = "Messe"

- SELECT * FROM instandhaltung
WHERE KmStand < 12000 ORDER BY KmStand ASC

- SELECT * FROM fahrzeug
WHERE Anschaffungsdatum >= "01-01-2015"
ORDER BY Anschaffungsdatum DESC, Fahrzeugmodell_ID ASC

---

### **3-5** 
- SELECT Bezeichnung, Kraftstoff, Verbrauch FROM fahrzeugmodell
WHERE Kraftstoff = "Diesel" AND Verbrauch <= 5

- SELECT * FROM Instandhaltung
WHERE Kosten <= 350 OR Kosten > 600

---

### **3-6**

- SELECT Kennzeichen, Anschaffungskosten FROM fahrzeug
 WHERE Anschaffungskosten BETWEEN 26000 AND 30000
 ORDER BY Anschaffungskosten DESC

---

### **3-7**
- SELECT * FROM fahrzeug
WHERE Kennzeichen IN ("HN-AB-45", "TBB-A-678", "TBB-D-9781", "WÜ-A-2435")

---

### **3-8**
- SELECT * FROM fahrzeug
WHERE Kennzeichen LIKE "TBB%"

- SELECT Bezeichnung, Kraftstoff, Verbrauch FROM fahrzeugmodell
WHERE Bezeichnung LIKE "%TDI%"

- SELECT * FROM fahrzeug
WHERE Kennzeichen LIKE "TBB%73%";

## **JOIN**
- SELECT Beginn, Ende, PersNr, Nachname FROM reservierung
INNER JOIN mitarbeiter ON Mitarbeiter_ID = mitarbeiter.ID

- SELECT Beginn, Ende, PersNr, Nachname FROM reservierung, mitarbeiter
Where Mitarbeiter_ID = mitarbeiter.ID

---

- SELECT VersNr, Kennzeichen, Kasko
FROM Versicherungsvertrag INNER JOIN Fahrzeug ON Fahrzeug_ID = Fahrzeug.ID;

- SELECT VersNr, Kennzeichen, Kasko
FROM Versicherungsvertrag, Fahrzeug Fahrzeug
WHERE Fahrzeug_ID = Fahrzeug.ID;
---
![Picture](https://media.discordapp.net/attachments/1139161006761857024/1139299615842254919/image.png?width=1442&height=99)
```SQL
SELECT  Kennzeichen, Hersteller, Bezeichnung 
FROM fahrzeug INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID 
WHERE Hersteller = "VW"
ORDER BY Bezeichnung DESC
```

```SQL
SELECT  Kennzeichen, Hersteller, Bezeichnung 
FROM fahrzeug, fahrzeugmodell
WHERE Hersteller = "VW" AND Fahrzeugmodell_ID = fahrzeugmodell.ID
ORDER BY Bezeichnung DESC
```
> in der Tabelle Fahrzeuge gibt es eine Spalte namens Fahrzeugmodell_ID diese ID gehört dann zu einer ID in der Tabelle Fahrzeugmodel in der Spalte ID
---
- SELECT Datum, Kosten, Kennzeichen, Anschaffungsdatum
FROM Instandhaltung INNER JOIN Fahrzeug ON Fahrzeug_ID = Fahrzeug.ID
WHERE Kosten BETWEEN 300 AND 500
ORDER BY Kosten ASC;

- SELECT Datum, Kosten, Kennzeichen, Anschaffungsdatum
FROM Instandhaltung, Fahrzeug 
WHERE Fahrzeug_ID = Fahrzeug.ID AND Kosten BETWEEN 300 AND 500
ORDER BY Kosten ASC;

> Bei der Between bedingung gehören die äußeren Werte mit dazu 
300 Between 500 -> 300 <= x <= 500