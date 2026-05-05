# Case 9: Move Method

## Before Refactoring

```java
class Customer {

    private String name;

    public String getName() {

        return name;
    }
}

class Order {

    private Customer customer;

    public String getCustomerName() {

        return customer.getName();
    }
}
```