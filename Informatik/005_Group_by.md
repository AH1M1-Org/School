# Group by
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
```
#### c
```SQL
```
#### d
```SQL
```
#### e
```SQL
```
#### f
```SQL
```