# Inner join
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
> in der Tabelle Fahrzeuge gibt es eine Spalte namens Fahrzeugmodell_ID diese ID gehört dann zu einer ID in der Tabelle Fahrzeugmodel in der Spalte ID
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
> Bei der Between bedingung gehören die äußeren Werte mit dazu 
300 Between 500 -> 300 <= x <= 500
### 3-10
#### a
```SQL
SELECT VersNr, Kennzeichen, Firma FROM versicherungsvertrag
INNER JOIN fahrzeug ON Fahrzeug_ID = fahrzeug.ID
INNER JOIN versicherungsgesellschaft ON Gesellschaft_ID = versicherungsgesellschaft.ID

SELECT VersNr, Kennzeichen, Firma FROM versicherungsvertrag, fahrzeug, versicherungsgesellschaft
WHERE fahrzeug ON Fahrzeug_ID = fahrzeug.ID AND Gesellschaft_ID = versicherungsgesellschaft.ID
```
#### b
```SQL
SELECT Beginn, Ende, Kennzeichen, Bezeichnung FROM Reservierung
INNER JOIN Fahrzeug ON Reservierung.Fahrzeug_ID = Fahrzeug.ID
INNER JOIN Fahrzeugmodell ON Fahrzeug.Fahrzeugmodell_ID = Fahrzeugmodell.ID

SELECT Beginn, Ende, Kennzeichen, Bezeichnung FROM Reservierung, Fahrzeug, Fahrzeugmodell
WHERE Fahrzeug_ID = Fahrzeug.ID AND Fahrzeugmodell_ID = Fahrzeugmodell.ID
```
#### c
```SQL
SELECT Beginn, Ende, Nachname, Kennzeichen, Bezeichnung FROM Reservierung
INNER JOIN Mitarbeiter ON Reservierung.Mitarbeiter_ID = Mitarbeiter.ID
INNER JOIN Fahrzeug ON Reservierung.Fahrzeug_ID = Fahrzeug.ID
INNER JOIN Fahrzeugmodell ON Fahrzeug.Fahrzeugmodell_ID = Fahrzeugmodell.ID;

SELECT Beginn, Ende, Nachname, Kennzeichen, Bezeichnung FROM Reservierung, Fahrzeug, Fahrzeugmodell
WHERE Reservierung.Mitarbeiter_ID = Mitarbeiter.ID AND Reservierung.Fahrzeug_ID = Fahrzeug.ID 
AND Fahrzeugmodell_ID = Fahrzeugmodell.ID;
```