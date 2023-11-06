---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-11-03 08:19**

---
### Aufgabe 3.2 - Bestimmen Sie die Verschlüsselung des Wortes IMPFUNG unter Anwendung des Atbasch Verfahrens.
RNKUMT
### Aufgabe 3.3 - Implementieren Sie eine Methode encrypt, welche den als Parameter übergebenen Text mit Atbasch verschlüsselt und zurückgibt. Gehen Sie davon aus, dass der übergebene Text lediglich aus Großbuchstaben besteht.
```java
public class Main {
    public static void main(String[] Args) {
        String plaintext = "ABC";
        String encryptedText = encryption(plaintext); 
          
        System.out.println(plaintext); 
        System.out.println(encryptedText);
    }
    
    public static String encryption(String text) {
        char[] chars = new char[text.length()];
        
        for (int i = 0; i < text.length(); i++) {
            int ascii = 25 - (text.charAt(i) - 65);
            chars[i] = (char)(ascii + 65);
        }
        
        return new String(chars);
    }
}
```
