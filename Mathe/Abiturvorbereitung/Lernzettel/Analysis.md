---
tags:
  - Mathe
  - Templates
---
*Marvin Baeumer* **2023-12-06 10:23**

---
### Ableitungsregeln
#### Produktregel
> Die Produktregel wird verwendet, um eine Funktion abzuleiten, die das Produkt aus zwei anderen Funktionen bildet.

**Beispiel**

$$
\begin{matrix}
\text{Produktregel} & =&  u' \cdot v + u \cdot v' \\\\
f(x) & = &(x^2 + 3x) \cdot (2x - 1) \\\\
u & = & (x^2 + 3x) \\
u' & = & (2x + 3) \\
v & = & (2x - 1) \\
v'&  = & 2 \\\\
\Leftrightarrow \text{Produktregel} \\\\
f'(x) & = & (2x + 3) \cdot (2x - 1) + (x^2 + 3x) \cdot 2 
\end{matrix}
$$

<div style="page-break-after: always;"></div>

#### Kettenregel
> Die Kettenregel wird verwendet, um die Ableitung einer zusammengesetzten Funktion zu berechnen. Dabei steht $g$ für die äußere Funktion und $h$ für die innere Funktion. Die Kettenregel besagt, dass die Ableitung der äußeren Funktion $g$ nach der inneren Funktion $h$ multipliziert mit der Ableitung der inneren Funktion $h$ nach der Variablen $x$ gleich der Ableitung der zusammengesetzten Funktion ist. Das kann man mathematisch wie folgt ausdrücken:

**Beispiel**
$$
\begin{matrix}
\text{Kettenregel} & = & g(h(x)) \\ 
\text{Kettenregel}' & = & g'(h(x)) \cdot h'(x) \\\\ 
f(x) & = & (3x^2 + 2)^5 \\\\
g & = & h^5 \\
g' & = & 5h^4 \\
h & = & (3x^2 + 2) \\
h' & = & 6x \\\\
\Leftrightarrow \text{Kettenregel} \\\\
f'(x) & = & 5(3x^2 + 2)^4 \cdot 6x \\
\end{matrix}
$$

<div style="page-break-after: always;"></div>

#### Ableitungen bilden
> Eine Ableitung beschreibt die Steigung einer Funktion, also ist die Ableitung die Steigungsfunktion der Stammfunktion. Die zweite Ableitung beschreibt die Änderungsrate der Stammfunktion. Eine Ableitung stellt man mit $f'(x)$ dar, vorausgesetzt unsere ursprüngliche Funktion war $f(x)$. Die zweite Ableitung stellt man dann mit $f''(x)$ dar.

**Berechnung - Formel**
> Die Berechnung erfolgt mit dem Wert vor dem $x$ mal dem Exponenten, dann zieht man $-1$ vom Exponenten ab. Konstanten fallen somit weg.
$$
\begin{matrix}
f(x) & = & a \cdot x^3 + b \cdot x^2 + c \cdot x + d \\
f'(x) & = & 3a \cdot x^2  + 2b \cdot x + c \\
f''(x) & = & 6a \cdot x + 2b
\end{matrix}
$$

<div style="page-break-after: always;"></div>

#### Ableitungen von $e$ Funktionen
> Eine Ableitung von $e^x$ ist immer $e^x$ selbst. Meistens steht die Ableitung von $e$ Funktionen in Verbindung mit der Produkt- und Kettenregel.

**Beispiel**
$$
f_a(x)=x \cdot e^{(-a \cdot x)}
$$
> Um die Funktion $f_a(t)$ abzuleiten, benötigen wir die Produktregel, weil wir $x\cdot e$ haben.

$$
\begin{matrix}
\text{Produktregel} \\\\
u' & = & 1 \\
u & = & x \\
v' & = & ? \\
v & = &e^{(-a \cdot x)} \\
\end{matrix} \\
$$
> Um nun die Ableitung von $v$ zu bekommen, benötigen wir die Kettenregel, weil wir eine verkettete Funktion $e^{(-a \cdot x)}$haben.

$$
\begin{matrix}
\text{Kettenregel} \\\\
I_a(x) & = & e^{(-a \cdot x)} \\\\
g & = & e^x \\
g' & = & e^x \\
h & = & (-a \cdot x) \\
h' & = & -a\\\\
I_a'(x) & = & e^{(-a \cdot x)} \cdot -a
\end{matrix}
$$
> Nun kennen wir also die Ableitung der $e$-Funktion. Somit haben wir das fehlende $v' = e^{-a \cdot x}$, das uns in der Produktregel fehlte. Nun können wir alles in die Produktregel einsetzen.

$$
\begin{matrix}
\Leftrightarrow \text{Produktregel} \\\\
u' \cdot v + u \cdot v' \\
f_a'(x) = 1 \cdot e^{(-a \cdot x)} + x \cdot (-a) \cdot e^{(-a \cdot x)} \\\\
\text{Zusammenfassen} \\\\
f_a'(x) = (1 - a \cdot x) \cdot e^{-a \cdot x} 
\end{matrix}
$$
<div style="page-break-after: always;"></div>

