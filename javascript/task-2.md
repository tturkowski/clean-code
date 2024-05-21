# Long Function

## Introduction

This function processes an order, including validating the order, processing the payment, and shipping the order. The single long function makes it hard to understand and maintain.

## Hint

- Break the function into smaller, single-responsibility functions.
- Extract repeated code into helper functions.
- Ensure each function name clearly describes its purpose.

## Code

```javascript
function processOrder(order) {
  if (!order.id || !order.items) {
    throw new Error("Invalid order");
  }

  if (!order.paymentDetails) {
    throw new Error("Payment details missing");
  }

  const paymentResult = processPayment(order.paymentDetails);
  if (!paymentResult.success) {
    throw new Error("Payment failed");
  }

  if (!order.shippingAddress) {
    throw new Error("Shipping address missing");
  }

  const shipmentResult = shipOrder(order);
  if (!shipmentResult.success) {
    throw new Error("Shipment failed");
  }

  console.log("Order processed successfully");
}
```
