---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### SQL
#### Abfragen
#### Datenmanipulation
#### Tabellenerzeugen
### ER-Modell
> Ein ER-Modell besteht meisten aus einem oder mehreren Entitätstypen, diese Entitätstypen können Attribut besitzen. Attribute sind Eigenschaften eines Entitätstypen, das heisst ein Entitätstyp Kunde könnte die Attriubute KundenNr, Vorname, Nachname enthalten. Entitätstypen können in einer Beziehung zu anderen Entitätstypen stehen. Dabei wird das Verhältniss zwischen den beiden Entitätstypen mit [[Datenbanken#Kardinalitäten|Kardinalitäten]] dargestellt. Zum Beispiel könnte die Tabelle Kunde in einer 1:n Bezihung mit dem Entitätstypen Produkt stehen. *Ein Kunde kauft ein oder mehrere Produkte. Ein Produkt wird genau von einem Kunden gekauft.* 
> Bei einem ER-Modell werde Primärschluessel $\underline{Unterstrichen}$.
### Kardinalitäten
| NC Notation | Verhaeltnis               |
| ----------- | ------------------------- |
| 1            |  genau einer                          |
| c           | keiner oder einer                     |
| n           | einer oder mehrere        |
| nc          | keine, einer oder mehrere |

> wichtig bei einer $n:n$ oder $nc:nc$ oder $n:nc$ Beziehung ersetzt man das eine n durch ein m.
### Relationsschema
> Ein Relationsschema wandelt meisten ein ER-Modell um.
> Aufbau für den Entitätstypen Kunde aus [[Datenbanken#ER-Modell|ER-Modell]] $\rightarrow Kunde(\underline{KundenNr}, Vorname, Nachname)$
 ### Normalform
1. Normalform $\rightarrow$ Eine Relation befindet sich in der ersten Normalform, wenn alle Atribute nur einfache Attributswerte aufweisen(Bezeichnung: atomar $\rightarrow$ nicht teilbar). (alles muss einzeld stehen) Der Primärschlüssel wird nicht mehr eindeutig also muss einer Zusammengesetzt werden muss aus zwei oder meht teilen
---
2. Normalform Eine Relation befindet sich in der zweiten Normalform, wenn: 
- Sie in der ersten Normalform ist
- Jedes Nicht-Schlüssel-Attribut vom Primärschlüssel voll funktional abhängig ist.
---
3. Normaleform Eine Relation befindet sich in der dritten Normalform, wenn
- sie in der zweiten Normalform ist 
- jedes Nichtschlüsselattribut nicht transitiv vom Primärschlüssel abhängig ist.
#### Transitiv
Transitiv bedeutet wenn Nichtschlüsselattribute abhängig von anderen Nichtschlüsselattributen sind.
### Begriffe
#### Redundanzen
#### Dateninkonsistenz
#### Referenzielle Integrität