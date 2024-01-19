---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### Verschiedene Sortierverfahren - Theorie
#### Bubble Sort
> Bubble Sort vergleicht benachbarte Elemente in der Liste und tauscht sie, bis die Liste sortiert ist. Das größte Element "blubbert" nach hinten.  In einem Beispiel würde erst der Vergleich zwischen 5 und 2 stattfinden. Dadurch, dass die 2 kleiner als die fünf ist, werden sie getauscht.
> 
> **Legende**
> Das Rote Element wird immer mit dem grauen Element verglichen.

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white, color=gray] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {2};
\draw[line width=1.5pt, fill=white, color=gray] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[line width=1.5pt, fill=white] (0, -2.5) rectangle (9, -2.5);

\draw[line width=1.5pt, fill=white] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {3};
\draw[line width=1.5pt, fill=white, color=gray] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {1};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\draw[line width=1.5pt, fill=white] (0, -4.5) rectangle (9, -4.5);

\draw[line width=1.5pt, fill=white] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {2};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {3};
\draw[line width=1.5pt, fill=white] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, color=gray] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {4};

\draw[line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {2};
\draw[line width=1.5pt, fill=white] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {3};
\draw[line width=1.5pt, fill=white] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {1};
\draw[line width=1.5pt, fill=white] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {4};
\draw[line width=1.5pt, fill=white, color=gray] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {5};

\draw[line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\end{tikzpicture} 
\end{document} 
``` 

<div style="page-break-after: always;"></div>

#### Insertion Sort
> Insertion Sort durchläuft die Liste und fügt jedes Element an seine korrekte Position ein, wodurch die Liste nach und nach sortiert wird. Die Fünf gilt von Anfang an als sortiert. Somit wird die Zwei erst mit der Fünf verglichen; die Zwei ist kleiner, also wird sie vor der Fünf eingefügt. Die Drei wird dann erst mit der Fünf verglichen; diese ist auch kleiner, also wird sie dann mit der Zwei verglichen. Dadurch, dass die Drei dann größer ist, wird die Drei zwischen 2 und 5 eingefügt. 
> 
> **Legende**
> Das rote Element wird immer mit dem grauen verglichen.
> Das umrandete Element steht für das "Pivot-Element".

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white, color=gray, draw=lime] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {2};
\draw[line width=1.5pt, fill=white, color=gray, draw=lime] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white, color=gray] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white, draw=lime] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {3};
\draw[line width=1.5pt, fill=white] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {1};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\draw[dotted, line width=2pt] (0, -4.5) -- (9, -4.5);

\draw[line width=1.5pt, fill=white] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {3};
\draw[line width=1.5pt, fill=white, draw=lime] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {5};
\draw[line width=1.5pt, fill=white] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {1};
\draw[line width=1.5pt, fill=white] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {4};

\draw[line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {2};
\draw[line width=1.5pt, fill=white, ] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {3};
\draw[line width=1.5pt, fill=white, color=gray, draw=lime] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {1};
\draw[line width=1.5pt, fill=white] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {4};

\end{tikzpicture} 
\end{document} 
``` 

<div style="page-break-after: always;"></div>

#### Selection Sort
>  Beim Selection Sort wird in jedem Schritt das kleinste Element ausgewählt und an die erste Position gesetzt. Dieser Prozess wiederholt sich, bis die gesamte Liste sortiert ist. In einem Beispiel wird das Minimum zu Beginn auf fünf festgelegt. Dann durchläuft der Algorithmus die Elemente und sucht das kleinste Element. Zuerst ist dies die Zwei, somit wird die Zwei das neue Minimum. Am Ende ist es die Eins. Die Eins wird dann mit der Fünf getauscht.
>  
>  **Legende:** 
>  Das rote Element wird immer mit dem umrandeten Element verglichen. 
>  Das graue Element zeigt, welches getauscht wird. 
>  Das umrandete Element zeigt das aktuelle Minimum.

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white, color=gray, draw=lime] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white, color=magenta] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white, color=gray] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {5};
\draw[line width=1.5pt, fill=white, draw=lime] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white, color=gray] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {5};
\draw[line width=1.5pt, fill=white, draw=lime] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {3};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {1};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\draw[dotted, line width=2pt] (0, -4.5) -- (9, -4.5);

