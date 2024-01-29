---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-12-06 10:20**

---
### Stack
>   Ein Stack ist eine Datenstruktur, die nach dem Prinzip "Last-In-First-Out" (LIFO) funktioniert. Das zuletzt hinzugefügte Element wird als erstes entfernt.
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at (-1,0.5) {push()};

\draw[line width=1.5pt, fill=white, draw=lime] (0,0) rectangle (1,1);
\node at (0.5,0.5) {0};

\draw[line width=1.5pt, fill=white, draw=lime] (2,0) rectangle (3,1);
\node at (2.5,0.5) {0};
\draw[line width=1.5pt, fill=white] (2,2) rectangle (3,3);
\node at (2.5,2.5) {1};

\draw[line width=1.5pt, fill=white, draw=lime] (4,0) rectangle (5,1);
\node at (4.5,0.5) {0};
\draw[line width=1.5pt, fill=white] (4,2) rectangle (5,3);
\node at (4.5,2.5) {1};
\draw[line width=1.5pt, fill=white] (4,4) rectangle (5,5);
\node at (4.5,4.5) {2};

\draw[line width=1.5pt, fill=white, draw=lime] (6,0) rectangle (7,1);
\node at (6.5,0.5) {0};
\draw[line width=1.5pt, fill=white] (6,2) rectangle (7,3);
\node at (6.5,2.5) {1};
\draw[line width=1.5pt, fill=white] (6,4) rectangle (7,5);
\node at (6.5,4.5) {2};
\draw[line width=1.5pt, fill=white] (6,6) rectangle (7,7);
\node at (6.5,6.5) {3};

\draw[line width=2pt] (-1,-0.5) rectangle (8,-0.5);
\node at (-1,-1) {pop()};

\draw[line width=1.5pt, fill=white] (0,-1) rectangle (1,-2);
\node at (0.5,-1.5) {3};
\draw[line width=1.5pt, fill=white] (0,-3) rectangle (1,-4);
\node at (0.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (0,-5) rectangle (1,-6);
\node at (0.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, draw=lime] (0,-7) rectangle (1,-8);
\node at (0.5,-7.5) {0};

\draw[line width=1.5pt, fill=white] (2,-3) rectangle (3,-4);
\node at (2.5,-3.5) {2};
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6);
\node at (2.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, draw=lime] (2,-7) rectangle (3,-8);
\node at (2.5,-7.5) {0};

\draw[line width=1.5pt, fill=white] (4,-5) rectangle (5,-6);
\node at (4.5,-5.5) {1};
\draw[line width=1.5pt, fill=white, draw=lime] (4,-7) rectangle (5,-8);
\node at (4.5,-7.5) {0};

\draw[line width=1.5pt, fill=white, draw=lime] (6,-7) rectangle (7,-8);
\node at (6.5,-7.5) {0};

\draw[dotted, line width=2pt, fill=white] (-0.5, 0) rectangle (-0.5,7);
\draw[dotted, line width=2pt, fill=white] (1.5, 0) rectangle (1.5,7);
\draw[dotted, line width=2pt, fill=white] (3.5, 0) rectangle (3.5,7);
\draw[dotted, line width=2pt, fill=white] (5.5, 0) rectangle (5.5,7);
\draw[dotted, line width=2pt, fill=white] (7.5, 0) rectangle (7.5,7);

\draw[dotted, line width=2pt, fill=white] (-0.5, -1) rectangle (-0.5,-8);
\draw[dotted, line width=2pt, fill=white] (1.5, -1) rectangle (1.5,-8);
\draw[dotted, line width=2pt, fill=white] (3.5, -1) rectangle (3.5,-8);
\draw[dotted, line width=2pt, fill=white] (5.5, -1) rectangle (5.5,-8);
\draw[dotted, line width=2pt, fill=white] (7.5, -1) rectangle (7.5,-8);

