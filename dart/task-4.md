# Task 4: Simplify Complex Logic

## Introduction

The calculatePay method in the PayrollCalculator class calculates the pay for employees based on various factors such as hours worked, overtime, and bonuses. However, the method contains complex nested conditionals, making it hard to understand and maintain.

## Hint

- Refactor the complex logic in calculatePay into smaller, focused methods with descriptive names.
- Use guard clauses to handle edge cases and simplify the main logic flow.
- Consider using polymorphism or strategy pattern to replace conditional logic with polymorphic behavior.

## Code

```dart
class PayrollCalculator {
  double calculatePay(Employee employee) {
    double pay = 0;
    if (employee.hoursWorked <= 40) {
      pay = employee.hoursWorked * employee.hourlyRate;
    } else {
      pay = 40 * employee.hourlyRate +
            (employee.hoursWorked - 40) * employee.hourlyRate * 1.5;
    }
    if (employee.hasBonus) {
      pay += employee.bonusAmount;
    }
    if (employee.hasInsurance && !employee.has401k) {
      pay -= employee.insuranceDeduction;
    }
    if (employee.has401k) {
      pay -= employee._calculate401kDeduction();
    }
    return pay;
  }
}

class Employee {
  double hoursWorked;
  double hourlyRate;
  bool hasBonus;
  double bonusAmount;
  bool hasInsurance;
  bool has401k;
  double insuranceDeduction;

  double _calculate401kDeduction() {
    // Calculate 401k deduction based on employee's contribution
    // and employer matching
  }
}
```
