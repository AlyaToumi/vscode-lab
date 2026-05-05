# Case 1: Rename Variables / Methods

## Before Refactoring

```java
public class Calculator {
    public double calc(double a, double b) {
        double x = a + b;
        double y = a * b;
        return x / y;
    }

    public void prtRes(double res) {
        System.out.println("Result: " + res);
    }
}
```
