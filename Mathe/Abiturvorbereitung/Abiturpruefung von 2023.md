---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-11-12 00:07**

---
[Mathematica](Abituraufgaben%202023.nb) 
![Abitur](4%20Abiturprüfung%20Mathe%202023%20MHIMI.pdf)
# Mit Hilfsmitteln
## Aufgabe 4
### Aufgabe 4.1
$Punkt ~ A_1 ~ (-10 | -5)$ 
$x = 0 - 10 = -10$
$y = 0 - 10 \div 2 = - 5$

$Punkt ~ B_1 ~ (-7 | + 5)$
$x = 0 - 7 = - 7$
$y = 0 + 10 \div 2 = - 5$ 

### Aufgabe 4.2
$$\vec {ON_t} = \begin{pmatrix} t \\ 0 \\ 0.88 + 0.0016 \cdot t ^ 2\end{pmatrix} mit ~ t \in [-5;5]$$
Die Netzoberkannte kann als Parabel gesehen werden.
$$f(x) = 0.88 + 0.0016 \cdot t ^ 2$$
$$f(x) = 0.8996 \Longleftrightarrow t_{1,2} \pm 3.5$$Abziehen von 5 wegen Mindestabstand von den seitlichen Spielfeld Markierungen. 
$$5 - 3.5 = 1.5; -5 - (-3.5) = -1.5$$
**Der Mindestabstand betraegt 1.5m von den Seitlichen Markierungen.**
### Aufgabe 4.3
aufstellen der Geradengleichung fuer den Ball
$$
g : \vec x = 
\begin{pmatrix} 
1 \\ 
-0.5 \\ 
1.5 \end{pmatrix} + t 
\cdot 
\begin{pmatrix} 
0.9 \\ 
1.4 \\
-0.3 \end{pmatrix}
$$
$x_2$ Koordinaten $= 0$ stellen, weil $x_2$ beschreibt die Laenge also wenn $x_2 = 0$ ist, ist der Ball auf Hoehe des Netzes
$$-0.5 + t \cdot 1.4 = 0 \Longleftrightarrow t = 0.357143$$
Einsetzen um die Hoehe des Balles zu erhalten
$$
\Leftrightarrow 
\begin{pmatrix} 
1 \\ 
-0.5 \\ 
1.5 \end{pmatrix} + 0.357143 
\cdot 
\begin{pmatrix} 
0.9 \\ 
1.4 \\
-0.3 \end{pmatrix} =
\begin{pmatrix}
1.32 \\
0 \\
1.39
\end{pmatrix}
$$
**Der $x_3$ Wert zeigt das der Ball in einer Hoehe von 1.39m ist, das Netz ist an der Hoechsten Stelle 0.92m Hoch also geht der Ball ueber das Netz.**

Berechnung des Schnittpunktes vom Ball mit der Spielflaeche($x_1, x_2$ Ebene) 
$$1.5 + t \cdot -0.3 = 0 \Longleftrightarrow t = 5$$
Einsetzen um den Schnittpunkt mit der Ebene zu erhalten also dort wo der Ball landet
$$
\Leftrightarrow 
\begin{pmatrix} 
1 \\ 
-0.5 \\ 
1.5 \end{pmatrix} + 5 
\cdot 
\begin{pmatrix} 
0.9 \\ 
1.4 \\
-0.3 \end{pmatrix} =
\begin{pmatrix}
5.5 \\
6.5 \\ 
0 \end{pmatrix}
$$
**Die $x_1$ Koordinate liegt bei $5.5$ dies ist ausserhalb des Feldes, heisst der Ball landet nicht Regelgerecht auf der anderen Seite.**
### Aufgabe 4.4
Wir berechnen erst die Distanz die zwischen den beiden Punkten liegt
$$
\begin{pmatrix} 
1 \\ 
8 \\ 
0 \end{pmatrix} - 
\begin{pmatrix} 
- 3 \\ 
- 2.1 \\ 
1.8 \end{pmatrix} =
\begin{pmatrix}\
4 \\
10.1 \\
- 1.8\\
\end{pmatrix}
$$
Von diesem Vektor Nehmen wir die Laenge damit wir die Meter durch die 15 Sekunden teilen koennen.
$$
\frac
{
\left |
\begin{pmatrix}\
4 \\
10.1 \\
- 1.8\\
\end{pmatrix}
\right |
}
{
15
}
= 0.73
$$
**Der Ball war ca. 0.73 Sekunden unterwegs.**
### Aufgabe 4.5
Mittelpunktberechnen
$$M (\frac{a_x + b_2}{2} | \frac{a_y + b_y}{2} | \frac{a_z + b_z}{2}) \Leftrightarrow M (\frac{2 + (-2)}{2} | \frac{-7 + 3}{2} | \frac{1 + 1}{2}) = (0 ,- 2 ,1)$$
$$M = (0 | - 2 | 1.5)$$
**$x_3$ kann ignoriert werden da wir es als Parabel betracheten, also sind die Koordinaten des Punktes $H = (0 | -2 | 1.5)$.**

