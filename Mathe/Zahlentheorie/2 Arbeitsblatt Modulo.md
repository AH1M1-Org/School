---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-10-31 12:43**

---
### **Teilbarkeit ganzer Zahlen**
$4 \mid -24$
$-5 \mid  20$
$6 \nmid -3$
$-3 \mid -15$
$2 \mid   0$

$\Rrightarrow Restklasse ~ 0 \mod 3 ~ ist ~ z.B. ~ \{-9, -6, -3, 0, 3, 6\}$\
$\Rrightarrow Restklasse ~ 1 \mod 3 ~ ist ~ z.B. ~ \{-8, -5, -2, 1, 4, 7\}$\
$\Rrightarrow ...$\
*"Restklassen sind Zahlen die beim Teilen den selben Rest ergeben"*

### **Kongruenz**
|       |N |R    |R    |
|-------|-:|:---:|:----|
|**mod**|  |**2**|**5**|
|       |-5|    1|    0|
|       |-4|    0|    1|
|       |-3|    1|    2|
|       |-2|    0|    3|
|       |-1|    1|    4|
|       | 0|    0|    0|
|       | 1|    1|    1|
|       | 2|    0|    2|
|       | 3|    1|    3|
|       | 4|    0|    4|
|       | 5|    1|    0|

### **Kongruent oder nicht Kongruent**
$27 \equiv 42 \mod 5 ~ Rest = 2$
$-3 \equiv 39 \mod 7 ~ Rest = 4$
$981273 \not\equiv 48276 \mod 2 ~ Rest \neq Rest$
$846 \equiv 14322 \mod 3 ~ Rest = 0$

### Äquivalent Aussagen
#### $a \equiv b \mod m \Leftrightarrow m| a - b$
##### *"a und b sind dann kongruent zueinander wenn das Ergebniss aus a - b teilbar durch den Modulo m ist"*
##### *"Der Abstand zwischen zwei konguenten Zahlen ist immer ein vielfaches von $m$."*
$4 \equiv 6 \mod 2 \Leftrightarrow m ~ | ~ 4 - 6 = 2 \mid 2$
$3 \equiv 9 \mod 3 \Leftrightarrow m ~ | ~ 3 - 9 = 3 \mid 3$
$20 \equiv 10 \mod 5 \Leftrightarrow m ~ | ~ 10 - 20 = 10 \mid 5$


### Rechenregeln fuer Kongruenz  
$a_1 \equiv b_1 \mod m$
$a_2 \equiv b_2 \mod m$
$\Longrightarrow a_1 + a_2 \equiv a_2 + b_2 \mod m$

$a_1 = 120 ~ a_2 = 80 ~ b_1 = 248 ~ b_2 = 116$

$120 \equiv 248 \mod 4 ~ Rest = 0$
$80 \equiv 116 \mod 4 ~ Rest = 0$
$\Leftrightarrow 120 + 80 \equiv 248 + 116 \mod 4 ~ Rest = 0$
##### *"Wir duerfen zwei Kongruenzen modulo m addieren"*
---
$a \equiv b \mod m \Longrightarrow a \cdot c \equiv b \cdot c \mod m$

$a = 6 ~ b = 9 ~ c = 2 \mod 3$
$6 \equiv 9 \mod 3 ~ Rest = 0$
$\Leftrightarrow 6 \cdot 2 \equiv 9 \cdot 2 \mod 3 ~ Rest = 0$
##### *"Wir duerfen beide Seiten einer Kongruenz mit der gleichen ganzen Zahl multiplizieren"* 
---
$a_1 \equiv b_1 \mod m $
$a_2 \equiv b_2 \mod m $
$\Longrightarrow a_1 \cdot a_2 \equiv a_2 \cdot b_2 \mod m$

$a_1 = 3 ~ a_2 = 9 ~ b_1 = 6 ~ b_2 = 12$

$3 \equiv 6 \mod 3 ~ Rest = 0$
$9 \equiv 12 \mod 3 ~ Rest = 0$
$\Leftrightarrow 3 \cdot 9 \equiv 6 \cdot 12 \mod 3 ~ Rest = 0$
##### *"Wir duerfen zwei Kongruenzen modulo m multiplizieren"*