\end{tikzpicture} 
\end{document} 
```

<div style="page-break-after: always;"></div>

### Queue
>   Eine Queue ist eine Datenstruktur, die Elemente nach dem Prinzip "First-In-First-Out" (FIFO) verwaltet. Das bedeutet, dass das zuerst eingefügte Element auch als erstes wieder entfernt wird.
```tikz 
\begin{document} 
\begin{tikzpicture}

\node at (-1,0) {enqueue()};

\draw[line width=1.5pt, fill=white, draw=lime] (0,0) rectangle (1,1); 
\node at (0.5,0.5) {0}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,2) rectangle (1,3); 
\node at (0.5,2.5) {0}; 
\draw[line width=1.5pt, fill=white] (2,2) rectangle (3,3); 
\node at (2.5,2.5) {1}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,4) rectangle (1,5); 
\node at (0.5,4.5) {0}; 
\draw[line width=1.5pt, fill=white] (2,4) rectangle (3,5); 
\node at (2.5,4.5) {1}; 
\draw[line width=1.5pt, fill=white] (4,4) rectangle (5,5); 
\node at (4.5,4.5) {2}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,6) rectangle (1,7); 
\node at (0.5,6.5) {0}; 
\draw[line width=1.5pt, fill=white] (2,6) rectangle (3,7); 
\node at (2.5,6.5) {1}; 
\draw[line width=1.5pt, fill=white] (4,6) rectangle (5,7); 
\node at (4.5,6.5) {2}; 
\draw[line width=1.5pt, fill=white] (6,6) rectangle (7,7); 
\node at (6.5,6.5) {3}; 

\draw[line width=2pt] (-1,-0.5) rectangle (8,-0.5);

\node at (-1,-1) {dequeue()};


\draw[line width=1.5pt, fill=white, draw=lime] (0,-1) rectangle (1,-2); 
\node at (0.5,-1.5) {0}; 
\draw[line width=1.5pt, fill=white] (2,-1) rectangle (3,-2); 
\node at (2.5,-1.5) {1}; 
\draw[line width=1.5pt, fill=white] (4,-1) rectangle (5,-2); 
\node at (4.5,-1.5) {2}; 
\draw[line width=1.5pt, fill=white] (6,-1) rectangle (7,-2); 
\node at (6.5,-1.5) {3}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,-3) rectangle (1,-4); 
\node at (0.5,-3.5) {1}; 
\draw[line width=1.5pt, fill=white] (2,-3) rectangle (3,-4); 
\node at (2.5,-3.5) {2}; 
\draw[line width=1.5pt, fill=white] (4,-3) rectangle (5,-4); 
\node at (4.5,-3.5) {3}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,-5) rectangle (1,-6); 
\node at (0.5,-5.5) {2}; 
\draw[line width=1.5pt, fill=white] (2,-5) rectangle (3,-6); 
\node at (2.5,-5.5) {3}; 

\draw[line width=1.5pt, fill=white, draw=lime] (0,-7) rectangle (1,-8); 
\node at (0.5,-7.5) {3}; 

\draw[dotted, line width=1.5pt, fill=white] (-1, 1.5) rectangle (8,1.5);
\draw[dotted, line width=1.5pt, fill=white] (-1, 3.5) rectangle (8,3.5);
\draw[dotted, line width=1.5pt, fill=white] (-1, 5.5) rectangle (8,5.5);
\draw[dotted, line width=1.5pt, fill=white] (-1, -2.5) rectangle (8,-2.5);
\draw[dotted, line width=1.5pt, fill=white] (-1, -4.5) rectangle (8,-4.5);
\draw[dotted, line width=1.5pt, fill=white] (-1, -6.5) rectangle (8,-6.5);

