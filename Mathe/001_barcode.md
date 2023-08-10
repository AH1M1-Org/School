# **Operationen mit Modulo**

### Barcodes 
- Barcode 1 ist false
- Barcode 2 ist true

### Beispeiele
- Barcode: 6554566789128 -> false
- Barcode: 1524566789128 -> true

## *Code*
```java
public class Main {
    public static void main(String[] args) {
        String barcode = "7564566789128"; //Sollte true sein
        char[] numbers = barcode.toCharArray();

        int sum = value(numbers);
        System.out.println("Der gegebene Barcode ist: " + check(sum) + " " + sum);
    }

    public static int value(char[] numbers) {
        int sum = 0;

        for (int i = 0; i <= 12; i++) {
            int temp = Integer.parseInt(String.valueOf(numbers[i]));
            if(i % 2 == 0) {
                sum += temp;
            } else {
                sum += 3*temp;
            }
        }

        return sum;
    }

    public static boolean check(int sum) {
        return sum % 10 == 0;
    }
}
```