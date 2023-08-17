# Aufgaben zur Schuldatenbank
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
WHERE SchuelerName = "Messner" 
AND schuelerdaten.Klasse = lehrer_zu_klasse.Klasse
AND lehrer_zu_klasse.LehrerNr = lehrerdaten.LehrerNr
AND schuelerdaten.WNr = wahlfach.WNr
AND lehrerdaten.Lehrer_Nr = wahlfach.LehrerNr
```