\end{tikzpicture} 
\end{document} 
``` 

<div style="page-break-after: always;"></div>

### List
#### Beschreibung einer List
> Eine Liste ermöglicht den direkten Zugriff auf jedes Element und unterscheidet sich daher von einer Queue, bei der der Zugriff in der Regel auf das vorderste Element beschränkt ist. In einer Liste können Elemente an beliebigen Positionen eingefügt oder entfernt werden, was durch die Verwendung von Pointern wie "First", "Last" und "It" ermöglicht wird. Eine Liste kann entweder einfach verkettet sein, wobei jeder Knoten den nächsten Knoten speichert, oder doppelt verkettet, wobei jeder Knoten sowohl den nächsten als auch den vorherigen Knoten speichert.
#### Knoten Klasse
> Die Knotenklasse repräsentiert einen einzelnen Knoten in einer verketteten Datenstruktur. Jeder Knoten enthält eine Datenkomponente und einen Verweis auf den nächsten Knoten in der Kette. Diese Klasse wird häufig verwendet, um verkettete Listen zu implementieren.
#### Visualisierung von Knoten als List
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at(-1,0.5) {einfach verkettet};

\draw[line width=1.5pt, fill=white] (0,4) rectangle (1,5); 
\node at (0.5,4.5) {K}; 
\draw[line width=1.5pt, fill=white] (2,4) rectangle (3,5); 
\node at (2.5,4.5) {K}; 
\draw[line width=1.5pt, fill=white] (4,4) rectangle (5,5); 
\node at (4.5,4.5) {K}; 
\draw[line width=1.5pt, fill=white] (6,4) rectangle (7,5); 
\node at (6.5,4.5) {K}; 
\draw[line width=1.5pt, fill=white] (8,4) rectangle (9,5); 
\node at (8.5,4.5) {null}; 

\draw[line width=1.5pt, ->, fill=white] (1,4.5) -- (2,4.5);
\draw[line width=1.5pt, ->, fill=white] (3,4.5) -- (4,4.5);
\draw[line width=1.5pt, ->, fill=white] (5,4.5) -- (6,4.5);
\draw[line width=1.5pt, ->, fill=white] (7,4.5) -- (8,4.5);

\draw[line width=1.5pt, ->, fill=white] (0.5,4) -- (0.5,3);
\draw[line width=1.5pt, ->, fill=white] (2.5,4) -- (2.5,3);
\draw[line width=1.5pt, ->, fill=white] (4.5,4) -- (4.5,3);
\draw[line width=1.5pt, ->, fill=white] (6.5,4) -- (6.5,3);

\draw[line width=1.5pt, fill=white] (0,2) rectangle (1,3); 
\node at (0.5,2.5) {O}; 
\draw[line width=1.5pt, fill=white] (2,2) rectangle (3,3); 
\node at (2.5,2.5) {O}; 
\draw[line width=1.5pt, fill=white] (4,2) rectangle (5,3); 
\node at (4.5,2.5) {O}; 
\draw[line width=1.5pt, fill=white] (6,2) rectangle (7,3); 
\node at (6.5,2.5) {O}; 

\draw[line width=1.5pt, ->, fill=white] (0.5,5.5) -- (0.5,5);
\draw[line width=1.5pt, ->, fill=white] (6.5,5.5) -- (6.5,5);
\draw[line width=1.5pt, ->, fill=white] (8.5,5.5) -- (8.5,5);
\node at(0.5,6) {First};
\node at(6.5,6) {Last};
\node at(8.5,6) {It};

\end{tikzpicture} 
\end{document} 
``` 
> In einer Liste zeigt der Zeiger "First" immer auf das erste Element, während der Zeiger "Last" auf das letzte Element verweist. Der Zeiger "It" kann den Wert "null" haben und muss manuell einem Element zugewiesen werden. Mit Hilfe dieses Zeigers greift man auf einzelne Knoten und ihre Objekte zu, was Operationen wie das Einfügen, Löschen usw. ermöglicht.

<div style="page-break-after: always;"></div>

#### Implementierung
```java
public class Container {
	//Attribute
	Object item;
	Container next;
	// Konstuktor
	public Container(Object object) {
		this.object = object;
		this.next = null;
	}
	// get- und set Methoden
	public Object getObject() {
		return this.object;
	}
	public Container getNext() {
		return this.next;
	}
	public void setObject(Object object) {
		this.object = object;
	}
	public void setNext(Container next) {
		this.next = next;
	}
}
```

