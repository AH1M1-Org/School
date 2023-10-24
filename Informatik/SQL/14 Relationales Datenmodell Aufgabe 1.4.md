Project($\underline{ID}$, startdatum, enddatum, Bezeichnung, Kurzbeschreibung $\uparrow$ Projekt_arbeitet_Mitarbeiter)

Mitarbeiter($\underline{ID}$, Vorname, Nachname, Personalnummer, $\uparrow$ Projekt_ID, Projekt_arbeitet_Mitarbeiter)

Ressort($\underline{ID}$, Bezeichnung, $\uparrow$ Mitarbeiter_ID)

Projekt_arbeitet_Mitarbeiter($\uparrow$ Mitarbeiter_ID, $\uparrow$ Projekt_ID)