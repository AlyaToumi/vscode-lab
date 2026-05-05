# Case 10: Singleton Pattern

## After Refactoring

```java
public class DatabaseConnection {

    private static DatabaseConnection instance;

    private DatabaseConnection() {

        System.out.println("Database connected");
    }

    public static DatabaseConnection getInstance() {

        if (instance == null) {

            instance = new DatabaseConnection();
        }

        return instance;
    }
}
```