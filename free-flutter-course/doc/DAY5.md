# DAY 5
# Deeper into Advanced Dart concepts

<u>**Extensions**</u> in Dart do exactly what the name suggests, they 'extend' the functionality of a class.\
They are created using the `extension` ...`on` keyword pair.\
Example, consider a class **Cat**:
```dart
class Cat{
final String name;

Cat(this.name);
}

extension Run on Cat{
  void run(){
    print('Cat $name is running');
  }
}
```
**!NOTE!**- the `=>` is a concise function definition or *lambda* function definition. In Dart it is a short way of defining a quick function. \
It is the equivalent of `funcName () {return x;}`

<u>**Future**</u> in Dart is the way to work with asychronous operations. i.e operations that promise to return data in future or later in execution\
**!Note!** - <u>Asynchronous operations</u> as I understand them are operations meant to return a value **NOT** immediately but at some future point in execution. \
Future is implemented using the `Future` keyword.\
**Food for thought** - As I understand them, Asynch functions such those used with `Future` in Dart work in tandem with the functional programming paradigm of *functions as values*\
Also when working with async functions, they must be specified as being async at the call site using the `async` keyword
Example
```dart
void test() async {
  futureFuction();
}
```
what is returned is actually not the value of the computation but a `Future` object. In order to extract the value of the computation we use the `await` keyword.\
example:
```dart
void test() async{
  await futureFunction();
}
```

<u>**Streams**</u> are a pipeline of data that *completes successfully* or *never completes* or *errors out and dies*. It is in some sense a 'never ending Future', kinda like a subclass of a Future.\
Created using the `Stream` keyword. For example
```dart
Stream<String> getName(){
  return Stream.periodic(const duration(seconds: 1) (value){
    reurn 'Foo';
  });
}
```
then to get the value we use this syntax using the `await for` keyword:
```dart
void test(){
  await for(final value in getName()){
    print(value);
  }
}
```

<u>**Generators**</u> are created using the `Iterable` keyword in combination with `sync*` or `async*` and work as sort of a lazy collection of items that are created and added to the collection on a need basis.\
Taking the analogy of a restaurant that prepared meals as they are ordered as opposed to a supermarket where the meals are readily packaged.\
`sync*` generators are calculated syncronously while `async*` generators are calculated asynchronously and returned as a Stream.\
Within the generator function we have to use the `yield` keywork as such:
```dart
Iterable<int> getOneTwoThree(){
  yield ;
}

void test(){
  for(final value in getOneTwoThree()){
    print(value);
    if (value == 2){
      break;
    }
  }
}
```

<u>**Generics**</u> are kinda like templates used to create classes that may be similar in logic but operate on different types. For example consider creating a class *Pair* that contains two similar variables that can be either string or int. Instead of creating separate pair classes for string and int we can do this:
```dart
class pair<A, B>{
  final A value1;
  final B value2;
}
```
**!NOTE!** Generics are a whole thing and Dart and they go really deep into the weeds.
