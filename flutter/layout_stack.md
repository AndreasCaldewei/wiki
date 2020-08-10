### Stack
#### Basic
##### Stack
Displays the children in absolute ways.
```dart 
 SizedBox.expand( // Expands to the size of the parent.
         child: Stack( 
           children: <Widget>[
             Icon( // Children can be placed directly inside the childrens array.
               Icons.camera,
               size: 100,
               color: Colors.red,
             ),
             Align( // Allows to implicitly position a children.
                 alignment: Alignment.center,
                 child: Icon(
                   Icons.camera,
                   size: 100,
                   color: Colors.blue,
                 )),
             Positioned( // Positioned allows to position the children explicitly.
                 bottom: 20,
                 left: 100,
                 child: Icon(
                   Icons.camera,
                   size: 100,
                   color: Colors.green,
                 ))
           ],
         ),

```
