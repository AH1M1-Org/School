# euklidischeverfahren

### **Euklidischer algorithmus**
$a = b \cdot x + r$\
$a = b, b = a \mod b$
#### **Beispiel**
$ggt(630, 282)$

$630 = 282 \cdot 2 + 66$\
$282 = 66 \cdot 4 + 18$\
$66 = 18 \cdot 3 + 12$\
$18 = 12 \cdot 1 + 6$\
$12 = 6 \cdot 2 + 0$

$\Longrightarrow ggt(630, 282) = 6$

### **Erweiterter Euklidischer Algorithmus**
$a \cdot r + b \cdot s = ggt(a, b)$
#### **Beispiel**
$ggt(302, 128)$

1. Euklidischer Algorithmus
2. Umstellen nach Rest
3. Erweiterter Euklidischer Algorithmus

#### Euklidischer Algorithmus & Umstellen nach Rest
$302 = 128 \cdot 2 + 46 ~ | ~ 46 = 302 - 128 \cdot 2$\
$128 = 46 \cdot 2 + 36  ~ | ~ 36 = 128 - 46 \cdot 2$\
$46 = 36 \cdot 1 + 10  ~ | ~ 10 = 46 - 36 \cdot 1$\
$36 = 10 \cdot 3 + 6  ~ | ~ 6 = 36 - 10 \cdot 3$\
$10 = 6 \cdot 1 + 4  ~ | ~ 4 = 10 - 6 \cdot 1$\
$6 = 4 \cdot 1 + 2  ~ | ~ 2 = 6 - 4 \cdot 1$\
$4 = 2 \cdot 2 + 0$

$ggt(302, 128) = 2$

#### Erweiterter Euklidischer Algorithmus
|                                        |                                                                    |                      |
|----------------------------------------|--------------------------------------------------------------------|----------------------|
|$2 = 6 - \textbf{\underline{4}} \cdot 1$|$= 6 - \textbf{\underline{(10 - 6 ⋅ 1)}} \cdot 1$                    | vereinfachen        |
|                                        |$= 6 - 10 + 6$                                                      |zusammenfassen       |
|                                        |$= 2 \cdot \textbf{\underline{6}} - 10$                             |**fuer 6 einsetzen** |
|                                        |$= 2 \cdot \textbf{\underline{(36 - 10 ⋅ 3)}} - 10$                  |vereinfachen         |
|                                        |$= 2 \cdot 36 - 10 \cdot 6 - 10$                                    |zusammenfassen       |
|                                        |$= 2 \cdot 36 - \textbf{\underline{10}} \cdot 7$                    |**fuer 10 einsetzen**|
|                                        |$= 2 \cdot 36 - 7 \cdot \textbf{\underline{(46 - 36 ⋅ 1)}}$          |vereinfachen         |
|                                        |$= 2 \cdot 36 - 7 \cdot 46 + 7 \cdot 36$                            |zusammenfassen       |
|                                        |$= 9 \cdot \textbf{\underline{36}} - 7 \cdot 46$                    |**fuer 36 einsetzen**|
|                                        |$= 9 \cdot \textbf{\underline{(128 - 2 ⋅ 46)}} - 7\cdot 46$          |vereinfachen         |
|                                        |$= 9 \cdot 128 - 18 \cdot 46 - 7 \cdot 46 $                         |zusammenfassen       |
|                                        |$= 9 \cdot 128 - 25 \cdot \textbf{\underline{46}}$                  |**fuer 46 einsetzen**|
|                                        |$= 9 \cdot 128 - 25 \cdot \textbf{\underline{(302 - 128 ⋅ 2)}} $     |vereinfachen         |
|                                        |$= 9 \cdot 128 - 25\cdot 302 + 50 \cdot 128$                        |zusammenfassen       |
|                                        |$= - 25 \cdot 302 + 59 \cdot 128$                                   |BITTERES ENDE        |