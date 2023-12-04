---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-11-27 16:17**

---
# Vektoren
### Grundlagen
#### Geradengleichung
> Eine Geradengleichung besteht aus einem Ortsvektor und einem Bewegungsvektor. Dabei gibt der Ortsvektor die Startposition des Vektors zum Zeitpunkt $t = 0$ an, und der Bewegungsvektor gibt die Richtung und den Betrag der Verschiebung des Vektors an. Der Bewegungsvektor lässt sich mit $t$ multiplizieren, um somit die Bewegung nach $t$ Schritten darzustellen.

$$\large Form$$
$$
g : \vec x = 
\begin{pmatrix} 
x_1 \\ 
y_1 \\
z_1 \\
\end{pmatrix} 
+ 
t 
\cdot 
\begin{pmatrix} 
x_2 \\ 
y_2 \\
z_2 \\
\end{pmatrix}
$$
> Einen Bewegungsvektor kann man berechnen, indem man die Spitze $-$ Fuss rechnet.

##### Beispiel
> Wir haben zwei Punkte $A$ und $B$ und sollen nun eine Geradengleichung aufstellen, die durch beide Punkte verläuft. Punkt $A$ ist in diesem Fall unser Ortsvektor, und unser Bewegungsvektor ergibt sich, indem wir vom Punkt $B$ den Punkt $A$ subtrahieren.

$$
\large A
\normalsize
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
,
\large B
\normalsize
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
$$
$$
g : \vec x = 
\begin{pmatrix} 
x_1 \\ 
y_1 \\ 
z_1 \\
\end{pmatrix} 
+ 
t 
\cdot 
\begin{pmatrix} 
x_2 - x_1 \\ 
y_2 - y_1 \\
z_2 - z_1 \\
\end{pmatrix}
$$

<div style="page-break-after: always;"></div>

#### Ebenengleichung
> Eine Ebenengleichung setzt sich zusammen aus einem Ortsvektor und Bewegungsvektoren. Eine Ebenengleichung dient dazu, eine Ebene im dreidimensionalen Raum darzustellen. Diese ist unendlich groß, aber in vielen Anwendungszwecken auf einen bestimmten Bereich begrenzt.

$$\large Form$$
$$
E : \vec x = 
\begin{pmatrix} 
x_1 \\ 
y_1 \\ 
z_1 \\
\end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
x_2 \\ 
y_2 \\ 
z_2 \\
\end{pmatrix} + v 
\cdot 
\begin{pmatrix} 
x_3 \\ 
y_3 \\ 
z_3 \\ 
\end{pmatrix}
$$

#### Distanzen - Laengen
> Zieht man zwei Punkte voneinander ab, erhält man die Distanz zwischen den beiden Punkten. Dies hilft oft dabei, Bewegungsvektoren zu erstellen oder auf Orthogonalität zu überprüfen. Punkte lassen sich immer in Vektoren umschreiben. Nimmt man nun die Länge des Vektors, erhält man die Strecke. Dies ist insbesondere wichtig, um zu sehen, wie weit sich etwas in einer bestimmten Zeit bewegt hat. Man bezeichnet Strecken als Längeneinheiten (LE).

$$\large Formel$$
$$
\large
\sqrt
{
x^2 +
y^2 +
z^2
}
=
c ~ LE
$$
```Mathematica
Norm[{x, y, z}]
```

<div style="page-break-after: always;"></div>

### Ebenen
> Im dreidimensionalen Raum gibt es drei Ebenen: $x_1x_2, ~ x_1x_3, ~ x_2x_3$. Jede dieser Ebenen hat an ihrer nicht aufgezählten Koordinate den Wert $= 0$. Möchte man nun feststellen, ob ein Punkt auf einer dieser Ebenen liegt, stellt man die Gleichung der nicht aufgezählten Koordinate auf $= 0$.

$$
g : \vec x
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
+
t
\cdot
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
$$
#### $x_1x_2 - Ebene$ 
> Man nimmt die Gleichung der dritten Koordinate und setzt sie gleich $0$.

