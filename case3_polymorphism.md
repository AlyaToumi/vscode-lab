# Case 3: Replace Conditional with Polymorphism

## Before Refactoring

```java
public class Employee {

    public double calculateBonus(String type) {

        if (type.equals("Manager")) {

            return 5000;

        } else if (type.equals("Developer")) {

            return 3000;

        } else {

            return 1000;
        }
    }
}
```

## After Refactoring

```java
abstract class Employee {

    abstract double calculateBonus();
}

class Manager extends Employee {

    @Override
    double calculateBonus() {

        return 5000;
    }
}

class Developer extends Employee {

    @Override
    double calculateBonus() {

        return 3000;
    }
}

class Intern extends Employee {

    @Override
    double calculateBonus() {

        return 1000;
    }
}
```

## Benefits of Refactoring

- Removes complex conditional statements.
- Improves readability and maintainability.
- Makes adding new employee types easier.
- Follows the Open/Closed Principle.
```