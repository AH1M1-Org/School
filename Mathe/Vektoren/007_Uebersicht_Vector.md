# Lernzettel Vektoren

### Was ist ein Vektor?
Ein Vektor ist eine Verschiebung im Raum, sie werden mit $\vec a, \vec b, \vec c$ usw. dargestellt. Vektoren die zwischen zwei Punkten verlaufen werdem mit $\vec {AB}, \vec {AB},\vec {AB}$ dargestellt und beschreiben eine Strecke.

### Eigenschaften
- laenge $\rightarrow$ beschreibt die Geschwindigkeit
- richtung $\rightarrow$ beschreibt die Verschiebung

### Arten von Vektoren
- Ortsvektoren $\rightarrow$ Verbindung vom Ursprung $(0 | 0)$ zu einem Punkt $(x|y)$

- Vektoren $\rightarrow$ Eine Strecke zwischen zwei Punkten im Raum $(x|y) \rightarrow (x|y)$ 

## **Berechnungen**
### **Vektor - Addition**
$\begin{pmatrix}x\\y\end{pmatrix} + \begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}x + x\\y + y\end{pmatrix} = \begin{pmatrix}x\\y\end{pmatrix}$

$\begin{pmatrix}4\\1\end{pmatrix} + \begin{pmatrix}2.5\\3\end{pmatrix} = \begin{pmatrix}4 + 2.5\\1 + 3\end{pmatrix} = \begin{pmatrix}6.5\\4\end{pmatrix}$

### **Vektor - Subtraktion**
$\begin{pmatrix}x\\y\end{pmatrix} - \begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}x - x\\y -x\end{pmatrix} = \begin{pmatrix}x\\y\end{pmatrix}$

$\begin{pmatrix}10\\5\end{pmatrix} - \begin{pmatrix}6\\3\end{pmatrix} = \begin{pmatrix}10 - 6\\5 - 3\end{pmatrix} = \begin{pmatrix}4\\2\end{pmatrix}$

### **Vektor - Multiplikation**
$\begin{pmatrix}x\\y\end{pmatrix} \cdot a = \begin{pmatrix}x \cdot a\\y \cdot a\end{pmatrix} = \begin{pmatrix}x\\y\end{pmatrix}$

$\begin{pmatrix}4\\5\end{pmatrix} \cdot 2 = \begin{pmatrix}4 \cdot 2\\5 \cdot 2\end{pmatrix} = \begin{pmatrix}8\\10\end{pmatrix}$

### **Vektor - Laengenberechnung**
Um die Laenge eines Vektors zu berechnen braucht man den Satz des Pythagoras $a^2 + b^2 = c^2$ um nun nur c herauszubekommen zieht man die Wurzel $\sqrt{a^2 + b^2} = c$

$|\vec a | = \bigg|\begin{pmatrix}x\\y\end{pmatrix}\bigg| = \sqrt{a_x^2 + a_y^2} = c $

$|\vec a | = \bigg|\begin{pmatrix}8\\4\end{pmatrix}\bigg| = \sqrt{8^2 + 4^2} = c $

$\sqrt{64 + 16} = c$

$\sqrt{80} = 8,94 ~ LE \longrightarrow (Laengeneinheiten)$

Bei mehreren Dimensionen haengt man den zusaetzlichen Parameter dran $\sqrt{x^2 + y^2 + z^2...} = c$

## Geradengleichung
Eine Geradengleichung besteht aus dem Ortsvektor, dieser gibt den Startpunkt des Vektors an. Dieser wird dann mit der variable t mit addiert der die Zeit angibt (Verschiebungsschritte). Dieser wird dann mit dem Richtungsvektor multipliziert, der Richtungsvektor gibt die Verschiebung an.

$g: \vec a =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}= \begin{pmatrix}x\\y\end{pmatrix}$

### Schnittpunkte 
#### **X-Achse**
$g: \vec a =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}= \begin{pmatrix}x\\0\end{pmatrix}$
```mathematica
f[t_]: = {x,y} + t * {x,y}
Solve[f[t] == {x,0}]
t -> 
```
#### **Y-Achse**
$g: \vec a =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}= \begin{pmatrix}0\\y\end{pmatrix}$
```mathematica
f[t_]: = {x,y} + t * {x,y}
Solve[f[t] == {0,x}]
t -> 
```
#### **zweier Vektoren**
Man stellt zwei Geradengleichungen gleich.

$g: \vec a =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}$

$f: \vec b =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}$

$\vec a = \vec b$

**Mathematica**
```mathematica
f[t_]: = {x,y} + t * {x,y}
g[t_]: = {x,y} + t * {x,y}
Solve[f[t] == g[t]]
t -> 
```
#### **Berechnung von t**
$g: \vec a =\begin{pmatrix}x\\y\end{pmatrix} + t \cdot \begin{pmatrix}x\\y\end{pmatrix}$

Gegebender Punkt $(x|y)$

Loesung mit LGS

#### **Beispiel**
$g: \vec a =\begin{pmatrix}6\\12\end{pmatrix} + t \cdot \begin{pmatrix}-2\\2\end{pmatrix}$

Punkt $(0|y)$

$g: \vec a =\begin{pmatrix}6\\12\end{pmatrix} + t \cdot \begin{pmatrix}-2\\2\end{pmatrix} = \begin{pmatrix}0\\y\end{pmatrix}$

### *LGS* oder *Mathematica*
#### **LGS**
$\begin{vmatrix}
6 + t \cdot (-2) = 0\\
12 + t \cdot 2 = y \\
\end{vmatrix}$
> umstellen mit der Gleichung wo nur eine variable ist.

$6 + t \cdot (-2) = 0 | - 6$\
$t \cdot (-2) = -6 | \div (-2)$\
$t = 3$
> t in die andere Gleichung einsetzen um Y zu bekommen

$\Leftrightarrow 12 + 3 \cdot 2 = 18$\
$y = 18$\
$g: \vec a =\begin{pmatrix}6\\12\end{pmatrix} + 3 \cdot \begin{pmatrix}-2\\2\end{pmatrix} = \begin{pmatrix}0\\18\end{pmatrix}$

#### **Mathematica**
```mathematica
g[t_] := {6, 12} + t*{-2, 2}

Solve[g[t] == {0, y}]

{{t -> 3, y -> 18}}
```