\draw[line width=1.5pt, fill=white, color=gray] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {5};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {2};
\draw[line width=1.5pt, fill=white] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {3};
\draw[line width=1.5pt, fill=white, draw=lime] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, color=magenta] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {4};

\draw[line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {1};
\draw[line width=1.5pt, fill=white, color=gray, draw=lime] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {3};
\draw[line width=1.5pt, fill=white] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {5};
\draw[line width=1.5pt, fill=white] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {4};

\end{tikzpicture} 
\end{document} 
```

<div style="page-break-after: always;"></div>

#### Quick Sort

<div style="page-break-after: always;"></div>

### Verschiedene Sortierverfahren
> In den folgenden Beispielen sieht man einen Schreibtischtest der den print nach der 1- äußeren Schleifen iteration darstellt. 
#### Bubble Sort
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {2};
\draw[line width=1.5pt, fill=white] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {4};
\draw[line width=1.5pt, fill=white, color=magenta] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {5};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {3};
\draw[line width=1.5pt, fill=white] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {1};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {4};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {5};

\draw[dotted, line width=2pt] (0, -4.5) -- (9, -4.5);

\draw[line width=1.5pt, fill=white] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {2};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {3};
\draw[line width=1.5pt, fill=white] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {4};
\draw[line width=1.5pt, fill=white] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {5};

\draw[dotted, line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {1};
\draw[line width=1.5pt, fill=white, color=magenta] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {2};
\draw[line width=1.5pt, fill=white] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {3};
\draw[line width=1.5pt, fill=white] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {4};
\draw[line width=1.5pt, fill=white] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {5};

\end{tikzpicture} 
\end{document} 
```

#### Insertion Sort

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white, color=magenta] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {2};
\draw[line width=1.5pt, fill=white, draw=lime] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {5};
\draw[line width=1.5pt, fill=white] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {3};
\draw[line width=1.5pt, fill=white, draw=lime] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {5};
\draw[line width=1.5pt, fill=white] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {1};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\draw[dotted, line width=2pt] (0, -4.5) -- (9, -4.5);

\draw[line width=1.5pt, fill=white, color=magenta] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {1};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {2};
\draw[line width=1.5pt, fill=white] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {3};
\draw[line width=1.5pt, fill=white, draw=lime] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {5};
\draw[line width=1.5pt, fill=white] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {4};

