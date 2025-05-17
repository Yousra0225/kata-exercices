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
12. [Triangles made of random points](https://www.codewars.com/kata/5ec1692a2b16bb00287a6d8c/train/java)
```java
public class Solution {
    public static double[] maxminAreas(int[][] points) {
        int n = points.length;
        double max = 0.0;
        double min = Double.MAX_VALUE;
        boolean foundTriangle = false;

        for (int i = 0; i < n - 2; i++) {
            int[] p1 = points[i];
            for (int j = i + 1; j < n - 1; j++) {
                int[] p2 = points[j];
                for (int k = j + 1; k < n; k++) {
                    int[] p3 = points[k];
                    double area = triangleArea(p1, p2, p3);
                    if (area > 0) {
                        foundTriangle = true;
                        if (area > max) max = area;
                        if (area < min) min = area;
                    }
                }
            }
        }
        if (!foundTriangle) return new double[]{0, 0};
        
        return new double[]{
            Math.round(max * 10.0) / 10.0,
            Math.round(min * 10.0) / 10.0
        };
    }
    private static double triangleArea(int[] a, int[] b, int[] c) {
        return 0.5 * Math.abs(
            a[0] * (b[1] - c[1]) +
            b[0] * (c[1] - a[1]) +
            c[0] * (a[1] - b[1])
        );
    }
}
```

14. [Remove a specific element](https://www.codewars.com/kata/581bb3c1c221fb8e790001ef/train/java)
```java
import java.math.BigInteger;
import java.util.*;

public class Kata {
    public static int[][] selectSubarray(final int[] arr) {
        int n = arr.length;
        List<int[]> result = new ArrayList<>();
        BigInteger minProduct = null;
        double minQ = Double.MAX_VALUE;

        for (int i = 0; i < n; i++) {
            int sum = 0;
            BigInteger product = BigInteger.ONE;
            boolean valid = true;

            for (int j = 0; j < n; j++) {
                if (j != i) {
                    sum += arr[j];
                    product = product.multiply(BigInteger.valueOf(arr[j]));
                }
            }
            if (sum == 0) continue;

            double q = product.abs().doubleValue() / Math.abs(sum);
            if (q < minQ) {
                minQ = q;
                result.clear();
                result.add(new int[]{i, arr[i]});
            } else if (q == minQ) {
                result.add(new int[]{i, arr[i]});
            }
        }
        result.sort(Comparator.comparingInt(a -> a[0]));
        return result.toArray(new int[0][]);
    }
}
```
```java
@Test
public void exampleTests() {
    Tester.doTest(new int[]{1, 23, 2, -8, 5}, new int[][]{{3, -8}});
    Tester.doTest(new int[]{1, 3, 23, 4, 2, -8, 5, 18}, new int[][]{{2, 23}});
    Tester.doTest(new int[]{10, 20, -30, 100, 200}, new int[][]{{3, 100}, {4, 200}});
}

```

