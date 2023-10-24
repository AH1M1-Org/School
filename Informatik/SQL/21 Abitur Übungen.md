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
- jedes Nichtschlüsselattribut nicht transitiv vom Primärschlüssel abhängig ist

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
### Aufgabe c

### Aufgabe d
Der Vorschlag des praktikanten ist unguenstig da man sich erstens nur auf 5 Sprachen beschraenken kann ausserdem muesste man Datensetze leer lassen wenn die Serie nur auf einer Sprache verfuegbar ist. Des Weitern muesste man den ganzen datensatz bearbeiten sobald man eine Sprache hinzufuegen will.

Der Beziehungstyp zwischen Episode und Sprache wird modelliert indem wir Primaerschluessel von Episoden also die ID einem Primaerschluessel der Sprach zuweisen. Somit kann eine Episode mehrere Sprachen haben

Bei dem Beziehungstzp original Sprache gibt es nur eine moeglichkeit welche Sprache die Episode als original sprache hat diese Sprache kann aber wiederrum bei mehreren Episoden die Original sprache sein

---
Eine Relation ist dann in der ersten Normalform wenn all ihre Attributswerte Atomar sind und der Primaerschluessel sich aus zwei oder mehr Teilen zusammensetzt

Eine Relation ist in der zweiten Normalform wenn sie in der ersten Normalform ist und alle nicht Schluessel Attribute vom Primaerschluessel voll funktional abhaengig sind.

Eine Relation befindet sich in der dritten Normalform wenn sie in der zweiten Normalform ist und alle Nichtschluesselattribute nicht transitiv abhaengig vom Primaerschlueesel sind

```SQL
INSERT INTO [Tabelle]
VALUES ([Attribut1], [Attribut2], [Attribut3])

UPDATE [Tabelle] 
SET([Spalte]=[NeuerWert])

REMOVE FROM [Tabble]
WHERE [Bedingung]
```

Welche Sachen koennen mit der dritten Normalform verhindert werden?
- Redundanzen in der Datenbank
- Einfuege Anomalie, Aenderungsanomalie und Loeschanomalie

CREATE TABLLE Kunde (
    ID INTEGER NOT NULL,
    Name VARCHAR(30) NOT NULL,
    Vorname VARCHAR(30) NOT NULL,
    Bestellung_ID INTEGER,
    PRIMARY KEY(ID),
    FOREIGN KEY(Bestellung_ID) REFRENCES Bestellung(ID) 
);

CREATE VIEW Name AS 
SELECT 

INSERT INTO Tabelle
VALUES (dsada,dsada,sdsa)

UPDATE Tabelle
SET (Spalte=Neuer Wert)
WHERE ID = 1

REMOVE FROM Name
WHERE

1 -> genau eins
c -> einer oder keiner
n -> einer oder mehrere
nc -> keiner einer mehrere

Primaerschluessel macht einen daten satz eindeutig es gibt kuenstlich Erzeugte Primaerschluessel oder Natuerliche

Mit einem Fremdschluessel greift man auf den Primaerschluessel in einem anderen Datensatz zu um diese zum Beispiel mit einem Inner Join zu verbinden

Vorteile einer VIEW
- Berechtigung

Stand alone bedeutet das die Datenbank nur von einer Person benutzt wird, die Datenbank steht somit alleine und wir nicht gleichzeitig von mehreren Leuten bedient. 

Eine Client Server Datenbank wir benutzt wenn mehrere Leute auf eine Datenbank zugreifen muessen. Zum Beispiel in einem Krankenhaus muessen Behandlungen der Patienten und Registrierungen gleichzeitig gespoeichert werden.

# Abiturpruefung 2020
### Aufgabe a

 Es gibt die Entitaet Kunde, ein Kunde hat die Attribute Email Adresse und Name, die Emailadresse ist der Primaerschluessel.

 Ausserdem gibt es die Entitaet Episode, diese hat die Attribute ID, Staffelnr, Episodennr und Titel. Die ID ist der Primaerschluessel

 Zudem gibt es noch die Entitaet Serie mit den Attributen ID und Titel. ID ist hier der Primaerschluessel

 Kunde und Episode in einer n:m Beziehung "hat Angsehen" diese Beziehung traegt das Attribut Bewertung und dient dazu Kunden einer Episode zuzuordnen.

 Episode und Serie stehen in einer n:1 Beziehung "gehoert zu" diese dient dazu Episoden einer Serie zuzuordnen.

