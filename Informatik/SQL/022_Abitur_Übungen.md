# Aufgaben 
### 1.2
1. Normalform $\rightarrow$ Eine Relation befindet sich in der ersten Normalform, wenn alle Atribute nur einfache Attributswerte aufweisen(Bezeichnung: atomar)\
Der Primärschlüssel wird nicht mehr eindeutig also muss einer Zusammengesetzt werden aus zwei oder meht teilen
---
2. Normalform Eine Relation befindet sich in der zweiten Normalform, wenn: 
- Sie in der ersten Normalform ist
- Jedes Nicht-Schlüssel-Attribut vom Primärschlüssel voll funktional abhängig ist.
---
3. Normaleform Eine Relation befindet sich in der dritten Normalform, wenn
- sie in der zweiten Normalform ist 
- jedes Nichtschlüsselattribut nicht transitiv vom Primärschlüssel abhängig ist, d.h. aus keienm Nichtschlüsselattribut folgt ein anderes Nichtschlüsselattribut

1 Eine Relation befindet sich dann in der 1. Normalform wenn alle Attribute nur atomare Attributswerte enthalten.

2 Wenn sie in der ersten Normalform steht und jedes nicht schluessel attribut vom Primaerschlueessel voll funktional abhaengg ist.

3 wenn sie in der 2 normal form steht wenn jedes nicht schluessel attribut nicht transitiv vom Primaerschluessel abhaengig ist

### 1.3
Durch eine Normaliesierugn einer Datenbank in die dritte Normalform sollen redundazen vermieden werden und Anomalien wie die Einfuege- und loesch Anomalie

### 1.4
Veranstaltung($\underline{VID}$, Datum, Name, $\uparrow$ OID)\
Veranstaltung_Wettbewerb($\uparrow$ VID, $\uparrow$ WID)\
Wettbewerbe($\underline{WID}$, Beschreibung, Ditanz)\
Ort($\underline{OID}$, Name, $\uparrow$ BID)\
Bundesland($\underline{BID}$, Name)


### 1.5
Bei einem Inner Join wird die Schnittmenge ausgegeben von allen Trainingsplänen die auch einen Trainer haben, also wo der Fremdschlüssel TID dem Primärschlüssel TID in der Tabelle Trainer zugeordnet werden kann.\
Bei einem Left Join werden alle Trainingspläne ausgegeben auch wenn diese nicht einen Trainer haben, also wenn der Fremdschlüssel TID nicht einem Trainer zugeordnet werden kann werden diese Trainingspläne trotzdem zugeordnet.

### 1.6
```SQL
UPDATE Trainer
SET (Grundpreis=Grundpreis*0.95)
```

### 1.7
```SQL
SELECT Tag, SollZeit, SollDistanz FROM Traingingseinheit
INNER JOIN Traingsplan ON Traingsplan.TPID = Traingingseinheit.TPID
INNER JOIN Trainer ON Trainer.TID = Trainingsplan.TID
WHERE Vorname = "Max" AND Nachname = "Mustermann"
ORDER BY TPID ASC, Traingsplan.Tag ASC
```

### 1.8
```SQL
SELECT Bezeichnung, SUM(Grundpries*Faktor) FROM Ziel
INNER JOIN Traingsplan ON Trainigsplan.ZID = Ziel.ZID
INNER JOIN Trainer ON Trainingsplan.TID = Trainer.TID
GROUP BY Bezeichnung, ZID
```

### 1.9
```SQL
CREATE VIEW durschschnitt AS
SELECT AVG(Grundpreis) AS Durschnitt FROM Trainer
INNER JOIN Traingsplan ON Trainingsplan.TID = Trainer.TID
GROUP BY Trainer.TID
HAVING 100 < (SELECT COUNT(*) FROM Trainingsplan)
```
---
### Aufgabe a
In der Teilmoddellierung gibt es die Entitaet Kund mit den Attributen EmailAdresse und Name, die EmailAdress ist hier ein Primaerschluessel. Der Kunde steht in eine n:m Beziehung mit Episode, die Beziehung weisst ein Attribut Bewertung auf was dazu dient zu checken ob ein Kunde den Film gesehen hat oder nicht. Die Entitaet Episode hat die Attribute ID, Staffelnr, EpisodenNr und Titel. Die ID ist der Primaerschluessel. Episode steht in einer n:1 Beziehung mit der Entitaet Serie. Serie besteht aus den Attributen ID und Titel, ID ist hier der Primaerschlueesel.\
Die kardinalitaet zwischen Serie und Episode 1:n sagen aus das eine Serie, 1 oder mehrere Episoden haben kann da eine Serie im regelfall immer in Staffeln und Folgen unterteilt ist und somit eine Serie mehrere Folgen also Episoden haben kann.\
Eine Episode muss aber immer zu genau einer Serie gehoehren da eine Episode ohne Serie keinen Sinn ergeben wuerde.\
Die kardinalitaet zwichen Kunde und Episode sagt aus das ein Kunde eine oder mehrere Episoden gesehen hat und eine Episode von einem oder mehreren Kunden gesehen werden kann.

Die m:n Beziehung verwaltet zwei Fremdschluessel, die Schluessel aus Kunde(Email Adresse) und Episode(ID) somit kann in einer extra Tabelle mehrere Episoden einem Kunden zugeordnet werden oder ein Kunde zu mehreren Episoden

In der n:1 Beziehung werden die Episoden ID und die Serien ID verwaltet und zugeordnet sodass eine Serie mehrere Episoden haben kann oder eine Episode genau eine Serie

### Aufgabe b
```SQL
SELECT Titel FROM Serie
WHERE Titel LIKE "%SPIEL%"
ORDER BY Titel ASC
```
```SQL
SELECT Titel, AVG(Bewertung) AS Durschschnittsbewertung FROM Serie
INNER JOIN Episode ON Episode.ID = Serie.ID
INNER JOIN hatAngesehen ON hatAngesehen.EpisodeID = Episode.ID
GROUP BY Serie.ID
ORDER BY Durschschnittsbewertung DESC
```
```SQL
SELECT Name, COUNT(*) AS Anzahl_Bewertung FROM Kunde
LEFT JOIN hatAngesehen ON hatAngesehen.KundeEmailAdresse = Kunde.EmailAdresse
GROUP BY Name
ORDER BY Anzahl_Bewertung DESC, Name ASC
```