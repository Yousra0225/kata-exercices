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