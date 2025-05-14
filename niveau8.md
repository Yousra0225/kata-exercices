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