---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-11-15 14:56**

---
$p = 19 ; ~ q = 23$

$n = 19 \cdot 23 = 437$ 

$\varphi(n) = 18 \cdot 22 = 396$

$e = 19$

$d = ?$
### Berechnung von $d$ mit Erweiterter Euklidischer Algorithmus
$$
\begin{matrix}
396 & = & 19 & \cdot & 20 & + & 16 & (I) \\
19  & = & 16 & \cdot & 1 & + & 3 & (II) \\
16 & = & 3 & \cdot & 5 & + &  1 & (III) \\
3 & = & 1 & \cdot & 3 & + & 0 \\
ggt & = & 1
\end{matrix}
$$
**Umstellen nach Rest**
$$
\begin{matrix}
(I)   & 16 & = & 396 & - & 20 & \cdot & 19 & \\
(II)  & 3 & = & 19 & - & 16 & \cdot & 1& \\
(III) & 1 & = & 16 & - & 5 & \cdot & 3 &
\end{matrix}
$$
**Erweiterter Euklidischer Algorithmus** 
$$
\begin{matrix}
(III) \Leftrightarrow & 1 & = & 16 & - & 5 & \cdot & 3 & \\
&& = & 16 & - & 5 & \cdot & (& 19 & - & 16 & \cdot & 1 & ) & \\
&& = & - & 5 & \cdot & 19 & + & 6 & \cdot & 16 & \\
&& = & - & 5 & \cdot & 19 & + & 6 & \cdot & ( & 396 & - & 20 & \cdot & 19 & ) & \\
&& = & - & 125 & \cdot & 19 & + & 6 & \cdot & 396 &
\end{matrix}
$$
**Nach d aufloesen**
$$
\begin{matrix}
- & 125 & \cdot & 19 & + & 6 & \cdot & 396 & \equiv & 1 & \mod 396 \\
- & 125 & \cdot & 19 & &&&& \equiv & 1 & \mod 396 \\
\end{matrix}
$$
$$
\begin{matrix}
d & = &- & 125 & + & 396 & = & 271 &\\
e & = & 19
\end{matrix}
$$
---
### Verschluesseln/Entschluesseln
$$4^{19} \mod 437 = 308$$
$$308^{271} \mod 437 = 4$$
