# Aufgaben Biathleten
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
WHERE Geschlecht = "w"
AND Nation IN (FIN, DAN, SWE, NOR)
GROUP BY Nation
```
#### 6
```SQL
SELECT COUNT(*) AS Anzahl FROM 09_BiathletenSchueler_OPP
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
WHERE Nation IN (GER, FRA, AUT, NOR)
GROUP BY Geschlecht
ORDER BY Nationsiege DESC
```