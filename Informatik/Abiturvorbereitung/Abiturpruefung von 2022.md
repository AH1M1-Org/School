---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-14 16:21**

---
![PDF](PDF/Informatik/4%20Abiturpruefung%202022.pdf)
### Aufgabe 1.1
In einer Artztpraxis muss der Datenschutz der Patienten Akte gewaehrt sein heisst nur leute mit der passenden Berechtigung duerfen darauf zugreifen. Ausserdem ist es wichtig das mehrere Leute in der Artztpraxis gleichzeitig mit dem System arbeiten koennen.
### Aufgabe 1.3
Die Relation ist nicht in der zweite Normalform, weil in R1 nicht schluesselattribut nicht voll funktional von geanu einem primaerschluessel abhaengig sind. Das ist bei dem Attribut Ersttungssatz der Fall dies ist naemlich nur abhaengig von TID und nicht von KIDD. Ausserdem ist die R2 nicht in der dritten Normalform, weil hier nicht Schluesselattribute abheaenig von anderen nicht Schluessel attributen sind. Das ist der Fall bei der KKID, weil die Attribute Kassennam und Hauptsitz abhaengig von der KKID sind und das ist in R2 ein nicthschluessel attribut.
### Aufgabe 1.4
Krankenkasse($\underline{KKID}$, Kassenname, Hauptsitz)
Tarif($\underline{TID}$, Erstattungssatz)
Patienten($\underline{PID}$, Vorname, Nachname, $\uparrow$ KKID, $\uparrow$ TID)
### Aufgabe 1.5
```SQL
CREATE TABLE Patient (
PatientID TEXT NOT NULL,
Name TEXT NOT NULL,
Vorname TEXT NOT NULL,
GebDatum DATE NOT NULL,
Geschlecht VARCHAR(1),
Wohnort TEXT NOT NULL,
HausartztID INTEGER NOT NULL,
KKID TEXT NOT NULL,
PRIMARY KEY PatientID,
FORGEIN KEY HausartztID REFRENCES Arzt(ArztID),
FORGEIN KEY KKID REFRENCES Krankenkasse(KKID),
);

INSERT INTO Patinet (PatientID, Name, Vorname, GebDatum, Geschlecht, Wohnort, HausartztID, KKID)
VALUES ("P21461", "Mueller", "Lieschen", "1982-04-16", "W", "Duesseldorf", "2117", "BAR1621")


);
```
### Aufgabe 1.6
```SQL
SELECT Name, Vorname, Geburtsdatum FROM Patient
INNER JOIN Krankenkasse ON Krankenkasse.KKID = Patient.KKID
WHERE Mitglieder >= 2000000
ORDER BY Namen, ASC, Vornamen ASC
```
### Aufgabe 1.7
```SQL
CREATE VIEW Studie AS
SELECT PatientID, Geschlecht, Wohnort, Geburtsdatum
WHERE Geschlecht = "W"
AND WOHNORT IN (Duesseldorf, Ratingen)
AND Geburtsdatum <= "1957-05-01"
```
### Aufgabe 1.8
```SQL
SELECT KKID, COUNT(*) AS Anzahl FROM Patient
INNER JOIN Krankenkasse ON Krankenkasse.KKID = Patient.KKID
WHERE Wohnort = Duesseldorf
GROUP BY KKID
HAVING Anzahl > 10
```
### Aufgabe 3.1
Vertraulichkeit bedeutet das die Daten nur fuer bestimmte Personen sichbar sind in diesem Falle koennten das Aerzte sein. Die Integritaet bedeutet das die Patiendaten nicht unbemerkt veraendert werden koennen dass heisst also das Diagnosen eines Patienten nicht geaendert werden koennen und somit auch nicht verfaelscht. Authenzitaet bedeutet das die Nachricht von einer einduetig identifizeirten Person abgeschickt wurde das heisst man weiss genau von welchem Artzt die Diagnose kam.
### Aufgabe 3.2
IMPFUNG -> RNKUFMT
### Aufgabe 3.3

