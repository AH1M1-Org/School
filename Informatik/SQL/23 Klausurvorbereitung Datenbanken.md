---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-05 20:05**

---
### B1.1
Es kann die loesch Aenderungsanomalie auftreten, weil wenn ein Kunde den Namen aendert muesste man das fuer jeden Datensatz einzeln machen. Zudem ist der Kunde nicht Atomar, weil man den Vorname, Nachname und den Ort in einer Spalte speichert dies fuhert schnell zu Redundanzen. Ausserdem gibt es in dieser Datenbank redundanzen, dies sind wiederholte datensaetze/teile von Datensaetzen, zum Beispiel sieht man das beim Datensatz mit Maria Lustig dieser man braechte eine eigene Tabelle Kunde und kunde kauft Modell um diese zu vermeiden. Ausserdem kann es zu Dateninkonsistenz kommen, wenn man Daten abaendern will.

Kunde ($\underline{ID}$, Name, Vorname, Ort)
Hersteller ($\underline{ID}$, Hersteller)
Modell ($\underline{ID}$, Bezeichnung, Preis. $\uparrow$ Hersteller ID)
kauft (Kaufdatum, $\uparrow \underline{Kunde ~ ID}$,$\uparrow \underline{Modell ~ ID}$)

### B1.2
Zwischen Schauspieler und Film wuerde ich eine $n : m$ Beziehung waehlen, weil ein Schauspieler in einem oder mehreren Filmen mitspielen kann und in einem Film ein oder oder mehrere Schauspieler mit spielen, somit ergibt sich eine many too many beziehung.

Zwischen Firma und Film wuerde ich eine $1 : n$ Beziehung waehlen, weil ein Film von geanu einer Firma produziert wird und eine Firma einen oder mehrere Filme produzieren kann somit ergibt sich eine on too many beziehung.

```SQL
SELECT Titel FROM Film
WHERE Jahr = "2012-%"
AND Genre = "Action"
```

```SQL
SELECT Titel FROM Film]
WHERE Laenge BETWEEN 90 AND 120
```

```SQL
SELECT COUNT(*) AS Anzahl_Filme_in_2013 FROM Film
WHERE Jahr = "2013-%"
```

```SQL
SELECT Titel FROM
INNER JOIN Schauspieler ON Schauspieler.SID = Film.FID
ORDER BY Jahr DESC
```
### B1.3
![Bild](Kunden%20Aufgabe.png)
[Dia datei](Kunden%20Aufgabe.dia) 


### B1.1
```SQL
SELECT Film, Preis FROM Filme
WHERE Jahr > "2000"
```

| Land | Anzahl |
| ---- | ------ |
| USA  | 2      |
| DE   | 3      |
| FR   | 1      |

```SQL
SELECT Film FROM Filme
INNER JOIN bestellt ON bestellt.FID = Filme.FID
INNER JOIN Kunden ON Kunde.KID = bestellt.KID
WHERE KID = 3767 
AND Zeitpunkt = "2014-%"
```

```SQL
SELECT Land, SUM(Preis * Anzahl) FROM Filme
INNER JOIN bestellt ON bestellt.FID = Filme.FID
GROUP BY Land
```

Die Attribute FID KID und Zeitpunkt setzen den Primaerschluessel zusammen, die KID und FID koennten den Datensatz eindeutig machen aber wenn ein Kunde den Film 2x am selben Tag zu einer unterschiedlichen Zeit kauft braucht man den Zeitpunkt mit Sekunden um diesen Datensatz eindeutig zu machen.
### B1.2

![Bild](Politik%20Aufgabe.png)
[Dia datei](Politik%20Aufgabe.dia)
#### teil 2
Der Mitarbeiter braucht Lese und Schreibrechte, in der Tabelle Wahlergebniss muss er Werte ein Tragen und aus der Partei daten auslesen.
#### teil 3
Verschluesselungswort "Abi"
Text = "wahlrune"
Chiffre ="wbplvznf"
#### teil 4
Nachdem die laenge des Schluessel bekannt ist kann mit hilfe von Brut force oder Haeufigkeitsanalysen das verfahren knacken, weil es ab wann wenn schluessel laenge n bekannt ist nur noch Caeser verfahren ist und da das Alphabet nur 26 Buchstaben hat ist dies gut moeglich in lebzeiten zu knacken. 