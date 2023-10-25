### Berechnung ~ Skalarprodukt
$$\begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix} \cdot \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix} = x_1 \cdot x_2 + y_1 \cdot y_2 + z_1 \cdot z_2$$
```mathematica
{x, y, z}.{x, y, z}
```
> Wenn das Skalarprodukt = 0 ist, dann sind die beiden Vektoren senkrecht zueinander, also haben einen Winkel von $90 \textdegree$.

---
### Berechnung ~ Kreuzprodukt
$$\begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix} \cdot \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix} = \begin{pmatrix} a_2 \cdot b_3 - a_3 \cdot b_2 \\ a_3 \cdot b_1 - a_1 \cdot b_3 \\ a_1 \cdot b_2 - a_2 \cdot b_1 \end{pmatrix} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$$
```mathematica
Cross[]
```
> Das Kreuzprodukt gibt als Ergebniss einen Vektor der immer senkrecht zur Ebene steht. Dieser zeigt so an in welche Richtung die Ebene zeigt, das kann verwendet werden um Lichtreflektionen zu berechnen.
#### Flaecheninhalt
$$\begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix} \cdot \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix} = \begin{pmatrix} a_2 \cdot b_3 - a_3 \cdot b_2 \\ a_3 \cdot b_1 - a_1 \cdot b_3 \\ a_1 \cdot b_2 - a_2 \cdot b_1 \end{pmatrix} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$$
$$\sqrt{x^2 + y^2 + z^2} = Laenge$$
> Wenn man nun die Laenge des Kruezproduktes nimmt so erhaelt man den Flaecheninhalt der Flaeche.|

---
### Berechnung ~ Schnittwinkelgerade und Ebene
---