## Defining a Class
In JavaScript, classes are used to define blueprints for creating objects with similar properties and behaviors. The `class` keyword is used to define a class. Here's an example of a basic class definition:

```javascript
class MyClass {
  constructor() {
    // Constructor code
  }
  
  // Class methods
  method1() {
    // Method code
  }
  
  method2() {
    // Method code
  }
}
```

In the above example, `MyClass` is defined as a class using the `class` keyword. The `constructor` method is a special method that is called when an object is created from the class. You can define other methods within the class body as well.

## Adding Methods to a Class
Methods are functions that are associated with a class and can be called on objects created from that class. You can add methods to a class by defining them within the class body. Here's an example:

```javascript
class MyClass {
  method1() {
    // Method code
  }
  
  method2() {
    // Method code
  }
}
```

In the above example, `method1` and `method2` are added to the `MyClass` class. These methods can be called on objects created from the class.

## Static Methods in Classes
Static methods are methods that are associated with the class itself, rather than with instances of the class. They can be called directly on the class without creating an object. Static methods are defined using the `static` keyword. Here's an example:

```javascript
class MyClass {
  static staticMethod() {
    // Static method code
  }
  
  method() {
    // Instance method code
  }
}

MyClass.staticMethod(); // Calling static method directly on the class
const myObject = new MyClass();
myObject.method(); // Calling instance method on an object
```

In the above example, `staticMethod` is a static method that can be called directly on the `MyClass` class. The `method` method is an instance method that can be called on objects created from the class.

Static methods are useful when you have a behavior or functionality that is not specific to individual instances but is related to the class as a whole.

## Extending a Class
In JavaScript, you can create a new class that inherits properties and methods from an existing class. This is achieved using the `extends` keyword. The new class is called the child class or subclass, and the existing class is called the parent class or superclass. Here's an example:

```javascript
class ParentClass {
  parentMethod() {
    // Parent method code
  }
}

class ChildClass extends ParentClass {
  childMethod() {
    // Child method code
  }
}

const childObject = new ChildClass();
childObject.parentMethod(); // Calling parent method from child object
childObject.childMethod(); // Calling child method
```

In the above example, `ParentClass` is the parent class, and `ChildClass` is the child class that extends the parent class. The child class inherits the `parentMethod` from the parent class and defines its own `childMethod`.

## Metaprogramming and Symbols
Metaprogramming is the practice of writing code that can manipulate or modify other code. In JavaScript, symbols are often used in metaprogramming to create unique property keys. Symbols are created using the `Symbol()` function. Here's an example:

```javascript
const mySymbol = Symbol('mySymbol');
const obj = {
  [mySymbol]: 'value'
};

console.log(obj[mySymbol]); // Output: value
```

In the above example, `mySymbol` is a symbol that is used as a property key in the `obj` object. Symbols are unique, which helps prevent unintended conflicts with other properties.

Metaprogramming with symbols allows you to create properties that are hidden from standard object enumeration and can be used for advanced techniques like defining private members or implementing custom behavior.

