---
tags:
  - Mathe
  - Abitur
---
*Marvin Baeumer* **2023-11-14 14:32**

---
![Abitur](PDF/Mathe/5%20Abituraufgaben%202022%20oHIMI.pdf)
# Ohne Hilfsmittel
## Aufgabe 1.4
### Aufgab 1.4.1
$$
g : \vec x =
\begin{pmatrix} 
1 \\ 
1 \\ 
1 \\
\end{pmatrix} + t
\cdot
\begin{pmatrix} 
1 \\
-2 \\
0 \\
\end{pmatrix} ; 
mit ~ t \in [0 ; 3]
$$
$$g : \vec x = 
\begin{pmatrix} 
2.5 \\
-2 \\
1 \\
\end{pmatrix}$$
umstellen nach t es reicht eine Koordinate
$$
\begin{matrix}
1 + t \cdot 1 & = & 2.5 & |-1 \\
t & = & 1.5 \in [0 ; 3]
\end{matrix}
$$
$$
\begin{matrix}
1 + t \cdot (-2) & = & -2 & | & - 1 \\
- 2 \cdot t & = & - 3 & | & \div (-2) \\
t & = &  1.5 \in [0 ; 3]
\end{matrix}
$$
**Die Spitze des Roboterarms erreicht nach 1,5 Sekunden den Punkt $P(2,5|-2|1)$**.
### Aufgabe 1.4.2
$$
V : \vec x = 
\begin{pmatrix} 
0 \\ 
1 \\ 
0 \end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
1 \\ 
-2 \\ 
1 \end{pmatrix} + s 
\cdot 
\begin{pmatrix} 
1 \\ 
1 \\ 
0 \end{pmatrix}
$$
Gleichstellen um einen Schnittpunkt mit der Ebene festzustellen oder keinen Schnittpunkt
$$V : \vec x = g : \vec x$$
$$
\begin{pmatrix} 
0 \\ 
1 \\ 
0 \end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
1 \\ 
-2 \\ 
1 \end{pmatrix} + s 
\cdot 
\begin{pmatrix} 
1 \\ 
1 \\ 
0 \end{pmatrix} =
\begin{pmatrix} 
1 \\ 
1 \\ 
1 \\
\end{pmatrix} + t
\cdot
\begin{pmatrix} 
1 \\
-2 \\
0 \\
\end{pmatrix}
$$
Zuerst die 3. Gleichung um stellen
$$
\begin{matrix}
0 + r \cdot 1 + s \cdot 0 & = & 1 + t \cdot 0 & | & zusammenfassen \\
r & = & 1 \in[0 ; 2]&
\end{matrix}
$$
r in die erste Gleichung einsetzen
$$
\begin{matrix}
\Leftrightarrow & 0 + 1 \cdot 1 + s \cdot 1 & = & 1 + t \cdot 1 & | & zusammenfassen \\
& 1 + s & = & 1 + t & | & - 1 \\
& s & = & t
\end{matrix}
$$
r und s in die zweite Gleichung einsetzen
$$
\begin{matrix}
\Leftrightarrow & 1 + 1 \cdot (-2) + s \cdot 1 & = & 1 + s \cdot (-2) & | & zusammenfassen \\
& - 1 + s & = & 1 -2 \cdot s & | & + 2 s\\
& -1 + 3 \cdot s & = & 1 & | & + 1 \\
& 3 \cdot s & = & 2 & | & \div 3 \\
& s & = & \frac{2}{3} \notin [0;0,5]&
\end{matrix}
$$
**Der Roboterarm trifft nicht das Viereck.**


Frage? Heatte man nicht schon bei der ersten gleichung sehen koennen das es keine Loesung gibt und damit die Frage beantworten koennen?
$$
\begin{matrix}
0 + r \cdot 1 + s \cdot 1 & = & 1 + t \cdot 1 & | & zusammenfassen \\
r + s & = & 1 + t & | & - 1\\
-1 + r + s & = & t  
\end{matrix}
$$