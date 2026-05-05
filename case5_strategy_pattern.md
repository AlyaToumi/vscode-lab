# Case 5: Simplify Conditionals using Strategy Pattern

## Before Refactoring

```java
public class PaymentProcessor {

    public void processPayment(
        String paymentMethod,
        double amount
    ) {

        if (paymentMethod.equals("CreditCard")) {

            System.out.println(
                "Processing credit card payment of $" + amount
            );

        } else if (paymentMethod.equals("PayPal")) {

            System.out.println(
                "Processing PayPal payment of $" + amount
            );

        } else if (paymentMethod.equals("Bitcoin")) {

            System.out.println(
                "Processing Bitcoin payment of $" + amount
            );

        } else {

            throw new IllegalArgumentException(
                "Unknown payment method"
            );
        }
    }
}
```

## After Refactoring

```java
interface PaymentStrategy {

    void pay(double amount);
}

class CreditCardPayment
    implements PaymentStrategy {

    @Override
    public void pay(double amount) {

        System.out.println(
            "Processing credit card payment of $" + amount
        );
    }
}

class PayPalPayment
    implements PaymentStrategy {

    @Override
    public void pay(double amount) {

        System.out.println(
            "Processing PayPal payment of $" + amount
        );
    }
}

class BitcoinPayment
    implements PaymentStrategy {

    @Override
    public void pay(double amount) {

        System.out.println(
            "Processing Bitcoin payment of $" + amount
        );
    }
}

class PaymentProcessor {

    private PaymentStrategy paymentStrategy;

    public void setPaymentStrategy(
        PaymentStrategy paymentStrategy
    ) {

        this.paymentStrategy = paymentStrategy;
    }

    public void processPayment(double amount) {

        paymentStrategy.pay(amount);
    }
}
```

## Benefits of Refactoring

- Removes large conditional statements.
- Improves flexibility.
- Makes adding new payment methods easier.
- Follows the Open/Closed Principle.
- Improves maintainability and readability.