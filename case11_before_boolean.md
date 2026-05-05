# Case 11: Simplify Boolean Expressions

## Before Refactoring

```java
public class AccessManager {

    public boolean canAccess(boolean isAdmin) {

        if (isAdmin == true) {

            return true;

        } else {

            return false;
        }
    }
}
```