---
tags:
  - Mathe
  - Templates
---
*Marvin Baeumer* **2023-12-06 10:23**

---
### Ableitungsregeln
#### Produktregel
> Die Produktregel verwendet man dann um eine Funktion abzuleiten die das Produkt aus zweier anderen Funktionen bildet.

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
#### Kettenregel
> Die Kettenregel verwendet man um die Ableitung einer Zusammengesetzen Funktion zu berechnen. Dabei steht $g$ fuer die aeussere Funktion und h fuer die innere Funktion.

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
> Eine Ableitung beschreibt die Steigung einer Funktion, also ist die Ableitung die Steigungsfunktion der Stammfunktion. Die zweite Ableitung beschreibt die änderungsrate der Stammfunktion. Eine Ableitung stellt man mit $f'(x)$ da vorausgesetzt unsere ursprüngliche Funktion war $f(x)$. Die zweite Ableitung stellt man dann mit $f''(x)$ da.

**Berechnung - Formel**
> Die Berechnung erfolgt mit Wert vor dem $x \cdot Exponent$, dann zieht man $-1$ vom Exponenten ab. Konstanten fallen somit weg. 
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
> Um die Funktion $f_a(t)$ abzuleiten benoetigen wir die Produkt regel, weil wir $x \cdot e$ haben.

$$
\begin{matrix}
\text{Produktregel} \\\\
u' & = & 1 \\
u & = & x \\
v' & = & ? \\
v & = &e^{(-a \cdot x)} \\
\end{matrix} \\
$$
> Um nun die Ableitung von $v$ zu bekommen benötigen wir die Kettenregel, weil wir eine verkettet Funktion $e^{(-a \cdot x)}$

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
> Nun kennen wir also die Ableitung von der $e$ Funktion somit haben wir das fehlende $v'= e^{(-a \cdot x)}$ das uns in der Produktregel fehlte. Somit können wir jetzt alles in die Produktregel einsetzen.

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
> Bei der Extremstellen Berechnung schaut man sich Hochpunkte, Tiefpunkte und Wendepunkte an. Bei Hochpunkten und Tiefpunkten betrifft die Steigung $0$ das heißt also man nimmt die erste Ableitung und setzt diese $=0$ sprich $f'(x) = 0$ somit bekommt man dann den $X-Wert$. Um nun zu prüfen ob sich um einen Hochpunkt oder Tiefpunkt handelt muss man mit der zweiten Ableitung prüfen. Wenn das Ergebnis des eingesetzten  $X-Wertes$ negativ ist handelt es sich um einen Hochpunkt, ist dieser positiv handelt es sich um einen Tiefpunkt. Bei Einem Wendepunkt setzt man die zweite Ableitung $=0$ und prüft mit der dritten Ableitung.
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
> Eine Bedingung beschreibt meistens die Funktion die man aufstellen soll. Eine Bedingung kann zum Beispiel sein dass man weiß wo sich der Hochpunkt befindet. wir nehmen mal an der Hochpunkt waere bei $(5|40)$ somit haette man zwei Bedinungen. 
> 1. $f'(5) = 0$
> 2. $f(5) = 40$ 
> 
### Integrale

