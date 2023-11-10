---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-10-31 12:42**

---
**[Arbeitsblatt](2%20Lagebezeichnung%20Gerade%20und%20Ebene.pdf) - [Mathematica](Mathe/Mathematica/Laser%20Aufgabe.nb)** 
#### Welche Frage muss beantwortet werden?
- Trifft die Waffe mit dem Laser die Ebene oder nicht, wenn ja wo?
#### Wie kann man die Schussrichtung und die Position der Pistole modellieren? 
- Schuss $\begin{pmatrix} 2 \\ -0.4 \\ 0,5 \end{pmatrix}$
- Pistole $\begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix}$
#### Wie lässt sich der Bildschirm mit Vektoren beschreiben 
- $\begin{pmatrix} 10 \\ -10 \\ 5 \end{pmatrix} + t \cdot \begin{pmatrix} 0 \\ 0 \\ -10 \end{pmatrix} + r \cdot \begin{pmatrix} 2.5 \\ 20 \\ -10 \end{pmatrix}$
##### Wie kann man den Punkt berechnen auf den die Pistole zielt?
- Schuss = Ebene stellen und dann einsetzen wenn es einen Schnittpunkt gibt
#### Rechnung
$$Ebene : \vec x = \begin{pmatrix} 10 \\ -10 \\ 5 \end{pmatrix} + t \cdot \begin{pmatrix} 0 \\ 0 \\ -10 \end{pmatrix} + r \cdot \begin{pmatrix} 2.5 \\ 20 \\ -10 \end{pmatrix}$$
$$Pistole : \vec x = \begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix} + v \cdot \begin{pmatrix} 2 \\ -0.4 \\ 0,5 \end{pmatrix}$$
$$Pistole = Ebene$$
$$\begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix} + v \cdot \begin{pmatrix} 2 \\ -0.4 \\ 0,5 \end{pmatrix} = \begin{pmatrix} 10 \\ -10 \\ 5 \end{pmatrix} + t \cdot \begin{pmatrix} 0 \\ 0 \\ -10 \end{pmatrix} + r \cdot \begin{pmatrix} 2.5 \\ 20 \\ -10 \end{pmatrix}$$
$$v \rightarrow 5,48 ; t \rightarrow - 0,36 ; r \rightarrow 0,39$$
$$\Leftrightarrow \begin{pmatrix} 0 \\ 0 \\ 2 \end{pmatrix} + 5,48 \cdot \begin{pmatrix} 2 \\ -0.4 \\ 0,5 \end{pmatrix} = \begin{pmatrix} 10,97 \\ -2,19 \\ 4,74 \end{pmatrix}$$
#### Antwort
- Der Schuss landet innerhalb des Bildschirms, weil der Schnittpunkt zwischen A,B und C liegt.