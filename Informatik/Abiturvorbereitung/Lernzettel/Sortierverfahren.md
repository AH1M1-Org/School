---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### Verschiedene Sortierverfahren
#### Bubble Sort
> Bubble Sort vergleicht benachbarte Elemente in der Liste und tauscht sie, bis die Liste sortiert ist. Das größte Element "blubbert" nach hinten. Das rote Element wird mit dem grauen Element verglichen.

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white, color=gray] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white, color=purple] (2,0) rectangle (3,1);
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
\draw[line width=1.5pt, fill=white, color=purple] (4,-1) rectangle (5,-2);
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
\draw[line width=1.5pt, fill=white, color=purple] (6,-3) rectangle (7,-4);
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
\draw[line width=1.5pt, fill=white, color=purple] (8,-5) rectangle (9,-6);
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
#### Insertion Sort
> Insertion Sort durchläuft die Liste und fügt jedes Element an seine korrekte Position ein, wodurch die Liste nach und nach sortiert wird.

```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white, color=gray] (0,0) rectangle (1,1);
\node at (0.5,0.5) {5};
\draw[line width=1.5pt, fill=white, color=purple] (2,0) rectangle (3,1);
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
\draw[line width=1.5pt, fill=white, color=purple] (4,-1) rectangle (5,-2);
\node at (4.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2);
\node at (6.5,-1.5) {1};
\draw[line width=1.5pt, fill=white] (8,-1) rectangle (9,-2);
\node at (8.5,-1.5) {4};

\draw[dotted, line width=2pt] (0, -2.5) -- (9, -2.5);

\draw[line width=1.5pt, fill=white, color=gray] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {5};
\draw[line width=1.5pt, fill=white, color=purple] (4,-3) rectangle (5,-4);
\node at (4.5,-3.5) {3};
\draw[line width=1.5pt, fill=white] (6,-3) rectangle (7,-4);
\node at (6.5,-3.5) {1};
\draw[line width=1.5pt, fill=white] (8,-3) rectangle (9,-4);
\node at (8.5,-3.5) {4};

\end{tikzpicture} 
\end{document} 
``` 
#### Selection Sort
#### Quick Sort
### Laufzeiten
|                | worst-case | avarrage-case | best-case |
| -------------- | ---------- | ------------- | --------- |
| Bubble Sort    | $O(n^2)$           | $O(n^2)$              | $O(n)$          |
| Insertion Sort | $O(n^2)$           | $O(n^2)$              | $O(n)$          |
| Selection Sort | $O(n^2)$           | $O(n^2)$              | $O(n^2)$          |
| Quick Sort               | $O(n^2)$           | $O(n \cdot log \cdot n)$              | $O(n \cdot log \cdot n)$          |
### Stabile und nicht stabile Verfahren
> Ein Sortierverfahren gilt dann als stabil wenn die ursprüngliche Reinfolge bei gleichen Elementen im sortierten zustand bewahrt wird. Bei einem nicht stabilen Sortieralgorithmus hingegen geht die Reinfolge verloren. 

|  | Stabil | Begruendung |
| ---- | ---- | ---- |
| Bubble Sort | Ja | Beim Bubble Sort werden Elemente paarweise verglichen, und wenn die Reihenfolge falsch ist, werden sie getauscht. Wenn zwei Elemente denselben Schlüsselwert haben, wird kein Tausch vorgenommen. |
| Insertion Sort | Ja |  |
| Selection Sort | Nein |  |
| Quick Sort | Nein |  |
#### Beispiel - stabile Sortierung
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white] (0,0) rectangle (1,1);
\node at (0.5,0.5) {1};
\draw[line width=1.5pt, fill=white, color=gray] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white, color=purple] (4,0) rectangle (5,1);
\node at (4.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0,1.5) -- (9,1.5);

\draw[line width=1.5pt, fill=white] (0,2) rectangle (1,3);
\node at (0.5,2.5) {4};
\draw[line width=1.5pt, fill=white] (2,2) rectangle (3,3);
\node at (2.5,2.5) {1};
\draw[line width=1.5pt, fill=white] (4,2) rectangle (5,3);
\node at (4.5,2.5) {3};
\draw[line width=1.5pt, fill=white, color=gray] (6,2) rectangle (7,3);
\node at (6.5,2.5) {2};
\draw[line width=1.5pt, fill=white, color=purple] (8,2) rectangle (9,3);
\node at (8.5,2.5) {2};

\end{tikzpicture} 
\end{document} 
```
> Man sieht das die erste $2$ auch die erste sortierte $2$ bleibt.