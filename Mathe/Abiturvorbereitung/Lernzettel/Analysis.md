---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-12-06 10:23**

---
### Ableitungsregeln
#### Produktregel
#### Kettenregel
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

#### Ableitungen von $e$ Funktionen
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
### Funktion aus Bedingungen aufstellen
### Integrale