A = 50 
Z = 76

D = Z - B = 25
A + D = 75 
```java
public static String encrypt(String message) {
	char[] chars = new char[message.length()];
	for (int i = 0; i < message.length; i++) {
		chars[i] = (char) (()'Z' - message.charAt(i)) + 'A');
	}
}
```
### Aufgabe 3.4
Die Sicherheite des Atbasch verfahrens ist nicht sehr sicher da man hier mit brutforce die Verschiebung rausfinden kann. Dies ist moeglich, weil das Alphabet nur 26 Buchstaben hat und damit nicht all zu lang ist. Ausserdem kann man eine Haeufigkeitsanalyse machen, weil so erhaelt man wichtige Vokale oder buchstaben abfolgen und kann so langsam herrausfinden wie das Alphabet verschoben ist.
### Aufgabe 3.5
Die Hautpunterschiede sind die Schluessel. Bei einem Symetrischen Verfahren gibt es einen Schluessel. Mit diesem Schluessel kann person A die Nachricht verschluesseln und Person B mit dem selben Schluessel die Nachricht entschluesseln, heisst beide muessen den Schluessel kennen. Bei einem Asymetrischen Verfahren hingegen gibt es zwei Schluessel, einen public Key und einen pirvate Key. Mit dem Public Key kann man die Nachricht verschluesseln und mit dem private Key entschluesseln der public Key ist oeffentlich einsehbar und der private Key bleibt pro Person geheim. Also Person B will eine Nachricht an A schicken also nimmt Person B den public Key von Person A verschluesselt die Nachricht und schickt sie ab. Person A kann nun den private Key nehmen und die Nachricht entschluesseln.
### Aufgabe 3.6
Symetrische Verfahren und Asymetrische Verfahren werden dann kombiniert wenn es um das Schluessel austauschproblem geht. Durch den Fakt das beide Personen den Schluessel kennen muessen braucht man eine Sicheren austausch. Dies kann dann gemacht werden mithilfe von dem hybriden Verfahren Diffi Hellmann. Dort wird pro Person eine Zahl berechnet diese wird dann mit der anderen Person ausgetauscht um dann den gemeinsamen Schluessel n zu berechnen.
### Aufgabe 3.7
p = 23, q = 31, e = 43, n = 713 , phi(n) = 660, d = 307

660 = 43 * 15 + 15
43 = 15 * 2 + 13
15 = 13 * 1 + 2
13 = 2 * 6 + 1
1 = 2 * 1 + 0

1 = 13 - 6 * 2
2 = 15 - 1 * 13
13 = 43 - 2 * 15 
15 = 660 - 15 * 43

1 = 13 - 6 * 2 = 13  - 6 * (15 - 1 * 13) 
= - 6 * 15 + 7 * 13 = - 6 * 15 + 7 * (43 - 2 * 15)
= 7 * 43 - 20 * 15  = 7 * 43 - 20 * (660 - 15 * 43)
= - 20 * 660 + 307 * 43


= 307 * 43 kong 1 mod 660

private Key(307, 713)
### Aufgabe 3.8
m = 3

m^e mod n

3^43 mod 713

43 = 1 * 32 + 0 * 16 + 1 * 8 + 0 * 4 + 1 * 2 + 1 * 1
43 = 101011 = QM   QQMQQMQM

3^2^2 * 3^2^2 * 3^2 * 3 mod 713
9^2 * 3 ^2^2 * 3^2 * 3 mod 713
81 * 3 ^2^2 * 3^2 * 3 mod 713
243 ^2^2 * 3^2 * 3 mod 713
583 ^2 * 3 ^ 2 * 3
501 * 3 ^ 2 * 3 
77 ^ 2 * 3 
225 * 3 
675

### Aufgabe 3.9