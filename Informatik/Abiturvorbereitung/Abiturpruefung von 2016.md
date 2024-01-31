---
tags:
  - Informatik
---
*Marvin Baeumer* **2024-01-31 11:00**

---
### Aufgabe
```java
public void next() {
	if(list.hasAccess() && it != last) {
		it = it.getNaechster();
	} 
} 

public void insert(Object content) {
	if(list.isEmpty()) {
		list.append(content);
	} else if(first == it) {
		Knoten content = new Knoten(content, first.getNachfolger());
		first = content;
		it = content.getNachfolger;		
	} else if() {

	}
	if(list.hasAccess()) {
		while()
			Knoten newContent = new Knoten(content, it.getNachfolger);
			it = it.getNachfolger();
	}

}
```