---
tags:
  - Mathe
---
*Marvin Baeumer* **2023-10-31 12:43**

---
**[Mathematica](Flugzeug%20Aufgabe.nb)**
### Welche Frage soll beantwortet werden
> Höhe Flugzeug zur Landebahn soll berechnet werden
### Was muss dazu konkret berechnet werden?
> Ebenengleichung mit den gegebenen Punkten $(P, Q, R)$ aufstellen Abstand von der Flugzeugspitze zur Ebene .
### Welche Rechenschritte sind zur Beantwortung der Frage 
Notwendig
Ebenengleichung aufstellen 
Normalvektor, der die Richtung der Ebene liefert 
Zusammen mit Flugzeugspitze ergibt sich eine Geradengleichung 
Länge von V $\rightarrow$ S mit dem Befehlt Norm[] ausrechnen 
LE $\rightarrow$ 100 Meter
### Rechnung
Ebenengleichung
$$E : \vec x = \begin{pmatrix} 1,5 \\ 0 \\ 0,1 \end{pmatrix} + r \cdot \begin{pmatrix} -3 \\ 0 \\ 0 \end{pmatrix} + v \cdot \begin{pmatrix} -1,5 \\ -10 \\ -0,2 \end{pmatrix}$$
Ausrechnen des Normalvektors mit Kreuzprodukt für den Richtungsvektor 
$$\begin{pmatrix} -3 \\ 0 \\ 0 \end{pmatrix} \times \begin{pmatrix} -1,5 \\ -10 \\ -0,2 \end{pmatrix} = \begin{pmatrix} 0 \\ -0,6 \\ 30 \end{pmatrix}$$
Aufstellen der Geradengleichung für das Flugzeug
$$g : \vec x = \begin{pmatrix} 0 \\ 6,5 \\ 2 \end{pmatrix} + t \cdot \begin{pmatrix} 0 \\ -0,6 \\ 30 \end{pmatrix}$$
Gleichstellen für den Schnittpunkt
$$E : \vec x = g : \vec x$$
$$\begin{pmatrix} 1,5 \\ 0 \\ 0,1 \end{pmatrix} + r \cdot \begin{pmatrix} -3 \\ 0 \\ 0 \end{pmatrix} + v \cdot \begin{pmatrix} -1,5 \\ -10 \\ -0,2 \end{pmatrix} = \begin{pmatrix} 0 \\ 6,5 \\ 2 \end{pmatrix} + t \cdot \begin{pmatrix} 0 \\ -0,6 \\ 30 \end{pmatrix}$$
$$r \rightarrow 0,84; v \rightarrow -0,06; t \rightarrow -0,059$$
$$\Leftrightarrow g : \vec x$$
$$g : \vec x = \begin{pmatrix} 0 \\ 6,5 \\ 2 \end{pmatrix} + (-0,059) \cdot \begin{pmatrix} 0 \\ -0,6 \\ 30 \end{pmatrix} = \begin{pmatrix} 0 \\ -0,65 \\ 0,23 \end{pmatrix}$$
Entfernung zur Landebahn ausrechnen
$$\left | \begin{pmatrix} 0 \\ -0,65 \\ 0,23 \end{pmatrix} - \begin{pmatrix} 0 \\ 6,5 \\ 2 \end{pmatrix} \right | = 1,7696 = 176,96m$$
Antwort: Die Entfernung vom Flugzeug zur Landebahn beträgt 176,96m. 