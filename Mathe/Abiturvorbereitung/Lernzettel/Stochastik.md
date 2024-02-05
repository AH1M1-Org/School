---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-12-06 10:22**

---
### Baumdiagram
> Ein Baumdiagramm ist eine grafische Darstellung, die verwendet wird, um verschiedene mögliche Entscheidungswege oder Ergebnisse eines Ereignisses darzustellen. Es besteht aus einem Stamm, der das Ausgangsereignis darstellt, und Zweigen, die die verschiedenen möglichen Entscheidungspfade oder Ergebnisse repräsentieren.
```tikz
\begin{document} 
\begin{tikzpicture}
	\draw[line width=1.5pt, fill=black] (0.5,0) circle [radius = 0.1];
	\draw[->, line width=1.5pt, fill=white] (0.5,0) -- (4,4);
	\draw[->, line width=1.5pt, fill=white] (0.5,0) -- (4,-4);
	\node at(2,2.5) {$P(A)$};
	\node at(2,-2.5) {$P(\overline{A})$};
	
	\draw[line width=1.5pt, fill=white] (4.5,4.25) circle [radius = 0.5];
	\draw[line width=1.5pt, fill=white] (4.5,-4.25) circle [radius = 0.5];
	\node at(4.5,4.25) {$P(A)$};
	\node at(4.5,-4.25) {$P(\overline{A})$};

	\draw[->, line width=1.5pt, fill=white] (5,4.25) -- (8,7.25);
	\draw[->, line width=1.5pt, fill=white] (5,4.25) -- (8,1.25);
	\draw[->, line width=1.5pt, fill=white] (5,-4.25) -- (8,-7.25);
	\draw[->, line width=1.5pt, fill=white] (5,-4.25) -- (8,-1.25);
	
	\node at(6,6) {$P_A(B)$};
	\node at(6,2.5) {$P_A(\overline{B})$};
	\node at(6,-6) {$P_{\overline{A}}(\overline{B})$};
	\node at(6,-2.5) {$P_{\overline{A}}({B})$};
	
	\draw[line width=1.5pt, fill=white] (8.5,7.5) circle [radius = 0.5];
	\draw[line width=1.5pt, fill=white] (8.5,1) circle [radius = 0.5];
	\draw[line width=1.5pt, fill=white] (8.5,-7.5) circle [radius = 0.5];
	\draw[line width=1.5pt, fill=white] (8.5,-1) circle [radius = 0.5];
	
	\node at(8.5,7.5) {$B$};
	\node at(8.5,1) {$\overline{B}$};
	\node at(8.5,-7.5) {$\overline{B}$};
	\node at(8.5,-1) {$\overline{B}$};
	
	\node at(10,7.5) {$P(A \cap B)$};
	\node at(10,1) {$P(A \cap \overline{B})$};
	\node at(10,-7.5) {$P(\overline{A} \cap B)$};
	\node at(10,-1) {$P(\overline A \cap \overline{B})$};
	
\end{tikzpicture}
\end{document} 
```
### Vierfeldertafel
> Innerhalb einer Vierfeldertafel stehen die $\cap$ Wahrscheinlichkeiten, unten hingegen steht die Summe des jeweiligen Ereigniss das sich mit der Summenregel berechnen laesst.

|  | $A$ | $\overline{A}$ | Summe |
| ---- | ---- | ---- | ---- |
| $\textbf{B}$ | $P(A \cap B)$ | $P(\overline{A} \cap B)$ | $P(B)$ |
| $\overline{\textbf{B}}$ | $P(A \cap \overline{B})$ | $P(\overline{A} \cap \overline{B})$ | $P(\overline{B})$ |
| **Summe** | $P(A)$ | $P(\overline{A})$ | **100%** |

### Pfadregel
> Die Pfadregel besagt das man zusammenhaengende Pfade eines Baumdiagrammes miteinander multiplizieren kann um somit die die $\cap$ Wahrscheinlichkeit zu erhalten. Dabei ist wichtig es darf nur ein zusammenhaenger Pfad betrachtet werden.
> $P(A) \cdot P_A(B) = P(A \cap B)$ Es wird die Summe mit mit der Bedingung multiplizier. 
### Summenregel
> Die Summenregel besagt das die Ergebnisse unabhaengiger Pfade miteinander addiert werden duerfen um die Summe von bestimmten Ereignissen zu erhalten. 
> $P(A) = P(A \cap B) + P(A \cap \overline{B})$.
