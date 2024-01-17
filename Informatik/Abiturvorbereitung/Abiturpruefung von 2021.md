---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-13 16:30**

---
![PDF](PDF/Informatik/3%20Abiturpruefung%202021.pdf)
### Aufgabe 1.1
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
### Aufgabe 2.1 
Bubble Sort $\rightarrow$ Ein bubble Sort ist stabil, weil einzelene Schritte gemacht werden und nur wenn groesser ist wird getauscht.
Selection Sort $\rightarrow$ Ein Selection Sort ist nicht stabil, weil mehrere stellen uebersprugen werden
Insertionsort $\rightarrow$ Ein Inserstion Sort ist stabil, weil keine Position uebersprungen wird
### Aufgabe 2.2
a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z
Bubble Sort
Marie, Martha, Mohammed, Ava, Denys, Peter
Marie, Martha, Ava, Denys, Mohammed, Peter
Marie, Ava, Denys, Martha, Mohammed, Peter 

Insertionsort
Marie, Peter, Martha, Mohammed, Ava, Denys
Marie, Martha, Peter, Mohammed, Ava, Denys
Marie, Martha, Mohammed, Peter, Ava, Denys
### Aufgabe 2.3
Die Methode Quicksort erwartet ein int Array der unter feld gespeichert wird, einen Integer dieser wird unter u gespeichert und noch einen Integer der unter o gespeichert wird. Sobald die Methode ausgefuehrt wird schaut man mit der if Bedingung ob u kleiner o ist wenn dies der fall ist wird ein neuer Integer festgelegt, dieser ist das pivot element, der wird berechnet aus u+o / 2 somit ergibt sich die Mitte eines teil Arrays. Die Variable pn ist dann das neue pivot Element und wird mit der Methode zerlege berechnet. Die Methode ist rekursiv und dient dazu ein Pivot Element zu erzeugen. Durch das u, pn-1 oder pn+1, o wird somit links und rechts weiter gegangen um so die Pivots machen. 
### Aufgabe 2.4
| feld0 | feld1 | feld2 | feld3 | feld4 | feld5 | feld6 | feld7   | pn  | j   |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ------- | --- | --- |
| 5     | 9     | 2     | 7     | 8     | 4     | 2     | 1       |     |     |
| 5     | 9     | 2     | 1     | 8     | 4     | 2     | 7 Pivot | 0   | /   |
| 5     | 9     | 2     | 1     | 8     | 4     | 2     | 7 Pivot | 1   | 0   |
| 5     | 9     | 2     | 1     | 8     | 4     | 2     | 7 Pivot | 1   | 1   |
| 5     | 2     | 9     | 1     | 8     | 4     | 2     | 7 Pivot | 2   | 2   |
| 5     | 2     | 1     | 9     | 8     | 4     | 2     | 7 Pivot | 3   | 3   |
| 5     | 2     | 1     | 9     | 8     | 4     | 2     | 7 Pivot | 3   | 4   |
| 5     | 2     | 1     | 4     | 8     | 9     | 2     | 7 Pivot | 4   | 5   |
| 5     | 2     | 1     | 4     | 2     | 9     | 8     | 7 Pivot | 5   | 6   |
| 5      | 2      | 1      | 4      | 2      | 7 Pivot      | 8      | 9        | 5    | /    |
### Aufgabe 2.5
Pn liegt im Bereich von u bis o, weil pn mit u initialisiert wird und die Rekursion nur u-o mal ausgeführt wird (pn kann maximal o sein). Der Bereich wird nach jeder Rekursion kleiner. Jeden Durchlauf wird ein Element (Pivot Element) nicht weiter beachtet.
Irgendwann gibt es ein Ende, wenn nur noch ein Element da ist (u = o). Falls das Pivot Element am Rand liegt, ist die Länge von links oder rechts 0 weshalb o< u und deswegen wird abgebrochen

> Tipp: Nicht schauen wo terminiert wird sondern wir es erreicht wird das Terminiert wird. 
### Aufgabe 2.6
|  | worst-case | average-case | best-case |
| ---- | ---- | ---- | ---- |
| Bubble Sort | / | $O(n^2)$ | / |
| Insertion Sort | $O(n^2)$ | / | $O(n)$ |
| Selection Sort | / | $O(n^2)$ | $O(n^2)$ |
| Quick Sort | $O(n^2)$ | $O(n ~ log ~ n)$ | $O(n ~ log ~ n)$ |
> Binary search runtime = $O(log ~ n)$
### Aufgabe 2.7
|  | worst-case | best-case |
| ---- | ---- | ---- |
| 5-Elemente | $5 \cdot 2 = 10$ | $4$ |
| n-Elemente |  | $n - 1$ |
$$
(n-1) + (n-2)...+3+2+1=\sum_{i = 1}^{n -1} 
$$
$$
1+2+3+4+...+(n-1)+n=
\frac{n}{2} \cdot (n + 1) = 
\frac{n^2}{2} + \frac{n}{2} - n=
\frac{n^2}{2} + \frac{n}{2}=
\frac{n}{2} \cdot (n - 1)
$$
### Aufgabe 2.8
### Aufgabe 2.9
```java
public class CO2Object {
	public int compareTo(CO2Object object) {
		if(object.getBeyeichnung.compareTo()) {
		
		} else if () {

		return 0;
		} else if () {

		return 1;
		}
	}
}	
```
