# Task 5: Improve Variable Naming

## Introduction

The variable names in the DataProcessor class are unclear and do not convey their purpose effectively, making the code hard to understand. Improve the variable names for better readability and maintainability.

## Hint

- Rename variables to be more descriptive and expressive, conveying their purpose and intent.
- Use nouns for variables representing objects and verbs for methods and functions.
- Avoid abbreviations and acronyms unless they are universally understood in the context of the project.

## Code

```dart
class DataProcessor {
  void processData(List<String> data) {
    for (int i = 0; i < data.length; i++) {
      String item = data[i];
      if (item.startsWith('A')) {
        print('Processing item starting with A: $item');
      } else if (item.startsWith('B')) {
        print('Processing item starting with B: $item');
      } else {
        print('Unknown item: $item');
      }
    }
  }
}
```