### Extremstellen
> Bei der Berechnung von Extremstellen betrachtet man Hochpunkte, Tiefpunkte und Wendepunkte. Bei Hochpunkten und Tiefpunkten beträgt die Steigung $0$, das heißt, man nimmt die erste Ableitung und setzt sie gleich $0$, also $f'(x) = 0$. Somit erhält man den $x$-Wert. Um nun zu prüfen, ob es sich um einen Hochpunkt oder Tiefpunkt handelt, muss man mit der zweiten Ableitung prüfen. Wenn das Ergebnis des eingesetzten $x$-Wertes negativ ist, handelt es sich um einen Hochpunkt; ist es positiv, handelt es sich um einen Tiefpunkt. Bei einem Wendepunkt setzt man die zweite Ableitung gleich $0$ und prüft mit der dritten Ableitung.
#### Hochpunkt
1. $f'(x)$ aufstellen
2. $f''(x)$ aufstellen
3. Erste Ableitung $=0$ stellen | $f'(x) = 0$
4. Ergebnis prüfen $f''(...) < 0$ 
5. In $f(x)$ einsetzen für den $Y-Wert$
```mathematica
f[x_]:= a*x^3+b*x^2+c*x+d

f'[x]
f''[x]
%liefert die beiden Ableitungen%

Solve[f'[x] == 0]
x -> ...
f''(...)
%Ergebnis muss < 0 sein% 
f[...]
```
#### Tiefpunkt
1. $f'(x)$ aufstellen
2. $f''(x)$ aufstellen
3. Erste Ableitung $=0$ stellen | $f'(x) = 0$
4. Ergebnis prüfen $f''(...) > 0$ 
5. In $f(x)$ einsetzen für den $Y-Wert$
```mathematica
f[x_]:= a*x^3+b*x^2+c*x+d

f'[x]
f''[x]
%liefert die beiden Ableitungen%

Solve[f'[x] == 0]
x -> ...
f''[...]
%Ergebnis muss > 0 sein% 
f[...]
```
#### Wendepunkt
1. $f''(x)$ aufstellen
2. $f'''(x)$ aufstellen
3. Zweite Ableitung $=0$ | $f''(x) = 0$
4. Ergebnis prüfen $f'''(...) < 0$ 
5. In $f(x)$ einsetzen für den $Y-Wert$ 
```mathematica
f[x_]:= a*x^3+b*x^2+c*x+d

f''[x]
f'''[x]
%liefert die beiden Ableitungen%

Solve[f''[x] == 0]
x -> ...
f'''[...]
%Ergebnis muss < 0 sein% 
f[...]
```

<div style="page-break-after: always;"></div>

### Funktion aus Bedingungen aufstellen
> Eine Bedingung beschreibt meistens die Funktion, die man aufstellen soll. Eine Bedingung kann zum Beispiel sein, dass man weiß, wo sich der Hochpunkt befindet. Wir nehmen mal an, der Hochpunkt wäre bei $(5|40)$. Somit hätte man zwei Bedingungen. Bei einer Funktion 2. Grades braucht man 3 Bedingungen, da man 3 Parameter hat. Also könnte eine weitere Bedingung eine Nullstelle sein. Bei $(-5,0)$ liegt zum Beispiel eine Nullstelle. Somit ergeben sich drei Bedingungen.
> 1. $f'(5) = 0$
> 2. $f(5) = 40$ 
> 3. $f(-5)=0$

```Mathematica
f[x_] := a*x^2 + b*x + c
Solve[f[5] == 40 && f'[5] == 0 && f[0] == -5]
```
### Integrale 
> Das bestimmte Integral einer Funktion $f(x)$ auf dem Intervall $[a, b]$ steht für die Fläche unterhalb der Kurve $f(x)$ zwischen den Grenzen $a$ und $b$. Es wird symbolisch durch $\large \int_{a}^{b} f(x) \, dx$ dargestellt. Die grundlegenden Regeln für die Integration umfassen die lineare Eigenschaft, die Potenzregel und die Summenregel. 
> Das unbestimmte Integral $\large \int f(x) \, dx$ repräsentiert eine Familie von Funktionen, deren Ableitung $f(x)$ ist. Das bestimmte Integral $\large \int_{a}^{b} f(x) \, dx$ berechnet den Flächeninhalt zwischen der Kurve $f(x)$ und der $x$-Achse über dem Intervall $[a, b]$.
#### Aufleiten
> Aufleiten bedeutet von einer abgeleiteten Funktion $f'(x)$ die Stammfunktion $F(x)$ zu bilden. Dazu braucht man die Potenzgesetze und und das Verstaendnis zur Ableitung. 

**Beispiel**