\draw[dotted, line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {1};
\draw[line width=1.5pt, fill=white] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {2};
\draw[line width=1.5pt, fill=white] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {3};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {4};
\draw[line width=1.5pt, fill=white, draw=lime] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {5};

\end{tikzpicture} 
\end{document} 
```

<div style="page-break-after: always;"></div>

#### Selection Sort
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0, -0.5) rectangle (9, -0.5);

\draw[line width=1.5pt, fill=white, color=magenta] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (2,-1) rectangle (3,-2);
\node at (2.5,-1.5) {2};
\draw[line width=1.5pt, fill=white] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white, color=gray] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {5};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {1};
\draw[line width=1.5pt, fill=white, color=magenta] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {3};
\draw[line width=1.5pt, fill=white] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {5};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\draw[dotted, line width=2pt] (0, -4.5) -- (9, -4.5);

\draw[line width=1.5pt, fill=white] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {1};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {3};
\draw[line width=1.5pt, fill=white] (6,-5) rectangle (7,-6);
\node at (6.5,-5.5) {5};
\draw[line width=1.5pt, fill=white] (8,-5) rectangle (9,-6);
\node at (8.5,-5.5) {4};

\draw[dotted, line width=1.5pt, fill=white] (0, -6.5) rectangle (9, -6.5);

\draw[line width=1.5pt, fill=white] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {1};
\draw[line width=1.5pt, fill=white] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {2};
\draw[line width=1.5pt, fill=white] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {3};
\draw[line width=1.5pt, fill=white, color=magenta] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {4};
\draw[line width=1.5pt, fill=white, color=gray] (8,-7) rectangle (9,-8);
\node at (8.5,-7.5) {5};

\end{tikzpicture} 
\end{document} 
```

#### Quick Sort

<div style="page-break-after: always;"></div>

### Laufzeiten
|  | worst-case | avarrage-case | best-case |
| ---- | ---- | ---- | ---- |
| Bubble Sort | $O(n^2)$ | $O(n^2)$ | $O(n)$ |
| Insertion Sort | $O(n^2)$ | $O(n^2)$ | $O(n)$ |
| Selection Sort | $O(n^2)$ | $O(n^2)$ | $O(n^2)$ |
| Quick Sort | $O(n^2)$ | $O(n \cdot log \cdot n)$ | $O(n \cdot log \cdot n)$ |
### Feldelementvergleiche- und verschiebungen
> Für Sortieralgorithmen mit einer Durchschnitts Laufzeit von $O(n^2)$ gilt für den Worst-case der vergleiche $\frac{n(n - 1)}{2}$ und für den Best-case $n - 1$. Für die Feldelementbewegungen beim Worst-case gilt immer $n \cdot 3$ da man für jeder Bewegung $3$ Verschiebungen braucht. Beim Best-case sind es $0$ Bewegungen, weil keine Bewegungen bei einer Sortierten Reinfolge benötigt werden.
### Stabile und nicht stabile Verfahren
> Ein Sortierverfahren gilt dann als stabil wenn die ursprüngliche Reinfolge bei gleichen Elementen im sortierten zustand bewahrt wird. Bei einem nicht stabilen Sortieralgorithmus hingegen geht die Reinfolge verloren. 

|  | Stabil | Begruendung |
| ---- | ---- | ---- |
| Bubble Sort | Ja | Beim Bubble Sort werden Elemente paarweise verglichen, und wenn die Reihenfolge falsch ist, werden sie getauscht. Wenn zwei Elemente denselben Schlüsselwert haben, wird kein Tausch vorgenommen. |
| Insertion Sort | Ja | Insertion Sort ist im Allgemeinen stabil, da bei gleichem Schlüsselwert das neu eingefügte Element nach den bereits vorhandenen mit dem gleichen Schlüsselwert platziert wird. |
| Selection Sort | Nein | Selection Sort ist im Allgemeinen nicht stabil, da bei gleichen Schlüsselwerten keine Garantie besteht, dass die Reihenfolge beibehalten wird. |
| Quick Sort | Nein | Quick Sort ist im Allgemeinen nicht stabil, da während des Aufteilungsgesetz die Reihenfolge von Elementen mit gleichem Schlüsselwert nicht beibehalten wird. |
#### Beispiel - stabile Sortierung
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt] (0,0) rectangle (1,1);
\node at (0.5,0.5) {1};
\draw[line width=1.5pt, fill=white, color=gray] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (4,0) rectangle (5,1);
\node at (4.5,0.5) {2};
\draw[line width=1.5pt] (6,0) rectangle (7,1);
\node at (6.5,0.5) {3};
\draw[line width=1.5pt] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt] (0,1.5) -- (9,1.5);

\draw[line width=1.5pt] (0,2) rectangle (1,3);
\node at (0.5,2.5) {4};
\draw[line width=1.5pt] (2,2) rectangle (3,3);
\node at (2.5,2.5) {1};
\draw[line width=1.5pt] (4,2) rectangle (5,3);
\node at (4.5,2.5) {3};
\draw[line width=1.5pt, fill=white, color=gray] (6,2) rectangle (7,3);
\node at (6.5,2.5) {2};
\draw[line width=1.5pt, fill=white, color=magenta] (8,2) rectangle (9,3);
\node at (8.5,2.5) {2};

\end{tikzpicture} 
\end{document} 
```
> Man sieht das die erste $2$ auch die erste sortierte $2$ bleibt.