# Aufgaben Biathleten
#### 5
```SQL
SELECT * FROM 09_BiathletenSchueler_OPP (innen)
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


```
#### 10
```SQL
```