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
