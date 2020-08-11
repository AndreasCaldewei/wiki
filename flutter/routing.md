### Routing
#### Basic
##### Named Routes
In your main.dart add a router config to your app.

```dart 
class MyApp extends StatelessWidget {

 @override
  Widget build(BuildContext context) {
    return MaterialApp(
      // starting page
      initialRoute: '/', 
      routes: {
        // the üage route
        '/': (context) => Index() // These are normal widgets, organzie them in a sperate folder,
        '/about': (context) => About(),
      },
    );
  }
}
```

Navigation is done by the Navigator.

```dart 

class Index extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(),
      body: Container(
        padding: EdgeInsets.all(8.0),
        child: FlatButton(
          child: Text('Hello World'),
          onPressed: () => Navigator.pushNamed(context, '/about'),  // <-- navigates you to the About Page
        ),
      ),
    );
  }
}

```
#### Advanced
##### Generated Routes
Generated routes are especially usefull when want to check if the user can access the specific route or you want to pass dynamic data in to a screen. 
###### 1. Create handler fucntion for the routes.
```dart
class RouteGenerator {
  static Route<dynamic> generateRoute(RouteSettings settings) {
    // Getting arguments passed in while calling Navigator.pushNamed
    final args = settings.arguments;

    switch (settings.name) {
      case '/':
        return MaterialPageRoute(builder: (_) => FirstPage());
      case '/second':
        // Validation of correct data type
        if (args is String) {
          return MaterialPageRoute(
            builder: (_) => SecondPage(
                  data: args,
                ),
          );
        }
        // If args is not of the correct type, return an error page.
        // You can also throw an exception while in development.
        return _errorRoute();
      default:
        // If there is no such named route in the switch statement, e.g. /third
        return _errorRoute();
    }
  }

 static Route<dynamic> _errorRoute() {
    return MaterialPageRoute(builder: (_) {
      return Scaffold(
        appBar: AppBar(
          title: Text('Error'),
        ),
        body: Center(
          child: Text('ERROR'),
        ),
      );
    });
  }
}
```
After that register your function for routing.
```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      ...
      // Initially display FirstPage
      initialRoute: '/',
      onGenerateRoute: RouteGenerator.generateRoute,
    );
  }
}
```
And now you can navigate to other screens with data. 

```dart
class FirstPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      ...
            RaisedButton(
              child: Text('Go to second'),
              onPressed: () {
                // Pushing a named route
                Navigator.of(context).pushNamed(
                  '/second',
                  arguments: 'Hello there from the first page!',
                );
              },
            )
      ...
  }
}
```


