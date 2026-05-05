# Case 8: Remove Dead Code

## Before Refactoring

```java
public class UserManager {

    public void printUser() {

        System.out.println("User printed");
    }

    public void unusedMethod() {

        System.out.println("This method is never used");
    }
}
```