```java 
import java.util.*;

public class TwoToOne {

  public static String longest(String s1, String s2) {
    String tout = s1 + s2;

    Set<Character> lettres = new TreeSet<>();

    for (int i = 0; i < tout.length(); i++) {
      lettres.add(tout.charAt(i));
    }

    StringBuilder resultat = new StringBuilder();
    for (char c : lettres) {
      resultat.append(c);
    }

    return resultat.toString();
  }
}
```

3. [Exercice 4 - Calcule de nombre de voyelle dans une chaine de caractère ](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java 
import java.util.List;
import java.util.ArrayList;

public class Kata {
  
  public static List<Object> filterList(final List<Object> list) {
    List<Object> result = new ArrayList<>();
    
    for (Object item : list) {
      if (item instanceof Integer) {
        result.add(item);
      }
    }
    
    return result;
  }
}
```


3. [Exercice 5 - ordonner les chiffres ](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)
``` java
import java.util.Arrays;
import java.util.Collections;

public class Kata {

    public static long sortDesc(final int num) {
        String[] digits = String.valueOf(num).split("");
        Arrays.sort(digits, Collections.reverseOrder());
        String sorted = String.join("", digits);
        return Long.parseLong(sorted);
    }
}
```

7. [Exercice 7](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)
```java
public class NumberUtils {
    public static boolean isNarcissistic(int number) {
        String strNum = String.valueOf(number);
        int length = strNum.length();
        int sum = 0;

        for (char c : strNum.toCharArray()) {
            int digit = Character.getNumericValue(c);
            sum += Math.pow(digit, length);
        }

        return sum == number;
    }
}
```
8. [get the middle character](https://www.codewars.com/kata/56747fd5cb988479af000028/train/java)
```java
class Kata {
  public static String getMiddle(String word) {
    int n = word.length();
    if(n%2==0){
      return word.substring(n/2-1, n/2 +1);
    }else{
      return word.substring(n / 2, n / 2 + 1);
    }
  }
} 
```

9. [shortest word](https://www.codewars.com/kata/57cebe1dc6fdc20c57000ac9/train/java)
```java:
public class Kata {
    public static int findShort(String s) {
      String[] res = s.split(" ");
      int min = Integer.MAX_VALUE;
      for(String str: res){
        if(str.length() < min){
          min = str.length();
        }
      }
      return min;
    }
}
```

10. [sum of numbers](https://www.codewars.com/kata/55f2b110f61eb01779000053/train/java)
```java
public class Sum {
    public int GetSum(int a, int b) {
        int res = 0;
        if (a < b) {
            for (int i = a; i <= b; i++) {
                res += i;
            }
        } 
        else if (a > b) {
            for (int i = b; i <= a; i++) {
                res += i;
            }
        } 
        else {
            return a;  
        }
        
        return res;
    }
}
```

11. [friend or foe](https://www.codewars.com/kata/55b42574ff091733d900002f/train/java)
```java
public class FriendsFilter {
    public static List<String> friend(String[] x) {
        List<String> result = new ArrayList<>();
        
        for (String name : names) {
            if (name.length() == 4) {
                res.add(name);
            }
        }
        
        return res;
    }
}
```

12. [regex valdiation pin](https://www.codewars.com/kata/55f8a9c06c018a0d6e000132/train/java)
```java
public class Solution {

  public static boolean validatePin(String pin) {
    if (pin.length() != 4 && pin.length() != 6) return false;

    for (int i = 0; i < pin.length(); i++) {
      if (!Character.isDigit(pin.charAt(i))) return false;
    }

    return true;
  }
}
```
13. [recervse word](https://www.codewars.com/kata/5259b20d6021e9e14c0010d4/train/java)
```java
public class Kata {
  public static String reverseWords(final String original) {
    String[] words = original.split(" ", -1); 
    StringBuilder result = new StringBuilder();

    for (int i = 0; i < words.length; i++) {
      StringBuilder reversed = new StringBuilder(words[i]).reverse();
      result.append(reversed);
      if (i < words.length - 1) {
        result.append(" ");
      }
    }

    return result.toString();
  }
}

```
14. [hello word niveau 7](https://www.codewars.com/kata/584c7b1e2cb5e1a727000047/train/java)
```java 
public class HelloWorld {

    public static String helloWorld() {
        return new StringBuilder()
            .append((char)72)  
            .append((char)101) 
            .append((char)108) 
            .append((char)108) 
            .append((char)111) 
            .append((char)44)  
            .append((char)32)  
            .append((char)87)  
            .append((char)111) 
            .append((char)114) 
            .append((char)108) 
            .append((char)100) 
            .append((char)33) 
            .toString();
    }
}
```