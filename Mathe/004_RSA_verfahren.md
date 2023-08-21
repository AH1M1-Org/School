# RSA verfahren
**Situation:** RSA-Verfahren soll implementiert werden.

**Information:** Beschreibung des Algorithmus

Algorithmus benötigt:
- Primzahlen
- ggT 
- mod
- ggT berechnen 
- erweiterter    
- öffenlicher und privater Schlüssel
- $\varphi (n) $

### Beispiel
$p = 11 ~ q = 17$\
$n = p \cdot q = 11 \cdot 17 = 187$\
$(p - 1) \cdot (q - 1) = (11 - 1) \cdot (23 - 1)$\
$e \rightarrow 7$

Verschlüsselungsexponent e muss zwischen 1 und 160 liegen und darf keinen nicht trivialen gemeinsamen Teiler haben.

### Primzahlfactor 
$214 = 2 \cdot 107 $\
$320 = 2 \cdot 160 = 2 \cdot 2 \cdot 80 = 2 \cdot 2 \cdot 2 \cdot 40...$
> Man schaut welche Primzahlen zusammen multipliziert die Zahl ergeben

Teilfremde Zahl zu 320 gesucht: Welche Primzahlfactoren dürfen in dieser Zahl icht vorkommen? 2 und 5\
$3 \cdot 7$ wäre damit teilerfremd zu 320 
