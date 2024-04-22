What is ES6?

ES6 stands for ECMAScript 6, which is the sixth edition of the ECMAScript standard. It is a version of JavaScript, the programming language used to create dynamic and interactive websites. ES6 introduced several new features and improvements to JavaScript, making it more powerful and easier to work with.
Example: In ES6, you can use the let and const keywords to declare variables.

New features introduced in ES6

ES6 introduced many new features, including:
Arrow functions: A shorter syntax for writing functions.
Template literals: A way to create strings with placeholders.
Classes: A new way to define objects and create object-oriented code.
Destructuring assignment: A convenient way to extract values from objects or arrays.
Spread and rest operators: Used to manipulate arrays and function arguments.
Promises: A way to handle asynchronous operations.
Modules: A standardized way to organize and share code.
Example: In ES6, you can use arrow functions like this:

const sum = (a, b) => a + b;
The difference between a constant and a variable

A variable is a named container that can hold a value, and its value can change during the program's execution. On the other hand, a constant is a named container that holds a value, but once assigned, its value cannot be changed.
Example:

let age = 14; // variable
const PI = 3.14; // constant
age = 15; // value of variable 'age' can be changed
PI = 3.14159; // ERROR: Cannot change the value of a constant
Block-scoped variables

Block-scoped variables are variables that are only accessible within the block of code where they are defined. A block is a set of code enclosed within curly braces {}. In ES6, you can use the let and const keywords to declare block-scoped variables.
Example:

{
  let x = 10; // block-scoped variable
  console.log(x); // 10
}
console.log(x); // ERROR: 'x' is not defined
Arrow functions and function parameters default to them

Arrow functions are a shorter syntax for writing functions in JavaScript. They are often used as callback functions or when a concise function syntax is desired. Additionally, arrow functions can have default parameter values, which are used when the function is called without providing a value for that parameter.
Example:

// Arrow function without parameters
const sayHello = () => {
  console.log("Hello!");
};

// Arrow function with default parameter
const greet = (name = "Anonymous") => {
  console.log(`Hello, ${name}!`);
};

sayHello(); // Hello!
greet(); // Hello, Anonymous!
greet("Alice"); // Hello, Alice!
Rest and spread function parameters

Rest and spread operators are used in function parameters to handle multiple values. The rest operator (...) allows a function to accept any number of arguments as an array. The spread operator (...) allows an array or iterable to be expanded into individual elements.
Example:

// Rest parameter
const sum = (...numbers) => {
  let total = 0;
  for (let number of numbers) {
    total += number;
  }
  return total;
};

console.log(sum(1, 2, 3)); // 6

// Spread operator
const numbers = [4, 5, 6];
console.log(...numbers); // 4 5 6
String templating in ES6

String templating, also known as template literals, allows you to create strings with embedded expressions or variables. You can use backticks () to enclose the template string and use ${}` to insert expressions or variables within the string.
Example:

const name = "Alice";
const age = 14;

const message = `My name is ${name} and I am ${age} years old.`;
console.log(message); // My name is Alice and I am 14 years old.
Object creation and their properties in ES6

In ES6, object creation and manipulation have become more convenient. You can use the object literal syntax to create objects with key-value pairs. Additionally, you can define shorthand property names, computed property names, and methods within objects.
Example:

// Object creation using object literal syntax
const person = {
  name: "Alice",
  age: 14,
  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  },
};

console.log(person.name); // Alice
console.log(person.age); // 14
person.greet(); // Hello, my name is Alice and I am 14 years old.

// Shorthand property names
const username = "Bob";
const age = 15;

const user = {
  username,
  age,
};

console.log(user.username); // Bob
console.log(user.age); // 15

// Computed property names
const propertyName = "email";

const user = {
  [propertyName]: "bob@example.com",
};

console.log(user.email); // bob@example.com
Iterators and for-of loops

Iterators are objects that provide a sequence of values, and for-of loops are used to iterate over these values. In ES6, you can use iterators with objects that implement the iterable protocol. This includes arrays, strings, maps, sets, and more.
Example:

// Array iteration with for-of loop
const numbers = [1, 2, 3, 4, 5];

for (let number of numbers) {
  console.log(number);
}

// Output:
// 1
// 2
// 3
// 4
// 5

// String iteration with for-of loop
const message = "Hello";

for (let char of message) {
  console.log(char);
}

// Output:
// H
// e
// l
// l
// o
