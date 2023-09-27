# Aufgaben 

### 1.5
Bei einem Inner Join wird die Schnittmenge ausgegeben von allen Trainingsplänen die auch einen Trainer haben, also wo der Fremdschlüssel TID dem Primärschlüssel TID in der Tabelle Trainer zugeordnet werden kann.\
Bei einem Left Join werden alle Trainingspläne ausgegeben auch wenn diese nicht einen Trainer haben, also wenn der Fremdschlüssel TID nicht einem Trainer zugeordnet werden kann werden diese Trainingspläne trotzdem zugeordnet.

### 1.6
```SQL
UPDATE Trainer
SET (Grundpreis=Grundpreis*0.95)
```

### 1.7
```SQL
SELECT Tag, SollZeit, SollDistanz FROM Traingingseinheit
INNER JOIN Traingsplan ON Traingsplan.TPID = Traingingseinheit.TPID
INNER JOIN Trainer ON Trainer.TID = Trainingsplan.TID
WHERE Vorname = "Max" AND Nachname = "Mustermann"
ORDER BY TPID ASC, Traingsplan.Tag ASC
```

### 1.8
```SQL
SELECT Bezeichnung, SUM(Grundpries*Faktor) FROM Ziel
INNER JOIN Traingsplan ON Trainigsplan.ZID = Ziel.ZID
INNER JOIN Trainer ON Trainingsplan.TID = Trainer.TID
GROUP BY Bezeichnung, ZID
```

### 1.9
```SQL
CREATE VIEW durschschnitt AS
SELECT AVG(Grundpreis) AS Durschnitt FROM Trainer
INNER JOIN Traingsplan ON Trainingsplan.TID = Trainer.TID
GROUP BY Trainer.TID
HAVING 100 < (SELECT COUNT(*) FROM Trainingsplan)
```