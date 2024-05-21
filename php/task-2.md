# Task 2: Long Method with Mixed Responsibilities

## Introduction
Welcome to Task 2! In this task, we'll be tackling the issue of long methods with mixed responsibilities. Long methods can be difficult to understand and maintain, especially when they handle multiple tasks. By breaking down these methods into smaller, more focused functions, we can improve readability and simplify our codebase.

##  Hint

- Identify distinct responsibilities within the method.
- Consider creating separate functions for each responsibility.

## Code

```php
function processData($data) {
    // Validate data
    if (empty($data['name']) || empty($data['email'])) {
        return 'Invalid data';
    }

    // Save data
    $conn = new mysqli('localhost', 'user', 'password', 'database');
    if ($conn->connect_error) {
        return 'Connection failed: ' . $conn->connect_error;
    }
    $stmt = $conn->prepare("INSERT INTO users (name, email) VALUES (?, ?)");
    $stmt->bind_param("ss", $data['name'], $data['email']);
    $stmt->execute();

    // Send confirmation email
    mail($data['email'], 'Welcome!', 'Thanks for signing up!');

    return 'Success';
}

$response = processData(['name' => 'John', 'email' => 'john@example.com']);
echo $response;
```
