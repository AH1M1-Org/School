```java
public class Main {
    public static void main(String[] args) {
        String encryptionText = "GLHUXQGIXQNJHEXHKUHQVROOHQCXP4DSULO5338XP;9FHQWPRQDWOLFKVWHLJH\n" +
                "QHUVWPDOVIROJHQGLHODHQGHUQLFKWGHUXQDEKDHQJLJHQJHEXHKUHQNRPPLVV\n" +
                "LRQGLHHLQHHUKRHKXQJVFKRQCXMDKUHVEHJLQQYRUVFKODHJWGLHFKHIVYRQDU\n" +
                "GXQGCGIVLQGDHXVVHUVWXQCXIULHGHQ0XQGEHKDOWHQVLFKHLQHYHUIDVVXQJV\n" +
                "NODJHYRURHIIHQWOLFK0UHFKWOLFKHVHQGHUDUGXQGCGI;9FHQWXQGVSDUPDVV\n" +
                "QDKPHQDPFGSDRHIIHQWOLFK0UHFKWOLFKHVHQGHUDUGXQGCGI;9FHQWXQGVSDU\n" +
                "PDVVQDKPHQEHUOLQ0ZHQLJHUJHEXHKUHQDOVHUKRIIWXQGGDCXDXFKQRFKVSDU\n" +
                "PDVVQDKPHQQHEHQGHUJHULQJHUDOVJHSODQWDXVIDOOHQGHQEHLWUDJVVWHLJH\n" +
                "UXQJIRUGHUWHQGLHODHQGHUGLHRHIIHQWOLFK0UHFKWOLFKHQVHQGHDQVWDOWH\n" +
                "QCXHLQVSDUXQJHQLPPHKUVWHOOLJHQPLOOLRQHQEHUHLFKDXIXPGLHGLIIHUHQ\n" +
                "CCZLVFKHQGHPJHEXHKUHQYRUVFKODJGHUODHQGHUXQGGHUNRPPLVVLRQDXVCXJ\n" +
                "OHLFKHQJHEXHKUHQUXQWHUVWHOOHQZHJGLHDUGVROOCXVDHWCOLFK588VWHOOH\n" +
                "QVWUHLFKHQ633ZHLWHUHGDVCGIDXVVHUGHPVROOHQGLHVHQGHULKUHDXVJDEHQ\n" +
                "IXHUPDUNHWLQJXQGRQOLQH0DQJHERWHGHXWOLFKGURVVHOQXQGDXIHLQHQEHVW\n" +
                "LPPWHQKRHFKVWEHWUDJHLQIULHUHQGLHHQGJXHOWLJHHQWVFKHLGXQJXHEHUGD\n" +
                "VNXHQIWLJHJHEXHKUHQDXVPDVVIDHOOWDXIHLQHUNRQIHUHQCDOOHU49PLQLVW\n" +
                "HUSUDHVLGHQWHQYRP9ELV;RNWREHUGHUYRUVLWCHQGHGHUUXQGIXQNNRPPLVVL\n" +
                "RQGHUODHQGHUGHUUKHLQODQG0SIDHOCLVFKHUHJLHUXQJVFKHINXUWEHFNVSGZ\n" +
                "DUQWHYRUHLQHUYHUIDVVXQJVNODJHHUUDHXPWHCZDUHLQGDVVEHGHQNHQGXUFK\n" +
                "DXVEHUHFKWLJWVHLHQGDGLHJHEXHKUHQHUKRHKXQJCXP4MDQXDUHUIROJHQPXH\n" +
                "VVWHGRFKHLQUHFKWVVWUHLWGDXHUHCZHLELVGUHLMDKUHLQGHUGLHWDULIDQKH\n" +
                "EXQJQLFKWZLUNVDPZHUGHQNRHQQHZRGXUFKDUGXQGCGIPLOOLRQHQYHUOLHUHQ\n" +
                "ZXHUGHQGLHODHQGHUVHLHQHLJHQWOLFKIXHUHLQHJHEXHKUHQHUKRHKXQJXP:<\n" +
                "FHQWVFKOXHJHQDEHUDOVDXVJOHLFKIXHUGLHCHLWOLFKHYHUCRHJHUXQJ;9FHQ\n" +
                "WYRUGDKHUVROOWHQGLHVHQGHUGDVHWZDVJHGUHFKVHOWHHUJHEQLVDNCHSWLHU\n" +
                "HQEHWRQWHEHFNGHUEHWUDJXQGGDVYHUIDKUHQVLQGSUREOHPDWLVFKEHJUXHQG\n" +
                "HWHDUG0LQWHQGDQWMREVWSORJVHLQHUHFKWOLFKHQEHGHQNHQGLHRSWLRQHLQH\n" +
                "UYHUIDVVXQJVNODJHEHKDOWHPDQVLFKYRUSORJXQGCGI0LQWHQGDQWPDUNXVVF\n" +
                "KDHFKWHUPDFKWHQNODUGDVVLKQHQGLHYRUJHVFKODJHQHHUKRHKXQJCXJHULQJ\n" +
                "DXVIDOOHVFKDHFKWHUHUNODHUWHCXUYRUJHKHQVZHLVHGHUODHQGHUGLHVPXVV\n" +
                "HLQPDOLJEOHLEHQXQGJXWEHJUXHQGHWZHUGHQGLHEXQGHVWDJVIUDNWLRQGHUJ\n" +
                "UXHQHQXQGGLHJHZHUNVFKDIWYHUGLIRUGHUWHQGLHODHQGHUDXIGHQYRUVFKOD\n" +
                "JGHUXQDEKDHQJLJHQNRPPLVVLRQHADNWCXEHIROJHQYHUGLEHIXHUZRUWHWHHL\n" +
                "QHYHUIDVVXQJVNODJHXPPRHJOLFKHHLQJULIIHLQGLHUXQGIXQNIUHLKHLWCXX\n" +
                "HEHUSUXHIHQELVKHUZDUHQGLHODHQGHUVWHWVGHPYRUVFKODJGHUNRPPLVVLRQ\n" +
                "JHIROJWVWRLEHUEHWRQWDEVWLPPXQJVEHGDUIGLHWHLOQHKPHUGHVEHUOLQHUW\n" +
                "UHIIHQVEHWRQWHQGHUMHWCLJHYRUVFKODJVHLODHQJVWQLFKWXQWHUGDFKXQGI\n" +
                "DFKGHUEDBHULVFKHPLQLVWHUSUDHVLGHQWHGPXQGVWRLEHUFVXVDJWHHVEHVWH\n" +
                "KHQRFKDEVWLPPXQJVEHGDUICZLVFKHQGHQPLQLVWHUSUDHVLGHQWHQVSDHWHVW\n" +
                "HQVDXILKUHUNRQIHUHQCLPRNWREHUZROOWHQVLHHLQHJHPHLQVDPHOLQLHILQG\n" +
                "HQHVVHLQLFKWHLQIDFKGLHXQWHUVFKLHGOLFKHQLQWHUHVVHQGHU49ODHQGHUX\n" +
                "QWHUHLQHQKXWCXEHNRPPHQNODUVHLDEHUGDVVVLFKGLHRHIIHQWOLFK0UHFKWO\n" +
                "LFKHQVHQGHUGHPDOOJHPHLQHQVSDUGUXFNQLFKWHQWCLHKHQNRHQQWHQGLHEXH\n" +
                "UJHUYHUVWXHQGHQQLFKWGDVVXHEHUDOOJHNXHUCWZHUGHGLHVHQGHUDEHUDXVV\n" +
                "HQYRUEOLHEHQGLHJHEXHKUHQHUKRHKXQJPXHVVHDOOHUGLQJVVRCLDOYHUWUDH\n" +
                "JOLFKHUIROJHQEHWRQWHQEHFNXQGVWRLEHUDOVZHLWHUHVSDUPDVVQDKPHQVFK\n" +
                "OXJHQGLHPLQLVWHUSUDHVLGHQWHQYRUGLHEXQGHVZHLWHHPSIDQJVJDUDQWLHI\n" +
                "XHUDUGXQGCGIYLDDQWHQQHDECXVFKDIIHQVDWHOOLWXQGNDEHOVHLHQJXHQVWL\n" +
                "JHDOWHUQDWLYHQ";

        double[] countLetters = analysis(encryptionText);
        print(countLetters);

        encryptionText = encryptAndDecrypt(encryptionText, 3, '-');
        countLetters = analysis(encryptionText);
        print(countLetters);
    }

    public static double[] analysis(String text) {
        double[] countLetters = new double[26];

        for (int i = 0; i < text.length(); i++) {
            for (int j = 0; j < countLetters.length; j++) {
                if (text.charAt(i) - 65 == j) {
                    countLetters[j]++;
                }
            }
        }

        double percent;

        for (int i = 0; i < countLetters.length; i++) {
            percent = countLetters[i] / text.length() * 100;
            countLetters[i] = percent;

            int temp = (int) (countLetters[i] * 100);
            countLetters[i] = ((double) temp / 100);

        }
        return countLetters;
    }

    public static String encryptAndDecrypt(String text, int key, char operator) {
        text = text.toLowerCase();
        char[] encryptText = new char[text.length()];

        for (int i = 0; i < text.length(); i++) {
            int ascii;

            if (operator == '+') ascii = ((text.charAt(i) + key) - 96) % 26;
            else ascii = ((text.charAt(i) - key) - 96) % 26;
            if (ascii == 0) ascii = 26;

            encryptText[i] = (char) (ascii + 96);
        }
        return new String(encryptText);
    }

    public static void print(double[] countLetters) {
        int ascii = 65;
        System.out.println("----------------------------------------------------------------");
        for (int i = 0; i < countLetters.length; i++) {
            System.out.print((char) ascii + ": " + countLetters[i] + "%, ");
            ascii++;
        }
        System.out.println();
        System.out.println("----------------------------------------------------------------");
    }
}
```
