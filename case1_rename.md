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

## After Refactoring

```java
public class Calculator {

    public double calculateSumProductRatio(double num1, double num2) {
        double sum = num1 + num2;
        double product = num1 * num2;
        return sum / product;
    }

    public void printResult(double result) {
        System.out.println("Result: " + result);
    }
}
```