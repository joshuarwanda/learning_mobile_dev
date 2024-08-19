# Day 3
# Getting deeper into Dart

Dart needs explicit statement if a variable or data type is expected to contain a null value.\
This is done using the `?` operator\
For example:\
`String? name = null;`\
This allows the name variable to be nullable.\
Other data structures also follow this convention for example to create a nullable list we use:\
`List<String>? names = null;`\
This initializes an empty list that can contain string values.\ 
**NOTE** This does not mean the values in the list can be null, only the List itself.\
To make the values inside the list nullable as well as the list itself we put two `?` marks, one inside the data type specifier and one outside as such:\
`List<String?>? names = [null, null];`\
The `??` operator is used to compare two values and proceed execution with the one among them that is not `null`. Example:
```dart
const firstNonNullName = firstName ?? secondName ?? thirdName
```
This will assign the first non-null value between firstName, secondName, and thirdName to firstNonNullName.\

The `??=` operator is the *null-aware* assignment operator. It assigns a value to the variable name on the left only if the variable doesnt currently have a value assigned, i.e only if it is null.
```dart
name ??= middleName;
```
this will only assign the value of `middleName` to `name` if `name` is `null`\

The `?.` is the *conditional invocation* operator which invokes a method only if the attatched variable meets defined conditions. It is used to check if <u>optional values</u> i.e those that can be null, contain a value before invoking the method. 