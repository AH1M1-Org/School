### **Rechenregeln**
$a_1 \equiv b_1 \mod m$
$a_2 \equiv b_2 \mod m$
$\Longrightarrow a_1 + a_2 \equiv a_2 + b_2 \mod m$

$a_1 = 120 ~ a_2 = 80 ~ b_1 = 248 ~ b_2 = 116$

$120 \equiv 248 \mod 4 ~ Rest = 0$
$80 \equiv 116 \mod 4 ~ Rest = 0$
$\Leftrightarrow 120 + 80 \equiv 248 + 116 \mod 4 ~ Rest = 0$
#### *"Wir duerfen zwei Kongruenzen modulo m addieren"*
---
$a \equiv b \mod m \Longrightarrow a \cdot c \equiv b \cdot c \mod m$

$a = 6 ~ b = 9 ~ c = 2 \mod 3$
$6 \equiv 9 \mod 3 ~ Rest = 0$
$\Leftrightarrow 6 \cdot 2 \equiv 9 \cdot 2 \mod 3 ~ Rest = 0$
#### *"Wir duerfen beide Seiten einer Kongruenz mit der gleichen ganzen Zahl multiplizieren"* 
---
$a_1 \equiv b_1 \mod m$
$a_2 \equiv b_2 \mod m$
$\Longrightarrow a_1 \cdot a_2 \equiv a_2 \cdot b_2 \mod m$

$a_1 = 3 ~ a_2 = 9 ~ b_1 = 6 ~ b_2 = 12$

$3 \equiv 6 \mod 3 ~ Rest = 0$
$9 \equiv 12 \mod 3 ~ Rest = 0$
$\Leftrightarrow 3 \cdot 9 \equiv 6 \cdot 12 \mod 3 ~ Rest = 0$
#### *"Wir duerfen zwei Kongruenzen Modulo m multiplizieren"*
---
#### *Modulo teilen*
$8 \cdot x \equiv 0 \mod 20 ~ | \div 8$ 
> durch 8 teilen

> Suche des ggts von 20 und 8, in unserem Fall ist das 4

$ggt(8,20) = 4$
> Teilen des mods durch den ggt, also $20 \div 4 = 5$

$x \equiv 0 \mod 5$ 
> Neuer Modulo gleich 5
---
### **Teilbarkeitsregeln**
$2 \rightarrow$ wenn die Zahl auf ${0,2,4,6,8}$ endet.
$3 \rightarrow$ wenn die Quersumme durch 3 Teilbar ist. Die Quersumme von $18 \rightarrow 9$
$4 \rightarrow$ wenn die letzten 2 Ziffern zusammen durch 4 teilbar sind $420 \rightarrow 20$
$5 \rightarrow$ wenn die Zahl auf ${0,5}$ endet.
$6 \rightarrow$ wenn die Zahl durch 2 oder 3 teilbar ist
$8 \rightarrow$ wenn die letzten 3 Ziffern zusammen durch 8 teilbar sind
$9 \rightarrow$ wenn die Quersumme durch 9 teilbar ist Die Quersumme von $18 \rightarrow 9$

$7 \rightarrow$ man nehme die letzte Ziffer und multipliziert sie mit 2, diese Zahl zieht man von der uebrigen Zahl ab. Wenn dieses Ergebnis durch 7 teilbar ist dann ist die Zahl durch 7 teilbar.
$532 \rightarrow 2 \cdot 2 = 4$
$53 - 4 = 49$
$49 \div 7 = 7$
> bei hoehren Zahlen macht man das solange bis man auf kleine Zahlen kommt
### **Prueffziffer-Verfahren**
![Picture](https://cdn.discordapp.com/attachments/1139161006761857024/1151908043953549342/image.png)
Allgemeine Formel $= a_1 + 3 \cdot a_2 + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} + a_{13} \mod 10 = 0$
oder ISBN =
$$10 - \bigg(\sum_{i = 1}^{12} \cdot d_i \cdot 3^{(i + 1) \mod 2}\bigg) \mod 10$$

**Prueffziffer Berechnen**
$d_{13} = a_1 + 3 \cdot a_2 + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} \mod 10 = 0$

### Welche Fehler lassen sich nicht erkennen?
- wenn man $a_1$ und $a_3$ tauscht $\rightarrow$ kommutativgesetz
- wenn man $a_2$ und $a_4$ tauscht $\rightarrow$ kommutativgesetz
---
- wenn $a_1$ und $a_2 \equiv 0 \mod 5$ sind, dann wird eine Vertauschung nicht erkannt!

### **Begruendung**
**I.** 
$= \underline{a_1} + 3 \cdot \underline{a_2} + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} + a_{13} \mod 10 \equiv 0$

**II.** $= \underline{a_2} + 3 \cdot \underline{a_1} + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} + a_{13} \mod 10 \equiv 0$

#### **LGS**
**II-I**
$$\underline{a_2} + 3 \cdot \underline{a_1} + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} + a_{13})  - (\underline{a_1} + 3 \cdot \underline{a_2} + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} + a_{13})  \equiv  0 \mod 10 ~ | ~ Formel ~ kuerzt ~ sich ~ weg, ~ weil ~ identisch$$

$(\underline{a_2} + 3 \cdot \underline{a_1})-(\underline{a_1} + 3 \cdot \underline{a_2}) \equiv 0 \mod 10 ~ | ~ aus multiplizieren$

$a_2 + 3 \cdot a_1 - a_1 - 3 \cdot a_2 \equiv 0 \mod 10 ~ | ~ Zusammenfassen$

$- 2 \cdot a_2 + 2 \cdot a_1 \equiv 0 \mod 10 ~ | \div 2$

$-a_2 + a_1 \equiv 0 \mod 5 \rightarrow ggt(2,10)$  
---
*Marvin Baeumer* **2023-10-30 17:05** #Mathe