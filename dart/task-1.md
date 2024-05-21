# Task 1: Messy Function

## Introduction

The function processData in the DataProcessor class is responsible for handling data processing, but it's grown into a tangled mess of nested loops, conditionals, and variable assignments. It's hard to follow and violates the Single Responsibility Principle.

## Hint

- Break down the processData function into smaller, focused methods, each responsible for a single task.
- Use meaningful names for variables and methods to improve readability.
- Consider extracting repetitive code into helper methods or utility classes.

## Code

```dart
class DataProcessor {
  void processData(List<String> data) {
    for (int i = 0; i < data.length; i++) {
      if (data[i].startsWith('A')) {
        print('Processing A: ${data[i]}');
        // More complex processing logic here
        if (data[i].contains('X')) {
          // Handle special case
        } else {
          // Handle regular case
        }
      } else if (data[i].startsWith('B')) {
        print('Processing B: ${data[i]}');
        // More complex processing logic here
      } else {
        print('Unknown data: ${data[i]}');
      }
    }
  }
}
```
