---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-10-31 12:52**

---
### Zahlentheorie
### Rechenregeln

$a_1 \equiv b_1 \mod m$
$a_2 \equiv b_2 \mod m$

$a_1 + a_2 \equiv b_1 + b_2 \mod m$
*Zwei kongruenzen duerfen miteinader addiert werden*

$a_1 \equiv b_2 \mod m$
$a_1 \cdot c \equiv b_2 \cdot c \mod m$
*Eine kongruenz darf mit einer beliebiegen Zahl auf beiden Seiten multipliziert werden*

$a_1 \equiv b_1 \mod m$
$a_2 \equiv b_2 \mod m$

$a_1 \cdot a_2 \equiv b_1 \cdot b_2 \mod m$
*Zwei kongruenzen duerfen miteinader multiplziert werden*

### Teilbarkeitsregeln
- Eine Zahl kann durch zwei geteilt werden wenn ihre einerstelle auf {2,4,6,8} endet
- Eine Zahl kann durch 3 geteilt werden wenn ihre Quersumme durch 3 teilbar ist
- Eine Zahl kann durch 4 geteilt werden wenn man die letzeten beiden Ziffern zusammen druch 4 teilen kann
- Eine Zahl kann durch 5 geteilt werden wenn ihr einerziffer auf 0 oder 5 endet
- Eine Zahl kann durch 6 geteilt werden wenn sie durch 2 und 3 teilbar ist
- Eine Zahl kann durch 8 geteilt werden wenn die letzeten 3 stellen durch 8 teilbar sind
- Eine Zahl kann durch 9 geteilt werden wenn ihr Quersumme durch 9 geteilt werden kann

### Prufziffer verfahren
$d_{13} = a_1 + 3 \cdot a_2 + a_3 + 3 \cdot a_4 + a_5 + 3 \cdot a_6 + a_7 + 3 \cdot a_8 + a_9 + 3 \cdot a_{10} + a_{11} + 3 \cdot a_{12} \rightarrow$ so das dann durch mod 10 = 0 ergibt differenz 

Welche tippfehler koennen nicht erkannt werden?

Wenn $a_1$ und $a_3$ getauscht werden oder $a_2$ und $a_4$ getauscht werden $\rightarrow$ kommunitativ gesetz

Ausserdem kann ein tipp fehler nicht erkannt werden wenn $a_1$ und $a_2$ getauscht werden wenn das ergebnis dann durch mod 5 geteilt werden kann.

$(x_2 + 3 \cdot x_1) - (x_1 + 3 \cdot x_2) \equiv 0 \mod 10$

$x_2 + 3 \cdot x_1 - x_1 - 3 \cdot x_2  \equiv 0 \mod 10$

$- 2 \cdot x_2 + 2 \cdot x_2  \equiv 0 \mod 10 ~ | \div 2$

$- x_2 + x_2 \equiv 0 \mod 5 \rightarrow ggt(2,10)$

### RSA - Verfahren
p und q waehlen (zwei Primzahlen)

$p = 5$

$q = 7$

$n = 35$

$\varphi(n) = 24$

$e = 5$

$d = 5$

$public key (n, e)

private key (n, d)

$24 = 5 \cdot 4 + 4$\
$5 = 4 \cdot 1 + 1$\
$4 = 1 \cdot 4$

$1 = 5 - 4 \cdot 1$\
$4 = 24 - 5 \cdot 4$

$1 = 5 - 1 \cdot (24 - 5 \cdot 4) = 5 - 1 \cdot 24 + 4 \cdot 5$

$- 1 \cdot 24 + 5 \cdot 5 \equiv 1 \mod 24$

$5 \cdot 5 \equiv 1 \mod 24$

$d = 5$

$m = 2$

public key (35, 5)

private key (35, 5)

$m` = 2^5 \mod 35$

$m` = 32$

$32^5 \mod 35$

$m = 2$