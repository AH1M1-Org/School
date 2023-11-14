---
tags:
  - Informatik
---

*Marvin Baeumer* **2023-11-10 09:28**

---
### Theorie
- Zwei Zahlen $p , g$ diese sind oeffentlich einsehbar, fuer p gilt $\mathbb{P}$,  fuer gilt $g \rightarrow \mathbb{N}, g < p$   
- Waeheln eines $a < p$ und $b < p$ diese sind privat, fuer beide gilt $\in \mathbb{N}$  
- Berechnung $A = g^a \mod p$ und $B = g^b \mod p$ 
- Austausch von $A$ und $B$
- Berechnung von $K = B^a \mod p$ und $K = A^b \mod p$
Das Diffi-Hellmann verfahren dient dem Schluesselaustausch, $K$ ist dann der geheime Schluessel.
### Beispiel
$p = 31, g = 15$

| Person A                   | Person B                  |
| -------------------------- | ------------------------- |
| $a = 25$                   | $b = 14$                  |
| $A = 15^{25} \mod 31$ = 30 | $B = 15^{14} \mod 31 = 2$ |
| $K = 2^{25} \mod 31 = 1$   | $K = 30^{14} \mod 31 = 1$ |

Private Key = 1