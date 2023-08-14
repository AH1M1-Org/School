# Uebersicht
## SELECT ... FROM ...
```SQL
SELECT [spalte], [spalte]... FROM [tabelle] 

//auswaehlen einer spalte von Tabelle, mit "," werden mehrere spalten ausgewaehlt 
```
## Distinct
```SQL
SELECT DISTINCT...

//gibt bei doppelten ergebnissen nur eines zuruk
```
|Nachname|
|-|
|Maier|
|Haug|
|Maier|
|Sommer|

$\Longrightarrow Ausgabe$ 

|Nachname|
|-|
|Haug|
|Maier|
|Sommer|

## ORDER BY 
```SQL
SELECT [spalte], [spalte]... FROM [tabelle] 
ORDER BY [spalte] {DESC} {ASC}, [spalte] {DESC} {ASC}...

//auwaehlen einer spalte dann angeben ob es absteigenden {DESC} oder aufsteigend {ASC} geordnet werden soll
```

## WHERE
```SQL
...
WHERE [bedingung]

//bedingungen koennen Zahlen vergleiche sein oder auch String abgleiche sein
```

|Operator|Bedeutung|
|--------|---------|
|=|gleich|
|$\neq$|ungleich|
|<|kleiner als|
|>|groesser gleich|
|$\leq$|kleiner gleich|
|$\geq$|groesser gleich|
|%|ergaenzt|
```SQL
...
WHERE %A%

//Sucht einen String der den Buchstaben A enthaelt
```
## INNER JOIN
