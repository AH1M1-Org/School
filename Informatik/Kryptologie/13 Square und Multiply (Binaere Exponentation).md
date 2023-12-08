---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-08 11:04**

---
$$
x^{23} = 22 ~ \text{Multiplikationen}
$$
1. Schritt: 23 in Binaer schreiben (immer die zweier Potenzen nehmen)
$$
23 = 1 \cdot 16 + 0 \cdot 8 + 1 \cdot 4 + 1 \cdot 2 + 1 \cdot 1
$$
$$
10111
$$
2. Schritt: Jede 1 wird ersetzt durch $QM$ und jede $0$ durch $Q$
	- $QM \rightarrow Quadrieren$
	- $Q \rightarrow Multiplizieren$
$$
10111 = QMQQMQMQM
$$
3. Schritt: Erstes QM streichen! $\rightarrow$ jede pos Binaer Zahl faengt mit 1 an!
$$
10111 = QQMQMQM
$$
$$
(((((x^2)^2) \cdot x)^2)\cdot x)^2 \cdot x
$$
$$
((x^4 \cdot x)^2 \cdot x)^2 \cdot x = (x^{10} \cdot x)^2 \cdot x = x^{22} \cdot x = x^{23}
$$
> 7 Multiplikationen statt 22!

### Beispiel
$$
2^{18} \mod 39
$$
$$
10010 = QQQMQ
$$
$$
= (((2^2)^2)^2) \cdot 2)^2 \mod 39
$$
$$
(256 \cdot 2)^2 \mod 39 = (22 \cdot 2)^2 \mod 39 = 44^2 \mod 39 = 5^2 \mod 39= 25 \mod 39 = 25
$$

$$
17 = 1 \cdot 16 + 0 \cdot 8 + 0 \cdot 4 + 0 \cdot 2 + 1 \cdot 1  
$$
$$
= 10001 = QQQQM
$$
$$
= ((((82^2)^2)^2)^2) \cdot 82 \mod 20
$$
$$
= (((4^2)^2)^2) \cdot 2 \mod 20
$$
$$
= 256^2 \cdot 2 \mod 20
$$

$$
46^{78} \mod 1277
$$
$$
78 = 1 \cdot 64 + 0 \cdot 32 + 0 \cdot 16 + 1 \cdot 8 + 1 \cdot 4 + 1 \cdot 2 + 0 \cdot 0
$$
$$
= 1001110 = QQQMQMQMQ
$$
$$
\begin{align*}
46^{78} \mod 1277 & \\
78 &= 1 \cdot 64 + 0 \cdot 32 + 0 \cdot 16 + 1 \cdot 8 + 1 \cdot 4 + 1 \cdot 2 + 0 \cdot 1 = 1001110 \\
1001110 &= \text{QMQQQMQMQMQ} = \text{QQQMQMQMQ} \\
& \\
& ((((46^2)^2)^2 \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = ((((((839^2)^2) \cdot 46)^2 \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = ((((((294^2) \cdot 46)^2 \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = (((((877 \cdot 46)^2 \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = ((((755^2) \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = (((483 \cdot 46)^2 \cdot 46)^2 \mod 1277 \\
& = ((509^2 \cdot 46)^2 \mod 1277 \\
& = (1127 \cdot 46)^2 \mod 1277 \\
& = 762^2 \mod 1277 \\
& = 886
\end{align*}
$$
