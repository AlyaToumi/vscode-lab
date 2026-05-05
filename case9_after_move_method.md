# Case 9: Move Method

## After Refactoring

```java
class Customer {

    private String name;

    public String getName() {

        return name;
    }
}

class Order {

    private Customer customer;

    public Customer getCustomer() {

        return customer;
    }
}
```