<div style="page-break-after: always;"></div>

### Documentation Queue
| Art | Beschreibung |
| ---- | ---- |
| Konstruktor | Queue() - eine leere Queue wird erzeugt |
| Anfrage | boolean isEmpty() - Die Anfrage liefert den Wert true, wenn die Schlange keine Objekte enthält, sonst liefert sie den Wert false. |
| Auftrag | void enqueue(Object item) - Das Objekt item wird an die Schlange angehängt. Falls item gleich null ist, bleibt die Schlange unverändert. |
| Auftrag | void dequeue() - Das erste Objekt wird aus der Schlange entfernt. Falls die Schlange leer ist, wird sie nicht verändert. |
| Anfrage | Object front() Die Anfrage liefert das erste Objekt der Schlange. Die Schlange bleibt unverändert. Falls die Schlange leer ist, wird null zurückgegeben. |

<div style="page-break-after: always;"></div>

### Documentation List
| Art | Beschreibung |
| ---- | ---- |
| Konstruktor | List() Eine leere Liste wird erzeugt. |
| Anfrage | boolean isEmpty() Die Anfrage liefert den Wert true, wenn die Liste keine Objekte enthält, sonst liefert sie den Wert false. |
| Anfrage | boolean hasAccess() Die Anfrage liefert den Wert true, wenn es ein aktuelles Objekt gibt, sonst liefert sie den Wert false. |
| Auftrag | void next() Falls die Liste nicht leer ist, es ein aktuelles Objekt gibt und dieses nicht das letzte Objekt der Liste ist, wird das dem aktuellen Objekt in der Liste folgende Objekt zum aktuellen Objekt, andernfalls gibt es nach Ausführung des Auftrags kein aktuelles Objekt. |
| Auftrag | void toFirst() Falls die Liste nicht leer ist, wird das erste Objekt der Liste aktuelles Objekt. Ist die Liste leer, geschieht nichts. |
| Auftrag | void toLast() Falls die Liste nicht leer ist, wird das letzte Objekt der Liste aktuelles Objekt. Ist die Liste leer, geschieht nichts. |
| Anfrage | Object getObject() Falls es ein aktuelles Objekt gibt, wird das aktuelle Objekt zurückgegeben, andernfalls gibt die Anfrage den Wert null zurück. |
| Auftrag | void setObject(Object pObject) Falls es ein aktuelles Objekt gibt und pObject ungleich null ist, wird das aktuelle Objekt durch pObject ersetzt. |
| Auftrag | void append(Object pObject) Ein neues Objekt pObject wird am Ende der Liste angefügt. Das aktuelle Objekt bleibt unverändert. Wenn die Liste leer ist, wird das Objekt pObject in die Liste eingefügt und es gibt weiterhin kein aktuelles Objekt. Falls pObject gleich null ist, bleibt die Liste unverändert. |
| Auftrag | void insert(Object pObject) Falls es ein aktuelles Objekt gibt, wird ein neues Objekt vor dem aktuellen Objekt in die Liste eingefügt. Das aktuelle Objekt bleibt unverändert. Falls die Liste leer ist und es somit kein aktuelles Objekt gibt, wird pObject in die Liste eingefügt und es gibt weiterhin kein aktuelles Objekt. Falls es kein aktuelles Objekt gibt und die Liste nicht leer ist oder pObject gleich null ist, bleibt die Liste unverändert. |
| Auftrag | void concat(List pList) Die Liste pList wird an die Liste angehängt. Das aktuelle Objekt bleibt unverändert. Falls pList null oder eine leere Liste ist, bleibt die Liste unverändert. |
| Auftrag | void remove() Falls es ein aktuelles Objekt gibt, wird das aktuelle Objekt gelöscht und das Objekt hinter dem gelöschten Objekt wird zum aktuellen Objekt. Wird das Objekt, das am Ende der Liste steht, gelöscht, gibt es kein aktuelles Objekt mehr. Wenn die Liste leer ist oder es kein aktuelles Objekt gibt, bleibt die Liste unverändert. |