S als Ortvektor von Punkt Q den Punkt S abziehen und vom Punkt H den Punkt S abziehen.
$$
E : \vec x = 
\begin{pmatrix} 
2 \\
-7 \\
1 \\
\end{pmatrix} + r
\cdot
\begin{pmatrix} 
- 4 \\
- 10 \\
0 \\
\end{pmatrix} + v
\begin{pmatrix} 
-2 \\
5 \\
0.5 \\
\end{pmatrix}
$$
### Aufgabe 4.6
$$
E : \vec x = 
\begin{pmatrix} 
0 \\ 
0 \\ 
0 \end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
0 \\ 
7 \\ 
0 \end{pmatrix} + v 
\cdot 
\begin{pmatrix} 
5 \\ 
7 \\ 
0 \end{pmatrix}
$$
$$
\left |
\begin{pmatrix} 
5 \\ 
0 \\ 
3 \end{pmatrix} -
\begin{pmatrix}
x \\
y \\
0 \\
\end{pmatrix}
\right| = 
9.08955 
\Longleftrightarrow x = -3.49, y = 1.25
$$
$$
\left |
\begin{pmatrix} 
-5 \\ 
6 \\ 
4 \end{pmatrix} -
\begin{pmatrix}
x \\
y \\
0 \\
\end{pmatrix}
\right| = 
6,38905
\Longleftrightarrow x = -0.1, y = 6.9
$$
$$Pos1
\begin{pmatrix}
-3.49 \\
1.25 \\
0
\end{pmatrix};
Pos2
\begin{pmatrix}
-0.1 \\
6.9 \\
0
\end{pmatrix};
$$
$Pos 1$ liegt nicht im Bereich, weil $x_1$ im negativen Bereich ist und somit nicht mehr auf der Ebene $E : \vec x$ liegt das selbe gilt fuer $Pos 2$.
### Aufgabe 4.7
$$
S_1: \begin{pmatrix} 
\frac{1}{2} & 0 \\ 
0 & \frac{1}{2}
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} + 
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}
$$
$$
S_2: \begin{pmatrix} 
1 & 0 \\ 
0 & 1
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} + 
\begin{pmatrix}
0 \\
40 \\
\end{pmatrix}
$$
$$
S_3: \begin{pmatrix} 
0 & - 1 \\ 
1 & 0
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} + 
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}
$$
$$
S_4: \begin{pmatrix} 
0 & 1 \\ 
1 & 0
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} + 
\begin{pmatrix}
40 \\
0 \\
\end{pmatrix}
$$
```
´´´´´´¶¶¶¶ 
´´´´´¶´´´´¶¶ 
´´´´´¶´´´´´¶ 
´´´´´´¶´´´´¶ 
´´´´´´¶´´´¶ 
´´´´¶¶¶¶¶¶¶¶¶¶¶¶ 
´´´¶´´´´´´´´´´´´¶ 
´´¶´´´´´´´´´´´´¶ 
´¶¶´´´¶¶¶¶¶¶¶¶¶¶¶ 
´¶´´´´´´´´´´´´´´´¶ 
´¶´´´´´´´´´´´´´´´¶ 
´´¶´´´¶¶¶¶¶¶¶¶¶¶¶ 
´´´¶´´´´´´´´´´´¶ 
´´´´¶¶¶¶¶¶¶¶¶¶¶
```