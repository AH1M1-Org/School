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

public void insert(Object pObj) {
      if(this.isEmpty()) {
         append(pObj);
      }
      else if(this.hasAccess() && pObj != null) {
         Knoten neu = new Knoten(pObj, aktuell);
         if(aktuell == kopf) {
            kopf = neu;
         }
         else {
	         Knoten k = kopf;
	            while(k.getNachfolger() != aktuell) {
                 k = k.getNachfolger();
                }
                k.setNachfolger(neu);
            }
        }
    }
```

```java
public void insertSorted(String s) {
	if(s != null) {
		if(isEmpty()) append(s);
		else {
			toFirst();
			while(hasAccess() && ((String) getObject).compareTo(s) < 0) {
				next();
			} 
			if(hasAccess()) insert(s);
			else append(s);
		}
	}	
}
```