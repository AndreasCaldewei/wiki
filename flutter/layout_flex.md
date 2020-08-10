### FlexLayout
#### Basic
##### Column
```dart
Column(
    mainAxisAlignment: MainAxisAlignment.center, // MainAxisAlignment.min, .max, .spaceEvenly, spaceBetween, .center
    crossAxisAlignment: CrossAxisAlignment.stretch, 
    children: <Widget>[
     Icon(Icons.cake, color: Colors.white, size: 50,),
     Icon(Icons.cake, color: Colors.white, size: 100,),
     Icon(Icons.cake, color: Colors.white, size: 200,),
    ],
 )

```
##### Row
```dart
Row(
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.stretch,
    children: <Widget>[
     Icon(Icons.cake, color: Colors.white, size: 50,),
     Icon(Icons.cake, color: Colors.white, size: 100,),
     Icon(Icons.cake, color: Colors.white, size: 200,),
    ],
 )

```
#### Best Practices
```dart
Column(
    mainAxisAlignment: MainAxisAlignment.spaceBetween, 
    crossAxisAlignment: CrossAxisAlignment.stretch, 
    children: <Widget>[

    ],
 )

```
