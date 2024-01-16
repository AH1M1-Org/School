---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### Begrifflichkeiten
#### Alphabet
Ein Alphabet ist eine endlich, nicht leere Menge $\sum$ von Zeichen. Zum Beispiel für die Sprache Schulnoten: $\{1, 2, 3, 4, 5, 6, +, -\}$ 
#### Wort
Ein Wort ist eine endliche Menge an Zeichen aus $\sum$. Zum Beispiel für die Sprache Schulnoten waeren $\{123, 2+ , 454-\}$ dies waeren zulaessige Worte der Sprache Schulnote.
#### Leeres Wort $\Huge \epsilon$ 
Das leere Wort $\large \epsilon$ enthält jede Sprache und dient als neutraler Multiplikator. $\epsilon \cdot 1- = 1-$
fuer das Beispiel Schulnoten.
#### Alle Moeglichkeiten $\large \sum^*$ 
alle denkbaren Aneinanderreihungen der Sprache, heißt $∑^∗$ ist unendlich lang. Eine Formale Sprache ist nun die Teilmenge von $∑^∗$.  Beispiel Schulnote: {1+, 1, 1-, 2+, 2, 2-, 3+, 3, 3-, 4+, 4, 4-, 5+, 5, 5-, 6} ⊂ $∑^*$
#### Sprache
Eine Sprache ist eine Teilmenge der möglichen Worte über einem Alphabet $\sum$
### Grammatik
#### Definition
Eine Grammatik $G = (N, \sum, S, P)$ ist ein 4-Tupel bestehend aus:
- der Menge $N$ an Nichtterminalsymbolen
- der Menge $\sum$ an Terminalsymbolen
- einem start symbol $S$
- einer Menge P an Produktionsregeln
Dabei gilt $N \cap \sum = \emptyset$, dass heißt ein Nichtterminalsymbol kann nicht gleichzeitig ein Terminalsymbol sein. Außerdem gilt $S \in N$, dass heißt ein start symbol muss ein Nichtterminalsymbol sein. Die durch eine Grammatik $G$ beschriebene formal Sprache ist die Sprache, die genau aus den Worten über $\sum$ besteht, die man mithilfe der Produktionsregeln $P$ aus dem start symbol $S$ ableiten kann.  
#### Bilden von Produktionsregeln - Schulnoten
Produktionsregeln werden gebildet in dem man seine Nichtterminalsymbole, die terminal Symbole und den Startpunkt definiert. Somit ergibt sich die Form $\sigma B$. 
**Beispiel**
$$
\begin{matrix}
N & \rightarrow & \{S\} \\
\sum  & \rightarrow & \{+, -, \large{\epsilon}\} \\
S & \rightarrow & \{S\} \\
P & \rightarrow & \\
\{ \\
S & \rightarrow & 1T, 2T, 3T, 4T, 5T, 6T \\
T & \rightarrow & +, -, \epsilon \\
\}
\end{matrix}
$$
> Man kann nun bei $S$ starten und muss dann $T$ aufrufen. $T$ ist dann die Abbruch Bedingung. Es lassen sich nun alle Schulnoten ableiten.
#### Definition einer regulären Grammatik


