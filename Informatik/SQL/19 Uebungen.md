---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:29**

---
### Relations Modell

Kunde($\underline{KundenNr}$, Name, Vorname)

Bestellung($\underline{BestellNr}$, Datum, $\uparrow$ KunderNr_Nr)

Artiekl($\underline{ArtikelNr}$, Bezeichnung, Preis)

Artikel_erhält_Bestellung($\uparrow \underline{BestellungNr\_Nr}, \uparrow \underline{ArtikelNr\_Nr}$ )

```SQL
CREATE TABLE Kunde(
    KundenNr INT NOT NULL,
    Name VARCHAR(30) NOT NULL,
    Vorname VARCHAR(30) NOT NULL,
    PRIMARY KEY(KundenNr)

);

CREATE TABLE(
    BestellNr INT NOT NULL,
    Datum date NOT NULL,
    KundenNr_Nr INT NOT NULL,
    PRIMARY KEY(BestellNr),
    FOREIGN KEY(KundenNr_Nr) REFRENCES Kunde(KundenNr));
```