$$
\begin{matrix}
z_1 
+
t
\cdot
z_2
=
0 \\
t 
\rightarrow
a
\end{matrix}
$$
> Nun haben wir eine Lösung für $t$. Diese wird dann in die Gleichung $g : \vec x$ eingesetzt, und so erhält man den Spurpunkt der $x_1​x_2​$ Ebene.
#### $x_1x_3 - Ebene$ 
> Man nimmt die Gleichung der zweiten Koordinate und setzt sie gleich $0$.

$$
\begin{matrix}
y_1 
+
t
\cdot
y_2
=
0 \\
t 
\rightarrow
a
\end{matrix}
$$
> Nun haben wir eine Lösung für $t$. Diese wird dann in die Gleichung $g : \vec x$ eingesetzt, und so erhält man den Spurpunkt der $x_1​x_3​$ Ebene.
#### $x_2x_3 - Ebene$ 
> Man nimmt die Gleichung der erste Koordinate und setzt sie gleich $0$.

$$
\begin{matrix}
x_1 
+
t
\cdot
x_2
=
0 \\
t 
\rightarrow
a
\end{matrix}
$$
> Nun haben wir eine Lösung für $t$. Diese wird dann in die Gleichung $g : \vec x$ eingesetzt, und so erhält man den Spurpunkt der $x_2​x_3$ Ebene.

```Mathematica
(*x1x2 Ebene*) Solve[z1 + t * z2 == 0]
(*x1x3 Ebene*) Solve[y1 + t * y2 == 0]
(*x2x3 Ebene*) Solve[x1 + t * x2 == 0]
(*oder*)
(*x1x2 Ebene*) Solve[{x1, y1, z1} + t * {x2, y2, z2} == {x,y,0}]
(*x1x3 Ebene*) Solve[{x1, y1, z1} + t * {x2, y2, z2} == {x,0,z}]
(*x2x3 Ebene*) Solve[{x1, y1, z1} + t * {x2, y2, z2} == {0,y,z}]
```


<div style="page-break-after: always;"></div>

### Skalarprodukt
> Mit dem Skalarprodukt lässt sich prüfen, ob zwei Vektoren orthogonal zueinander sind. Es lässt sich auch der Winkel zwischen zwei Vektoren berechnen.
#### Orthogonal
$$\large Formel$$
$$
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
\times
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
= 
x_1 \cdot x_2
+
y_1 \cdot y_2
+
z_1 \cdot z_2
$$
> Es kann nun zwei Ergebnisse geben, $0$ oder $\neq 0$. Ist das Ergebnis $0$, sind die beiden Vektoren orthogonal zueinander. Wenn das Ergebnis nicht $0$ ist, dann sind sie nicht orthogonal.
```Mathematica
{x1, y1, z1}.{x2, y2, z2} (*Berechnung in Mathematica*)
```
$$
\vec a
=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
,
\vec b
=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
,
\vec c
=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
,
\vec b
=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
$$
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[very thin,color = black] (-5,-5) grid (5,5); 
\draw[ultra thick, ->] (-5,0) -- (5.1,0) node[right] {$x_1$}; 
\draw[ultra thick, ->] (0,-5) -- (0,5.1) node[above] {$x_2$}; 

\draw[ultra thick, ->] (-4,-4) -- (-2,-3) node[below] {$\vec a$}; 
\draw[ultra thick, ->] (-2,-3) -- (-3,-1) node[above] {$\vec b$};

\draw[ultra thick, ->] (1,1) -- (2,3) node[below] {$\vec c$}; 
\draw[ultra thick, ->] (2,3) -- (1,5) node[above] {$\vec d$};

