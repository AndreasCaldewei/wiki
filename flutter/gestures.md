### Gestures 
#### Basics 
##### GestureDetector
Has multiple gesture events.
```dart
 child: GestureDetector(
   onTapDown: (details) => print(details.globalPosition.dx),
   child: Container(
     width: 100,
     height: 100,
     color: Colors.red
   ),
 ),
```
##### InkWell (Marterial only)
Has multiple gesture events and a marterial wave animation.
```dart
 child: InkWell(
   onTapDown: (details) => print(details.globalPosition.dx),
   child: Container(
     width: 100,
     height: 100,
     color: Colors.red
   ),
 ),
```
##### Button
```dart
 child: RaisedButton( // FlatButton,  IconButton, FLoatingActionButton 
   child: Text('Hello World'),
   onPressed: () => print('Hello World!'),
 ),
```
