# Flutter Navigation and Routing Practice

This Flutter project demonstrates basic navigation and routing between two screens: `FirstPage` and `HomePage`. It includes named routes and navigation using buttons.

## Getting Started

These instructions will help you set up and run the project on your local machine.

### Prerequisites

- Flutter SDK: [Install Flutter](https://flutter.dev/docs/get-started/install)
- Dart SDK (included with Flutter)
- An IDE with Flutter support (e.g., VSCode, Android Studio)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Isaiah-Essien/Let-s_route.git
    cd Let-s_route
    ```

2. Install dependencies:
    ```bash
    flutter pub get
    ```

3. Run the app:
    ```bash
    flutter run
    ```

## Project Structure

The project contains the following files:

- `main.dart`: Entry point of the application.
- `first_page.dart`: Defines the `FirstPage` widget.
- `home_page.dart`: Defines the `HomePage` widget.

### Link to Video  walk through for Product and list:
- https://youtu.be/kDUzB6uAKU0

### Link to video walk through of animation:
- https://www.loom.com/share/f00ce8e55cb84ab08a920af0f36b3885?sid=efc5aab2-a30b-402a-bf6a-993820d4ef4d
### `main.dart`

```dart
import 'package:flutter/material.dart';
import 'package:lets_route/pages/first_page.dart';
import 'package:lets_route/pages/home_page.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      theme: ThemeData(
        primaryColor: Colors.deepPurple,
        appBarTheme: const AppBarTheme(
          backgroundColor: Color(0xFF00A89B),
          titleTextStyle: TextStyle(
            color: Colors.white,
            fontSize: 20,
            fontWeight: FontWeight.bold,
          ),
          iconTheme: IconThemeData(color: Colors.white),
        ),
        elevatedButtonTheme: ElevatedButtonThemeData(
          style: ElevatedButton.styleFrom(
            backgroundColor: Color(0xFF004B5C),
            foregroundColor: Colors.white,
          ),
        ),
        textButtonTheme: TextButtonThemeData(
          style: TextButton.styleFrom(
            foregroundColor: Colors.white,
          ),
        ),
      ),
      home: const FirstPage(),
      routes: {
        '/firstpage': (context) => const FirstPage(),
        '/homepage': (context) => const HomePage(),
      },
    );
  }
}
