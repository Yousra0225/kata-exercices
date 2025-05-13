# kata-exercices
# Auteur : Yousra Chbib

##  Niveau 8

1. [Exercice 1 - Pair ou Impair](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java
public class Kata {
    public static String evenOrOdd(int number) {
      if(number%2==0){
        return "Even";
      }else{
        return "Odd";
      }
    }
}
``` 

2. [Exercice 2 - Somme des élément d'une liste](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)
```java
public class SumArray {
    public static double sum(double[] numbers) {
        double sum = 0;
        for (int i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }
        return sum;
    }
}
```
3. [Exercice 3 - Calcule de nombre de voyelle dans une chaine de caractère ](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java
public class Vowels {

    public static int getCount(String str) {
        String vowels = "aeiouAEIOU";
        int cpt = 0;
        for (int i = 0; i < str.length(); i++) {
            if (vowels.indexOf(str.charAt(i)) != -1) {
                cpt += 1;
            }
        }
        return cpt;
    }
}
```


4. [Exercice 4 - Multiplies of two numbers ](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java
public class Multiply {
    public static Double multiply(Double a, Double b) {
        return a * b;
    }
}
```

5. [Exercice 5 - show who likes a post ](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)

```java 
public class Solution {
    public static String whoLikesIt(String... names) {
        int n = names.length;

        switch (n) {
            case 0: return "no one likes this";
            case 1: return names[0] + " likes this";
            case 2: return names[0] + " and " + names[1] + " like this";
            case 3: return names[0] + ", " + names[1] + " and " + names[2] + " like this";
            default: return names[0] + ", " + names[1] + " and " + (n - 2) + " others like this";
        }
    }
}
``` 
6. [Exercice 6 - Determines if the order of the braces is valid](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/java)
```java
import java.util.Stack;

public class BraceChecker {
    public static boolean isValid(String braces) {
        Stack<Character> stack = new Stack<>();

        for (char ch : braces.toCharArray()) {
            switch (ch) {
                case '(': case '[': case '{':
                    stack.push(ch);
                    break;
                case ')':
                    if (stack.isEmpty() || stack.pop() != '(') return false;
                    break;
                case ']':
                    if (stack.isEmpty() || stack.pop() != '[') return false;
                    break;
                case '}':
                    if (stack.isEmpty() || stack.pop() != '{') return false;
                    break;
            }
        }
        return stack.isEmpty();
    }
}
```

7. 1. [Exercice 1 - Convert a number to a string ](https://www.codewars.com/kata/5265326f5fda8eb1160004c8/train/java)
```java
public class Kata {
    public static String numberToString(int num){
        return String.valueOf(num);
    }
}
```