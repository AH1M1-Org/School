---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-10-31 12:42**

---
**[Mathematica](Übungsaufgaben.nb)**
### Aufgabe 1
$$\cos^{-1} \begin{pmatrix} \frac{\begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix} \times \begin{pmatrix} -1 \\ 3 \\ 2 \end{pmatrix}}{\left| \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix} \right| \cdot \left| \begin{pmatrix} -1 \\ 3 \\ 2 \end{pmatrix} \right|} \end{pmatrix} = 70,89°$$
```mathematica
N[VectorAngle[{1,2,-1},{-1,3,2}]]
```
### Aufgabe 2
$$\begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} \times \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix} = - 3$$
```mathematica
{2,-1,3}.{1,2,-1}
```
### Aufgabe 3
$$\left | \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix} \times \begin{pmatrix} 2 \\ 1 \\ -1 \end{pmatrix} \right | = 9,11$$
```mathematica
N[Norm[Cross[{1, 2, 3}, {2, 1, -1}]]]
```
### Aufgabe 4
$$\begin{pmatrix} -3 \\ 0 \\ 1 \end{pmatrix} \times \begin{pmatrix} -3 \\ 2 \\ 0 \end{pmatrix} = \begin{pmatrix} -2 \\ -3 \\ -6 \end{pmatrix}$$
$$90 - \cos^{-1} \begin{pmatrix} \frac{\begin{pmatrix} -2 \\ 2 \\ -1 \end{pmatrix} \times \begin{pmatrix} -2 \\ -3 \\ -6 \end{pmatrix}}{\left| \begin{pmatrix} -2 \\ 2 \\ -1 \end{pmatrix} \right| \cdot \left| \begin{pmatrix} -2 \\ -3 \\ -6 \end{pmatrix} \right|} \end{pmatrix} = 46,50°$$
```mathematica
Cross[{-3, 0, 1}, {-3, 2, 0}]
90 - N[VectorAngle[{-2, 1, -3}, {-2, -3, -6}]/°] 
```