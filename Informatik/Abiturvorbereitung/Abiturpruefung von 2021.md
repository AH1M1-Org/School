---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-13 16:30**

---
![PDF](PDF/Informatik/3%20Abiturpruefung%202021.pdf)
### Aufgabe 1.1
![DIA](F.png)
### Aufgabe 1.2
atomar: Atomar bedeutet das ein Wert nicht mehr geteilt werden kann zum Beispiel waere Name nicht Atomar, weil man ihn in Nachname, Vorname aufteilen koennte. Diese beiden Attribute waeren dann aber Atomar

voll funktional abhaengig: Voll funktional abhaengig bedeutet das ein Nichtschluesselattribut eindeutig mithilfe eines Primaerschluessels identifizeirt werden kann.

transitiv abhaengig: transitiv abhaengig bedeutet das ein Nichtschluessel Attribut von einem anderen Nichtschluessel abhaengig ist. Zum Beispiel ist der Ort immer abhaengig von der Posleitzahl, heisst wenn man die Tabelle Kunde hat und dort immer den Ort und die PLZ speicher und die Kunden NR der Primaerschluessel ist ist Ort abhaengig von einem nichtschluessel Attriut (PLZ)
### Aufgabe 1.3
Benutzer($\underline{BenutzerID}$, Email, Vorname, Nachname, Strasse, Hausnummer, Ort)
Nachricht($\underline{NachrichtenID}$, Zeitstempel, Nachrichtentext, $\uparrow$ GruppenID, $\uparrow$  Benutzer ID)
Gruppe_Benutzer($\uparrow \underline{GruppenID}$, $\uparrow \underline{BenutzerID}$, GruppenmitgliedSeitDatum, Geburtsdatum)
Gruppe($\underline{GruppenID}$, Gruppenname)
### Aufgabe 1.4
Bei der Neuen Relation ist das Problem das der Primaerschluessel nicht mehr aus Jahr LandID und Kategorie zusammengesetyzt wird sondern nun noch aus Jahr und LandId. Somit kann man fuer ein Land im gleichen Jahr nicht mehrere CO2 Tonnen in unterschiedlichen Kategorien speichern da so der Datensatz nicht mehr eindeutig waere.
### Aufgabe 1.5
```SQL
CREATE TABLE CO2Wert (
Jahr DATE NOT NULL,
LandID INTEGER NOT NULL,
KategorieID INTEGER NOT NULL,
CO2InTonnen DOUBLE,
PRIMAERY KEY JAHR, 
FORGEIN KEY LandID REFRENCES Land(LandID),
FORGEIN KEY KategorieID REFRENCES Land(KategorieID)
): 
```
### Aufgabe 1.6
```SQL
SELECT SUM(CO2InTonnen) AS CO2-Emissionswert FROM CO2Wert
WHERE Jahr 2020
```
### Aufgabe 1.7
```SQL
SELECT CO2InTonnen, Land FROM CO2Wert 
INNER JOIN Land ON Land.LandID = CO2Wert.LandID
INNER JOIN Kategorie ON Kategorie.KategorieID = CO2Wert.KategorieWertID
WHERE Land = "Deutschland"
AND Kategorie = "Fluessig Brennstoff"
ORDER BY Jahr DESC
```
### Aufgabe 1.8
```SQL
SELECT Land , SUM(CO2INTonnen) AS SummeProLand FROM CO2Wert 
INNER JOIN Land ON Land.LandID = CO2Wert.LandID
WHERE Jahr BETWEEN 2010 AND 2020
GROUP BY Land.LandID
HAVING SummeProLand >= 0.1 (SELECT SUM(CO2InTonnen) FROM CO2Wert)
ORDER BY SummeProLand DESC
```
### Aufgabe 1.9
Die SQL Anweisung gib die Kategorie das Land, und die Summe des CO2 ausstoesses an und speicher die Summe unter total. Dannach werden alle Tabellen miteinandern Verknuepft und es werden Kategorien und Laender gruppiert. Die SQL Anweisung gibt die Summer alle Laender pro Kategorie pro Jahr aus. Die Kategorien werden aufsteigend sortiert und dannach die Totale Summer Absteigend sortiert

