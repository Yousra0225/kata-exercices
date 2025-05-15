8. [Exercice 8 : show the time in a himan readable format](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java
public class TimeFormatter {
    public static String makeReadable(int seconds) {
        int hours = seconds / 3600;
        int minutes = (seconds % 3600) / 60;
        int secs = seconds % 60;

        return String.format("%02d:%02d:%02d", hours, minutes, secs);
    }
}

```

9. [Exercice 9 : show the time in a himan readable format](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)
``` java 
public class Solution {

  public int solution(int number) {
    int sum = 0;
    for (int i = 0; i < number; i++) {
      if (i % 3 == 0 || i % 5 == 0) {
        sum += i;
      }
    }
    return sum;
  }
}
```
10. [say hello world](https://www.codewars.com/kata/5b0a80ce84a30f4762000069/train/java)
```java
import java.util.*;

public class Dinglemouse {

  private String name;
  private int age;
  private char sex;

  // Pour suivre l'ordre des setters appelés (sans doublons)
  private final List<String> setOrder = new ArrayList<>();

  public Dinglemouse() {}

  public Dinglemouse setAge(int age) {
    this.age = age;
    addOnce("age");
    return this;
  }

  public Dinglemouse setSex(char sex) {
    this.sex = sex;
    addOnce("sex");
    return this;
  }

  public Dinglemouse setName(String name) {
    this.name = name;
    addOnce("name");
    return this;
  }

  private void addOnce(String field) {
    if (!setOrder.contains(field)) {
      setOrder.add(field);
    }
  }

  public String hello() {
    StringBuilder sb = new StringBuilder("Hello.");
    for (String field : setOrder) {
      switch (field) {
        case "name":
          sb.append(" My name is ").append(name).append(".");
          break;
        case "age":
          sb.append(" I am ").append(age).append(".");
          break;
        case "sex":
          sb.append(" I am ").append(sex == 'M' ? "male" : "female").append(".");
          break;
      }
    }
    return sb.toString();
  }
}
```

11. [split the string](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001/train/java)
```java
import java.util.*;

public class StringSplit {
    public static String[] solution(String s) {
        if (s.length() % 2 != 0) {
            s += "_";
        }

        String[] result = new String[s.length() / 2];

        for (int i = 0; i < s.length(); i += 2) {
            result[i / 2] = s.substring(i, i + 2);
        }

        return result;
    }
}
```