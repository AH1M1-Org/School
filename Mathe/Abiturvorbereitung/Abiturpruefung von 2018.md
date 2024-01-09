---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-12-18 09:56**

---
# oHIMI
![PDF](PDF/Mathe/10%20Abiturpruefung%20Mathe%202018%20oHIMI.pdf)
## Aufgabe 1
### Aufgabe 1.1.1
$$
f(t) = a \cdot t^3 + b \cdot t^2 + c \cdot t + d
$$
Informationen = 
$$
\begin{matrix}
f(10) & = & 0 \\
f(0) & = & 0 \\
f(5) & = & 1500 \\
f'(0) & = & 0 \\
&&& \text{Nun stellen wir aus unseren Informationen gleichungen auf und loesen diese} &
\end{matrix}
$$
$$
\begin{matrix}
I. & f(10) & = & a \cdot 1000 & + & b \cdot 100 \\
II. & f(5) & = & a \cdot 125 & + & b \cdot 25 \\
&&&&&&\text{parameter c und d fallen weg weil 0} \\
III. & f(0) & = & 0 & | & 0 \rightarrow d & \text{ alles muss 0 sein da der Wert 0 ist} \\
IV. & f'(0) & = & 0 & | & 0 \rightarrow c &\text{ alles muss 0 sein da der Wert 0 ist} \\
\end{matrix}
$$
$$
\begin{matrix}
\left |
\begin{matrix}
I. & f(10) & = & a \cdot 1000 & + & b \cdot 100 \\
II. & f(5) & = & a \cdot 125 & + & b \cdot 25 \\
& I +  (-4)  \cdot  II \\
\end{matrix} 
\right |
\text{wir waehlen -4 da sich so das b aufhebt}
\end{matrix}
$$
$$
\begin{matrix}
\left |
\begin{matrix}
500 & \cdot & a & = & -6000 & | & \div & 500 \\
&& a & = & -12 &
\end{matrix} 
\right |
\end{matrix}
$$
$$
\text{um nun den Parameter d Herauszufinden setzen wir a in eine der beiden gleichungen ein}
$$
$$
\begin{matrix}
\Leftrightarrow & 1000 & \cdot & (-12) & + & 100 & \cdot & b & = & 0 & \\
& -12000 & + & 100 &&& \cdot & b & = & 0 & | & +12000 & \\
& 100 & \cdot & b &&&&& = & 0 & | & \div 100 \\
&&& b &&&&& = &120
\end{matrix}
$$
### Aufgabe 1.1.2
$$
\begin{matrix}
f'(t) & = & -30 \cdot t^2 + 180 \cdot t + 100 \\
f''(t) & = & -60 \cdot t + 180 \\
f'''(t) & = & -60
\end{matrix}
$$
Ansatz
> Die 2 Ableitung gleich 0 stellen da man die staertkste Aenderungsrate moechte.
$$
\begin{matrix}
-60 & \cdot &  t & + & 180 & = & 0 & & | &-180 \\
-60 & \cdot & t &&&= & 180 & | &\div (-60) \\
t &&&&& = & 3 \\
&&&&t &\rightarrow & 3
\end{matrix}
$$
## Aufgabe 2
### Aufgabe 1.2.1
- Bei 0.25 ist eine 0 Stelle in der Ableitung g das heisst bei der Funktion f muss ein Extrempunkt sein. Dies ist hier der Fall.
- Der Extrempunkt der gerade g liegt bei 0.5 das heisst bei der Funktion f muesste dort der Wendepunkt liegen, dies koennte hinkommen.
### Aufgabe 1.2.2
$$
\begin{matrix}
\large  f(x) = x \cdot e^{-4 \cdot x} \\
f'(x) = 
\end{matrix}
$$
$$
\text{um die Funktion abzuleiten benoetigt man in diesem Falle die Produkt und Kreuzregel. Die Produktregek wegen } x \cdot e \text{ und die Kreuzregel wegen } e^{-4 \cdot x} 
$$
#### Kettenregel
$$
\begin{matrix}
f(x) = & g(h(x)) & \\
f'(x) = & h'(x) & \cdot & g'(h(x))
\end{matrix}
$$
$$
\large
\begin{matrix}
f(x) & = & e^{-4 \cdot x} \\
g(x) & = & e^x \\
h(x) & = & -4 \cdot x \\
g'(x) & = & e^x \\
h'(x) & = & -4 \\
\end{matrix}
$$
$$
\text{Anwendung der Kettenregel, man setzt die Funktionen ein und erhaelt so die Ableitung}
$$
$$
\begin{matrix}
f'(x) = -4 \cdot e^{-4 \cdot x}
\end{matrix}
$$
#### Produktregel
$$
\begin{matrix}
f(x) & = & g(x) & \cdot & h(x) & \\
f'(x) & = & g'(x) & \cdot & h(x) & + & g(x) & \cdot & h(x) &
\end{matrix}
$$
$$
\begin{matrix}
f(x) & = & e^{x} \cdot x \\
g(x) & = & x \\
h(x) & = & e^{-4 \cdot x} \\
g'(x) & = & 1 \\ 
h'(x) & = & -4 \cdot e^{-4 \cdot x} \text{ konnten wir mit der Kettenregel ableiten} \\
\end{matrix}
$$
$$
\text{Einsetzen in die Kettenregel}
$$
$$
\begin{matrix}
\large f'(x) = 1 \cdot e^{-4 \cdot x} + x \cdot (-4) \cdot e^{-4 \cdot x} \\
\text{nun folgt ausklammern} \\
\large f'(x) = (-4 \cdot x + 1) \cdot e^{-4 \cdot x} \\
\end{matrix}
$$
$$
\text{Die ableitung koennen wir nun = 0 stellen um so das lokale minimum zu erhalten. Zudem brauchen wir noch die 2. Ableitung um zu pruefen fuer minimum}
$$
#### lokales Minimum 
$$
0 = (-4 \cdot x + 1) \cdot e^{-4 \cdot x}
\text{ Satz vom Nullprodukt der Teil mit e kann nur > 0 sein deswegen zaehlt nur der Fordere teil der auch wirklich 0 werden kann}
$$
$$
\begin{matrix}
0 & = & 1 & -4 & \cdot & x & | & + 1 & \\
1 & = & 4 & & \cdot & x & | & \div 4 & \\
0,25 & = & x
\end{matrix}
$$
$$
f''(x) = 8 \cdot e^{-4 \cdot x} \cdot (2 \cdot x - 1)
$$
$$
f''(0,25) = > 0
$$
#### Beispiel Produktregel bei der Funktion $x \cdot e^x$
$$
\begin{matrix}
f(x) & = & g(x) & \cdot & h(x) & \\
f'(x) & = & g'(x) & \cdot & h(x) & + & g(x) & \cdot & h(x) &
\end{matrix}
$$
$$
\begin{matrix}
f(x) & = & e^{x} \cdot x \\
g(x) & = & e^{x} \\
h(x) & = & x \\
g'(x) & = & e^{x} \\ 
h'(x) & = & 1 \\
\end{matrix}
$$
$$
\text{Anwendung der Produktregel, man setzt in die Funktion ein und so erhaelt man die Ableitung}
$$
$$
\begin{matrix}
f'(x) & = & e^x \cdot x + e^x \cdot 1 \\
& = & e^x \cdot (x + 1) \\
\end{matrix}
$$
# mHIMI
[Mathematica](Mathematica/Abiturpruefung%202018.nb)  
![PDF](PDF/Mathe/9%20Abiturpruefung%20Mathe%202018%20mHIMI.pdf)