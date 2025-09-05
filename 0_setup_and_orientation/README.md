

# Core components 


- **Goal:** Explain what `main.dart`, `MaterialApp`, `Scaffold`, and `build` do.  
- **Accept:** `README.md` in repo with short explanations and a diagram of the widget tree. 


## main.dart

main.dart is the entry point of a Flutter application. It contains the main() function, which runs the app using runApp(). This file typically initializes the root widget (often a MaterialApp or CupertinoApp) and sets up the app’s structure.

## MaterialApp 

MaterialApp is a convenience widget that wraps several widgets commonly required for Material Design applications. It sets up navigation, theming, localization, and more. It’s often the root widget of the app.

Material Design is desin system developed by Google that provides guidelines for visual, motion and interaction design across platforms and services. So consistent layouts, responseive animations, bold colours and standardised UI components like buttons, cards and navigation elements. 

Key properties of the Material App include home (default route of the app - usually a scaffold), routes a map of routes for navigation, theme of data for the app etc.


## Scaffold 

Scaffold provides a high-level structure for Material Design apps. It includes slots for common layout elements like AppBar, Drawer, BottomNavigationBar, FloatingActionButton, and body.


| UI Component      | Flutter Widget         | How to Apply with MaterialApp Example                                     |
|-------------------|-----------------------|----------------------------------------------------------------------------|
| Button            | ElevatedButton, TextButton, OutlinedButton | Place inside Scaffold's body or actions.              |
| Card              | Card                  | Use as a child in Column, ListView, or GridView.                           |
| App Bar           | AppBar                | Assign to the `appBar` property of Scaffold.                               |
| Navigation Drawer | Drawer                | Assign to the `drawer` property of Scaffold.                               |
| Bottom Navigation | BottomNavigationBar    | Assign to the `bottomNavigationBar` property of Scaffold.                 |
| Floating Action   | FloatingActionButton   | Assign to the `floatingActionButton` property of Scaffold.                |
| List              | ListView              | Use as the body of Scaffold for scrollable lists.                          |
| Grid              | GridView              | Use as the body of Scaffold for grid layouts.                              |
| Snackbar          | SnackBar              | Show using `ScaffoldMessenger.of(context).showSnackBar(...)`.              |
| Dialog            | AlertDialog           | Show using `showDialog(context: ..., builder: ...)`.                       |
| Tab Bar           | TabBar, TabBarView    | Use with DefaultTabController and Scaffold's appBar and body.              |


## build 



The build() method is responsible for describing the widget tree based on the current state and context. It does not directly manage dependencies or state, but it reflects them in the UI by rebuilding the widget tree when changes occur.

| **Part**                  | **Description**                                                                 |
|---------------------------|---------------------------------------------------------------------------------|
| `Widget`                  | The return type of the method — it returns a widget or a widget tree.          |
| `build`                   | The method name — Flutter calls this to render the UI of the widget.           |
| `(BuildContext context)` | The parameter — provides access to the widget tree and inherited data.         |
| `{ ... }`                 | The method body — contains the logic to construct and return the widget tree.  |
| `return ...;`             | Returns the widget(s) that should be displayed on the screen.                  |

 

