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
8. [check if a number is a perfect power](https://www.codewars.com/kata/54d4c8b08776e4ad92000835/train/java)
```java 
import java.util.*;

public class PerfectPower {
    public static int[] isPerfectPower(int n) {
        for (int k = 2; k <= (int)(Math.log(n) / Math.log(2)) + 1; k++) {
            double root = Math.pow(n, 1.0 / k);
            int m = (int) Math.round(root);
            if (Math.pow(m, k) == n) {
                return new int[]{m, k};
            }
        }
        return null;
    }

}

```

9. [reverse a string ](https://www.codewars.com/kata/54d4c8b08776e4ad92000835/train/java)
a. Solution 1
```java
public class Kata {
    public static String reverse(String str){
        return new StringBuilder(str).reverse().toString();
    }
}
```
b. Solution 2
```java
public class Kata {
    public static String solution(String str) {
        char[] chars = str.toCharArray(); 
        int i = 0;
        int j = chars.length - 1;
        while (i < j) {
            char temp = chars[i];
            chars[i] = chars[j];
            chars[j] = temp;
            i++;
            j--;
        }
        
        return new String(chars); 
    }
}
```
10. [convert a number to negative ](https://www.codewars.com/kata/55685cd7ad70877c23000102/train/java)
a. Solution 1
```java
public class Kata {

  public static int makeNegative(final int x) {
    if(x<0){
      return x;
    }else{
      return x*-1;
    }  
  }
}
```
b. Solution 2
```java 
public class Kata {
    public static int makeNegative(final int x) {
        return x > 0 ? -x : x;
    }
}
```

11. [opposit number ](https://www.codewars.com/kata/56dec885c54a926dcd001095/solutions/java)
```java 
public class Kata {
    public static int opposite(int number) {
        return -number;
    }
}
``` 

12. [sum of positive ](https://www.codewars.com/kata/56dec885c54a926dcd001095/solutions/java)
A. Solution 1
```java 
public class Positive {
    public static int sum(int[] arr) {
        int res = 0; 
        for (int i = 0; i < arr.length; i++) { 
          if(arr[i]>0){
            res += Math.abs(arr[i]); 
          }
        }
        return res;
    }
}
```
B. Solution 2
```java
public class Kata{
    public static int sum(int[] arr){
        int res = 0;
        for (int i =0; i<arr.length; i++){
            res = res + (arr[i]>0 ? arr[i] : 0);
        }
        return res;
    }
}
```
13. [repeat string ](https://www.codewars.com/kata/57a0e5c372292dd76d000d7e/train/java)
A. Solution 1
```java
public class Kata {
    public static String repeatStr(int n, String s) {
        return s.repeat(n);
    }
}
```
B. Solution 2
```java 
public class Solution {
    public static String repeatStr(int n, String s) {
        String res = "";
        for(int i = 0; i < n; i++) {
            res += s;
        }
        return res;
    }
}
```

13. [Hello world](https://www.codewars.com/kata/523b4ff7adca849afe000035)
```java
public class HelloWorld {
    public static String greet() {
       return "Hello World";
    }
}
```

14. [remove string space](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/java)
```java 
public class Kata {
    public static String noSpace(final String x) {
        String res = "";
        for (int i = 0; i < x.length(); i++) {
            if (x.charAt(i) != ' ') {  
                res = res + x.charAt(i); 
            }
        }
        return res; 
    }
}
```

15. [convert boolean to a string](https://www.codewars.com/kata/551b4501ac0447318f0009cd/train/java)
```java
public class BooleanToString{
    return b== "true" ? "true" : "false";

}
```

16. [basic mathematical operations](https://www.codewars.com/kata/57356c55867b9b7a60000bd7/train/java)

```java 
public class BasicOperations
{
  public static Integer basicMath(String op, int v1, int v2)
  {
   switch(op){
       case "+":
          return v1 + v2;
       case "-":
          return v1 - v2;
      case "*":
          return v1 * v2;
      default :
          return v1 / v2;
   }
  }
}
```
17. [make upper case](https://www.codewars.com/kata/57a0556c7cb1f31ab3000ad7/train/java)
```java 
class Upper {
    public static String makeUpperCase(String str) {
        return str.toUpperCase();
    }
}
```

18. [simple multiplication](https://www.codewars.com/kata/583710ccaa6717322c000105/train/java)
```java
public class Sid {
    public static int simpleMultiplication(int n) {
        return n%2 ==0 ? n*8 : n*9;
    }
}
```

19. [calculate average](https://www.codewars.com/kata/57a2013acf1fa5bfc4000921/train/java)
```java
public class Kata {
    public static double findAverage(int[] array) {
        if (array.length == 0) return 0;

        int sum = 0;
        for (int i = 0; i < array.length; i++) {
            sum = sum + array[i];
        }
        double res = (double) sum / array.length;
        return res;
    }
}
```
20. [is devisible by x and y ](https://www.codewars.com/kata/5545f109004975ea66000086/train/java)
```java 
public class DivisibleNb {
	public static boolean isDivisible(long n, long x, long y) {
		return x>0 && y>0 && (n % x==0) && (n % y==0)? true: false;
	}
}
```

21. [remove exclamation marks ](https://www.codewars.com/kata/57a0885cbb9944e24c00008e/solutions/java)
```java 
public class Kata {
    public static String removeExclamationMarks(String s) {
        return s.replaceAll("!", "");
    }
}
```

22. [area or perimeter ](https://www.codewars.com/kata/5ab6538b379d20ad880000ab/solutions/java)
```java 
public class Solution {
    public static int areaOrPerimeter(int l, int w) {
        if (l == w) {
            return l * w; 
        } else {
            return 2 * (l + w); 
        }
    }
}

```

23. [is gonna survive](https://www.codewars.com/kata/59ca8246d751df55cc00014c/train/java)
```java
class Solution {
  public static boolean hero(int bullets, int dragons) {
    return bullets >= (long)dragons * 2;
  }
}
```
24. [sum mixed array](https://www.codewars.com/kata/57eaeb9578748ff92a000009/train/java)
```java

public class MixedSum {
  public int sum(List<?> mixed) {
          int total = 0;
          for (Object item : mixed) {
              if (item instanceof Integer) {
                  total += (Integer) item;
              } else if (item instanceof String) {
                  total += Integer.parseInt((String) item);
              }
          }
          return total;
}}
```

25. [array plus array](https://www.codewars.com/kata/5a2be17aee1aaefe2a000151/train/java)
```java
public class Kata {
    public static int arrayPlusArray(int[] arr1, int[] arr2) {
        int sum = 0;
        for (int i = 0; i < arr1.length; i++) {
            sum += arr1[i];
        }
        for (int i = 0; i < arr2.length; i++) {
            sum += arr2[i];
        }
        return sum;
    }
}
```

26. [keep hydrated](https://www.codewars.com/kata/582cb0224e56e068d800003c/train/java)
```java
public class KeepHydrated  {
  public static int liters(double time)  {    
    return (int) Math.floor(time*0.5);
  }
}
```

27. [reversed words](https://www.codewars.com/kata/51c8991dee245d7ddf00000e/train/java)
```java 
public class ReverseWords {

    public static String reverseWords(String str) {
        String[] res = str.split(" "); 
        StringBuilder result = new StringBuilder();

        for (int i = res.length - 1; i >= 0; i--) {
            result.append(res[i]);
            if (i != 0) {
                result.append(" ");
            }
        }

        return result.toString();
    }
}


``` 

26. [powers of two](https://www.codewars.com/kata/57a083a57cb1f31db7000028/train/java)
```java 
public class Kata{
  public static long[] powersOfTwo(int n){
    long[] res = new long[n+1];
    for(int i=0; i<=n;i++){
      res[i] = (long) Math.pow(2, i);
    }
    return res;
  }
}
```
27. [square sum](https://www.codewars.com/kata/515e271a311df0350d00000f/train/java)
```java
import java.lang.Math;
public class Kata
 {
  public static int squareSum(int[] n)
  { 
   int res = 0; 
   for(int i = 0; i<n.length; i++){
     res += Math.pow(n[i],2);
     // res = res + Math.pow(n[i],2); !!!!!!
   }
    return (int) res;
  }
 }
 ```
28. [check how good are you](https://www.codewars.com/kata/5601409514fc93442500010b/train/java)
```java
public class Kata {
  public static boolean betterThanAverage(int[] classPoints, int yourPoints) {
    int sum = 0;
    for (int score : classPoints) {
      sum += score;
    }
    double average = (double) sum / classPoints.length;
    return yourPoints > average;
  }
}
```
29. [calculate BMI](https://www.codewars.com/kata/57a429e253ba3381850000fb/train/java)
```java
public class Calculate {
  public static String bmi(double weight, double height) {
    double bmi = weight / (height * height); 
    if (bmi <= 18.5) {
      return "Underweight";
    } else if (bmi <= 25.0) {
      return "Normal";
    } else if (bmi <= 30.0) {
      return "Overweight";
    } else {
      return "Obese";
    }
  }
}
```
30. [find max and min values of a list](https://www.codewars.com/kata/577a98a6ae28071780000989/train/java)
```java
import java.util.Arrays;
public class Kata{
    public int min(int[] list){
        return Arrays.stream(list).min().getAsInt();
    }
    public int max(int[] list){
        return Arrays.stream(list).max().getAsInt();
    }
}
```

31. [calculate the volume of a cuboid](https://www.codewars.com/kata/58261acb22be6e2ed800003a/train/java)
```java
public class Kata {

  public static double getVolumeOfCuboid(final double length, final double width, final double height) {
    // Your code here
     return length * width * height;
  }
  
}
```

32. [calculate total points](https://www.codewars.com/kata/5bb904724c47249b10000131/solutions/java)
```java
public class TotalPoints {
  
    public static int points(String[] games) {
      int totalpoints = 0;
      for(String res : games){
        String[] points = res.split(":");
        int x = Integer.parseInt(points[0]);
        int y = Integer.parseInt(points[1]);
        if(x>y){
          totalpoints+=3;
        }
        else if(x<y){
          totalpoints=totalpoints;
        }
        else{
          totalpoints+=1;
        }
      }
      return totalpoints;
    }
}
```

33. [Say hello in special way](https://www.codewars.com/kata/55225023e1be1ec8bc000390/train/java)
```java 
public class Greeter {
  public static String greet(String name) {
    
    String res = String.format("Hello, %s!", name);
    
    if(name.equals("Johnny")){
       res = "Hello, my love!";
    }
    return res;
  }
}
```
34. [Thinkful - Logic Drills: Traffic ligh](https://www.codewars.com/kata/58649884a1659ed6cb000072/train/java)
```java
public class TrafficLights {

  public static String updateLight(String current) {
    String res = "";
    if( current == "green"){
      res = "yellow";
    }
    else if( current == "yellow"){
      res = "red";
    }else{
      res = "green";
    }
    return res;
  }
  
}
```

35. [calculate the third angle of a triangle](https://www.codewars.com/kata/5a023c426975981341000014/train/java)
```java 
public class ThirdAngle {
    public static int otherAngle(int angle1, int angle2) {
        return 180 -(angle1 + angle2);
    }
}
```
36. [set alarm](https://www.codewars.com/kata/568dcc3c7f12767a62000038/train/java)
```java
public class Alarm {
  
  public static boolean setAlarm(boolean employed, boolean vacation) {
    return employed == true && vacation == false ? true : false;
  }

}
```

36. [calculate the sum of elements of a table without including the min and the max](https://www.codewars.com/kata/576b93db1129fcf2200001e6/train/java)
```java
import java.util.Arrays;

public class Kata {
    public static int sum(int[] numbers) {
        if (numbers == null || numbers.length <= 2) return 0;

        int min = Arrays.stream(numbers).min().getAsInt();
        int max = Arrays.stream(numbers).max().getAsInt();
        int some = 0;

        boolean minRemoved = false;
        boolean maxRemoved = false;

        for (int i = 0; i < numbers.length; i++) {
            if (numbers[i] == min && !minRemoved) {
                minRemoved = true;
                continue;
            }

            if (numbers[i] == max && !maxRemoved) {
                maxRemoved = true;
                continue;
            }

            some += numbers[i];
        }

        return some;
    }
}
```
37. [double char]
```java 
public class Solution{
    public static String doubleChar(Strings){
        char[] res = new char[s.length()*2];
        int i = 0;
        for(char element : s.toCharArray()){
            res[i] = element ;
            res[i+1] = element;
            i+=2;
        }
        return new String();
        }
    }
```

38. [the feasts of many beasts](https://www.codewars.com/kata/5aa736a455f906981800360d/train/java)
```java 
public class Kata {

  public static boolean feast(String beast, String dish) {
    return beast.charAt(0) == dish.charAt(0) && beast.charAt(beast.length()-1) == dish.charAt(dish.length()-1) ;
    
  }
  
}
```

39. [keep up the hoop](https://www.codewars.com/kata/55cb632c1a5d7b3ad0000145/train/java)
```java 
public class HelpAlex{
  public static String hoopCount(int n){
   return n >= 10 ? "Great, now move on to tricks" : "Keep at it until you get it";
  }
}
```

40. [calculate average](https://www.codewars.com/kata/563e320cee5dddcf77000158/train/java)
```java 
import java.util.*;
public class School{

 	public static int getAverage(int[] marks){
		return Arrays.stream(marks).sum() / marks.length;
	}

}
```

41. [cock roach speed](https://www.codewars.com/kata/55fab1ffda3e2e44f00000c6/train/java)
```java
public class Cockroach{
  public int cockroachSpeed(double x){
        return (int) Math.floor(x * 100000 / 3600);  }
}
```

42. [switch up](https://www.codewars.com/kata/5808dcb8f0ed42ae34000031/train/java)
```java 
public class Kata {
    public static String switchItUp(int number) {
        switch (number) {
            case 0: return "Zero";
            case 1: return "One";
            case 2: return "Two";
            case 3: return "Three";
            case 4: return "Four";
            case 5: return "Five";
            case 6: return "Six";
            case 7: return "Seven";
            case 8: return "Eight";
            case 9: return "Nine";
            default: return "Invalid";
        }
    }
}
```

43. [calculate a square](https://www.codewars.com/kata/523b623152af8a30c6000027/train/java)
```java 
public class Kata {
    public static int square(int n) {
        return n * n;
    }
}
```

44. [terminal game move function](https://www.codewars.com/kata/563a631f7cbbc236cf0000c2/train/java)
```java 
public class Move {
    public static int move(int position, int roll) {
        return position + roll * 2;
    }
}
```

45. [delete first and last character of a string](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0/train/java)
```java 
public class RemoveChars {
    public static String remove(String str) {
      return str.substring(1,str.length()-1);
    }
}
```

46. [counting sheeps](https://www.codewars.com/kata/54edbc7200b811e956000556/train/java)
```java
import java.util.*;
public class Counter {
    public static int countSheeps(Boolean[] arrayOfSheeps) {
        return (int) Arrays.stream(arrayOfSheeps).filter(Objects::nonNull).filter(element -> element).count() ;
    }
}
```

47. [lost without a map](https://www.codewars.com/kata/57f781872e3d8ca2a000007e/train/java)
```java
public class Maps {
  public static int[] map(int[] arr) {
    int[] newmap = new int[arr.length];
    for (int i = 0; i < arr.length; i++) {
      newmap[i] = arr[i] * 2;
    }
    return newmap;
  }
}
```

48. [convert number to reversed array of digits](https://www.codewars.com/kata/5583090cbe83f4fd8c000051/train/java)
```java
public class Kata {
  public static int[] digitize(long n) {
    String str = String.valueOf(n);
    int[] result = new int[str.length()];
    
    for (int i = 0; i < str.length(); i++) {
      result[i] = str.charAt(str.length() - 1 - i) - '0';
    }
    
    return result;
  }
}
```

49. [found the needle in the haystacj](https://www.codewars.com/kata/56676e8fabd2d1ff3000000c/train/java)
```java 
public class Kata {
  public static String findNeedle(Object[] haystack) {
    String res ="";
    for (int i = 0; i<haystack.length; i++){
      if("needle".equals(haystack[i])){
       res =  "found the needle at position " + i;
      }
    }
    return res;
  }
}
```

50. [invert values](https://www.codewars.com/kata/5899dc03bc95b1bf1b0000ad/train/java)
```java 
import java.util.*;
public class Kata {
  public static int[] invert(int[] array) {
    return Arrays.stream(array).map(e -> e*-1).toArray();
    }
}
```

51. [reduce but grow](https://www.codewars.com/kata/57f780909f7e8e3183000078/train/java)
```java 
import java.util.*;
public class Kata {
  public static int grow(int[] x) {
    int res = 1;
    for (int i = 0; i < x.length; i++) {
      res *= x[i];
    }
    return res;
  }
}
```

52. [sentence smash](https://www.codewars.com/kata/53dc23c68a0c93699800041d/train/java)
```java 
public class SmashWords {
  public static String smash(String[] words) {
    return String.join(" ", words);
  }
}
```

53. [count positive/ sum of negatives](https://www.codewars.com/kata/576bb71bbbcf0951d5000044/train/java)
```java 
public class Kata {
  public static int[] countPositivesSumNegatives(int[] input) {
    if (input == null || input.length == 0) return new int[0];

    int countPositive = 0;
    int sumNegative = 0;

    for (int num : input) {
      if (num > 0) countPositive++;
      else if (num < 0) sumNegative += num;
    }

    return new int[]{countPositive, sumNegative};
  }
}
```

54. [count what is between](https://www.codewars.com/kata/55ecd718f46fba02e5000029/train/java)
```java 
public class Kata {
  public static int[] between(int a, int b) {
    int[] result = new int[b - a + 1];
    for (int i = 0; i < result.length; i++) {
      result[i] = a + i;
    }
    return result;
  }
}
```

55. [expression matter](https://www.codewars.com/kata/5ae62fcf252e66d44d00008e/train/java)
```java
public class Kata {
  public static int expressionsMatter(int a, int b, int c) {
    return Math.max(
      Math.max(a + b + c, a * b * c),
      Math.max(a + b * c, Math.max(a * (b + c), (a + b) * c))
    );
  }
}
```

56. [My head is at the wrong end](https://www.codewars.com/kata/56f699cd9400f5b7d8000b55/train/java)
```java
public class Kata {
  public static int[] fixTheMeerkat(String[] items) {
    return new String[]{items[2], items[1], items[0]};
  }
}
```
57. [short long short](https://www.codewars.com/kata/50654ddff44f800200000007/train/java)
```java
public class ShortLongShort {
  public static String solution(String a, String b) {
    if (a.length() < b.length()) {
      return a + b + a;
    } else {
      return b + a + b;
    }
  }
}
```

58. [get the nth even number](https://www.codewars.com/kata/5933a1f8552bc2750a0000ed/train/java)
```java
public class Kata {
  public static int nthEven(int n) {
    return (n - 1) * 2;
  }
}
```

59. [stringy strings](https://www.codewars.com/kata/563b74ddd19a3ad462000054/train/java)
```java 
public class Kata {
  public static String stringy(int size) {
    StringBuilder result = new StringBuilder();
    for (int i = 0; i < size; i++) {
      result.append(i % 2 == 0 ? "1" : "0");
    }
    return result.toString();
  }
}

```

60. [Find numbers which are divisible by given number](https://www.codewars.com/kata/55edaba99da3a9c84000003b/train/java)
```java 
import java.util.*;

public class EvenNumbers {
    public static int[] divisibleBy(int[] numbers, int divisor) {
        List<Integer> res = new ArrayList<>();
        for (int element : numbers) {
            if (element % divisor == 0) {
                res.add(element);
            }
        }
        
        return res.stream().mapToInt(Integer::intValue).toArray();
    }
}
```

61. [convert to binary](https://www.codewars.com/kata/59fca81a5712f9fa4700159a/train/java)
```java 
public class Kata {
    public static int toBinary(int b) {
        String binaryString = Integer.toBinaryString(b);
        int result = Integer.parseInt(binaryString);
        
        return result;
    }

}
```

62. [to square or not to square](https://www.codewars.com/kata/57f6ad55cca6e045d2000627/train/java)
```java 
    public static int[] squareOrSquareRoot(int[] array) {
        int[] result = new int[array.length];
        for (int i = 0; i < array.length; i++) {
            double sqrt = Math.sqrt(array[i]);
            if (sqrt == (int) sqrt) {
                result[i] = (int) sqrt;
            } else {
                result[i] = array[i] * array[i];
            }
        }
        return result;
    }

```
63. [calculate surface and area of a boxe](https://www.codewars.com/kata/565f5825379664a26b00007c/train/java)
```java
public class Kata {
    public static int[] getSize(int width, int height, int depth) {
        int surfaceArea = 2 * (width * height + width * depth + height * depth);
        int volume = width * height * depth;
        return new int[] {surfaceArea, volume};
    }
}
```

64. [calculate area of a square](https://www.codewars.com/kata/5748838ce2fab90b86001b1a/train/java)
```java
public class Geometry{
  public static double squareArea(double A){
    double r = (2 * A) / Math.PI;
    double area = r * r;
    return Math.round(area * 100.0) / 100.0;
  }
}
```

65. [color Ghost](https://www.codewars.com/kata/53f1015fa9fe02cbda00111a/train/java)
```java
import java.util.*;

public class Ghost {
    public static final String[] COLORS = {"yellow", "red", "white", "purple"};
    private String color;

    public Ghost() {
        Random rand = new Random();
        this.color = COLORS[rand.nextInt(COLORS.length)];
    }

    public String getColor() {
        return this.color; 
    }
}
```
```java 
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

class SolutionTest {
    @Test
    void testColorIsValid() {
        Ghost ghost = new Ghost();
        String color = ghost.getColor();
        assertTrue(
            color.equals("white") || color.equals("yellow") ||
            color.equals("purple") || color.equals("red")
        );
    }
}
```

66. [Simple Calculator](https://www.codewars.com/kata/5810085c533d69f4980001cf/train/java)
```java 
public class Calculator {
  public static double calculate(double a, double b, String op) {
    switch(op) {
      case "+":
        return a + b;
      case "-":
        return a - b;
      case "*":
        return a * b;
      case "/":
        if (b != 0) return a / b;
        throw new IllegalArgumentException("Cannot divid by zero");
      default:
        throw new IllegalArgumentException("Invalid operator");
    }
  }
}
```
67.[Sort and Star](https://www.codewars.com/kata/57cfdf34902f6ba3d300001e/solutions/java)
```java
import java.util.Arrays;

public class SortAndStar {

  public static String twoSort(String[] s) {
    // Trier le tableau
    Arrays.sort(s);
    // Prendre la première chaîne
    String first = s[0];
    // Construire la chaîne avec "***" entre les lettres
    StringBuilder sb = new StringBuilder();
    for (int i = 0; i < first.length(); i++) {
      sb.append(first.charAt(i));
      if (i < first.length() - 1) {
        sb.append("***");
      }
    }
    return sb.toString();
  }

}
```

68. [remove an element from an array](https://www.codewars.com/kata/5769b3802ae6f8e4890009d2/train/java)
```java
import java.util.Arrays;
public class Kata {

  public static Object[] removeEveryOther(Object[] arr) {
    int newSize = (arr.length + 1) / 2;
    Object[] result = new Object[newSize];
    for (int i = 0, j = 0; i < arr.length; i += 2, j++) {
      result[j] = arr[i];
    }

    return result;
  }

}

```
69. [printing array elements with comma delimiters](https://www.codewars.com/kata/56e2f59fb2ed128081001328/train/javascript)
```java
public class ArrayPrinter {

    public static String printArray(Object[] array) {
        String res = "";
        for (int i = 0; i < array.length; i++) {
            res += array[i];
            if (i != array.length - 1) {
                res += ",";
            }
        }
        return res;
    }
}
```

70. [Count the monkeys](https://www.codewars.com/kata/56f69d9f9400f508fb000ba7/train/java)
```java 
public class MonkeyCounter {
    public static int[] monkeyCount(final int n) {
        int[] res = new int[n];
        for (int i = 0; i < n; i++) {
            res[i] = i + 1;
        }
        return res;
    }
}
```

71. [remove duplicates from an array](https://www.codewars.com/kata/57a5b0dfcf1fa526bb000118/train/java)
```java
public class Solution {
  public static int[] distinct(int[] values) {
    int[] res = new int[values.length];
    int j = 0;
    for (int i = 0; i < values.length; i++) {
      boolean found = false;
      for (int k = 0; k < j; k++) {
        if (res[k] == values[i]) {
          found = true;
          break;
        }
      }
      if (!found) {
        res[j] = values[i];
        j++;
      }
    }
    int[] resf = new int[j];
    for (int i = 0; i < j; i++) {
      resf[i] = res[i];
    }
    return resf;
  }
}
```

72. [Greet](https://www.codewars.com/kata/56f69f9a0e947263f3000052/train/java)
```java 
class Kata {
    static String greet(String name, String owner) {
        return name.equals(owner) ? "Hello boss" : "Hello guest";
    }
}
```

73. [classy extensions]()
```java
public class Cat extends Animal{
  public Cat(String name){
    super(name);
  }
  public String speak(){
    return this.name + " meows.";
  }
}
```
74. [calculate student final grade](https://www.codewars.com/kata/5ad0d8356165e63c140014d4/train/java)
```java
public class StudentFinalGrade{

    public static int finalGrade(int exam, int projects) {
        if (exam > 90 || projects > 10) {
            return 100;
        } else if (exam > 75 && projects >= 5) {
            return 90;
        } else if (exam > 50 && projects >= 2) {
            return 75;
        } else {
            return 0;
        }
    }

}
```
75. [classic hello world](https://www.codewars.com/kata/57036f007fd72e3b77000023/train/java)
```java 
public class Solution {
  public static String main(String args) {
    return String.format("Hello World!");
  }
}
```

76. [making 6 toasts](https://www.codewars.com/kata/5834fec22fb0ba7d080000e8/train/java)
```java
public class Kata{
  public static int sixToast(int num){
    return Math.abs(num-6);
  }
}
```
77. [filtering even numbers](https://www.codewars.com/kata/566dc566f6ea9a14b500007b/train/java)
```java
import java.util.List;

public class Kata13December {
    public static List<Integer> filterOddNumber(List<Integer> listOfNumbers)
    {
        return listOfNumbers.stream().filter(element-> element %2!=0).toList();
    }
}
```

78. [exlamation marks](https://www.codewars.com/kata/57fb09ef2b5314a8a90001ed/train/java)
```java 
public class Solution {
    public static String replace(final String s) {
        String vowels = "aeiouAEIOU";
        String result = "";

        for (int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            if (vowels.indexOf(c) != -1) {
                result += "!";
            } else {
                result += c;
            }
        }

        return result;
    }
}
```

79. [draw stairs](https://www.codewars.com/kata/5b4e779c578c6a898e0005c5/train/java)
```java 
public class Stairs {
    public static String draw(int n) {
        String result = "";
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < i; j++) {
                result += " ";
            }
            result += "I";
            if (i != n - 1) {
                result += "\n";
            }
        }
        return result;
    }
    public static void main(String[] args) {
        System.out.println(draw(7));
    }
}
```

80. [sum the strings ](https://www.codewars.com/kata/5966e33c4e686b508700002d/train/java) 
```java
public class Kata{
  
  public static String sumStr(String a, String b){ 
        int num1 = a.isEmpty() ? 0 : Integer.parseInt(a);
        int num2 = b.isEmpty() ? 0 : Integer.parseInt(b);
        return String.valueOf(num1 + num2);
  }
 
}
```

81. [String cleaning](https://www.codewars.com/kata/57e1e61ba396b3727c000251/train/java)
```java 
public class StringCleaning {
    public static String stringClean(String str) {
        return str.replaceAll("[0-9]", "");
    }
}
```
82. [age range equation](https://www.codewars.com/kata/5803956ddb07c5c74200144e/train/java)
```java
public class Kata{
  public static String datingRange(int age) {
     int min, max;

        if (age <= 14) {
            min = (int) Math.floor(age - age * 0.10);
            max = (int) Math.floor(age + age * 0.10);
        } else {
            min = (int) Math.floor(age / 2.0 + 7);
            max = (int) Math.floor((age - 7) * 2);
        }

        return min + "-" + max;
  }
}
```
83. [is it digit](https://www.codewars.com/kata/567bf4f7ee34510f69000032/train/java)
```java
public class StringUtils {
    public static boolean isDigit(String s) {
        return s != null && s.length() == 1 && Character.isDigit(s.charAt(0));
    }
}
```

84.[you only need one](https://www.codewars.com/kata/57cc975ed542d3148f00015b/train/java)
```java 
import java.util.*;
public class Solution {
    public static boolean check(Object[] a, Object x) {
        return Arrays.asList(a).contains(x);
    }
}
```
85. [return substring instance count](https://www.codewars.com/kata/5168b125faced29f66000005/train/java)
```java 
public class Solution {
    public static int substringCount(String fullText, String searchText) {
        if (searchText == null || searchText.isEmpty()) return 0;
        int count = 0;
        int index = 0;
        while ((index = fullText.indexOf(searchText, index)) != -1) {
            count++;
            index += searchText.length(); 
        }
        return count;
    }
}
```

86. [find the integral](https://www.codewars.com/kata/59811fd8a070625d4c000013/train/java)
```java
public class Kata {
    public static String integrate(int coefficient, int exponent) {
        return (coefficient / (exponent + 1)) + "x^" + (exponent + 1);
    }
}
```

87. [Convert US dollars to CNY](https://www.codewars.com/kata/5977618080ef220766000022/train/java)
```java
public class Kata {
    public static String usdcny(double usd) {
        double res = usd * 6.75;
        return String.format("%.2f Chinese Yuan", res);
    }
}

```

88. [add length](https://www.codewars.com/kata/559d2284b5bb6799e9000047/train/java)
```java
public class AddLength{
  public static String[] addLength(String[] str) {
    String[] res = str.split(" ");
    for (int i=0; i<res.length; i++){
      res[i] = re[i] + " " + res[i].length();
    }
}}
```

89. [drink about age](https://www.codewars.com/kata/56170e844da7c6f647000063/train/java)
```java 
public class Drinks {
    public static String peopleWithAgeDrink(int age) {
        if (age < 14) {
            return "drink toddy";
        } else if (age < 18) {
            return "drink coke";
        } else if (age < 21) {
            return "drink beer";
        } else {
            return "drink whisky";
        }
    }
}
```

90. [if else syntaxe](https://www.codewars.com/kata/57089707fe2d01529f00024a/train/java)
```java 
public class Solution {
  public static boolean checkAlive(int health) {
    return health > 0 ? true : false;
  }
}
```

91. [plural](https://www.codewars.com/kata/52ceafd1f235ce81aa00073a/train/java)
```java 
public class Plural{
  public static boolean isPlural(float f){
    return true && f!= 1.0;
  }
}
```
92. [counting characters](https://www.codewars.com/kata/55f1b763dd670651620000ce/train/java)
```java
interface Count {
	static int countCharOccurrences(String s, char c) {
    int cpt = 0;
    for( int i = 0; i<s.length(); i++){
      if(s.charAt(i) ==  c){
        cpt++;
      }
    }
    return cpt;
  }
}
```

93. [return the days of the week](https://www.codewars.com/kata/59dd3ccdded72fc78b000b25/train/java)
```java
public class DayOfWeek {

    public static String getDay(int n) {
        switch(n){
            case 1:
              return "Sunday";
            case 2:
              return "Monday";
            case 3:
              return "Tuesday";
            case 4: 
              return "Wednesday";
            case 5: 
              return "Thursday";
            case 6:
              return "Friday";
            case 7:
              return "Saturday";
            default:
              return "Wrong, please enter a number between 1 and 7";
          }
        }
 }
```

94. [Multiply table of number ](https://www.codewars.com/kata/5a2fd38b55519ed98f0000ce/train/java)
```java
public class Kata {
    public static String multiTable(int num) {
        int i = 1;
        String res = "";
        while (i <= 10) {
            res += i + " * " + num + " = " + (i * num);
            if (i != 10) res += "\n"; 
            i++;
        }
        return res;
    }
}
```

95. [fix the bug of infinished loop](https://www.codewars.com/kata/55c28f7304e3eaebef0000da/train/java)
```java
import java.util.*;

class Kata {
    public static List<Integer> CreateList(int number) {
        List<Integer> list = new ArrayList<>(number);

        for (int count = 1; count <= number;count++) {
            list.add(count);
        }
        return list;
    }
}
```
96. [delete zeros at the and of a number](https://www.codewars.com/kata/570a6a46455d08ff8d001002/train/java)
```java
public class NoBoring {
    public static int noBoringZeros(int n) {
        if (n == 0) return 0;
        while (n % 10 == 0) {
            n /= 10;
        }
        return n;
    }
}
```
97. [tip calculator](https://www.codewars.com/kata/56598d8076ee7a0759000087/train/java)
```java 
public class TipCalculator {
    public static Integer calculateTip(double amount, String rating) {
        if (rating == null) return null;
        switch (rating.toLowerCase()) {
            case "terrible":
                return 0;
            case "poor":
                return (int) Math.ceil(amount * 0.05);
            case "good":
                return (int) Math.ceil(amount * 0.10);
            case "great":
                return (int) Math.ceil(amount * 0.15);
            case "excellent":
                return (int) Math.ceil(amount * 0.20);
            default:
                return null;
        }
    }
}
```
98. [sum of multiples](https://www.codewars.com/kata/57241e0f440cd279b5000829/train/java)
```java
public class Kata {
    public static long sumMul(int n, int m) {
        if (n <= 0 || m <= 0) {
            throw new IllegalArgumentException("n and m must be greater than 0");
        }
        int i = 1;
        long res = 0;
        while (n * i < m) {
            res += n * i;
            i++;
        }
        return res;
    }
}
```
100. [count odd numbers](https://www.codewars.com/kata/59342039eb450e39970000a6/train/java)
```java 
public class Kata {

  public static int oddCount(int n){

    return n/2;
  }

}
```
101. [smallest unused ID](https://www.codewars.com/kata/55eea63119278d571d00006a/train/java)
```java
import java.util.HashSet;

public class Kata {
    public static int nextId(int[] ids) {
        HashSet<Integer> used = new HashSet<>();
        for (int id : ids) {
            if (id >= 0) {
                used.add(id);
            }
        }
        int smallest = 0;
        while (used.contains(smallest)) {
            smallest++;
        }
        return smallest;
    }
}
```
102. [remove time from a date](https://www.codewars.com/kata/56b0ff16d4aa33e5bb00008e/train/java)
```java

import java.util.Arrays;

public class Solution {
  public static String shortenToDate(String longDate) {
    String[] res = new String[1];
    String[] str = longDate.split(",");
    res[0] = str[0].trim();
    
    return String.join("", res);
  }
}
```
103. [generate range of integers](https://www.codewars.com/kata/55eca815d0d20962e1000106/train/java)
```java
public class Solution {
    public static int[] generateRange(int start, int stop, int step) {
        int size = ((stop - start) / step) + 1;
        int[] range = new int[size];
        int index = 0;
        for (int i = start; i <= stop; i += step) {
            range[index++] = i;
        }
        return range;
    }
}
```

104. [A strange trip to the market](https://www.codewars.com/kata/55ccdf1512938ce3ac000056/train/java)
```java
public class Nessie{
    public static boolean isLockNessMonster(String s) {
        String lower = s.toLowerCase();
        return lower.contains("tree fiddy") || lower.contains("3.50") || lower.contains("three fifty");
    }
}
```
105. [check if the period is late](https://www.codewars.com/kata/578a8a01e9fd1549e50001f1/train/java)
```java
import java.time.LocalDate;
import java.time.temporal.ChronoUnit;

public class PeriodTime {
    public static boolean periodIsLate(LocalDate last, LocalDate today, int cycleLength) {
        long daysBetween = ChronoUnit.DAYS.between(last, today);
        return daysBetween > cycleLength;
    }
}
```
106. [compare within margin](https://www.codewars.com/kata/56453a12fcee9a6c4700009c/train/java)
```java
public class Solution {

  public static int closeCompare(double a, double b) {
    return closeCompare(a, b, 0.00001); // marge par défaut
  }
  
  public static int closeCompare(double a, double b, double margin) {
    if (Math.abs(a - b) <= margin) {
      return 0;
    } else if (a > b) {
      return 1;
    } else {
      return -1;
    }
  }
}
```

108. [leo and oscar](https://www.codewars.com/kata/56d49587df52101de70011e4/train/java)
```java 
public class Kata
{
  public static String leo(final int oscar)
  {
    if (oscar == 88){
      return "Leo finally won the oscar! Leo is happy";
    }
    else if(oscar == 86){
      return "Not even for Wolf of wallstreet?!";
    }
    else if(oscar <88){
      return "When will you give Leo an Oscar?";
    }else{
      return "Leo got one already!";
    }
    
  }
}
```

109. [is it a number ](https://www.codewars.com/kata/57126304cdbf63c6770012bd/train/java)
```java 
public class MyUtilities {

    public boolean isDigit(String s) {
        try {
            Double.parseDouble(s); 
            return true;
        } catch (NumberFormatException e) {
            return false;
        }
    }
}
```
110. [validator of username with regex](https://www.codewars.com/kata/56a3f08aa9a6cc9b75000023/solutions/java)
```java 
public class ZywOo {
  public static boolean validateUsr(String s) {
    return s.matches("[a-z_\\d]{4,16}");
  }
}
```

111. [replace `.` by `_`](https://www.codewars.com/kata/596c6eb85b0f515834000049/train/java)
```java 
public class Dinglemouse {

  public static String replaceDots(final String str) {
    return str.replaceAll("\\.", "-");
  }
  
}
```

112. [Playing with cubes]()
```java 
public class Cube
{
    private int Side = 0;
    public int GetSide(){
        return Side;
    }
    public void SetSide(int num)
    {
        Side = num;
    }
}
```

113. [Twice as old](https://www.codewars.com/kata/5b853229cfde412a470000d0/train/java)
```java
public class TwiceAsOld {
  public static int TwiceAsOld(int dadYears, int sonYears) {
    return Math.abs(dadYears - 2 * sonYears);
  }
}
```
114. [Cirles in polygons]()
```java 
function maxCircleDiameter(sides, sideLength) {
  return sideLength / Math.tan(Math.PI / sides);
}
```

115. [forme phythagorean triple](https://www.codewars.com/kata/5951d30ce99cf2467e000013/train/java)
```java 
import java.util.*;
public class PythagoreanTriple {
    public static int pythagoreanTriple(int[] numbers) {
        if (numbers.length != 3) return 0;
        Arrays.sort(numbers);

        int a = numbers[0];
        int b = numbers[1];
        int c = numbers[2];

        return (a * a + b * b == c * c) ? 1 : 0;
    }
}
```
116. [CSV representation of an array](https://www.codewars.com/kata/5a34af40e1ce0eb1f5000036/solutions/java)
```java
public class Kata {
  public static String toCsvText(int[][] array){
     StringBuilder sb= new StringBuilder();
        for(int i=0; i< array.length ; i++) {
            for (int j = 0; j < array[i].length; j++) {
                sb.append(array[i][j]);
                if (j < array[i].length-1) {
                    sb.append(",");
                }
            }
            if (i < array.length-1) {
                sb.append("\n");
            }
        }
        return sb.toString();
  }
}
```

117. [quarter of the year](https://www.codewars.com/kata/5ce9c1000bab0b001134f5af/train/java)
```java 
public class Kata {
    public static int quarterOf(int month) {
        return (month + 2) / 3;
    }
}
```

118. [holiday](https://www.codewars.com/kata/57e92e91b63b6cbac20001e5/train/java)
```java 
public class Kata {
  public static int dutyFree(int normPrice, int discount, int holidayCost) {
    double savingsPerBottle = normPrice * (discount / 100.0);
    return (int)(holidayCost / savingsPerBottle);
  }
}
```
119. [Pillars](https://www.codewars.com/kata/5bb0c58f484fcd170700063d/train/java)
```java 
public class Kata {
  public static int pillars(int n, int distance, int width) {
    if (n <= 1) return 0;
    return (n - 1) * distance * 100 + (n - 2) * width;
  }
}
```

120. [Will you make it](https://www.codewars.com/kata/5861d28f124b35723e00005e/train/java)
```java
public class Kata {
    public static boolean zeroFuel(int distanceToPump, int mpg, int fuelLeft) {
        return mpg * fuelLeft >= distanceToPump;
    }
}

```
121. [](https://www.codewars.com/kata/55cbc3586671f6aa070000fb)
```java
public class Kata {
    public static boolean checkForFactor(int base, int factor) {
        return base % factor == 0;
    }
}
```