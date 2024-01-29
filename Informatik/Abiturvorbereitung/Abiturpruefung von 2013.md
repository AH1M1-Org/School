---
tags:
  - Informatik
---
*Marvin Baeumer* **2024-01-28 22:01**

---

![PDF](PDF/Informatik/6%20Abiturpruefung%202013.pdf)
### Aufgabe 3.1
| 1. Durchlauf | A | M | T | H | E | I | N | F | O | L | K |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 2. Durchlauf | A | M | T | H | E | I | N | F | O | L | K |
| 3. Durchlauf | A | H | M | T | E | I | N | F | O | L | K |
| 4. Durchlauf | A | E | H | M | T | I | N | F | O | L | K |
|  |  |  |  |  |  |  |  |  |  |  |  |
| 1. Durchlauf | A | M | T | H | E | I | N | F | O | L | K |
| 2. Durchlauf | A | E | T | H | M | I | N | F | O | L | K |
| 3. Durchlauf | A | E | F | H | M | I | N | T | O | L | K |
| 4. Durchlauf | A | E | F | H | M | I | N | T | O | L | K |
|  |  |  |  |  |  |  |  |  |  |  |  |
### Aufgabe 3.2
Die Buchstaben sind absteigend sortiert dies ist deŕWorst-case. 
### Aufgabe 3.3
|            | Worst-case                            | Best-case |
| ---------- | ------------------------------------- | --------- |
| Vergleiche | $V(n) = \frac{n}{2} \cdot \frac{n-1}{2}$ | $n-1$     |
| Bewegung   | $M(n) = 3 \cdot V(n)$                 | $0$       |
### Aufgabe 3.4
Der bubble Sort ist stabil, weil
### Aufgabe 3.5
| Index        | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| ------------ | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Reinfolge    | 3    | 5    | 2    | 7    | 8    | 6    | 1    | 9    | 3    | 4    |
| 1. Durchlauf | 3    | 3    | 2    | 1    | 8    | 6    | 7    | 9    | 5    | 4    |
| 2. Durchlauf             |     |     |     |     |     |     |     |     |     |     |
i =  
j = 
### Aufgabe 3.6
Ein Worst Case für den Quick Sort wäre eine Sortierte Reinfolge, weil die Rekursiontro tzdem durchlaufen würde, das heisst der Sortierte Array würde in teil arrays gespaltet werden. Ausserdem nehmen wir ein rechts Pivot das heisst bei der Folge 1234567 würde man 7 als Pivot nehmen und somit würde niemlas ein Rechtes Feld entstehen, heisst das Prinzip teile und Hersche trifft nicht zu.

Ein Best Case für den Quick Sort wäre wenn das sortierte mitte Element -  1326574. Somit steht das Pivot Element dann nach der Exchange Methode immer in der Mitte.