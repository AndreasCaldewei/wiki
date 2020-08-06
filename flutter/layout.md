### Positioning
#### Basics
##### Center
```dart
body: Center(
    child: Icon(
        Icons.face,
    )
);
```
##### Alignment
```dart
body: Align(
    alignment: Alignment.topRight, // centerLeft, bottomLeft, ...
    child: Icon(
        Icons.face,
    )
);
```

##### Padding

```dart
body: Padding(
    padding: EdgeInsets.all(8.0), //  const EdgeInsets.only(top: 8.0, left: 8.0)
    child: Icon(
        Icons.face,
    )
);
```
#### Advanced
##### Container
A Container can do Center, Alignment and Padding at once. It contains all the properties of these Widgets and more.

```dart
body: Container(
    padding: EdgeInsets.all(8.0), //  const EdgeInsets.only(top: 8.0, left: 8.0)
    alignment: Alignment.topRight,
    margin: EdgeInsets.all(8.0)
    width: 100,
    height: 100,
    child: Icon(
        Icons.face,
    )
);
```
#### Best Practices
The body element of an Scaffold should be a Container. 
```dart
Scaffold(
    body: Container(
        child: Icon(Icons.star)
    )
)
```


