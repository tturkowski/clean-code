# Task 5: Complex Conditional Logic and Lack of Encapsulation

## Introduction

Welcome to Task 5, our final task! In this task, we'll be addressing complex conditional logic and lack of encapsulation. Complex conditional statements can make code difficult to understand and maintain, while lack of encapsulation can lead to code duplication and brittleness. We'll explore strategies to refactor the code to improve clarity and maintainability.

## Hint

- Look for opportunities to simplify conditional logic.
- Consider encapsulating conditional behavior into separate classes or functions.

## Code

```php
function getDiscountedPrice($userType, $totalAmount) {
    if ($userType == 'regular') {
        if ($totalAmount > 1000) {
            $discount = 0.1;
        } else {
            $discount = 0.05;
        }
    } elseif ($userType == 'premium') {
        if ($totalAmount > 1000) {
            $discount = 0.15;
        } else {
            $discount = 0.1;
        }
    } elseif ($userType == 'vip') {
        if ($totalAmount > 1000) {
            $discount = 0.2;
        } else {
            $discount = 0.15;
        }
    } else {
        $discount = 0;
    }

    return $totalAmount - ($totalAmount * $discount);
}

echo getDiscountedPrice('vip', 1200);
echo getDiscountedPrice('regular', 500);
```
