# Task 1: Complex Conditional Logic AKA Spaghetti Code

## Introduction

Introduction: This function calculates the discount for an order based on various conditions. The nested if-else statements make the logic hard to follow and maintain.

## Hint

- Simplify the logic by breaking it down into smaller functions.
- Use guard clauses to handle edge cases early.
- Make use of descriptive function names to clarify the purpose of each block of logic.

## Code

```javascript
function calculateDiscount(order) {
  let discount = 0;
  if (order.customer.isPremium) {
    if (order.total > 100) {
      discount = order.total * 0.2;
    } else {
      if (order.total > 50) {
        discount = order.total * 0.1;
      }
    }
  } else {
    if (order.total > 200) {
      discount = order.total * 0.15;
    } else {
      if (order.total > 100) {
        discount = order.total * 0.05;
      }
    }
  }
  return discount;
}
```
