### ScrollView
#### Basic
##### ListView
```dart
class MyApp extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
   return MaterialApp(
     home: Scaffold(
       body: ListView(
         scrollDirection: Axis.horizontal,
         children: _cards(),
       )
     ),
   );
 }

 List<Widget> _cards() {
   return [1,2,3,4,5,6,7,8,9].map((v) => Container(
       color: Colors.blue,
       margin: EdgeInsets.all(20),
       height: 100,
       child: Text('$v'),
     )
   ).toList();
 }
```
##### ListView.builder 
Creates items on the fly. Comparable to RecyclerViews in Android.
```dart
class MyApp extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
   return MaterialApp(
     home: Scaffold(
       body: ListView.build(itemBuilder(context, idx) {
            return Container {
                color: Colors.blue,
                margin: EdgeInsets.all(20),
                height: 100,
                child: Text('§idx') // Here you can add specific logic for rendering items.
            }
        },
     ),
   );
 }
```
Other Example
```dart
ListView.builder(
  // Let the ListView know how many items it needs to build.
  itemCount: items.length,
  // Provide a builder function. This is where the magic happens.
  // Convert each item into a widget based on the type of item it is.
  itemBuilder: (context, index) {
    final item = items[index];

    return ListTile(
      title: item.buildTitle(context),
      subtitle: item.buildSubtitle(context),
    );
  },
);
```

##### GridView

#### More

[Create lists with different types of items](https://flutter.dev/docs/cookbook/lists/mixed-list)
