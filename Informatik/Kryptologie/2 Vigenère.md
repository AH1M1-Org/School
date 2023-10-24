### a.1)
Schluesselwort: HUND
Klartext: Das ist einfach
Verschluesselung: Kuf 

### a.2)
Schluesselwort: Hund
Klartext: Juhu ich kanns
Verschluesselung: 

### b)
Schluesselwort: ROT
Klartext: Jetzt klappt es besser.  
Verschluesselung: Asmph bztgmd sl pxjgxi


```java
public class Main {  
	public static void main(String[] args) {  
		String plaintext = "HelloWorld";  
		String key = "ROT";  
  
		String encryptionText = encryption(plaintext, key, '+');  
		String decryptionText = encryption(encryptionText, key, '-');  
  
		System.out.println("Plaintext " + plaintext);  
		System.out.println("Encryption " + encryptionText);  
		System.out.println("Decryption " + decryptionText);  
	}  
  
	public static String encryption(String text, String key, char operation) {  
		text = text.toLowerCase();  
		key = key.toLowerCase();  
		int pointer = 0;  
		// Creating a pointer to get the current letter of the key.  
  
		char[] encryptionText = new char[text.length()];  
  
		for (int i = 0; i < text.length(); i++) {  
			int ascii;  
  
		if (operation == '+') {  
			ascii = ((text.charAt(i) - 97) + (key.charAt(pointer) - 97)) % 26;  
			if (ascii == 0) ascii = 26;  
		
			// When we have 26 % 26, we have a remainder of 0, but we only need the 26 since this is a 'z'.  
		} 
	 
		else {  
			ascii = ((text.charAt(i) - 97) - (key.charAt(pointer) - 97)) % 26;  
			if (ascii < 0) ascii += 26;  
			/*  
			* Apparently, this doesn't happen automatically.  
			* If the result is negative after the modulo operation,  
			* the modulo is not added, hence this 'if'  
			*/  
		}  
  
			pointer++;  
			if (pointer == key.length()) pointer = 0; 
			// To prevent the pointer from pointing outside the keys.  
			encryptionText[i] = (char) ((ascii + 97)); 
			// Adds the correct ASCII value as a character to the array.  
		}  
		return new String(encryptionText);  
	}  
}
```
