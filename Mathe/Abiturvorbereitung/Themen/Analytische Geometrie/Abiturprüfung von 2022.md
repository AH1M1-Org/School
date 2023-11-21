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
# Mit Hilfsmittel 
[Mathematica](Mathe/Mathematica/Abituraufgaben%202022.nb) 
![Bild](PDF/Mathe/5%20Abituraufgaben%202022%20mHIMI.pdf)
## Aufgabe 4
### Aufgabe 4.1
$$
\begin{pmatrix}
0 \\
50 \\
3 \\
\end{pmatrix}
-
\begin{pmatrix}
30 \\
50 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
-30 \\
0 \\
3 \\
\end{pmatrix}
$$
$$
\begin{pmatrix}
0 \\
30 \\
0 \\
\end{pmatrix}
-
\begin{pmatrix}
30 \\
50 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
-30 \\
-20 \\
0 \\
\end{pmatrix}
$$
$$
E : \vec x = 
\begin{pmatrix} 
30 \\ 
50 \\
0 \\
\end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
-30 \\ 
0 \\ 
3 \\ 
\end{pmatrix} + v 
\cdot 
\begin{pmatrix} 
-30 \\ 
-20 \\ 
0 \\
\end{pmatrix}
$$
Die Ebenengleichung lautet: siehe $E : \vec x$.
### Aufgabe 4.2.1
$$
M (
\frac{a_x + b_2}{2} | 
\frac{a_y + b_y}{2} | 
\frac{a_z + b_z}{2}) 
\Leftrightarrow 
M 
(\frac{30 + 0}{2} | 
\frac{50 + 30}{2} | 
\frac{0 + 0}{2}) = 
(15 ,40 ,0)
$$
Der Mittelpunkt liegt bei $(15 ,40 ,0)$.
### Aufgabe 4.2.2
$$
\begin{pmatrix}
15 \\
30 \\
0 \\
\end{pmatrix}
-
\begin{pmatrix}
20 \\
10 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
-5 \\
30 \\
0 \\
\end{pmatrix}
$$
$$
g : \vec x = 
\begin{pmatrix} 
20 \\ 
10 \\ 
0 \\ 
\end{pmatrix} + t 
\cdot 
\begin{pmatrix} 
-5 \\ 
30 \\
0 \\
\end{pmatrix}
$$
$$
g : \vec x 
= 
\begin{pmatrix}
5,5 \\
47 \\
0 \\
\end{pmatrix}
\rightarrow
\{ ~ \}
$$
Der proezierte Punkt $A'$ liegt nicht auf der Geraden $g : \vec x$. 
### Aufgabe 4.2.3
### Aufgabe 4.3
$$
\begin{pmatrix}
0 \\
50 \\
0 \\
\end{pmatrix}
-
\begin{pmatrix}
30 \\
0 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
-30 \\
50 \\
0 \\
\end{pmatrix}
$$
$$
P_2P_4 : \vec x = 
\begin{pmatrix} 
30 \\ 
0 \\ 
0 \\
\end{pmatrix} + t 
\cdot 
\begin{pmatrix} 
-30 \\ 
50 \\
0 \\
\end{pmatrix}
$$
$$
\begin{pmatrix}
0 \\
30 \\
0 \\
\end{pmatrix}
-
\begin{pmatrix}
30 \\
50 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
-30 \\
-20 \\
0 \\
\end{pmatrix}
$$$$
P_3P_5 : \vec x = 
\begin{pmatrix} 
30 \\ 
50 \\ 
0 \\
\end{pmatrix} + t 
\cdot 
\begin{pmatrix} 
-30 \\ 
-20 \\
0 \\
\end{pmatrix}
$$
$$P_2P_4=P_3P_5 \rightarrow t = \frac{5}{7}$$
$$
\left|
P_2P_4(\frac{5}{7}) 
- 
\begin{pmatrix} 
30 \\
0 \\
0 \\
\end{pmatrix}
\right|
+
\left|
\begin{pmatrix} 
0 \\
50 \\
3 \\
\end{pmatrix}
-
P_3P_5(\frac{5}{7}) 
\right|
\approx 
58,58
$$
Die Strecke die der Roboter zureucklegt betraegt 58,58m.
### Aufgabe 4.4.1
$$
shaun(t) = 
\begin{pmatrix}
30 \\
0 \\
\end{pmatrix}
+ t 
\cdot
\begin{pmatrix}
-0,1 \\
0,15 \\
\end{pmatrix}
$$
$$
timmy(t) = 
\begin{pmatrix}
29 \\
20 \\
\end{pmatrix}
+ t 
\cdot
\begin{pmatrix}
- 0,1 \\
- 0,1 \\
\end{pmatrix}
$$
$$
\left| 
shaun(t)-timmy(t) 
\right|
= 1,5 
\Rightarrow 75,56 < t < 84,47
$$
Zum Zeitpunkt 75,56 bis 84,47 unterschreiten Timmy und Shaun den Abstand von 1,5m.
### Aufgabe 4.4.2