---
tags:
  - Informatik
---
*Marvin Baeumer* **2024-01-10 08:14**

---
![PDF](PDF/Informatik/5%20Abiturpruefung%202023.pdf)
# Dynamische Datenstrukturen 

### In der Entwicklungsabteilung gibt es eine Arbeitsgruppe, die sich mit der Programmierung der Spiellogik befasst. Dabei geht es u. a. um die Verwaltung von Ereignissen, das Aufsummieren von Punkten oder die Spielerverwaltung. Ereignisse treten immer dann auf, wenn die Kugel einen Sensor trifft. Dies ist beispielsweise beim Durchlaufen einer Rampe der Fall. Sie sollen Vorschläge für einzelne Aspekte erarbeiten. Für die Programmierung der Spiellogik stehen die dynamischen Datenstrukturen Stack und Queue

---

### 3.1 Erklären Sie die Stack Queue zugrundliegenden Prinzipien (4 Punkte)
Ein Stack funktioniert mit dem LIFO Prinzip (Last in first out) und eine Queue nach dem FIFO Prinzip (First in first out). Das heißt bei einem Stack kann nur auf das letzte hinzugefügte Element zugegriffen werden, dieses wird auch beim löschen zuerst wieder entfernt. Bei einer Queue hingegen kann nur auf das erste Element zugegriffen werden das heißt beim löschen wird das erste Element entfernt

**Punkteverteilung**

| Zusammensetzung | Aufgabe                    | Punkte |
| ---------- | -------------------------- | ------ |
| 3.1.1      | erläutert das LIFO Prinzip | 2      |
| 3.1.2      | erläutert das FIFO Prinzip | 2      |
> Erklaerung:
> Eventuell erklaeren was ein Stack/ Queue ist wenn nicht allen klar ist was es war.
> Sack = Tellerstapel
> Queue = Warteschlange an einer Kasse
---

### Sie erinnern sich, dass zum Aufbau einer einfach verketteten Liste Containerobjekte verwendet werden können, die jeweils neben dem zu speichernden Objekt auch einen Verweis auf das nächste Containerobjekt enthalten.

### 3.2 Geben Sie den Programmcode einer Containerklasse mit den beschriebenen Eigenschaften an. Dabei sollen neben den Attributen ein Konstruktor sowie get- und set-Methoden realisiert werden. (7 Punkte)
```java
public class Knoten {
	//Attribute
	Object item;
	Knoten next;
	// Konstuktor
	public Knoten(Object object) {
		this.object = object;
		this.next = null;
	}
	// get- und set Methoden
	public Object getObject() {
		return this.object;
	}
	public Knoten getNext() {
		return this.next;
	}
	public void setObject(Object object) {
		this.object = object;
	}
	public void setNext(Knoten next) {
		this.next = next;
	}
}
```

| Zusammensetzung | Aufgabe | Punkte |
| --------------- | ------- | ------ |
| 3.2.1           | gibt die beiden Notwendigen Attribute an        | 2       |
| 3.2.2           | gibt den Konstruktor an         | 1       |
| 3.2.3                | programmiert get- und set Methoden        | 4       |
> Erklaerung: 
> Auf die Knotenklasse eingehen, was diese ist, ihre funktionen. 
> Get und set Methoden erklaeren, wie sie funktionieren.
---

### 3.3 Beschreiben Sie, welche Änderungen in der Containerklasse zur Realisierung einer doppelt verketteten Liste vorgenommen werden müssen (4 Punkte).
Für eine doppelt verkette Liste benötigt man eine zusätzliche Variable die auf das Element davor zugreifen kann also:
```java 
Container previos; 
```
Dieses Element müsste man dann noch im Konstruktor initialisieren also der variable previos ein Container geben.  Außerdem braucht man dann für die Variable get- und set Methoden. 

| Zusammensetzung | Aufgabe | Punkte |
| --------------- | ------- | ------ |
| 3.3.1           | erkennt die Notwendigkeit für ein weiteres Datenfeld        | 2        |
| 3.3.2           | erwähnt die Initialisierung im Konstuktor        | 1       |
| 3.3.3                | nennt die get- und set Methoden für das Datenfeld        | 1       |
> Doppelt verkettung erklaeren
---

### Sie entscheiden sich, Ereignisse mithilfe der dynamischen Datenstruktur Queue zu verarbeiten. Die von der Kugel während des Spiels ausgelösten Ereignisse werden von der Klasse $FlipperEvent$ (siehe Anlage 1) für die weitere Verarbeitung zur Verfügung gestellt, Wenn die Kugel ein Ereignis auslöst, wird die Methode $\text{private void ballEvent (FlipperEvent e)}$ der Klasse $Spiellogik$ (siehe Anlage 2) aufgerufen.

### 3.4 Beschreiben Sie die Bestandteile des Methodenkopfes der Methode ballEvent. (5 Punkte)
```java
private void ballEvent(FlipperEvent e) {
//...
}
```
Die Methode ist *private* das heißt die Methode ist nur in der Klasse *Spielelogik* sichtbar. Durch den alias void hat die Methode nichts zum wiedergeben *(return)*. Der name der Methode ist *ballEvent* und erwartet ein Object der Klasse *FlipperEvent* dieser Wert wird unter der Variable *e* gespeichert und kann so in der Methode verwendet werden. 

