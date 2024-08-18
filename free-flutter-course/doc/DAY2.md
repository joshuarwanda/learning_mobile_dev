# Day 2
## Introduction to Dart

Dart is the language underlying the flutter framework. I'd even go to say most people who learn dart do it for no other reason but to learn flutter but do not quote me on that one. 

`Ctrl + Shift + P` - Important vs code command for searching files and when you enter `>` in the search bar, allows running commands like `flutter: Select device`

This is a very beginner friendly course thus the tutor goes through a lot of foundation concepts like *keywords*, dart key words can be found
[here](https://dart.dev/language/keywords)

**Sidenote**: Just learned that constants are solidified at compile time...wonder how much memory this saves...
**NOTE**: `const` and `final` are not the same, the later provides a bit more flexibility on assiging value to the varible.

It is considered good convention to write dart functions, class names etc in <u>**camelCase**</u>
Dart prefers strings are enclosed around singel quotes`' '`

In Dart, when we want a variable to be able to take the type `null` we have to use `?` when instantiating it:
Example:
```dart
const String? name = null;
void main(){
    print('$name')
}
```
## Summary

Most of today involved getting a bearing on the **Dart Programming Language** ...yk the usual,
- keywords
- variables
- constants
- operators
- standard data types
- null values \
et cetra 

Fair to say, these notes wont help you much if you're an absolute beginner to programming. Definitely better resources for that exist.