<div style="page-break-after: always;"></div>

#### Relevante Faelle der Methode Insert - Graphische Darstellung
##### Fall 1 $\rightarrow$ leere Liste
> Bei einer leeren Liste zeigen die Zeiger `first`, `last` und `it` auf `null`. Beim Aufrufen der Methode `insert` wird nun ein Element eingefügt, wobei `it` weiterhin `null` bleibt und `first` und `last` auf das einzige Element $(0)$ in der Liste zeigen.
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at(0,3) {Zustand vor dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (-0.5,2) -- (0,1.25);
\draw[line width=1.5pt, fill=white, ->] (1,2) -- (1,1.25);
\draw[line width=1.5pt, fill=white, ->] (2.5,2) -- (2,1.25);

\node at(-0.5,2.25) {first};
\node at(1,2.25) {last};
\node at(2.5, 2.25) {it};

\draw[line width=1.5pt, fill=white] (0,0) rectangle (2,1); 
\node at (1,0.5) {null}; 

\draw[dotted, line width=2pt, fill=white] (-0.5,-1) -- (6,-1);
\node at(0,-1.5) {Zustand nach dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (-0.5,-2.25) -- (0,-3);
\draw[line width=1.5pt, fill=white, ->] (1,-2.25) -- (1,-3);
\draw[line width=1.5pt, fill=white, ->] (3.5,-2.25) -- (3.5,-3);

\node at(-0.5,-2) {first};
\node at(1,-2) {last};
\node at(3.5, -2) {it};

\draw[line width=1.5pt, fill=white] (0,-3.25) rectangle (2,-4.25); 
\node at (1,-3.75) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,-3.75) -- (2.5,-3.75);
\draw[line width=1.5pt, fill=white] (2.5,-3.25) rectangle (4.5,-4.25); 
\node at (3.5,-3.75) {null}; 

\end{tikzpicture} 
\end{document} 
```
##### Fall 2 $\rightarrow$ nicht leere Liste ohne aktuelles Object
> Wenn die `Insert`-Methode aufgerufen wird und es kein aktuelles Element in der Liste gibt, die Liste nicht leer ist, bleibt die Liste unverändert.
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at(0,3) {Zustand vor dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (6,2) -- (6,1.25);
\draw[line width=1.5pt, fill=white, ->] (1,2) -- (1,1.25);
\draw[line width=1.5pt, fill=white, ->] (3.5,2) -- (3.5,1.25);

\node at(1,2.25) {first};
\node at(3.5,2.25) {last};
\node at(6,2.25) {it};

\draw[line width=1.5pt, fill=white] (0,0) rectangle (2,1); 
\node at (1,0.5) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,0.5) -- (2.5,0.5);
\draw[line width=1.5pt, fill=white] (2.5,0) rectangle (4.5,1); 
\node at (3.5,0.5) {1}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,0.5) -- (5,0.5);
\draw[line width=1.5pt, fill=white] (5,0) rectangle (7,1); 
\node at (6,0.5) {null}; 

\draw[dotted, line width=2pt, fill=white] (-0.5,-1) -- (7.5,-1);

\node at(0,-1.5) {Zustand nach dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (6,-2.25) -- (6,-3);
\draw[line width=1.5pt, fill=white, ->] (1,-2.25) -- (1,-3);
\draw[line width=1.5pt, fill=white, ->] (3.5,-2.25) -- (3.5,-3);

\node at(1,-2) {first};
\node at(3.5, -2) {last};
\node at(6,-2) {it};

\draw[line width=1.5pt, fill=white] (0,-3.25) rectangle (2,-4.25); 
\node at (1,-3.75) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,-3.75) -- (2.5,-3.75);
\draw[line width=1.5pt, fill=white] (2.5,-3.25) rectangle (4.5,-4.25); 
\node at (3.5,-3.75) {1}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,-3.75) -- (5,-3.75);
\draw[line width=1.5pt, fill=white] (5,-3.25) rectangle (7,-4.25); 
\node at (6,-3.75) {null}; 

\end{tikzpicture} 
\end{document} 
```

<div style="page-break-after: always;"></div>

##### Fall 3 $\rightarrow$ Einfügen vor dem ersten Element
> Das aktuelle Element `it` muss dasselbe Element wie `first` sein. Danach wird die Methode `insert` aufgerufen. Das neue Element $(3)$ wird dann eingefügt, wobei `first` auf das neue Element $(3)$ zeigt und `it` auf dasselbe Element $(0)$ zeigt, nur eine Position weiter hinten.
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at(0,3) {Zustand vor dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (6,2) -- (6,1.25);
\draw[line width=1.5pt, fill=white, ->] (0.5,2) -- (0.5,1.25);
\draw[line width=1.5pt, fill=white, ->] (1.5,2) -- (1.5,1.25);

\node at(0.5,2.25) {first};
\node at(1.5,2.25) {it};
\node at(6,2.25) {last};

\draw[line width=1.5pt, fill=white] (0,0) rectangle (2,1); 
\node at (1,0.5) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,0.5) -- (2.5,0.5);
\draw[line width=1.5pt, fill=white] (2.5,0) rectangle (4.5,1); 
\node at (3.5,0.5) {1}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,0.5) -- (5,0.5);
\draw[line width=1.5pt, fill=white] (5,0) rectangle (7,1); 
\node at (6,0.5) {2}; 
\draw[line width=1.5pt, fill=white, ->] (7,0.5) -- (7.5,0.5);
\draw[line width=1.5pt, fill=white] (7.5,0) rectangle (9.5,1); 
\node at (8.5,0.5) {null}; 