---
Die Kardinalitaet zwischen Kund und Episode n:m wurde gewaehlt, weil ein Kunde eine oder mehrere Episoden gesehen hat. Eine Episode kann aber auch von nur einem oder mehreren Kunden gesehen werden. 

Die Kardinalitaet zwischen Episode und Serie n:1 wurde gewaehlt, weil jede Episode zu genau einer Serie gehoeren muss. Ausserdem besteht eine Serie aus einer oder mehreren Episoden.

---
Die n:m Beziehung wurde so umgesetzt das der Primaerschluessel aus Kunde "Emailadresse" in einer neuen Tabelle einem anderen Primaerschluessel zugerodnet wird. In diesem Fall wird hier jede Emailadresse mit einer ID von der Tabelle Episode zugeordnet.

Die n:1 Beziehung wird so umgesetzt das jede Episode einer Serien ID zugeordnet wird. Also SerienID in Episoden wird einer ID aus Serien zugeordnet.

### Aufgabe b
```SQL
SELECT Titel FROM Serie
WHERE Titel LIKE "%Spiel%"
ORDER BY Titel ASC
```
```SQL
SELECT Titel, AVG(Bewertung) AS Durchschnittsbewertung FROM Serie
INNER JOIN Episode ON Episode.SerienID  = Serie.ID
INNER JOIN hatAngesehen ON hatAngsehen.EpisodenID = Episode.ID
GROUP BY Serie.ID
ORDER BY Durchschnittsbewertung DESC
```
```SQL
SELECT Name, COUNT(*) AS Anzahl_Bewertungen FROM Kunde
LEFT JOIN hatAngesehen ON Kunde.EmailAdresse = hatAngesehen.EmailAdresse
GROUP BY Kunde.EmailAdresse
ORDER BY Anzahl_Bewertungen DESC, Name ASC
```
### Aufgabe c
In denZeilen 5 - 7 wird eine unterabfrage gemacht. Es werden alle Episoden ausgegeben mit ihrer Serien ID und ihrer StaffelNr von der Tabelle Episode. Diese Abfrage wird Redundazen vermeiden, da mit Distinct duplicate zusammengefasst werden. Das Ergebnis der Unterabfrage wird unter dem Namen Temp gespeichert und gibt alle Episoden einer Staffel aus in einer Serie

In den Zeilen 2 - 10 werden alle Serien Titel ausgegeben und es wird gezaehlt wie viele Episoden in einer Staffel sind. Durch den Group By befehelt erhaelt man nur das Ergbnis pro Serie. Die ausgabe wird unter Abfrage gespeichert. 

Die ganze Abfrage gibt also alle Serien aus die mehr als eine Staffel haben. Anschliessend wir nach den Titeln der Serien aufsteigend sortiert.

### Aufgabe d
Erstens muesste man den ganzen Datensatz bearbeiten sobald man eine Sprache anpassen moechte, eine Aenderungs Anomalie. Des Weitern wuerde man oft das ende eines Datensatzes sehr oft doppelt in der Datenbank haben. Wenn zum Beispiel 2 Episoden in jeweils den gleichen Sprachen angeboten wird. Ausserdem koennte man sich nur auf 5 Episoden beschraenken.

![Dia](https://cdn.discordapp.com/attachments/1139161006761857024/1156994525382836324/image.png?ex=6516fe9e&is=6515ad1e&hm=0bad80b7782cd630d0a962ebb2985dc1780a37e23167ca0e37105e2d8669f434&)

In meiner Entwickelten Erweiterung wird eine Episode in einer Extratabelle einer oder mehreren Sprachen zugeordnet, nicht jede Sprache muss aber zwingend eine Episode anbieten. Ausserdem wird meine Originalsprache so verwaltet in dem dort eine ID fuer Sprache zugeordnet wird. Eine Episode kann genau eine ID als Originalsprache haben aber eine Sprache kann bei mehreren Episoden die Originalsprache sein.

Die Sprachen werden in der Entitaet Sprache verwalatet und koennen mit dem Primaerschluessel Bezeichnung einduetig identifiziert werden. 

