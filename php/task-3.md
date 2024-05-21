# Task 3: Hardcoded Configuration and Logic in the Controller

## Introduction

Welcome to Task 3! In this task, we'll be addressing hardcoded configuration and logic in the controller. Hardcoding configuration values and business logic directly into the controller can make the code less flexible and harder to test. We'll explore ways to refactor the code to separate concerns and improve maintainability.

## Hint

- Look for configuration values and logic that can be extracted.
- Consider using dependency injection to decouple components.

## Code

```php
class UserController {
    public function register() {
        $name = $_POST['name'];
        $email = $_POST['email'];

        // Validate input
        if (empty($name) || empty($email)) {
            die('Invalid input');
        }

        // Database connection
        $conn = new PDO('mysql:host=localhost;dbname=test', 'root', '');

        // Save to database
        $stmt = $conn->prepare('INSERT INTO users (name, email) VALUES (?, ?)');
        $stmt->execute([$name, $email]);

        // Send email
        mail($email, 'Welcome', 'Thank you for registering!');

        echo 'User registered successfully';
    }
}

$userController = new UserController();
$userController->register();
```
