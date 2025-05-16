1. [sum string as numbers ](https://www.codewars.com/kata/5324945e2ece5e1f32000370/train/java)
```java
public class Kata {
  public static String sumStrings(String a, String b) {
    int res1 = Integer.parseInt(a);
    int res2 = Integer.parseInt(b);
    int res = res1 + res2;
    return String.valueOf(res);
  }
}
```

2. [differentiate a polynomial](https://www.codewars.com/kata/566584e3309db1b17d000027/train/java)
```java
 import java.math.BigInteger;

public class Equation {
    
    public static BigInteger differentiate(String equation, long x) {
        String[] arr = equation.split(" ");
        BigInteger res = new BigInteger("0");
        for (int i = 0; i < arr.length; i++) {
            if (arr[i].equals("+")) {
                res = res.add(new BigInteger(arr[i + 1]));
            } else if (arr[i].equals("-")) {
                res = res.add(new BigInteger(arr[i + 1]));
            }
        }
        return res;
    }
}
```
3. [string incrementer ](https://www.codewars.com/kata/54a91a4883a7de5d7800009c/train/java)
```java
import java.math.BigInteger;

public class StringIncrementer {
  public static String incrementString(String str) {
    String prefix = str.replaceAll("\\d+$", "");        
    String numberPart = str.substring(prefix.length()); 

    if (numberPart.isEmpty()) {
      return prefix + "1"; 
    }

    int numberLength = numberPart.length();               
    BigInteger number = new BigInteger(numberPart);      
    number = number.add(BigInteger.ONE);                

    String incremented = String.format("%0" + numberLength + "d", number);

    return prefix + incremented;
  }
}

```
4. [Adding big numbers ](https://www.codewars.com/kata/525f4206b73515bffb000b21/train/java)
```java
public class Kata {
  public static String add(String a, String b) {
    StringBuilder result = new StringBuilder();
    int i = a.length() - 1;
    int j = b.length() - 1;
    int carry = 0;

    while (i >= 0 || j >= 0 || carry != 0) {
      int digitA = (i >= 0) ? a.charAt(i) - '0' : 0;
      int digitB = (j >= 0) ? b.charAt(j) - '0' : 0;

      int sum = digitA + digitB + carry;
      result.append(sum % 10);
      carry = sum / 10;

      i--;
      j--;
    }
    while (result.length() > 1 && result.charAt(result.length() - 1) == '0') {
      result.setLength(result.length() - 1);
    }
    return result.reverse().toString();
  }
}

```