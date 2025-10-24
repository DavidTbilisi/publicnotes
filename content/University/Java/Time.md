
 (§2.12)

```java
// Milliseconds since 00:00:00 UTC, Jan 1, 1970 (the epoch).
System.currentTimeMillis()
```
[Easier method - Java Date and Time](https://www.w3schools.com/java/java_date.asp)

- ms -> s : /1000
- s -> m : /60
- m -> h : /60
- h -> day : /24
- withinValue = biggerUnit % divisor
- accumulate = biggerUnit / divisor


```java
public class Main {  
    public static void main(String[] args) {  
        // Obtain the total milliseconds since midnight, Jan 1, 1970 (the Unix epoch)  
        // System.currentTimeMillis() returns the number of milliseconds since that moment in GMT        
        // ms → s → m → h        
        byte timezone = 4; // Tbilisi +4  
        long ms = System.currentTimeMillis();  
        long totalSeconds = ms / 1000; // Remove 1000  
        long currentSecond = totalSeconds % 60; // Pop   
		long totalMinutes = totalSeconds / 60; // Remove (what we have taken prev)  
        long currentMinute = totalMinutes % 60; // Pop   
		long totalHours = totalMinutes / 60; // Remove  
        long currentHour = totalHours % 24 + timezone; // Pop   
        // zero-pad: 08:05:03        
        String time = String.format("%02d:%02d:%02d", currentHour, currentMinute, currentSecond);  
        System.out.println("Current time is " + time);  
    }  
}
```