| Zusammensetzung | Aufgabe | Punkte |
| --------------- | ------- | ------ |
| 3.4.1           | erläutert die Zugriffsmodifikation *private*        | 1       |
| 3.4.2           | beschreibt den Rückgabetyp *void*        | 1       |
| 3.4.3           | nennt den Methodennamen *ballEvent*        | 1       |
| 3.4.4                | beschreibt Name *e* und Typ des Parameters *FlipperEvent*         | 2       |
> Bestandteile eines Methoden kopfes erklaeren
---

### Die Methode $ballEvent$ muss das $e$ nach verschiedenen Kriterien auswerten. Handelt es sich um ein Event mit einer ID von $1 ~ bis ~ 99$, so wird das $FlipperEvent e$ zu der bereits initialisierten Queue $eventQueue$ (siehe Anlage 3) hinzugefügt. Handelt es sich bei dem Event-Typ um einen Schalter („Switch"), so Wird die Methode $switchlight$ aufgerufen. Ist die Sensorgruppennummer $999$, so wird die Methode $baliOut$ aufgerufen. (7 Punkte)

### 3.5 Implementieren Sie die Methode bai Event mit den oben beschriebenen Anforderungen.
```java
private void ballEvent(FlipperEvent e) {
	if(e.getID() >= 1 && e.getID() <= 99) {
		e.enque(e);
	}
	else if(e.getEventType.equals("Switch")) {
		switchLight(e);
	}
	else if(e.getID() == 999) {
		ballOut();
	}
}
```

---
### 3.6 Stellen Sie für alle relevanten Fälle der Methode insert graphisch den Zustand der Liste sowie die Positionen der Zeiger first, last und it jeweils vor und nach dem Aufruf der Methode dar. (10 Punkte)

**Fall 1: leere Liste**
![PDF](PDF/Informatik/Fall1.png)

**Fall 2: nicht leere Liste ohne aktuelles Objekt**
![PDF](PDF/Informatik/Fall2.png)

**Fall 3: Einfuegen vor dem ersten Element**
![PDF](PDF/Informatik/Fall3.png)

**Fall 4: Allgemeiner Fall - es gibt ein aktuelle Element, welches nicht das erste Element ist**
![PDF](PDF/Informatik/Fall4.png)
### 3.7 Implementieren Sie die Methode remove der Klasse List gemäß der Beschreibung in Anlage 4. Sie können alle anderen Methoden der Klasse List und die oben beschriebenen Zeiger first, last und it als gegeben voraussetzen.
```java
public void remove() {
	if(hasAccess()) { 
//Schauen ob Elemente in der Liste sind
		if(first == last) { 
//Schauen ob nur ein Element in der Liste ist
			first = null;
			last = null;
			it = null;
//Wenn nur ein Element vorhanden dann wird alles null da wir es entfernen wollen
		} else {
			if(first == it) { //Loeschen des ersten Elements
				it = first.getNext(); 
				first = it;
//Wenn nun das erste Element auch unser aktuelles Element ist so kann it das nachfolgende Element sein und first ebenso da wir so kein Pointer mehr auf dem vorherigen Element haben und es so geloscht wird
			}
			else {
				Knoten current = first;
//Current auf das erste Element setzen
				while(current.getNext() != it) {
					current = current.getNext();
				}
//Solange durchgehen bis der Nachfolger von current = dem it Element ist. 
				current.setNext(it.getNext());
				it = current.getNext();
//Nun setzen wir von current den Nachfolger auf den Nachfolger von it, it wird dann auf dessen Nachfolger gesetzt wodruch wir keinen Pointer mehr auf dem alten it Element haben.
				if(current.getNext() == null) {
					last = current;
				}
// Dies dient dazu um zu checken ob wir am Ende sind und last somit neu setzen muessen, it waere in diesem fall dann aber null. 
			}
		}
	}
}
```

