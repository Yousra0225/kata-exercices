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
