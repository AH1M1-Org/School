---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:28**

---
```SQL
CREATE TABLE Patient(
ID NOT NULL VARCHAR(6),
Name NOT NULL VARCHAR(30),
Vorname NOT NULL VARCHAR(30),
GebDatum NOT NULL DATE,
Geschlecht NOT NULL VARCHAR(1),
Wohnort NOT NULL VARCHAR(30),
HausartztID NOT NULL INTEGER,
KKID NOT NULL VARCHAR(7),
PRIMARY KEY(ID),
FOREIGN KEY (Hausartzt_ID) REFERENCES Arzt(ArztID),
FOREIGN KEY (KKID_ID) REFERENCES KKID(KKID));

INSERT INTO Patient
VALUES ("P21461","Mueller","Lieschen","1982-04-16","W","Duesseldorf",2117,"BAR1621")
```