# Caesar Verfahren

```java
public class Main {
    public static void main(String[] args) {
        String plaintext = "Hallo";
        int key = 3;

        String encryptText = encryptAndDecrypt(plaintext, key, '+');
        String decryptText = encryptAndDecrypt(encryptText, key, '-');

        System.out.println(plaintext.toLowerCase());
        System.out.println(encryptText.toUpperCase());
        System.out.println(decryptText);
    }

    public static String encryptAndDecrypt(String text, int key, char operator) {
        text = text.toLowerCase();
        char[] encryptText = new char[text.length()];

        for (int i = 0; i < text.length(); i++) {
            int hex;
            if (operator == '+') hex = ((text.charAt(i) + key) - 96) % 26;
            else hex = ((text.charAt(i) - key) - 96) % 26;
            if (hex == 0) hex = 26;
            encryptText[i] = (char) (hex + 96);
        }
        return new String(encryptText);
    }
}
```