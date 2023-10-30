#### a)
```SQL
SELECT * FROM versicherungsvertrag
WHERE Beitrag = (SELECT MIN(Beitrag) FROM versicherungsvertrag)
```
#### b)
```SQL
SELECT Kennzeichen, Bezeichnung, Anschaffungskosten FROM fahrzeug
INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID
WHERE Anschaffungskosten = (SELECT MAX(Anschaffungskosten) FROM fahrzeug)

SELECT Kennzeichen, Bezeichnung, Anschaffungskosten FROM fahrzeug, fahrzeugmodell
WHERE Fahrzeugmodell_ID = fahrzeugmodell.ID AND Anschaffungskosten = (SELECT MAX(Anschaffungskosten) FROM fahrzeug)
```

---
*Marvin Baeumer* **2023-10-30 17:07** #Informatik