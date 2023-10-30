## Skalarprodukt (Punktprodukt) 
### Beispiel 
![Picture](https://cdn.discordapp.com/attachments/1139161006761857024/1167490702612103299/image.png?ex=654e5172&is=653bdc72&hm=f4cd326b407730458d0ca4a1efb914058d63ac03879f1c0db5d0499cf0ed3f09&)
### Orthogonalität
$$\begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix} \times \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix} = x_1 \cdot x_2 + y_1 \cdot y_2 + z_1 \cdot z_2$$
> Wenn das Skalarprodukt = 0 ist, dann sind die beiden Vektoren senkrecht zueinander, sprich sie sind Orthogonal zueinander.

```mathematica
{x, y, z}.{x, y, z} 
```
### Winkel
$$\vec a = \begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix}, \vec b = \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix}$$
$$\gamma = \cos^{-1} \begin{pmatrix} \frac{\vec a \cdot \vec b}{\left| \vec a \right| \cdot \left| \vec b \right|} \end{pmatrix} = \cos^{-1} \begin{pmatrix} \frac{\begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix} \times \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix}}{\left| \vec a \right| \cdot \left| \vec b \right|} \end{pmatrix}$$
> Man rechnet das Skalarprodukt zweier Vektoren $\div$ durch das Produkt der Laengen von $\vec a, \vec b$

```mathematica
N[VectorAngle[{x, y, z},{x, y, z}]/°]
```
---
## Kreuzprodukt (Vektorprodukt)
### Beispiel 
![Picture](https://cdn.discordapp.com/attachments/1139161006761857024/1167490442674311198/image.png?ex=654e5134&is=653bdc34&hm=cc7257fce6b4a3c308301a091f87782d3d295a754a17a38e9006b92a96f1c39b&)
### Berechnung
$$\begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix} \times \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix} = \begin{pmatrix} y_1 \cdot z_2 - z_1 \cdot y_2 \\ z_1 \cdot x_2 - x_1 \cdot z_2 \\ x_1 \cdot y_2 - y_1 \cdot x_2 \end{pmatrix} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$$

> Das Kreuzprodukt gibt als Ergebniss einen Vektor der immer senkrecht zur Ebene steht. Dieser zeigt so an in welche Richtung die Ebene zeigt, das kann verwendet werden um Lichtreflektionen zu berechnen.

```mathematica
Cross[{x, y, z},{x, y, z}]
```
### Flaecheninhalt
$$\begin{pmatrix} x_1 \\ y_1 \\ z_1 \end{pmatrix} \times \begin{pmatrix} x_2 \\ y_2 \\ z_2 \end{pmatrix} = \begin{pmatrix} y_1 \cdot z_2 - z_1 \cdot y_2 \\ z_1 \cdot x_2 - x_1 \cdot z_2 \\ x_1 \cdot y_2 - y_1 \cdot x_2 \end{pmatrix} = \left| \begin{pmatrix} x \\ y \\ z \end{pmatrix} \right| = \sqrt{x^2 + y^2 + z^2} = Laenge$$

> Wenn man nun die Laenge des Kruezproduktes nimmt so erhaelt man den Flaecheninhalt der Flaeche.

```mathematica
Norm[Cross[{x, y, z},{x, y, z}]]
```
---
## Schnittwinkel 
### Beispiel
![Picture](https://cdn.discordapp.com/attachments/1139161006761857024/1167492585141588028/image.png?ex=654e5333&is=653bde33&hm=bb9124ab5954f9f747a4db2d252cd44e2809ee0777d5ada0f26e45e412c27369&)
### Berechnung
$$g : \vec x = \vec u + t \cdot \vec v$$
$$E : \vec x = \vec u_E + t \cdot \vec v_E + r \cdot \vec w_E$$
- Zuerst berechnet man den Normalvektor $\vec n$, also das Kreuzprodukt der Flaeche.
$$\vec n = \vec v_E \times \vec w_E$$
- Dann berechnet man den Winkel zwischen Bewegungsvektor von $g : \vec x$ und  dem Normalvektor $\vec n$
$$\gamma = \cos^{-1} \begin{pmatrix} \frac{\vec n \cdot \vec v}{\left| \vec n \right| \cdot \left| \vec v \right|} \end{pmatrix}$$
- Danach gilt $\alpha = 90° - \gamma$ , so erhaehlt man den Schnittwinkel $\alpha$ zur Ebene $E : \vec a$ und der geraden $g : \vec x$


## [Zum Infomaterial](1%20Infomaterial%20Vektoren.pdf)







---
*Marvin Baeumer* **2023-10-30 17:06** #Mathe