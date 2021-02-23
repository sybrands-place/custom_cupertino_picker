# custom_cupertino_picker
The default cupertino picker does not allow customization to the border color and scroll physics. So I've copied the class and added some properties to it.

Added the following properties:
 - highlighterBorderColor 
    - // Border color for the magnifier.
 - highlighterBorder 
    - // Border for the magnifier. If this one is set
    the highlighterBorderColor will be ignored.

 - highlighterBorderWidth
    - // Border width for the magnifier if you
    don't fill the border to the full width
 - scrollPhysics
    - // ScrollPhysics for the ScrollView if you want
    to override the default physics.

## Getting Started

import the package
```dart
import 'package:custom_cupertino_picker/custom_cupertino_picker.dart';
```
and use it for example like below

```dart
CustomCupertinoPicker(
    highlighterBorder: Border(
        top: BorderSide(
            width: 1.0, color: Colors.orange),
        bottom: BorderSide(
            width: 1.0, color: Colors.orange),
    ),
    highlighterBorderWidth: 60,
    scrollPhysics: const FixedExtentScrollPhysics(
        parent: BouncingScrollPhysics()),
    children: ...
)
```
![preview](https://github.com/sybrands-place/custom_cupertino_picker/blob/main/preview.png "Customized cupertino picker")