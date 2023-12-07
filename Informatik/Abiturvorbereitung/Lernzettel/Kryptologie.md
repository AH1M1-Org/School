---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-07 16:16**

---
### Symetrische/Asymetrische Verfahren
> Ein symmetrisches Verschlüsselungsverfahren wird angewendet, wenn derselbe Schlüssel sowohl für die Verschlüsselung als auch für die Entschlüsselung verwendet wird. Beim Caesar, Vigenere- oder One Time Pad Verfahren wird beispielsweise ein gemeinsamer Schlüssel genutzt, um die Chiffre zu entschlüsseln oder den Klartext zu verschlüsseln. Dies setzt voraus, dass sowohl der Sender als auch der Empfänger den Schlüssel kennen. Dazu muss der Schlüssel ausgetauscht werden.

$$
\huge \text{Formel fuer Anzahl Schluessel fuer n Teilnehmer}
$$
$$
\frac
{
n \cdot ( n - 1 )
}
{
2
}
$$

> Ein asymmetrisches Verschlüsselungsverfahren, wie das RSA-Verfahren, verwendet hingegen nicht denselben Schlüssel für die Ver- und Entschlüsselung einer Nachricht. Stattdessen werden ein privater und ein öffentlicher Schlüssel verwendet. Der private Schlüssel bleibt geheim, während der öffentliche Schlüssel öffentlich zugänglich ist. Wenn man nun eine Nachricht von Person A an Person B schicken will, muss Person A den öffentlichen Schlüssel von Person B nehmen und damit die Nachricht verschlüsseln. Mit dem Privat Key von Person B kann Person B nun die Nachricht entschlüsseln.

$$
\huge \text{Formel fuer Anzahl Schluessel fuer n Teilnehmer}
$$
$$
2 \cdot n
$$
#### Schlüsselaustauschproblem
> Das Schlüsseltauschproblem in der Kryptologie bezieht sich darauf, wie zwei Parteien sicher einen gemeinsamen geheimen Schlüssel austauschen können. Dies ist entscheidend für sichere Kommunikation. In asymmetrischer Kryptografie müssen die Parteien ihre öffentlichen Schlüssel austauschen, während in symmetrischer Kryptografie der gemeinsame Schlüssel sicher geteilt werden muss. Beispiele für Lösungen sind das Diffie-Hellman-Schlüsselaustauschprotokoll und hybride Verfahren.
### Diffie-Hellmann Verfahren
- Waehlen zweier Zahlen $p,g$
	- $p \rightarrow \mathbb{P}$
	- $g \rightarrow \mathbb{N}, g < p$ 
- Waehlen von $a \in \mathbb{N}; ~ a < p; ~~ b \in \mathbb{N}; ~ b < p$
- Berechnung von $A, B$ 
$$
Formel
$$
$$
\begin{matrix}
A = g^a \mod p && B = g^b \mod p
\end{matrix}
$$
- Berechnung von $K$
$$
Formel
$$
$$
\begin{matrix}
K = B^a \mod p && B = A^b \mod p
\end{matrix}
$$
> Das Diffie-Hellman-Verfahren dient dem sicheren Schlüsselaustausch zwischen zwei Parteien. $K$ ist dann der gemeinsame geheime Schlüssel und löst somit das [[Kryptologie#Schlüsselaustauschproblem|Schlüsselaustauschproblem]]. Das Diffie-Hellman-Verfahren wird bei symmetrischen Verschlüsselungsverfahren benötigt.
#### Beispiel
$$
p = 31, 
g = 15
$$

| Person A                   | Person B                  |
| -------------------------- | ------------------------- |
| $a = 25$                   | $b = 14$                  |
| $A = 15^{25} \mod 31$ = 30 | $B = 15^{14} \mod 31 = 2$ |
| $K = 2^{25} \mod 31 = 1$   | $K = 30^{14} \mod 31 = 1$ |
#### Beweis
Unter Anwendung der Potenzgesetze erhält man $K_1 = B^a \mod p = (g^b \mod p)^a \mod p = (g^{a \cdot b}) \mod p = (g^a \mod p)^b \mod p = A^b \mod p$
- Zuerst betrachtet man die Berechnung von $B$, dadurch das $B$ mit $g^b \mod p$ berechnet wird kann man für $B$ einsetzen. Somit erhält man $(g^b \mod p)^a$.
- Daraus folgt nach den Potenzgesetzen $(g^{a \cdot b}) \mod p$, zudem faellt das Innere $\mod p$ weg, weil wir immernoch in der selben Restklasse sind.
- Nun will man in die Form $A$, weil man beweisen will das $B^a \mod p = A^b \mod p$ ist. $A$ entspricht $g^a \mod p$ deswegen formt man um zu $(g^a \mod p)^b \mod p$ somit kann man dann $(g^a \mod p)^b \mod p$ vereinfachen zu $A^b \mod p$ rechnen.
- Somit ist Bewiesen das $B^a \mod p = A^b \mod p$
### Caesar Verfahren
> Bei dem Caesar Verfahren wird das Alphabet zum Verschluesseln um $n$ Schritte nach rechts verschoben und zum Entschluesseln nach $n$ Schritte nach links. 

| A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

| Klartext   | H   | A   | L   | L   | O   | n = 3 |
| ---------- | --- | --- | --- | --- | --- |-------|
| Ciphertext | K   | D   | O   | O   | R   | n = 3 |
### Vigenere Verfahren
|   | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
| B | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A |
| C | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B |
| D | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C |
| E | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D |
| F | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E |
| G | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F |
| H | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G |
| I | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H |
| J | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I |
| K | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J |
| L | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K |
| M | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L |
| N | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M |
| O | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N |
| P | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O |
| Q | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P |
| R | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q |
| S | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R |
| T | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S |
| U | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T |
| V | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U |
| W | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V |
| X | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W |
| Y | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X |
| Z | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y |
### [[Zahlentheorie#RSA-Verfahren|RSA Verfahren]]

