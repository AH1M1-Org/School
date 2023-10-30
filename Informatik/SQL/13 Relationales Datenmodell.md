Versicherungsgesellschaft($\underline{ID}$ , Firma, Strasse, PLZ, Telefon, HNr, Ort, $\uparrow$ Versciherungsvertrag_ID)

Versciherungsvertrag($\underline{ID}$, Kasko, VersNr, Beitrag, $\uparrow$ Fahrzeug_ID)

Fahrzeug($\underline{ID}$, Kennzeichen, Anschaffungsdatum, Anschaffungskosten, $\uparrow$ Instandhaltung_ID , $\uparrow$ Fahrzeugmodell_ID , $\uparrow$ Reservierung\_ID)

Instandhaltung($\underline{ID}$, Datum, Kosten, KMstand, Beschreibung)

Fahrzeugmodell($\underline{ID}$, Bezeichnung, Kraftstoff, Hersteller, Verbrauch)

Reservierung($\underline{ID}$, Beginn, Zweck, Ende, $\uparrow$ Mitarbeiter_ID)

Mitarbeiter($\underline{ID}$, PersNr, Vorname, Nachname)

Mitarbeiter_faehrt_mit($\uparrow Mitarbeiter\_ID$, $\uparrow Reservierung\_ID$)

---
*Marvin Baeumer* **2023-10-30 17:08** #Informatik