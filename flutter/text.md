### Text 
#### Basic
```dart
    Expanded(
        Text(
            'Hello World',
            overflow: TextOverflow.ellipsis,
            style: TextStyl(
                fontSize: 15,
                fontWeight: FontWeight.bold
            )
    )
```
#### Advanced
##### Outsource styles
```dart
    Expanded(
        Text(
            'Hello World',
            overflow: TextOverflow.ellipsis,

            style: Theme.of(context).textTheme.myStyle
    )
```
// TODO:  link to the custom styles
