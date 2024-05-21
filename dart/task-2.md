# Task 2: Refactor Monolithic Widget

## Introduction

The HomePage widget in the Flutter application is responsible for displaying various components such as user information, recent activities, and a list of products. However, the widget has grown too large and contains multiple unrelated responsibilities, violating the Single Responsibility Principle.

## Hint

- Identify distinct UI components within the HomePage widget and extract them into separate widgets.
- Use composition to combine smaller widgets into the HomePage.
- Apply the Flutter framework's layout and composition features to manage the relationships between widgets.

## Code

```dart
// Original Monolithic Widget
class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Home'),
      ),
      body: ListView(
        children: <Widget>[
          // User information
          Container(
            padding: EdgeInsets.all(16.0),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                Text('Welcome, John Doe', style: TextStyle(fontSize: 18.0)),
                Text('Email: john.doe@example.com', style: TextStyle(fontSize: 16.0)),
                // More user information
              ],
            ),
          ),
          // Recent activities
          Container(
            padding: EdgeInsets.all(16.0),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                Text('Recent Activities', style: TextStyle(fontSize: 18.0)),
                // List of recent activities
              ],
            ),
          ),
          // List of products
          Container(
            padding: EdgeInsets.all(16.0),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                Text('Featured Products', style: TextStyle(fontSize: 18.0)),
                // List of featured products
              ],
            ),
          ),
          // More components...
        ],
      ),
    );
  }
```
