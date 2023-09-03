# Abituraufgaben
1.6
```SQL
SELECT Name, Vorname, Geburstdatum FROM Patient
INNER JOIN Krankenkasse ON Patient.KID = Krankenkasse.KID
WHERE Mitglieder >= 2000000
ORDER BY Name ASC, Vorname ASC
```
1.7
```SQL
SELECT PatientID From Patient
WHERE Geschlecht = "W" 
AND Wohnort IN (Duesseldorf, Ratingen)
AND Gebdatum <= "1957-05-01"
```
### Was ist eine VIEW mit der Bezeichnung "Studie" als Abfrage.

Eine VIEW "Abfrage" kann dir eine Tabelle erstellen mit datensätzen die bereits in der Datenbank vorhanden sind. Daraufhin kann man mit SQL Querys Abfragen gegenüber dieser Tabelle erstellen. Wichtig es erstellt keine neue Tabelle es fungiert mehr als refrence.
```SQL
CREATE VIEW name AS
...
```SQL
1.8
```SQL
SELECT Krankenkasse.KKID, COUNT(*) AS Anzahl FROM Patient
INNER JOIN Krankenkasse ON Patient.KID = Krankenkasse.KID
WHERE Wohnort = "Duesseldorf"
GROUP BY Krankenkasse.Name
HAVING Anzahl > 10
```

DBMS
- DAtenschutz
- Mehrbenutzersystem
- Datenunabhängigkeit
  - ausstausch der Daten mit anderen Programmen ermöglichen