### Division mit Rest
*"Man sucht die Zahl r fuer die $z \equiv r ~ gilt \mod m$"*

$z = 208 ~ m = 12 ~ r = ?$
$208 \mod 12 $
$208 \div 12 = 17 + \frac{4}{12} ~ teilen ~ durch ~ m$
$208 = 17 \cdot 12 + 4 ~ ergebniss ~ multiplizieren ~ mit ~ m ~ + Rest$
$208 = 17 \cdot 12 + 4 \Longrightarrow 208 \equiv 4 \mod 12$

### Division mit Rest
$42 = 5 \cdot 8 + 2 \Rightarrow 42 \equiv 1 \mod 8$
$96 = 13 \cdot 7 + 5 \Rightarrow 96 \equiv 5 \mod 7$
$129 = 64 \cdot 2 + 1 \Rightarrow 129 \equiv 1 \mod 2$
$358 = 59 \cdot 6 + 4 \Rightarrow 358 \equiv 4 \mod 6$

### Einerziffer entscheidet
#### *"Alle Stellen außer der Einerstelle ist durch 10 Teilbar"*
$4723 = 4 \cdot 200 \cdot 5 + 7 \cdot 20 \cdot 5 + 2 \cdot 2 \cdot 5 + 3 \cdot 1 \mod 5$
$\equiv 0 \mod 5 \equiv 0 \mod 5 \equiv 0 \mod 5 \equiv 3 \mod 5$

$4723 = 4 \cdot 500 \cdot 2 + 7 \cdot 50 \cdot 2 + 2 \cdot  5 \cdot 2 + 2 \cdot 1 \cdot 1 \mod 2$
$\equiv 0 \mod 5 \equiv 0 \mod 5 \equiv 0 \mod 5 \equiv  3 \mod 5$

### Ziffernsummer entscheidet
##### *"Eine natuerliche Zahl liget immer in der selben Restklasse wie ihre Ziffernsumme"*
$4723 = 4 \cdot (999 + 1) + 4 + 7 \cdot (99 + 1) + 7 + 2 \cdot (9 + 1) + 2 + 3 \cdot 1$
$4723 = 4 \cdot 3 \cdot 333 + 4 + 7 \cdot 3 \cdot 33 + 7 + 2 \cdot 3 \cdot 3 + 2 + 3 \cdot 1 \equiv 4 + 7 + 2 + 3 \mod 3$
##### *"Eine natuerliche Zahl ist dann immer durch 3 oder 9 teilbar wenn ihre Ziffernsumme durch 3 oder 9 teilbar ist"*

### Addition und Multiplikation Modulo 4
### 1)
Rest von $(x + x) \div 4$

|+|0|1|2|3|
|-|-|-|-|-|
|0|0|1|2|3|
|1|1|2|3|0|
|2|2|3|0|1|
|3|3|0|1|2|

Rest von $(x \cdot x) \div 4$

|$\cdot$|0|1|2|3|
|-|-|-|-|-|-|
|0|0|0|0|0|
|1|0|1|2|3|
|2|0|2|0|2|
|3|0|3|2|1|

##### *"Multiplikation von Factoren $\neq$ 0 kann 0 sein $\rightarrow$ Division nicht möglich"*
### 2)
$23 = 5 \cdot 4 + 3 \Rightarrow 23 \equiv 3 \mod 4$
$42 = 10 \cdot 4 + 2 \Rightarrow 42 \equiv 2 \mod 4$
### 3)
$23 + 42 = 65 \equiv 3 + 2 \equiv 1 \mod 4$
$23 \cdot 42 = 966 \equiv 3 \cdot 2 \equiv 2 \mod 4$
> $23 \equiv 3$ liegen in der selben Restklasse sowie $42 \equiv 2$ heisst bei selben $\mod 4$ und laut der zweiten Rechenregel fuer Konguenzz liegen 966 und 6 in der selben Restklasse
### 4)
##### Es gibt drei Loesungen bei einer Grundmnege von {0, 1, 2, 3}
$2 \cdot x \equiv 2 \mod 4$
$2 \cdot 1 \equiv 2 \mod 4$
$2 \cdot 3 \equiv 2 \mod 4$