\draw[dotted, line width=2pt, fill=white] (-0.5,-1) -- (12.5,-1);

\node at(0,-1.5) {Zustand nach dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (8.5,-2.25) -- (8.5,-3);
\draw[line width=1.5pt, fill=white, ->] (1,-2.25) -- (1,-3);
\draw[line width=1.5pt, fill=white, ->] (3.5,-2.25) -- (3.5,-3);

\node at(1,-2) {first};
\node at(8.5, -2) {last};
\node at(3.5,-2) {it};

\draw[line width=1.5pt, fill=white] (0,-3.25) rectangle (2,-4.25); 
\node at (1,-3.75) {3}; 
\draw[line width=1.5pt, fill=white, ->] (2,-3.75) -- (2.5,-3.75);
\draw[line width=1.5pt, fill=white] (2.5,-3.25) rectangle (4.5,-4.25); 
\node at (3.5,-3.75) {0}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,-3.75) -- (5,-3.75);
\draw[line width=1.5pt, fill=white] (5,-3.25) rectangle (7,-4.25); 
\node at (6,-3.75) {1}; 
\draw[line width=1.5pt, fill=white, ->] (7,-3.75) -- (7.5,-3.75);
\draw[line width=1.5pt, fill=white] (7.5,-3.25) rectangle (9.5,-4.25); 
\node at (8.5,-3.75) {2};
\draw[line width=1.5pt, fill=white, ->] (9.5,-3.75) -- (10,-3.75);
\draw[line width=1.5pt, fill=white] (10,-3.25) rectangle (12,-4.25); 
\node at (11,-3.75) {null};

\end{tikzpicture} 
\end{document} 
```
##### Fall 4 $\rightarrow$ Allgemeiner Fall – es gibt ein aktuelles Element, welches nicht das erste Element ist.
> Bei diesem Fall gibt es ein aktuelles Element, und die Liste ist nicht leer. Wenn nun die Methode `Insert` aufgerufen wird, wird das neue Element $(3)$ vor dem aktuellen Element eingefügt. Das aktuelle Element bleibt dabei unverändert, also weiterhin die
```tikz 
\begin{document} 
\begin{tikzpicture} 

