---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-10-31 15:29**

---
VIEWS sind Abfragen, die in der Datenbank als Objekt fest gespeichert sind! Ergebnis sind virtuelle Tabellen!\
Sie können in jedem Select-Befehl anstelle einer echten Tabelle verwendet werden.\
**Syntax:**
```SQL
CREATE VIEW [Name] AS SELECT [Spalten]
```
VIEW wird dann wie eine normalle Tabelle in abfragen benutzt.
```SQL
SELECT * FROM [VIEW Name] ORDER BY [VIEW Spalte]
```
Warum benutzt man VIEW abfragen?
- Berechtigung

#### [Arten von Joins](https://www.tinohempel.de/info/info/datenbank/operation.htm)