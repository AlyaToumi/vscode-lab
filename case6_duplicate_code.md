# Case 6: Eliminating Duplicate Code

## Before Refactoring

```java
class OrderProcessor {

    public double calculateTotal(Order order) {

        double total = 0;

        for (Item item : order.getItems()) {

            total += item.getPrice() * item.getQuantity();
        }

        return total;
    }
}

class InvoiceGenerator {

    public double calculateTotal(Order order) {

        double total = 0;

        for (Item item : order.getItems()) {

            total += item.getPrice() * item.getQuantity();
        }

        return total;
    }
}
```

## After Refactoring

```java
class OrderUtils {

    public static double calculateTotal(Order order) {

        double total = 0;

        for (Item item : order.getItems()) {

            total += item.getPrice() * item.getQuantity();
        }

        return total;
    }
}

class OrderProcessor {

    public double calculateTotal(Order order) {

        return OrderUtils.calculateTotal(order);
    }
}

class InvoiceGenerator {

    public double calculateTotal(Order order) {

        return OrderUtils.calculateTotal(order);
    }
}
```

## Benefits of Refactoring

- Removes duplicated code.
- Centralizes the calculation logic in one place.
- Makes future changes easier.
- Improves maintainability.
- Reduces the risk of mistakes.