---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:26**

---
#### 2
```SQL
SELECT COUNT(*) AS AnzahlSchueler FROM schülerdaten
WHERE schülerdaten.Klasse = "6D"
```
#### 3
```SQL
SELECT lehrer_zu_klass.Klasse From lehrer_zu_klasse 
INNER JOIN lehrerdaten ON lehrer_zu_klasse.LehrerNr = lehrerdaten.LehrerNr
WHERE LehrerName = "Meier"
```
#### 4
```SQL
SELECT SchuelerName FROM schuelerdaten, lehrer_zu_klasse, lehrerdaten
WHERE lehrer_zu_klasse.LehrerNr = lehrerdaten.LehrerNr
AND lehrer_zu_klasse.Klasse = schuelerdaten.Klasse
AND LehrerName = "Gans" 
AND Geburt BETWEEN "1992-01-01" AND "1995-01-01"
```
#### 5
```SQL
SELECT LehrerName, LehrerVorname FROM schuelerdaten, wahlfach, lehrer_zu_klasse, lehrerdaten
WHERE schuelerdaten.Klasse = lehrer_zu_klasse.Klasse
AND lehrer_zu_klasse.LehrerNr = lehrerdaten.LehrerNr
AND schuelerdaten.WNr = wahlfach.WNr
AND lehrerdaten.Lehrer_Nr = wahlfach.LehrerNr
AND SchuelerName = "Messner" 
```
#### 6
```SQL
SELECT Klasse, COUNT(Klasse) AS Klassenstärke FROM schülerdaten
GROUP BY Klasse 
```
#### 7
```SQL
SELECT Klasse, COUNT(Klasse) AS Klassenstärke FROM schülerdaten
GROUP BY Klasse 
HAVING COUNT(Klasse) > 4
```
#### 8
```SQL
SELECT MAX(Geburt) AS Jüngester, SchülerName, SchülerVorname FROM schülerdaten
```
#### 9
```SQL
SELECT MAX(SELECT COUNT(schülername) AS Klassenstärke FROM schülerdaten)
GROUP BY Klasse

SELECT Klasse, COUNT(Klasse) AS Klassenstärke FROM schülerdaten
GROUP BY Klasse
ORDER BY Klassenstärke DESC
LIMIT 1
```