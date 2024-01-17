---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### Verschiedene Sortierverfahren
#### Bubble Sort
#### Insertion Sort
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

#### Beispiel - stabile Sortierung
```tikz 
\begin{document} 
\begin{tikzpicture} 

\draw[line width=1.5pt, fill=white] (0,0) rectangle (1,1);
\node at (0.5,0.5) {1};
\draw[line width=1.5pt, fill=white] (2,0) rectangle (3,1);
\node at (2.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (4,0) rectangle (5,1);
\node at (4.5,0.5) {2};
\draw[line width=1.5pt, fill=white] (6,0) rectangle (7,1);
\node at (6.5,0.5) {3};
\draw[line width=1.5pt, fill=white] (8,0) rectangle (9,1);
\node at (8.5,0.5) {4};

\draw[line width=1.5pt, fill=white] (0,1.5) -- (9,1.5);

\draw[line width=1.5pt, fill=white] (0,2) rectangle (1,3);
\node at (0.5,2.5) {4};
\draw[line width=1.5pt, fill=white] (2,2) rectangle (3,3);
\node at (2.5,2.5) {2};
\draw[line width=1.5pt, fill=white] (4,2) rectangle (5,3);
\node at (4.5,2.5) {2};
\draw[line width=1.5pt, fill=white] (6,2) rectangle (7,3);
\node at (6.5,2.5) {1};
\draw[line width=1.5pt, fill=white] (8,2) rectangle (9,3);
\node at (8.5,2.5) {3};

\end{tikzpicture} 
\end{document} 
```
