---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-11-10 13:03**

---
### Eine Matrix
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
#### Berechnung
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
> Berechnung erfolgt mit Zeile $\cdot$ Spalte. 
#### Bestandteile
$\begin{pmatrix}  a_1 & b_1 \\  c_1 & d_1 \end{pmatrix} \rightarrow$ Parameter koennen eine Matrix **Strecken/Stauchen**, **Spiegeln** und **Drehen**.
##### Spiegeln
> Veraenderung der Parameter $a_1 ~ ; ~ d_1$ ins positive oder Negative
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
> Die Matrix $\begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}$ funktioniert wie eine $\cdot$ 1 operation, es veraendert nichts. Abb 1

2 $\rightarrow$ Spieglung an der $x_2$ Achse $= \begin{pmatrix} -1 & 0 \\ 0 & 1\end{pmatrix}$

3 $\rightarrow$ Spieglung an der $x_1$ Achse $= \begin{pmatrix} 1 & 0 \\ 0 & -1\end{pmatrix}$

4 $\rightarrow$ Spieglung an der $x_1$ und $x_2$ Achse $= \begin{pmatrix} -1 & 0 \\ 0 & -1\end{pmatrix}$
##### Strecken/Stauchen
##### Drehen
##### Verschiebung
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
\filldraw[very thick](3,1) circle (0.1) node[left] {$A$};
\draw[ultra thick, -] (3,1) -- (2,4);

\filldraw[very thick](2,4) circle (0.1) node[above] {$C$};
\draw[ultra thick, -] (2,4) -- (1,2);

\filldraw[very thick](1,2) circle (0.1) node[above] {$B$}; 
\draw[ultra thick, -] (1,2) -- (3,1);

\filldraw[very thick](-2,-4) circle (0.1) node[left] {$3$};
\filldraw[very thick](-4,-4) circle (0.1) node[left] {$D$};
\draw[ultra thick, -] (-4,-4) -- (-2,-3);

\filldraw[very thick](-2,-3) circle (0.1) node[above] {$E$};
\draw[ultra thick, -] (-2,-3) -- (-1,-5);

\filldraw[very thick](-1,-5) circle (0.1) node[above] {$F$}; 
\draw[ultra thick, -] (-1,-5) -- (-4,-4);


\filldraw[very thick](-2.5,-1) circle (0.1) node[left] {$4$};
\filldraw[very thick](-4,-1) circle (0.1) node[left] {$D$};
\draw[ultra thick, -] (-4,-1) -- (-2,0);

\filldraw[very thick](-2,0) circle (0.1) node[above] {$E$};
\draw[ultra thick, -] (-2,0) -- (-1,-2);

\filldraw[very thick](-1,-2) circle (0.1) node[above] {$F$}; 
\draw[ultra thick, -] (-1,-2) -- (-4,-1);

\end{tikzpicture} 
\end{document} 
```
1 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 0 \end{pmatrix}$
2 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 4 \\ 0 \end{pmatrix}$
> Die Punkte $A, B, C$ sind um $4$ auf der $x_1$ Achse verschoben.

3 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 0 \end{pmatrix}$
4 $\rightarrow$ $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 0 \\ 3 \end{pmatrix}$
> Die Punkte $D, E, F$ sind um $4$ auf der $x_2$ Achse verschoben.