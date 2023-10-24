#### 1
```SQL
SELECT Nachname, Vorname FROM 09_BiathletenSchueler_OPP
WHERE Geschlecht = "m" AND Preisgeld BETWEEN 10000 AND 50000
GROUP BY Nachname, Vorname
```
#### 2
```SQL
SELECT SUM(Weltcupsiege) AS DeutscheSiege FROM 09_BiathletenSchueler_OPP
WHERE Nation = "GER"
```
#### 3
```SQL
SELECT COUNT(*) AS Norweger FROM 09_BiathletenSchueler_OPP
WHERE Nation = "NOR"
```
#### 4
```SQL
SELECT Nachname, Vorname FROM 09_BiathletenSchueler_OPP
WHERE Vorname LIKE "%Sch%"
```
#### 5
```SQL
SELECT * FROM 09_BiathletenSchueler_OPP
WHERE Geschlecht = "w" AND Nation IN (FIN, DAN, SWE, NOR)
GROUP BY Nation
```
#### 6
```SQL
SELECT Nation, COUNT(*) AS Anzahl FROM 09_BiathletenSchueler_OPP
GROUP BY Nation
```
#### 7
```SQL
SELECT DISTINCT Nation, MAX(Weltcupsiege) AS maxSiege FROM 09_BiathletenSchueler_OPP
```
#### 8
```SQL
SELECT SUM(Weltcupsiege) AS DeutscheSiege FROM 09_BiathletenSchueler_OPP
WHERE Nation = "GER"
GROUP BY Geschlecht
```
#### 9
```SQL
SELECT Nachname, Vorname, Quote FROM 09_BiathletenSchueler_OPP
WHERE Geschlecht = "m" AND Quote BETWEEN 70 AND 90
ORDER BY Quote DESC
GROUP BY Nation
```
#### 10
```SQL
SELECT SUM(Nationssiege) FROM  09_BiathletenSchueler_OPP
GROUP BY Geschlecht, Nation
HAVING Nation IN (GER, FRA, AUT, NOR)
ORDER BY Geschlecht ASC Nationsiege DESC
```
### Aufgaben geschachtelten Anweisung
#### 1
```SQL
SELECT Max(Preisgeld) FROM Biathleten
WHERE Geschlecht = "w" 

SELECT Nachname, Vorname, Weltcupsiege, Geschlecht, Preisgeld FROM Biathleten
WHERE Geschlecht = "w"
AND Preisgeld = 750000 

SELECT Nachname, Vorname, Weltcupsiege, Geschlecht, Preisgeld FROM Biathleten
WHERE Geschlecht = "w" AND Preisgeld = (SELECT Max(Preisgeld) FROM Biathleten
WHERE Geschlecht = "w") 
```
#### 2
```SQL
SELECT Nachname, Vorname, Weltcupsiege FROM Biathleten
WHERE Weltcupsiege = (SELECT MIN(Weltcupsiege) FROM Biathleten) 
```
#### 3
```SQL
SELECT Nachname, Vorname, Geschlecht, Geburtsdatum, Weltcupsiege, Preisgeld FROM Biathleten
WHERE Geburtsdatum = (SELECT MAX(Geburtsdatum) FROM Biathleten
WHERE Geburtsdatum <= 1976.04.08)
```
#### 4
```SQL
SELECT Nachname, Vorname, Geschlecht, Quote FROM Biathleten
WHERE Geschlecht="w" AND Quote=(SELECT Max(Quote) FROM Biathleten
WHERE Geschlecht="w") OR Geschlecht="m" AND Quote=(SELECT Max(Quote) FROM Biathleten
WHERE Geschlecht="m") 
```
#### 5
```SQL
SELECT Nachname, Vorname, Quote, Weltcupsiege, Aktiv, Preisgeld FROM Biathleten
WHERE Aktiv = TRUE AND Weltcupsiege = 0 AND Preisgeld = (SELECT Max(Preisgeld) FROM Biathleten
WHERE aktiv = TRUE AND Weltcupsiege = 0); 
```
#### 6
```SQL
SELECT Nachname, Vorname, Nation, Weltcupsiege, Geschlecht, Preisgeld FROM Biathleten
WHERE Geschlecht = "w" AND (Geburtsdatum = (SELECT MAX(Geburtsdatum) FROM Biathleten
WHERE Nation ="GER" AND Geschlecht = "w") OR Geburtsdatum = (SELECT MIN(Geburtsdatum) FROM Biathleten
WHERE Nation = "NOR")) AND Geschlecht = "w")
```