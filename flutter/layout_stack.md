### Stack
#### Basic
##### Stack
Displays the children in absolute ways.
```dart 
// Expands to the size of the parent.
 SizedBox.expand(  
         child: Stack( 
           children: <Widget>[
             // Children can be placed directly inside the childrens array.
             Icon( 
               Icons.camera,
               size: 100,
               color: Colors.red,
             ),
            // Allows to implicitly position a children.
             Align( 
                 alignment: Alignment.center,
                 child: Icon(
                   Icons.camera,
                   size: 100,
                   color: Colors.blue,
                 )),
            // Positioned allows to position the children explicitly.
             Positioned( 
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
