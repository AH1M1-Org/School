---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:26**

---
### 3-13
#### a
```SQL
SELECT Bezeichnung, AVG(Anschaffungskosten) AS AK_Durchschnitt FROM Fahrzeug 
INNER JOIN Fahrzeugmodell ON Fahrzeugmodell_ID = Fahrzeugmodell.ID
GROUP BY Bezeichnung

SELECT Bezeichnung, AVG(Anschaffungskosten) AS AK_Durchschnitt FROM Fahrzeug, Fahrzeugmodell
WHERE Fahrzeugmodell_ID = Fahrzeugmodell.ID
GROUP BY Bezeichnung
```
#### b
```SQL
SELECT Bezeichnung, Anschaffungskosten, AVG(Anschaffungskosten) AS Durschnitt From fahrzeug
INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID
GROUP BY Bezeichnung

SELECT Bezeichnung, Anschaffungskosten, AVG(Anschaffungskosten) AS Durschnitt From fahrzeug, fahrzeugmodell
WHERE Fahrzeugmodell_ID = fahrzeugmodell.ID
GROUP BY Bezeichnung
```
#### c
```SQL
SELECT Nachname, Vorname, COUNT(*) AS Anzahl_Reservierungen
FROM Reservierung INNER JOIN Mitarbeiter ON Mitarbeiter_ID = Mitarbeiter.ID
GROUP BY Mitarbeiter.ID

SELECT Nachname, Vorname, COUNT(*) AS Anzahl_Reservierungen
FROM Reservierung, Mitarbeiter
WHERE INNER JOIN Mitarbeiter_ID = Mitarbeiter.ID 
GROUP BY Mitarbeiter.ID
```
#### d
```SQL
SELECT Hersteller, Bezeichnung, COUNT(*) AS Anzahl
FROM Fahrzeug INNER JOIN Fahrzeugmodell ON Fahrzeugmodell_ID =F ahrzeugmodell.ID
GROUP BY Bezeichnung

SELECT Hersteller, Bezeichnung, COUNT(*) AS Anzahl
FROM Fahrzeug, Fahrzeugmodell 
WHERE Fahrzeugmodell_ID = Fahrzeugmodell.ID
GROUP BY Bezeichnung
```
#### e
```SQL
SELECT Hersteller, Bezeichnung, SUM(Kosten) AS Gesammtkosten FROM fahrzeug
INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID
INNER JOIN instandhaltung ON Fahrzeug_ID = fahrzeug.ID
GROUP BY Bezeichnung

SELECT Hersteller, Bezeichnung, SUM(Kosten) AS Gesammtkosten FROM fahrzeug, fahrzeugmodell, instandhaltung
WHERE Fahrzeugmodell_ID = fahrzeugmodell.ID AND Fahrzeug_ID = fahrzeug.ID
GROUP BY Bezeichnung
```
#### f
```SQL
SELECT Hersteller, MAX(Anschaffungskosten) Max_Kosten FROM fahrzeugmodell
INNER JOIN fahrzeug ON Fahrzeugmodell_ID = fahrzeug.ID
GROUP BY Hersteller

SELECT Hersteller, MAX(Anschaffungskosten) Max_Kosten FROM fahrzeugmodell, fahrzeug
WHERE Fahrzeugmodell_ID = fahrzeug.ID
GROUP BY Hersteller
```