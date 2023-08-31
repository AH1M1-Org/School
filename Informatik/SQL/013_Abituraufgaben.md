# Abituraufgaben
1.6
```SQL
SELECT Name, Vorname, Geburstdatum FROM Patient
INNER JOIN Krankenkasse ON Patient.KID = Krankenkasse.KID
WHERE Mitglieder > 2000000
```
1.7
```SQL
SELECT PatientID From Patient
WHERE Geschlecht = "W" 
AND Wohntort IN (Duesseldorf, Ratingen)
AND Gebdatum >= "1957-05-01"
```
### Was ist eine VIEW mit der Bezeichnung "Studie" als Abfrage.

1.8
```SQL
SELECT KKID, COUNT(*) AS Anzahl FROM Patient
WHERE Wohnort = "Duesseldorf"
INNER JOIN Krankenkasse ON Patient.KID = Krankenkasse.KID
WHERE 10 < (SELECT COUNT(*) AS Anzahl FROM Patient)
```
