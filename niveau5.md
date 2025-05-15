1. [Build a car](https://www.codewars.com/kata/5832d6e2565e120ae60000bb/train/java)
```java 
public class Car {
    public Body body;
    public Chassis chassis;

    public class Body {
        public String component;
    }

    public class Chassis {
        public String component;
    }

    public Car(int length, int doors) throws Exception {
        // Vérification des contraintes
        if (length < 7) {
            throw new Exception("Car length must be at least 7");
        }
        if (doors < 1) {
            throw new Exception("There must be at least one door");
        }
        if (doors > length - 3) {
            throw new Exception("Too many doors for this length");
        }

        body = new Body();
        chassis = new Chassis();

    
        // Lignes
        int layer1Length = length - 2;
        int layer2Length = length - 1;

        // ---- Construction de la 1re ligne : " ____\n"
        StringBuilder top = new StringBuilder(" ");
        for (int i = 0; i < layer1Length; i++) {
            top.append("_");
        }
        top.append("\n");

        // ---- Construction de la 2e ligne : "|[][]  []\\\n"
        StringBuilder mid = new StringBuilder("|");
        char[] middle = new char[layer2Length - 2]; // contenu entre | et \
        for (int i = 0; i < middle.length; i++) {
            middle[i] = ' ';
        }
        int front = 0;
        int rear = middle.length - 1;
        boolean toFront = true;
        for (int i = 0; i < doors; i++) {
            if (toFront) {
                middle[front] = '[';
                middle[front + 1] = ']';
                front += 2;
            } else {
                middle[rear - 1] = '[';
                middle[rear] = ']';
                rear -= 2;
            }
            toFront = !toFront;
        }

        mid.append(new String(middle));
        mid.append("\\\n");

        // ---- Construction de la 3e ligne : "-o--o-'\n"
        StringBuilder bottom = new StringBuilder();

        int axles = 2;
        if (length >= 12) {
            axles++;
            int extra = (length - 12) / 2;
            axles += extra;
        }

        int totalAxleWidth = axles * 2 - 1;
        int dashes = length - totalAxleWidth - 2; // -2 pour le quote et tiret final

        boolean placeRear = true;
        StringBuilder wheels = new StringBuilder();
        for (int i = 0; i < axles; i++) {
            if (i > 0) wheels.append("-");
            wheels.append("o");
        }

        StringBuilder axleLine = new StringBuilder("-");
        int leftDashes = dashes / 2;
        int rightDashes = dashes - leftDashes;

        for (int i = 0; i < leftDashes; i++) axleLine.append("-");
        axleLine.append(wheels);
        for (int i = 0; i < rightDashes; i++) axleLine.append("-");
        axleLine.append("o-'");

        // Attribution
        body.component = top.toString() + mid.toString();
        chassis.component = axleLine.toString();
    }
}

```

2. [simple pig latin](https://www.codewars.com/kata/520b9d2ad5c005041100000f/train/java)
```java
import java.util.*;

public class PigLatin {
    public static String pigIt(String str) {
        List<String> strl = new ArrayList<>();
        String[] mots = str.split(" ");
      
        for (int i = 0; i < mots.length; i++) {
            strl.add(mots[i]);
        }

        for (int i = 0; i < strl.size(); i++) {
            String mot = strl.get(i);
            if (mot.matches("[a-zA-Z]+")) {
                String firstLetter = mot.substring(0, 1);
                String reste = mot.substring(1);
                strl.set(i, reste + firstLetter + "ay");
            }
        }

        return String.join(" ", strl);
    }}
```

3. [Human readable time](https://www.codewars.com/kata/52685f7382004e774f0001f7/train/java)
```java
public class HumanReadableTime {
    public static String makeReadable(int seconds) {
        int hours = seconds / 3600;
        int minutes = (seconds % 3600) / 60;
        int secs = seconds % 60;

        return String.format("%02d:%02d:%02d", hours, minutes, secs);
    }

}
```
4. [Human Readable Time](https://www.codewars.com/kata/52685f7382004e774f0001f7/train/java)
```java
public class HumanReadableTime {
    public static String makeReadable(int seconds) {
        int hours = seconds / 3600;
        int minutes = (seconds % 3600) / 60;
        int secs = seconds % 60;
        return String.format("%02d:%02d:%02d", hours, minutes, secs);
    }
}
```

5. [Create phone number ](https://www.codewars.com/kata/525f50e3b73515a6db000b83/solutions/java)
```java 
public class Kata {
  public static String createPhoneNumber(int[] numbers) {
    return String.format("(%d%d%d) %d%d%d-%d%d%d%d",numbers[0],numbers[1],numbers[2],numbers[3],numbers[4],numbers[5],numbers[6],numbers[7],numbers[8],numbers[9]);
  }
}
```
6. [Validator od password](https://www.codewars.com/kata/52e1476c8147a7547a000811/solutions/java)
```java 
class PasswordRegex {
// asssign your pattern string to REGEX, it will be
// compiled to a Pattern and matched with matches()
    static final String REGEX = "^(?=.*[a-z])(?=.*[A-Z])(?=.*\\d)[A-Za-z\\d]{6,}$";
}
```


```java  

6. [string mix](https://www.codewars.com/kata/5629db57620258aa9d000014/solutions/java)
```java 
public class Mixing {

    public static String mix(String s1, String s2) {
        int[] freq1 = countLowerCase(s1);
        int[] freq2 = countLowerCase(s2);

        java.util.List<String> parts = new java.util.ArrayList<>();

        for (int i = 0; i < 26; i++) {
            int f1 = freq1[i];
            int f2 = freq2[i];
            int maxFreq = Math.max(f1, f2);

            if (maxFreq > 1) {
                char c = (char) ('a' + i);
                StringBuilder sb = new StringBuilder();
                if (f1 > f2) {
                    sb.append("1:");
                    for (int j = 0; j < f1; j++) sb.append(c);
                } else if (f2 > f1) {
                    sb.append("2:");
                    for (int j = 0; j < f2; j++) sb.append(c);
                } else {
                    sb.append("=:");
                    for (int j = 0; j < f1; j++) sb.append(c);
                }
                parts.add(sb.toString());
            }
        }

        parts.sort((a, b) -> {
            int lenDiff = b.length() - a.length();
            if (lenDiff != 0) return lenDiff;
            return a.compareTo(b);
        });

        return String.join("/", parts);
    }

    private static int[] countLowerCase(String s) {
        int[] freq = new int[26];
        for (char ch : s.toCharArray()) {
            if (ch >= 'a' && ch <= 'z') freq[ch - 'a']++;
        }
        return freq;
    }
}
```
7. [Battle ships](https://www.codewars.com/kata/58d06bfbc43d20767e000074/train/java)
```java
import java.util.*;

public class BattleShips {
    public static Map<String, Double> damagedOrSunk(int[][] board, int[][] attacks) {
        Map<Integer, Integer> boatSizes = new HashMap<>();
        Map<Integer, Integer> boatHits = new HashMap<>();

        int rows = board.length;
        int cols = board[0].length;

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                int val = board[i][j];
                if (val > 0) {
                    boatSizes.put(val, boatSizes.getOrDefault(val, 0) + 1);
                }
            }
        }
        for (int[] attack : attacks) {
            int x = attack[0] - 1;
            int y = rows - attack[1];
            if (x >= 0 && x < cols && y >= 0 && y < rows) {
                int hit = board[y][x];
                if (hit > 0) {
                    boatHits.put(hit, boatHits.getOrDefault(hit, 0) + 1);
                }
            }
        }
        int sunk = 0;
        int damaged = 0;
        int notTouched = 0;
        double points = 0.0;

        for (Integer boatId : boatSizes.keySet()) {
            int size = boatSizes.get(boatId);
            int hits = boatHits.getOrDefault(boatId, 0);

            if (hits == 0) {
                notTouched++;
                points -= 1;
            } else if (hits < size) {
                damaged++;
                points += 0.5;
            } else if (hits == size) {
                sunk++;
                points += 1;
            }
        }

        Map<String, Double> result = new HashMap<>();
        result.put("sunk", (double) sunk);
        result.put("damaged", (double) damaged);
        result.put("notTouched", (double) notTouched);
        result.put("points", points);

        return result;
    }
}
```