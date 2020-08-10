### Routing
##### Basic
In your main.dart add a router config to your app.

```dart 
class MyApp extends StatelessWidget {

 @override
  Widget build(BuildContext context) {
    return MaterialApp(
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
