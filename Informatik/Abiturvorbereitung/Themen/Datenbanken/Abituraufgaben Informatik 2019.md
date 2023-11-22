![Bild](PDF/Informatik/2%20Abiturpruefung%20GK%202019.pdf) 
# Datenbanken
### Aufgabe a
**teil 1**
Der Entitaetstyp Kunde besitzt vier Attribute, HandyNr, Naachname, Vorname KundenNr. Das Attribut KundenNr stellt den Primaerschluessel des Entitaetstyp Kunde da.

Der Entitaetstyp Fahrrad besitzt vier Attribute, SerienNr, Typ, Baujahr und Farbe. Das Attribut SerienNr stellt den Primaerschluessel des Entitaetstypen Fahrrad da.

Der Entitaetstyp Station besitzt vier Attribute, Stationsname, Strasse, HausNr und AnzahlFahrradstellplaetze. Das Attribut Stationsname stellt den Primaerschluessel des Entitaetstyp Station da.

Der Entitaetstyp Kund und Fahrrad stehen in einer Beziehung zueinander "leihtAus". Die Bezeihung hat die Attribute Ausleihzeitpunkt, Rueckgabezeitpunkt undGefahreneKilometer. Das Attribut Ausleihzeitpunkt stellt den Primaerschluessel da.

Der Entitaetstyp Fahrrad und Station stehen in einer Beziehung zueinander "ausleihbarBei"

**teil 2**
Die Kardinalitaet zwischen Fahrrad und Kunde sollte eine $n:m$ sein da ein Kunde 1 oder mehrere Fahrradeder ausleihen kann und ein Fahrrad von einem oder mehreren Kunden ausgeliehen werden kann, weil ein Fahrrad zu unterschiedlichen Zeitpunkten verliehen werden kann.

Die Kardubakutaet zwischen Fahrrad und Station sollte eine $n:1$ sein da ein Fahrrad genau einer Station zugeordnet ist aber eine Station ein oder mehrere Fahrraeder haben kann.

**teil 3**
Die Attribute KundenNr, SerienNr und Ausleihzeitpunkt ergeben den Primaerschluessel, weil ein Kunde das selbe Fahrrad ausleihen koennte, sprich KundenNr und SerienNr koennten sich doppeln. Fuegt man nun das Attribut Ausleihzeitpunkt hinzu kann es zwar immer noch sein das ein Kunde das selber Fahrrad ausleiht aber zu einem anderen Zeitpunkt. Sprich der Zeitpunkt macht den Primaerschluessel deutlich.
Wueder man ueberlegen einzelene Attribute nehmen haette man Redundanzen, um dies zu vermeiden nimmt man also alle drei Attribut als Primaerschluessel.
### Aufgabe b
1. ```
```SQL
SELECT SerienNr FROM Fahrrad
WHERE Farbe = "rot"
AND Baujahr <= 2017
ORDER BY SerienNr ASC
```
2. 
```SQL
SELECT Vorname, Nachname, HandyNr FROM KUNDE
INNER JOIN leihtAus ON Kunde.KundenNr = leihtAus.SerienNr
WHERE Rueckgabezeitpunkt IS NOT NULL
AND GefahreneKilometer > 10
```
3. 
```SQL
SELECT Typ, COUNT(*) AS Anzahl_Typ FROM Fahrrad
INNER JOIN leihtAus ON Fahrrad.SerienNr = leihtAus.SerienNr
GROUP BY Fahrrad.Typ
HAVING Anzahl_Typ > 0
```
### Aufgabe c#
In den Zeilen 3 - 6 werden die Spalten Baujahr SerienNr und Stationsname von der Tabelle Fahrrad ausgegeben. Zudem werden die Kilometer aus der Tabelle leiht aus Summiert und unter x gespeichert. Zudem werden die Zeile gezaehlt und unter z gespeichert. Danach werden die Tabellen leiht aus und Fahrrad verbunden und es wird nach der SerienNr gruppiert. Dieses Ergebnis wird unter temp gespeichert. 
Die gesamte SQL Anweisung gibt die gefahrenen Kilometer zurueck pro SerienNr also pro Fahrrad. Dies gilt aber nur fuer Fahraeder mit mehr als 500 kilometern oder die mehr als 50 mal ausgeliehen wurden. 
Dies passiert mit temp.X > 500 und temp.Y > 50.
### Aufgabe d
Kunde($\underline{Kundennr}$, Vorname, Nachname, Handynr)
leihtAus($\uparrow$Kundennr, $\uparrow$seriennr, $\underline{Ausleihzeitpunkt}$, Rueckgabezeitpunkt, GefahreneKi10meter)
Fahrrad($\underline{serinenr}$, $\uparrow$Typ, Baujahr, $\uparrow$stationsname)
Typen($\underline{Typ}$, Farbe)
Station($\underline{stationsname}$, Strasse, Hausnr, AnzahlFahrradstellplaetze)

Die Farbe ist abhaengig vom Typen also ist ein nichtschluessel attribut abhaengig von einem anderen Nichtschluesselattribut. Dies entspricht nicht der dirtten Normalform. Also legt man eine dritte Tabelle Typen an wo Typ der Primaerschluessel ist. Es ist sehr sinnvoll es zu anzulegen, da man nur einen neuen Datensatz anlegt zum Beispiel mit der Farbe Gelb und somit nur darauf verweisst das selbe gilt auch fuers löschen. 
### Aufgabe e
