### Decoration
#### Basics
##### BoxDecoration
Can be used to for BoxShadows and Gradients.
```dart
Container(
  alignment: Alignment.center,

  decoration: BoxDecoration(
      color: Colors.blue,
      border: Border.all(width: 5, color Colors.Red),
      boxShadow: [ // BoxShadows can be stacked
        BoxShadow(offset: Offset(40, 40), color: Colors.pink),
        BoxShadow(offset: Offset(20, 20), color: Colors.yellow),
      ],
      gradient: RadialGradient(colors: [Colors.yellow, Colors.pink]), // RadialGradient
      shape: BoxShape.circle, 

  ),
)
```