\end{tikzpicture}
\end{document} 
```
> Die Vektoren $\vec{a}$ und $\vec{b}$ sind orthogonal zueinander. Die Vektoren $\vec{c}$ und $\vec{d}$ sind nicht orthogonal.

<div style="page-break-after: always;"></div>

#### Winkel
$$\large Formel$$
$$
\vec a
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
,
\vec b 
=
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
$$
$$
\large
\gamma
=
\cos^{-1}
\huge
\begin{pmatrix}
\frac
{
\vec a 
\times
\vec b
}
{
\left|
\vec a
\right|
\cdot
\left|
\vec b
\right|
}
\end{pmatrix}
$$
> Man berechnet das Skalarprodukt zweier Vektoren, indem man es durch das Produkt der Längen von $\vec{a}$ und $\vec{b}$ teilt.
```Mathematica
N[VectorAngle[{x, y, z},{x, y, z}]/°] (*/° gibt den output als ° Zahl*)
```

<div style="page-break-after: always;"></div>

### Kreuzprodukt
> Mit dem Kreuzprodukt lässt sich ein Vektor erzeugen, der immer orthogonal zur Ebene steht. Das wird verwendet, um z.B. den Abstand zu einem Objekt über der Ebene zu bestimmen, den Schnittwinkel einer Geraden zu finden, usw. Die Länge des Kreuzproduktes ergibt den Flächeninhalt der Fläche.

$$\large Formel$$
$$
\begin{pmatrix} 
x_1 \\ 
y_1 \\ 
z_1 \\
\end{pmatrix} 
\times 
\begin{pmatrix} 
x_2 \\ 
y_2 \\ 
z_2 \\ 
\end{pmatrix} 
= 
\begin{pmatrix} 
y_1 \cdot z_2 - z_1 \cdot y_2 \\ 
z_1 \cdot x_2 - x_1 \cdot z_2 \\ 
x_1 \cdot y_2 - y_1 \cdot x_2 \\
\end{pmatrix} 
= 
\begin{pmatrix} 
x \\ 
y \\ 
z \\ 
\end{pmatrix}
$$
> Nimmt man nun die Länge des Vektors, erhält man den Flächeninhalt.
```Mathematica
Cross[{x1, y1, z1},{x2, y2, z2}]
```

<div style="page-break-after: always;"></div>

### Schnittwinkel
> Schnittwinkel sind Winkel zwischen einer Geradengleichung $g : \vec{x}$ und einer Ebene $E : \vec{x}$. Diese werden oft verwendet, um den Eintrittswinkel von Lichtstrahlen zu berechnen. Man benötigt also eine Geradengleichung $g : \vec{x}$, eine Ebenengleichung $E : \vec{x}$, das Kreuzprodukt $\vec{n}$ und den Winkel zwischen $g : \vec{x}$ und $\vec{n}$.

$$\large Berechnung$$
$$g : \vec x 
= \vec u 
+ 
t 
\cdot 
\vec 
v$$
$$
E : \vec x 
= 
\vec u_E 
+ 
t 
\cdot 
\vec v_E 
+ 
r 
\cdot 
\vec w_E
$$
$$
\vec n =
\vec v_E
\times
\vec w_E
$$
> Berechnung des Winkels $\gamma$ zwischen $\vec{n}$ und der Geraden $g : \vec{x}$.

$$
\gamma = 
\cos^{-1} 
\begin{pmatrix} 
\frac
{
\vec n 
\cdot 
\vec v
}
{
\left| 
\vec n 
\right| 
\cdot 
\left| 
\vec v 
\right|
} 
\end{pmatrix}
$$
> Der Winkel $\alpha$ zwischen $\vec{n}$ und der Ebene $E : \vec{x}$ beträgt $90^\circ$, weil $\vec{n}$ orthogonal zur Ebene steht.

$$
\alpha
-
\gamma
=
\beta
$$
> Der Winkel $\beta$ ist dann unser Schnittwinkel.
### Spiegelung eines Punktes
> Wenn man einen Punkt spiegeln möchte, stellt man eine Geradengleichung auf. Man verwendet das Kreuzprodukt der Ebene als Bewegungsvektor und den Punkt selbst als Ortsvektor. Die Geradengleichung setzt man gleich der Ebenengleichung und erhält so einen Schnittpunkt. Anschließend multipliziert man den Schnittpunkt mit $2$, um den gespiegelten Punkt zu erhalten. Man geht also nur die doppelte Menge an Schritten, um den Punkt auf der anderen Seite zu bekommen.

$$
E : \vec x = 
\begin{pmatrix} 
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix} + r 
\cdot 
\begin{pmatrix} 
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix} + v 
\cdot 
\begin{pmatrix} 
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
$$
$$
g : \vec x = 
\begin{pmatrix} 
x_4 \\
y_4 \\
z_4 \\
\end{pmatrix} + t 
\cdot
\left(
\begin{pmatrix} 
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
\times
\begin{pmatrix} 
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
\right)
$$
$$
\begin{matrix}
g : \vec x && 
= &&
E : \vec x 
\\
t \rightarrow a && r \rightarrow b && v \rightarrow c
\end{matrix}
$$
$$
Gespiegelter ~ Punkt = 
g : \vec x
(a \cdot 2)
=
\begin{pmatrix}
x_5 \\
y_5 \\
z_5 \\
\end{pmatrix}
$$

<div style="page-break-after: always;"></div>

### Spiegelung einer Geraden
> Um eine Geradengleichung zu spiegeln, benötigen wir einen gespiegelten Punkt. Von diesem Punkt aus berechnen wir die Distanz zum Schnittpunkt zur Ebene, um so unseren Bewegungsvektor zu erhalten. Somit können wir eine Geradengleichung aufstellen, die eine gespiegelte Gerade darstellt. In diesem Beispiel repräsentiert $p'$ den gespiegelten Punkt, $s$ den Schnittpunkt und $g'$ die gespiegelte Gerade.

$$
p'
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
;
s
=
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
$$
$$
g' : \vec x = 
\begin{pmatrix} 
x_1 \\ 
y_1 \\
z_1 \\
\end{pmatrix} 
+ 
t 
\cdot 
\begin{pmatrix} 
x_2 - x_1 \\ 
y_2 - y_1 \\
z_2 - z_1 \\
\end{pmatrix}
$$

<div style="page-break-after: always;"></div>

### Lagebeziehung
> Man unterscheidet zwischen vier verschiedenen Lagen zweier Vektoren zueinander:
 > 1. Sie haben einen Schnittpunkt.
 > 2. Sie haben unendlich viele Schnittpunkte, die identisch sind.
 > 3. Sie haben überhaupt keinen Schnittpunkt und verlaufen parallel zueinander.
 > 4. Sie haben überhaupt keinen Schnittpunkt und sind windschief zueinander.
#### Schnittpunkt
>Man erhält genau eine Lösung für $t$.

$$
g : \vec x
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
+
t
\cdot 
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
,
h : \vec x
=
\begin{pmatrix}
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
+
t
\cdot 
\begin{pmatrix}
x_4 \\
y_4 \\
z_4 \\
\end{pmatrix}
$$
$$
\begin{matrix}
g : \vec x
=
h : \vec x \\
t \rightarrow a
\end{matrix}
$$
```Mathematica
g[t_]:= {x1, y1, z1} + t * {x2, y2, z2}
h[t_]:= {x3, y3, z3} + t * {x4, y4, z4}
Solve[g[t] == h[t]]
t -> a
```

> Setzt man nun die Lösung für $t$ ein, erhält man den Schnittpunkt. Wichtig ist, um eine Kollision zu berechnen, benötigt man einen Schnittpunkt zum gleichen Zeitpunkt. Möchte man jedoch nur wissen, ob zwei Vektoren sich schneiden können, kann dies auch zu unterschiedlichen Zeitpunkten passieren. Das bedeutet, man verwendet zwei unterschiedliche Variablen.

<div style="page-break-after: always;"></div>

#### Identisch
> Man erhält eine Formel, mit der sich unendlich viele Lösungen berechnen lassen. Hierbei ist es wichtig, zwei unterschiedliche Variablen zu verwenden.

$$
g : \vec x
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
+
t
\cdot 
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
,
h : \vec x
=
\begin{pmatrix}
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
+
r
\cdot 
\begin{pmatrix}
x_4 \\
y_4 \\
z_4 \\
\end{pmatrix}
$$
$$
\begin{matrix}
g : \vec x
=
h : \vec x \\
t \rightarrow 
a
\cdot
r
\end{matrix}
$$
```Mathematica
g[t_]:= {x1, y1, z1} + t * {x2, y2, z2}
h[r_]:= {x3, y3, z3} + r * {x4, y4, z4}
Solve[g[t] == h[r]]
t -> a * r
```

<div style="page-break-after: always;"></div>

#### Parallel
> Man erhält keinen Schnittpunkt, da die beiden Vektoren parallel verlaufen und sich somit niemals schneiden. Parallele Vektoren erkennt man daran, dass ihre Bewegungsvektoren die gleiche Richtung darstellen und sie keinen Schnittpunkt haben. Dies lässt sich daran erkennen, wenn der Bewegungsvektor $a$ mit einer Zahl multipliziert werden kann, um auf den Bewegungsvektor $b$ zu kommen. In diesem Fall hat $t$ keine Lösung.

$$
g : \vec x
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
+
t
\cdot 
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
,
h : \vec x
=
\begin{pmatrix}
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
+
r
\cdot 
\begin{pmatrix}
x_4 \\
y_4 \\
z_4 \\
\end{pmatrix}
$$
$$
\begin{matrix}
g : \vec x
=
h : \vec x \\
t \rightarrow \{\}
\end{matrix}
$$
```Mathematica
g[t_]:= {x1, y1, z1} + t * {x2, y2, z2}
h[t_]:= {x3, y3, z3} + t * {x4, y4, z4}
Solve[g[t] == h[t]]
t -> a
```
#### Windschief
> Man erhält keinen Schnittpunkt, da die beiden Vektoren im Raum so liegen, dass sie sich nicht schneiden. Dies kann beispielsweise der Fall sein, wenn sie auf unterschiedlichen Koordinaten verlaufen, wie zum Beispiel in der Höhe. Solche Vektoren nennt man windschief.

$$
g : \vec x
=
\begin{pmatrix}
x_1 \\
y_1 \\
z_1 \\
\end{pmatrix}
+
t
\cdot 
\begin{pmatrix}
x_2 \\
y_2 \\
z_2 \\
\end{pmatrix}
,
h : \vec x
=
\begin{pmatrix}
x_3 \\
y_3 \\
z_3 \\
\end{pmatrix}
+
r
\cdot 
\begin{pmatrix}
x_4 \\
y_4 \\
z_4 \\
\end{pmatrix}
$$
$$
\begin{matrix}
g : \vec x
=
h : \vec x \\
t \rightarrow \{\}
\end{matrix}
$$
```Mathematica
g[t_]:= {x1, y1, z1} + t * {x2, y2, z2}
h[t_]:= {x3, y3, z3} + t * {x4, y4, z4}
Solve[g[t] == h[t]]
t -> a
```

<div style="page-break-after: always;"></div>

### Affine Abbildungen
$$
\begin{pmatrix} 
a_1 & b_1 \\ 
c_1 & d_1 \\
\end{pmatrix}
\cdot 
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} +
\begin{pmatrix}
c_1 \\
c_2 \\
\end{pmatrix}
$$
$$\large Berechnung$$
$$
\begin{pmatrix} 
a_1 \cdot x_1 & + & b_2 \cdot x_2 \\ 
c_1 \cdot x_1 & + & d_1 \cdot x_2 \\
\end{pmatrix} =
\begin{pmatrix}
x_1 \\
x_2 \\
\end{pmatrix} +
\begin{pmatrix}
c_1 \\
c_2 \\
\end{pmatrix}
$$
> Die Berechnung erfolgt durch Multiplikation der Spalte mit der Zeile.
#### Verschiebung
```tikz 
\begin{document} 
\begin{tikzpicture} 
\draw[very thin,color=gray] (-5,-5) grid (5,5); 
\draw[ultra thick, ->] (-5,0) -- (5,0) node[right] {$x_1$}; 
\draw[ultra thick, ->] (0,-5) -- (0,5) node[above] {$x_2$}; 


