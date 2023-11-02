---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:29**

---
### Aufgabe 
Begründen Sie, inwieweit das Relationenschema $'Sprechstunde'$ nicht den Kriterien der dritten [Normalform](17%20Normalisierung%20von%20Datenbanken) entspricht. Geben Sie alle Gründe an.
$$Sprechstunde(\underline{Kuerzel}, Name, Tag, Stunde, Anfangszeit, Raum)$$
Das Relationenschema befindet sich nicht in der dritten Normalform, weil es nicht in der ersten Normalform steht. Die Attributswerte sind nicht Vollständig aufgeteilt (nicht Atomar) z.B. $Name = Vorname, Nachname$. Außerdem sind nicht Schlüsselattribute [transitiv](17%20Normalisierung%20von%20Datenbanken) abhängig z.B. Anfangszeit ist abhängig vom Attribut Stunde und dies sind beide keine Primärschlüssel also verstößt dies gegen die dritte [Normalform](17%20Normalisierung%20von%20Datenbanken).

---
### Aufgabe 
Entwickeln Sie zum Relationenschema $'Sprechstunde'$ ein Datenbankschema, das sich in der dritten Normalform befindet, und erläutern Sie die Änderungen, die zur Überführung in die dritte  [Normalform](17%20Normalisierung%20von%20Datenbanken) nötig sind.

$$Sprechstunde(\underline{Kuerzel}, Vorname, Nachname, Tag, \uparrow Stunde, Raum)$$
$$Stunden(\underline{Stunde}, Anfangszeit)$$
Die Nötigen Änderungen wären den Namen in zwei Teile zu spalten $(Name, Vorname)$. Außerdem sollte man eine extra Tabelle $'Stundentaffel'$ anlegen da man so die Anfangszeit also nicht Schlüsselattribute vom neuen Primärschlüsselattribut $Stunde$ abhängig macht. Bei $'Sprechstunde'$ kann man nun Stundeneintragen und so hat man eine $1:n$ Beziehung. *"eine Sprechstunde hat genau eine Stunde, eine Stunde hat eine oder mehrere Sprechstunden"*.