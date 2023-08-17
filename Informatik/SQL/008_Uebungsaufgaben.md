# Uebungsaufgaben
#### 1.2.2
```SQL
SELECT DISTINCT Name, Nachname FROM teilnehmer
INNER JOIN belegung ON belegung.T_Nr = teilnehmer.T_Nr
ORDER BY Name ASC, Nachname ASC
```
#### 1.2.3
```SQL
SELECT Thema, Beginn, Name FROM seminare
INNER JOIN leiter ON seminar.L_Nr = leiter.L_Nr
WHERE Thema IN ("Küchenplanung", "Kundenwerbung") AND Name = "Hahn" AND Beginn = "%.03.2009"
```
#### 1.2.4
```SQL
SELECT Geschlecht COUNT(*) AS Anzahl FROM teilnehmer
GROUP BY Geschlecht 
```
#### 1.2.5
```SQL
SElECT Name AS Leitername, Dauer, Thema FROM Seminar
INNER JOIN leiter ON seminar.L_Nr = leiter.L_Nr
WHERE Dauer = (SELECT MIN(Dauer) FROM Seminar)
```