\filldraw[very thick](-2,2.5) circle (0.1) node[left] {$1$};
\filldraw[very thick](-1,1) circle (0.1) node[left] {$A$};
\draw[ultra thick, -] (-1,1) -- (-2,4);

\filldraw[very thick](-2,4) circle (0.1) node[above] {$C$};
\draw[ultra thick, -] (-2,4) -- (-3,2);

\filldraw[very thick](-3,2) circle (0.1) node[above] {$B$}; 
\draw[ultra thick, -] (-3,2) -- (-1,1);


\filldraw[very thick](2,2.5) circle (0.1) node[left] {$2$};
\filldraw[very thick](3,1) circle (0.1) node[left] {$\Large A'$};
\draw[ultra thick, -] (3,1) -- (2,4);

\filldraw[very thick](2,4) circle (0.1) node[above] {$\Large C'$};
\draw[ultra thick, -] (2,4) -- (1,2);

\filldraw[very thick](1,2) circle (0.1) node[above] {$\Large B'$}; 
\draw[ultra thick, -] (1,2) -- (3,1);

\filldraw[very thick](-2,-4) circle (0.1) node[left] {$3$};
\filldraw[very thick](-4,-4) circle (0.1) node[left] {$D$};
\draw[ultra thick, -] (-4,-4) -- (-2,-3);

\filldraw[very thick](-2,-3) circle (0.1) node[above] {$E$};
\draw[ultra thick, -] (-2,-3) -- (-1,-5);

\filldraw[very thick](-1,-5) circle (0.1) node[above] {$F$}; 
\draw[ultra thick, -] (-1,-5) -- (-4,-4);


\filldraw[very thick](-2.5,-1) circle (0.1) node[left] {$4$};
\filldraw[very thick](-4,-1) circle (0.1) node[left] {$'D$};
\draw[ultra thick, -] (-4,-1) -- (-2,0);

\filldraw[very thick](-2,0) circle (0.1) node[above] {$'E$};
\draw[ultra thick, -] (-2,0) -- (-1,-2);

\filldraw[very thick](-1,-2) circle (0.1) node[above] {$'F$}; 
\draw[ultra thick, -] (-1,-2) -- (-4,-1);

\end{tikzpicture} 
\end{document} 
```
1 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 0 \end{pmatrix}$
2 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 4 \\ 0 \end{pmatrix}$
> Die Punkte $A', B', C'$ sind um $4$ entlang der $x_1$-Achse verschoben.

3 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 0 \end{pmatrix}$
4 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 3 \end{pmatrix}$
> Die Punkte $D, E, F$ sind um $4$ entlang der $x_2$-Achse verschoben.

<div style="page-break-after: always;"></div>

#### Drehen
> Man setzt den Winkel in die Drehmatrix ein, und Mathematica erledigt den Rest.
 
$$\large Formel$$
$$
\begin{pmatrix}
\cos(\varphi) & - & \sin(\varphi) \\
\sin(\varphi) &   & \cos(\varphi) \\
\end{pmatrix}
$$
```Mathematica
Cos[phi\[Degree]]
Sin[phi\[Degree]]
```

<div style="page-break-after: always;"></div>

#### Strecken/Stauchen
>Man kann Streckungen und Stauchungen entlang der $x_1$-Achse und $x_2$-Achse vornehmen, indem man die Parameter $a_1$ und $d_1$ ändert.
```tikz 
\begin{document} 
\begin{tikzpicture} 
\draw[very thin,color=gray] (-5,-5) grid (5,5); 
\draw[ultra thick, ->] (-5,0) -- (5,0) node[right] {$x_1$}; 
\draw[ultra thick, ->] (0,-5) -- (0,5) node[above] {$x_2$}; 


\filldraw[very thick](-2,2.5) circle (0.1) node[left] {$1$};
\filldraw[very thick](-1,1) circle (0.1) node[left] {$A$};
\draw[ultra thick, -] (-1,1) -- (-2,4);

\filldraw[very thick](-2,4) circle (0.1) node[above] {$C$};
\draw[ultra thick, -] (-2,4) -- (-3,2);

\filldraw[very thick](-3,2) circle (0.1) node[above] {$B$}; 
\draw[ultra thick, -] (-3,2) -- (-1,1);

\filldraw[very thick](0,2.5) circle (0.1) node[left] {$2$};
\filldraw[very thick](1,1) circle (0.1) node[left] {$A'$};
\draw[ultra thick, -] (1,1) -- (0,4);

\filldraw[very thick](0,4) circle (0.1) node[above] {$C'$};
\draw[ultra thick, -] (0,4) -- (-1,2);

\filldraw[very thick](-1,2) circle (0.1) node[above] {$B'$}; 
\draw[ultra thick, -] (-1,2) -- (1,1);

\filldraw[very thick](-3,-4.5) circle (0.1) node[left] {$3$};
\filldraw[very thick](-5,-5) circle (0.1) node[left] {$A$};
\draw[ultra thick, -] (-5,-5) -- (-3,-4);

\filldraw[very thick](-3,-4) circle (0.1) node[above] {$C$};
\draw[ultra thick, -] (-3,-4) -- (-2,-5);

\filldraw[very thick](-2,-5) circle (0.1) node[above] {$B$}; 
\draw[ultra thick, -] (-2,-5) -- (-5,-5);

\filldraw[very thick](-3,-2.5) circle (0.1) node[left] {$4$};
\filldraw[very thick](-5,-3) circle (0.1) node[left] {$A'$};
\draw[ultra thick, -] (-5,-3) -- (-3,-2);

\filldraw[very thick](-3,-2) circle (0.1) node[above] {$C'$};
\draw[ultra thick, -] (-3,-2) -- (-2,-3);

\filldraw[very thick](-2,-3) circle (0.1) node[above] {$B'$}; 
\draw[ultra thick, -] (-2,-3) -- (-5,-3);

\end{tikzpicture} 
\end{document} 
```
2. Streckung auf der $x_1$-Achse: $\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$. Jede Koordinate wurde um zwei auf der $x_1$-Achse verschoben.
3. Streckung auf der $x_2$-Achse: $\begin{pmatrix} 1 & 0 \\ 0 & 2 \end{pmatrix}$. Jede Koordinate wurde um zwei auf der $x_2$-Achse verschoben.
4. Streckung auf der $x_1$- und $x_2$-Achse: $\begin{pmatrix} 2 & 0 \\ 0 & 2 \end{pmatrix}$. Jede Koordinate wurde um zwei auf der $x_1$- und $x_2$-Achse verschoben.

<div style="page-break-after: always;"></div>

#### Spiegeln
> Veränderung der Parameter $a_1$ und $d_1$ in positive oder negative Richtung.
```tikz 
\begin{document} 
\begin{tikzpicture} 
\draw[very thin,color=gray] (-5,-5) grid (5,5); 
\draw[ultra thick, ->] (-5,0) -- (5,0) node[right] {$x_1$}; 
\draw[ultra thick, ->] (0,-5) -- (0,5) node[above] {$x_2$}; 


\filldraw[very thick](2.5,1.5) circle (0.1) node[left] {$1$};
\filldraw[very thick](1,1) circle (0.1) node[left] {$A$};
\draw[ultra thick, -] (1,1) -- (2,3);

\filldraw[very thick](2,3) circle (0.1) node[above] {$C$};
\draw[ultra thick, -] (2,3) -- (4,0);

\filldraw[very thick](4,0) circle (0.1) node[above] {$B$}; 
\draw[ultra thick, -] (4,0) -- (1,-1);


\filldraw[very thick](-2.5,1.5) circle (0.1) node[left] {$2$};
\filldraw[very thick](-1,1) circle (0.1) node[right] {$A`$};
\draw[ultra thick, -] (-1,1) -- (-2,3);

\filldraw[very thick](-2,3) circle (0.1) node[above] {$C`$};
\draw[ultra thick, -] (-2,3) -- (-4,0);

\filldraw[very thick](-4,0) circle (0.1) node[above] {$B`$}; 
\draw[ultra thick, -] (-4,0) -- (-1,1);


\filldraw[very thick](2.5,-1.5) circle (0.1) node[left] {$3$};
\filldraw[very thick](1,-1) circle (0.1) node[left] {$A`$};
\draw[ultra thick, -] (1,-1) -- (2,-3);

\filldraw[very thick](2,-3) circle (0.1) node[below] {$C`$};
\draw[ultra thick, -] (2,-3) -- (4,0);

\filldraw[very thick](4,0) circle (0.1) node[below] {$B`$}; 
\draw[ultra thick, -] (4,0) -- (1,1);


\filldraw[very thick](-2.5,-1.5) circle (0.1) node[left] {$4$};
\filldraw[very thick](-1,-1) circle (0.1) node[right] {$A`$};
\draw[ultra thick, -] (-1,-1) -- (-2,-3);

\filldraw[very thick](-2,-3) circle (0.1) node[below] {$C`$};
\draw[ultra thick, -] (-2,-3) -- (-4,0);

\filldraw[very thick](-4,0) circle (0.1) node[below] {$B`$}; 
\draw[ultra thick, -] (-4,0) -- (-1,-1);

\end{tikzpicture} 
\end{document} 
```

1. $\rightarrow$ Die Matrix $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ wirkt wie eine $\cdot$-1-Operation und verändert nichts.
2. $\rightarrow$ Spiegelung an der $x_2$-Achse $= \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}$
3. $\rightarrow$ Spiegelung an der $x_1$-Achse $= \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$
4. $\rightarrow$ Spiegelung an der $x_1$- und $x_2$-Achse $= \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$