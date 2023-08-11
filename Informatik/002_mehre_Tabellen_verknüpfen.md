# Mehre Tabellen verknüpfen
### 3-10
#### a
```SQL
SELECT VersNr, Kennzeichen, Firma FROM versicherungsvertrag
INNER JOIN fahrzeug ON Fahrzeug_ID = fahrzeug.ID
INNER JOIN versicherungsgesellschaft ON Gesellschaft_ID = versicherungsgesellschaft.ID

SELECT VersNr, Kennzeichen, Firma FROM versicherungsvertrag, fahrzeug, versicherungsgesellschaft
WHERE fahrzeug ON Fahrzeug_ID = fahrzeug.ID AND Gesellschaft_ID = versicherungsgesellschaft.ID
```
#### b
```SQL
SELECT Beginn, Ende, Kennzeichen, Bezeichnung FROM Reservierung
INNER JOIN Fahrzeug ON Reservierung.Fahrzeug_ID = Fahrzeug.ID
INNER JOIN Fahrzeugmodell ON Fahrzeug.Fahrzeugmodell_ID = Fahrzeugmodell.ID

SELECT Beginn, Ende, Kennzeichen, Bezeichnung FROM Reservierung, Fahrzeug, Fahrzeugmodell
WHERE Fahrzeug_ID = Fahrzeug.ID AND Fahrzeugmodell_ID = Fahrzeugmodell.ID
```
#### c
```SQL
SELECT Beginn, Ende, Nachname, Kennzeichen, Bezeichnung FROM Reservierung
INNER JOIN Mitarbeiter ON Reservierung.Mitarbeiter_ID = Mitarbeiter.ID
INNER JOIN Fahrzeug ON Reservierung.Fahrzeug_ID = Fahrzeug.ID
INNER JOIN Fahrzeugmodell ON Fahrzeug.Fahrzeugmodell_ID = Fahrzeugmodell.ID;

SELECT Beginn, Ende, Nachname, Kennzeichen, Bezeichnung FROM Reservierung, Fahrzeug, Fahrzeugmodell
WHERE Reservierung.Mitarbeiter_ID = Mitarbeiter.ID AND Reservierung.Fahrzeug_ID = Fahrzeug.ID 
AND Fahrzeugmodell_ID = Fahrzeugmodell.ID;
```