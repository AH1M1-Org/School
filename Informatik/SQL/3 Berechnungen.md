### 3-11
#### a
```SQL
SELECT Bezeichnung, Hersteller, Verbrauch, Verbrauch*1.1 AS sportlich, Verbrauch*0.9 AS sparend FROM fahrzeugmodell
```
#### b
```SQL
SELECT Kennzeichen, Hersteller, Anschaffungskosten, Bezeichnung, Anschaffungskosten*1.2 AS USDoller FROM fahrzeug
INNER JOIN fahrzeugmodell ON Fahrzeugmodell_ID = fahrzeugmodell.ID

SELECT Kennzeichen, Hersteller, Anschaffungskosten, Bezeichnung, Anschaffungskosten*1.2 AS USDoller FROM fahrzeug, fahrzeugmodell
WHERE Fahrzeugmodell_ID = fahrzeugmodell.ID 
```
#### c
```SQL
SELECT VersNr, Firma, Beitrag, Kasko, Beitrag*0.9775 AS Rabatt FROM versicherungsvertrag
INNER JOIN versicherungsgesellschaft ON Gesellschaft_ID = versicherungsgesellschaft.ID

SELECT VersNr, Firma, Beitrag, Kasko, Beitrag*0.9775 AS Rabatt FROM versicherungsvertrag, versicherungsgesellschaft
WHERE Gesellschaft_ID = versicherungsgesellschaft.ID
```
### 3-11-II
```SQL
SELECT * FROM reservierung 
WHERE (Beginn LIKE '%-01-%'
    OR Beginn LIKE '%-02-%'
    OR Beginn LIKE '%-03-%'
    OR Beginn LIKE '%-04-%'
    OR Beginn LIKE '%-05-%'
    OR Beginn LIKE '%-06-%')
    AND (Beginn LIKE '2016-%')
```