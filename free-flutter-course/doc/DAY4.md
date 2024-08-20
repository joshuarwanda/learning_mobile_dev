# Day 4
# Dart OOP concepts and Enumerations

Enumeration is basically a named list of related items. It is good convention to name them **NOT** in *camel case* but in a different convention where the *first letter* of the first word is capitalized as well as the first letter of each subsequent word.\
They are declared using the `enum` keyword and can be thought of <u>kinda</u> like a struct in that they hold related properties in a single collection.\ 
- **NOTE**: enumerations are not the same as `classes` or `structs` but are similar in theory.\
Also, when working with **enums** it is considered good practice to use **switch...case** statements instead of **if...else if...else** statements

We then proceed to learn the usuall OOP stuff;\ 
- **classes**
- **objects**
- **constructors** (in Dart,  a constructor takes the form of a method of same name as the class)
- **inheritance** (done with the usual `extends` keyword)
- **class methods**
- **Abstract classes** - classes that cannot be instantiated (defined using `abstract` keyword)
- **Factory constructor**- useful where you notice that you keep instantiating objects of a certain class with the same property over and over and over again...might be time to change it to a factory constructor.
- **Custom operators** - (using the `@overide` decorator) allow us to define custom behaviour of operators within classes.

...all that good stuff.\

I reiterate, I wont be deeply documenting my thoughts on these concepts as there are better resources online for learning **OOP**, I am only gonna be documenting very *Dart*-specific concepts and *Mobile development concepts and best practices* 

**FOOD FOR THOUGHT**- Its kinda weird how a 'sub-class' is **kinda** in actuallity a superset of the class its inheriting from...just a random thought.
**More food for thought**- There is a concept of <u>**class clusters**</u> wherein a class factory constructor doesnt necessarily have to return an instance of the same class and may instead return an instance of a different class innit.\
**! Take some time and read more on factory constructors. !**

**NOTE**- Factory constructors are useful when working with a lot of data.