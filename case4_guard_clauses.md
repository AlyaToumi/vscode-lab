# Case 4: Simplify Conditionals with Guard Clauses

## Before Refactoring

```java
public double calculateDiscount(Order order) {

    double discount = 0.0;

    if (order.getTotalAmount() > 100) {

        if (order.getCustomer().isPremium()) {

            discount = 0.2;

        } else {

            discount = 0.1;
        }
    }

    return discount;
}
```

## After Refactoring

```java
public double calculateDiscount(Order order) {

    if (order.getTotalAmount() <= 100) {

        return 0.0;
    }

    if (order.getCustomer().isPremium()) {

        return 0.2;
    }

    return 0.1;
}
```

## Benefits of Refactoring

- Reduces nested conditions.
- Makes the code easier to read.
- Uses early return.
- Makes the method shorter and clearer. 