##### Es gibt keine Loesungen bei einer Grundmnege von {0, 1, 2, 3}
$2 \cdot x \equiv 1 \mod 4$

### Addition und Multiplikation Modulo 5
### 1)
Rest von $(x + x) \div 5$

|+|0|1|2|3|4|
|-|-|-|-|-|-|
|0|0|1|2|3|4|
|1|1|2|3|4|0|
|2|2|3|4|0|1|
|3|3|4|0|1|2|
|4|4|0|1|2|3|

Rest von $(x \cdot x) \div 5$

|$\cdot$|0|1|2|3|4|
|-|-|-|-|-|-|
|0|0|0|0|0|0|
|1|0|1|2|3|4|
|2|0|2|4|1|3|
|3|0|3|1|4|2|
|4|0|4|3|2|1|

### 2)
Es faellt auf das es es keinen Rest 0 mehr gibt und sich die zwei verschiebt. Ausserdem gilt fuer den Faktor $\neq 0$.

### 3)
???
### Addition und Multiplikation Modulo 6
### 1)
Rest von $(x + x) \div 6$

|+|0|1|2|3|4|5|
|-|-|-|-|-|-|-|
|0|0|1|2|3|4|5|
|1|1|2|3|4|5|0|
|2|2|3|4|5|0|1|
|3|3|4|5|0|1|2|
|4|4|5|0|1|2|3|
|5|5|0|1|2|3|4|

Rest von $(x \cdot x) \div 6$

|$\cdot$|0|1|2|3|4|5|
|-|-|-|-|-|-|-|
|0|0|0|0|0|0|0|
|1|0|1|2|3|4|5|
|2|0|2|4|0|2|4|
|3|0|3|0|3|0|3|
|4|0|4|2|0|4|2|
|5|0|5|4|3|2|1|
### 2)
Die Zeile 1 und die Zeile 5 enthalten alle Zahlen {0, 1, 2, 3, 4, 5} genau einmal, heisst die vier auesseren spalten haben bei jeder zahl {0, 1, 2, 3, 4, 5} genau einmal

### Kuerzungsregelen fuer Kongruenz
Rest von $(x + x) \div 7$

|$\cdot$|0|1|2|3|4|5|6|
|-|-|-|-|-|-|-|-|
|0|0|1|2|3|4|5|6|
|1|1|2|3|4|5|6|0|
|2|2|3|4|5|6|0|1|
|3|3|4|5|6|0|1|2|
|4|4|5|6|0|1|2|3|
|5|5|6|0|1|2|3|4|
|6|6|0|1|2|3|4|5|

Rest von $(x \cdot x) \div 7$

|$\cdot$|0|1|2|3|4|5|6|
|-|-|-|-|-|-|-|-|
|0|0|0|0|0|0|0|0|
|1|0|1|2|3|4|5|6|
|2|0|2|4|0|1|3|5|
|3|0|3|6|2|5|1|4|
|4|0|4|1|5|2|6|3|
|5|0|5|3|1|6|4|2|
|6|0|6|5|4|3|2|1|

Diese darstellung dient fuer Primzahlen, die regelmaessigkeit weisst sich dann auf wenn du Zahl nur durch sich selbst und eins Teilbar ist, z.B. ist die 7 nur durch sich selbst und eins Teilbar bei der 4 hingegen ist die Zahl noch zusaetzlich durch 2 teilbar und somit entsteht keine Zyklus.

Diese Rechenregel folgt fuer die division da es eine Primzahl ist heisst der Rest kann nur dann 0 sein wenn die Zahl druch sich selbst teilbar ist somit tritt jede Zahl in jeder spalte einmal auf.

Primzahlen: 
2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101, 103, 107, 109, 113, 127, 131, 137, 139, 149, 151, 157, 163, 167, 173, 179, 181, 191, 193, 197, 199, 211, 223, 227.