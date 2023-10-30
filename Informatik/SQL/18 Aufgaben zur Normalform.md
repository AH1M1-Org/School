### 1. ) [Normalform](17%20Normalisierung%20von%20Datenbanken.md)
#### Patient:

|$\underline{PatientenNr}$|Name|Geburtsdatum|Strasse|Hausnummer|PLZ|Ort|Krankenkasse|Station|Raum|
|-----------|----|------------|-------|----------|---|---|------------|-------|----|-|

#### Behandlung:

| $\underline{PatientenNr}$ | $\underline{Datum}$ | $\underline{DiagnoseNr}$ | Therapie | Systolwert | Dyastolwert |
| ------------------------- | ------------------- | ------------------------ | -------- | ---------- | ----------- |

---
### 2.  [Normalform](17%20Normalisierung%20von%20Datenbanken.md)
#### Patient

|$\underline{PatientenNr}$|Name|Geburtsdatum|Strasse|Hausnummer|PLZ|Ort|Krankenkasse|Station|Raum|
|-----------|----|------------|-------|----------|---|---|------------|-------|----|

#### Messwerte

|$\underline{PatientNr}$|$\underline{Datum}$|Szstole|Diastole|
|---------|-----|-------|--------|

#### Erkrankung

|$\underline{PatientNr}$|$\underline{Datum}$|$\underline{DiagnoseNr}$|
|---------|-----|----------|

#### Diagnose

|$\underline{DiagnoseNr}$|Diagnose|Therapie|
|----------|--------|--------|

---
### 3.  [Normalform](17%20Normalisierung%20von%20Datenbanken.md) 
#### Patient

|$\underline{PatientenNr}$|Name|Geburtsdatum|Strasse|Hausnummer|PLZ|Ort|Krankenkasse|Station|Raum|
|-----------|----|------------|-------|----------|---|---|------------|-------|----|

#### Messwerte

|$\underline{PatientNr}$|$\underline{Datum}$|Szstole|Diastole|
|---------|-----|-------|--------|

**Erkrankung**

|$\underline{PatientNr}$|$\underline{Datum}$|$\underline{DiagnoseNr}$|
|---------|-----|----------|

**Diagnose**

|$\underline{DiagnoseNr}$|Diagnose|Therapie|
|----------|--------|--------|

**Orte**

|$\underline{PLZ}$|Ort|
|-----------------|---|

**Räume**

|$\underline{Raum}$|Station|
|------------------|-------|

---
*Marvin Baeumer* **2023-10-30 17:09** #Informatik