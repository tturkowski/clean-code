# Task 3: Simplify Complex Conditionals

## Introduction

The validateUser method in the UserValidator class contains nested conditionals that make it hard to understand and maintain. It's prone to bugs and difficult to test.

## Hint

- Refactor complex conditionals into separate methods with descriptive names.
- Use guard clauses to handle edge cases early and simplify the main logic.
- Consider using a validation library or framework to simplify validation logic.

## Code

```dart
class UserValidator {
  bool validateUser(User user) {
    if (user != null) {
      if (user.age >= 18) {
        if (user.country == 'USA' || user.country == 'Canada') {
          if (user.subscriptionType == 'Premium') {
            return true;
          } else {
            return false;
          }
        } else {
          return false;
        }
      } else {
        return false;
      }
    } else {
      return false;
    }
  }
}
```
