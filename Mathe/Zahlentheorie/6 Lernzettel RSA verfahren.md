### **Vorgehen**
Waehlen zweier Primzahlen $p$ und $q$

Berechnung von $n$ mit $p \cdot q$

Berechnung von $\varphi(n)$ mit $(p − 1) \cdot (q − 1)$

Waehlen von $e$ $\rightarrow$ teilerfremd zu $\varphi(n)$ und $1 < e < \varphi(n)$

Berechnung von $d$ mit erweiterter euklidischer algorythmus mit $\varphi(n)$ und $e$
- fuer d gillt $e \cdot d \equiv 1 \mod \varphi(n)$

Bilden des Public Key $(n, e)$

Bilden des Private Key $(n, d)$

Eine Nachricht $m$ verschluesseln mit $m^{e} \mod n$

Die verschluesselte Nachricht $c$ entschluesseln mit $c^{d} \mod n$
### **Beispiel**
$p = 19 ~ q = 23$
$n = p \cdot q = 19 \cdot 23 = 437$
$\varphi(n) = (p - 1) \cdot (q - 1) = 18 \cdot 22 = 396$
$e = 23$\
$d = 155$
### **Berechnung von d**
#### **Euklidischer Algorytmus**
$396 = 23 \cdot 17 + 5$
$23 = 5 \cdot 4 + 3$
$5 = 3 \cdot 1 + 2$
$3 = 2 \cdot 1 + 1$
$2 = 1 \cdot 2 + 0$
#### **Umstellen nach Rest**
$5 = 396 - 23 \cdot 17$
$3 = 23 - 5 \cdot 4$
$2 = 5 - 3 \cdot 1$
$1 = 3 - 2 \cdot 1$
#### **Erweiter Euklidischer Algorythmus**
$1 = 3 - 2 \cdot 1 = 3 - 1 \cdot (5 - 3) = 3 - 5 + 3$
$- 5 + 2 \cdot 3 = - 5 + 2 \cdot (23 - 5 \cdot 4) = - 5 + 2 \cdot 23 - 8 \cdot 5$
$-9 \cdot 5 + 2 \cdot 23 = - 9 \cdot (396 - 17 \cdot 23) + 2 \cdot 23 = -9 \cdot 396 + 153 \cdot 23 + 2 \cdot 23$
$\underline{-9 \cdot 396 + 155 \cdot 23}$
#### **Nach d aufloesen**
$-9 \cdot 396 + 155 \cdot 23 \equiv 1 \mod 396 ~ | -9 \cdot 396$ faelt weg weil Rest $= 0$ wegen $\mod 396$
$155 \cdot 23 \equiv 1 \mod 396 ~ 23$ ist unser $e$ deswegen egal = $e \cdot d$
### **Ver- und entschluesselung**
Public Key $(437, 23)$
Private Key $(437, 155)$

$Verschluesselung: m^e \mod n ~ | ~ m = 420 = 420^{23} \mod 437 = 374$
$Entschluesselung: c^d \mod n ~ | ~ c = 374 = 374^{155} \mod 437 = 420$

### [Zum Code](5%20RSA%20Verfahren)

---
*Marvin Baeumer* **2023-10-30 17:05** #Mathe