### Aufgabe 3.8
```java
public class Spiellogik {

    private Queue eventQueue;
    private List eventList;
    private int score;

    private void ballOut() {
        while (!eventQueue.isEmpty()) {
// Diese while dient dazu solange den Prozess zu wiederholen bis die Queue leer ist

            boolean eingefuegt = false;
// Eingefuegt dient als abbruch bedingung nach dem man ein kleineres Element vor einem groesseren eingefuegt hat.

            eventList.toFirst();
// Dient dazu immer wieder bei einem neuem inneren durchlauf von voren zu starten

            FlipperEvent aktQueueEvent = (FlipperEvent) eventQueue.front();
// aktQueueEvent ist immer das erste Element das neu in die List eingefuegt werden soll

            while (eventList.hasAccess() && !eingefuegt) {
// Diese while wiederholt die durch gaenge der Elemente um diese zu vergleichen

                FlipperEvent aktListEvent = (FlipperEvent) eventList.getObject();
// Hier wird immer das aktuelle Element der Liste drin gespeichert

                if (aktListEvent.getSensorGroupNumber() <=  aktQueueEvent.getSensorGroupNumber()) {
                    eventList.next();
// Wenn unser aktuelles Element in der Liste eine kleinere Sensor Nummer hat als das front Element der Queue, wird in der Liste das aktuelle Element einen weiter nach links verschoben, dies dient dazu um alle Elemente, der Liste von der front bis zum Ende zu vergleichen mit dem front Queue Element. Mit next kann man somit am Ende das aktuelle Element vernichten um so eine abbruchbedinung fuer die Schleife zu haben, was dann durch die if das Element der Queue hinten an die Liste anfuegt, dies wird dann immer eine groessere Sensor nummer haben und ist somit sortiert.
                } else {
                    eventList.insert(aktQueueEvent);
                    eventQueue.dequeue();
                    eingefuegt = true;
// Dies dient dem Fall falls man ein kleineres Element zwischen drin einfuegen muss
                }
            }
            if (!eventList.hasAccess()) {
                eventList.append(aktQueueEvent);
                eventQueue.dequeue();
// Dient dazu um das front Element der Queue hinten dran zu haengen und dann das front Queue Element zu entfernen
            }
        }
    }
}
```

| Nummer | Text                                                                                                                  | Punkte  |
| ------ | --------------------------------------------------------------------------------------------------------------------- | ------- |
| 3.8.1  | implementiert eine Schleife über alle Elemente der Queue.                                                             | 2 (II)  |
| 3.8.2  | durchläuft die Liste, um die Einfügestelle zu finden.                                                                 | 3 (III) |
| 3.8.3  | implementiert das Entfernen der Elemente aus der Queue.                                                               | 2 (II)  |
| 3.8.4  | realisiert das Einfügen in die leere Liste, am Anfang und im Inneren der Liste, sowie das Anhängen am Ende der Liste. | 5 (III) |
### Aufgabe 3.9
```java
private void bonusScore() {
	eventList.toFirst();
// Setzen auf das erste Element der Liste
	
	 int bonus = 0;
	 int zaehler = 1;
	 int cmpGroupNumber = 0;
// Noetige variablen zum Berechnen des Scores
	 
	 FlipperEvent aktEvent = (FlipperEvent) eventList.getObject();
// Object damit wir auf die Sensorgruppe Nummer zugreifen koennen

	 cmpGroupNumber = aktEvent.getSensorGroupNumber();
	 eventList.next();
// cmpGroup speichert unsere aktuelle Sensor Gruppe dir wir zaehlen um so pro Einheit durchzaehlen zu koennen. Dadurch das wir das erste Element einer SensorGruppen einheit nutzen, koennen wir beim Nachfolger anfangen da der Zaehler schon auf 1 ist deswegen.next().
	 
	 while (eventList.hasAccess()) {
// While um die Liste durchzugehen um somit die alle Einheiten mitzunehemen fuer die korrekte Berechnung

		 aktEvent = (FlipperEvent) eventList.getObject();
// Speicherung des neuen Elements das man im Verlaufe mit .next() erhaelt um so wieder auf die Sensor Gruppen nummer zuzugreifen

		 if (cmpGroupNumber == aktEvent.getSensorGroupNumber()) {
			 zaehler++;
			 eventList.next();
		 }
// Berechnet den Zaehler pro Sensor Gruppe da wir immer checken ob wir noch in der gleichen SensirGruppe sind mithilfe der Group nummer und wenn das so ist zaehlen wir +1 und verschieben unser it Element eins weiter. Somit durch geht man jede Sensor gruppe

		 else {
			 bonus = bonus + ((zaehler / 10)+1)*1000*zaehler;
			 zaehler = 1;
			 cmpGroupNumber = aktEvent.getSensorGroupNumber();
			 eventList.next();
		 }
// Berechnet mithilfe des Zaehler den Bonus und sorgt dann dafuer das wir zur naechsten Sensor Gruppe gehen. Der Zaehler wird wieder auf 1 gesetzt, weil wir fuer jede Sensorgruppe neu durchzaehlen
	 }
	 
	 bonus += 1000;
	 score += bonus;
}
```

| Nummer | Text                                                                                                   | Punkte |
|--------|--------------------------------------------------------------------------------------------------------|--------|
| 3.9.1  | setzt das aktuelle Element auf den Anfang der Liste und deklariert benötigte Variablen.               | 2(II)  |
| 3.9.2  | berücksichtigt die Behandlung des ersten Elements der Liste.                                           | 3 (II) |
| 3.9.3  | implementiert die Ermittlung der Anzahl der Elemente pro Gruppe.                                       | 5 (III) |
| 3.9.4  | implementiert die Ermittlung des Faktors je nach Anzahl der Elemente pro Gruppe.                      | 3 (III) |
| 3.9.5  | implementiert die Ermittlung der Bonuspunkte und deren Addition zum vorhandenen Score.                 | 3 (II) |
