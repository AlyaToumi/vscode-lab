# Case 7: Replace Magic Numbers with Constants

## After Refactoring

```java
public class Circle {

    private static final double PI = 3.14159;

    public double calculateArea(double radius) {

        return PI * radius * radius;
    }
}
```