\node at(0,3) {Zustand vor dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (6,2) -- (6,1.25);
\draw[line width=1.5pt, fill=white, ->] (1,2) -- (1,1.25);
\draw[line width=1.5pt, fill=white, ->] (3.5,2) -- (3.5,1.25);

\node at(1,2.25) {first};
\node at(3.5,2.25) {it};
\node at(6,2.25) {last};

\draw[line width=1.5pt, fill=white] (0,0) rectangle (2,1); 
\node at (1,0.5) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,0.5) -- (2.5,0.5);
\draw[line width=1.5pt, fill=white] (2.5,0) rectangle (4.5,1); 
\node at (3.5,0.5) {1}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,0.5) -- (5,0.5);
\draw[line width=1.5pt, fill=white] (5,0) rectangle (7,1); 
\node at (6,0.5) {2}; 
\draw[line width=1.5pt, fill=white, ->] (7,0.5) -- (7.5,0.5);
\draw[line width=1.5pt, fill=white] (7.5,0) rectangle (9.5,1); 
\node at (8.5,0.5) {null}; 

\draw[dotted, line width=2pt, fill=white] (-0.5,-1) -- (12.5,-1);

\node at(0,-1.5) {Zustand nach dem Aufruf der Methode Insert};

\draw[line width=1.5pt, fill=white, ->] (8.5,-2.25) -- (8.5,-3);
\draw[line width=1.5pt, fill=white, ->] (1,-2.25) -- (1,-3);
\draw[line width=1.5pt, fill=white, ->] (6,-2.25) -- (6,-3);

\node at(1,-2) {first};
\node at(8.5, -2) {last};
\node at(6,-2) {it};

\draw[line width=1.5pt, fill=white] (0,-3.25) rectangle (2,-4.25); 
\node at (1,-3.75) {0}; 
\draw[line width=1.5pt, fill=white, ->] (2,-3.75) -- (2.5,-3.75);
\draw[line width=1.5pt, fill=white] (2.5,-3.25) rectangle (4.5,-4.25); 
\node at (3.5,-3.75) {3}; 
\draw[line width=1.5pt, fill=white, ->] (4.5,-3.75) -- (5,-3.75);
\draw[line width=1.5pt, fill=white] (5,-3.25) rectangle (7,-4.25); 
\node at (6,-3.75) {1}; 
\draw[line width=1.5pt, fill=white, ->] (7,-3.75) -- (7.5,-3.75);
\draw[line width=1.5pt, fill=white] (7.5,-3.25) rectangle (9.5,-4.25); 
\node at (8.5,-3.75) {2};
\draw[line width=1.5pt, fill=white, ->] (9.5,-3.75) -- (10,-3.75);
\draw[line width=1.5pt, fill=white] (10,-3.25) rectangle (12,-4.25); 
\node at (11,-3.75) {null};

\end{tikzpicture} 
\end{document} 
```

<div style="page-break-after: always;"></div>

### Implementierung der Methode `remove` und `insert`
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
			if(first = it) { //Loeschen des ersten Elements
				it = first.getNext(); 
				first = it;
//Wenn nun das erste Element auch unser aktuelles Element ist so kann it das nachfolgende Element sein und first ebenso da wir so kein Pointer mehr auf dem vorherigen Element haben und es so geloscht wird
			}
			else {
				Container current = first;
				while(current != it) {
					current = current.getNext();
				}
				current.setNext(it.getNext)
				it = current.getNext();
//Solnage durchgehen bis wir it erreichthaben
				if(current.getNext() == null) {
					last = current;
				}
			}
		}
	}
}
```

<div style="page-break-after: always;"></div>

#### void insert(Object item)
```java
public void insert(Object item) {
        if(this.isEmpty()) {
            append(item);
        }
        else if(this.hasAccess() && item != null) {
            Knoten neu = new Knoten(item, aktuell);
            if(aktuell == kopf) {
                kopf = neu;
            }
            else {
                Knoten front = kopf;
                while(front.getNachfolger() != aktuell) {
                    front = front.getNachfolger();
                }
                front.setNachfolger(neu);
            }
        }
    }
```