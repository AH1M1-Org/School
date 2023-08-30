# RSA verfahren
**Situation:** RSA-Verfahren soll implementiert werden.

**Information:** Beschreibung des Algorithmus

Algorithmus benötigt:
- Primzahlen
- ggT 
- mod
- ggT berechnen 
- erweiterter    
- öffenlicher und privater Schlüssel
- $\varphi (n) $

### Beispiel
$p = 11 ~ q = 17$\
$n = p \cdot q = 11 \cdot 17 = 187$\
$(p - 1) \cdot (q - 1) = (11 - 1) \cdot (23 - 1) = 160$\
$\Rightarrow$ Verschlüsselungsexponent 
 muss zwischen 1 und 160 liegen und darf keinen nicht trivialen gemeinsamen Teiler haben. $1 < e < 160$

### Primfaktorzerlegung von 214 
> alle Primzahlen die zusammen 214 ergeben

$214 = 2 \cdot 107 $

### Primfaktorzerlegung von 320 
> alle Primzahlen die zusammen 320 ergeben

$320 = 2 \cdot 160 = 2 \cdot 2 \cdot 80 = 2 \cdot 2 \cdot 2 \cdot 40 = 2 \cdot 2 \cdot 2 \cdot 2 \cdot 20 = 2 \cdot 2 \cdot 2 \cdot 2 \cdot 2 \cdot 10 = 2^6 \cdot 5$\
$ggT(214,320) = 2$\
Teilfremde Zahl zu 320 gesucht: Welche Primzahlfactoren dürfen in dieser Zahl icht vorkommen? 2, 5

Als Verschluesselungsexponente $e$ wird $7$ gewaehlt.

### Vorgehen privater Schluessel
Bedingung: $7 \cdot d \equiv 1 \mod 160$\
$\Leftrightarrow d = 23$\
Privater Schluessel $(p, q, d) = (11, 17, 23)$

### Verschluesseln
$d^e \mod p \cdot q \\ 13^7 \mod 187 = 106$

$(d^e \mod p)^d \\ 106^23 \mod 187 = 13$

$(m^e \mod n)^d \mod n = m$

```java
public class Main {
  public static void main(String[] args) {
      int p = 11, q = 17; 
      int phi = (p - 1) * (q - 1);
      int n = p * q;
      int e = eGenerator(phi);

      int d = privateKey(e, phi);

      int message = 186; //message muss kleiner als n sein
      int em = encrypt(message, e, n);
      System.out.println("encrypted: " + em);
      int dm = decrypt(em, d, n);
      System.out.println("Decrypted: " + dm);
  }

  public static int decrypt(int encrypted, int d, int n) {
      int decrypted = 1;
      for (int i = 0; i < d; i++) {
          decrypted = (decrypted * encrypted) % n;
      }
      return decrypted;
  }

  public static int encrypt(int message, int e, int n) {
      int encrypted = 1;
      for (int i = 0; i < e; i++) {
          encrypted = (encrypted * message) % n;
      }
      return encrypted;
  }

  public static int privateKey(int e, int phi) {
      int d = 0;
      while (true) {
          if ((e * d) % phi == 1) break;
          d++;
      }
      return d;
  }

  public static int gcd(int a, int b) {
      if (b == 0) return a;
      return gcd(b, a % b);
  }

  public static int eGenerator(int phi) {
      int e = 2;
      while (e < phi) {
          if (gcd(e, phi) == 1) break;
          e++;
      }
      return e;
  }
}
```

# Berechnung von Privat und Fremdschlüssel
Erzeuge den öffentlichen und den privaten RSA-Schliisscl mit $p = 7, q = 13$ und $e = 11$.

$n = p \cdot q$\
$\varphi(n) = (p - 1)(q - 1)$

$n = 7 \cdot 13 = 91$\
$\varphi(n) = (7 - 1)(13 - 1) = 72$

1. Euklidischer Algorithmus 
2. Umstellen
3. Erweiterter Euklidischer Algorithmus
4. Berechnung mit kongruenz
5. Bestimmen des öffentlichen & privatem schlüssels