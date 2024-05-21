# Magic Numbers

## Introduction

This function uses several "magic numbers" without any explanation, making it hard to understand what these numbers represent.

## Hint

- Replace magic numbers with named constants.
- Ensure the names of the constants clearly describe their purpose.

## Code

```javascript
function calculateFinalPrice(price) {
  let tax = price * 0.2;
  let discount = price * 0.1;
  let finalPrice = price + tax - discount;
  return finalPrice;
}
```
