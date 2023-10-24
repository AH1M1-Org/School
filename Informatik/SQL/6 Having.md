#### a)
```SQL
SELECT Fahrzeug_ID, COUNT(*) AS AnzahlInstandhaltungen, AVG(Kosten) AS Durchschnittskosten
FROM Instandhaltung
GROUP BY Fahrzeug_ID
HAVING AVG(Kosten) > 330
```
#### b)
```SQL
SELECT Bezeichnung, Hersteller, COUNT(*) AS Bestand FROM fahrzeugmodell
INNER JOIN fahrzeug ON Fahrzeugmodell_ID = fahrzeugmodell.ID
GROUP BY Hersteller, Bezeichnung
HAVING COUNT(*) >= 2

SELECT Bezeichnung, Hersteller, COUNT(*) AS Bestand FROM fahrzeugmodell, fahrzeug
WHERE Fahrzeugmodell_ID = fahrzeugmodell.ID
GROUP BY Hersteller, Bezeichnung
HAVING COUNT(*) >= 2
```
#### c)
```SQL
SELECT Firma, SUM(Beitrag) AS kosten FROM versicherungsgesellschaft
INNER JOIN versicherungsvertrag ON Gesellschaft_ID = versicherungsgesellschaft.ID
GROUP BY Firm
HAVING SUM(Beitrag) > 3000

SELECT Firma, SUM(Beitrag) AS kosten FROM versicherungsgesellschaft, versicherungsvertrag
WHERE Gesellschaft_ID = versicherungsgesellschaft.ID
GROUP BY Firm
HAVING SUM(Beitrag) > 3000
```