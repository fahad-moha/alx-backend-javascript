## Using map, filter, and reduce on Arrays
In JavaScript, the `map`, `filter`, and `reduce` methods are powerful array methods for transforming, filtering, and aggregating data.

### 1. `map`: 
The `map` method creates a new array by applying a provided function to each element of the original array. It returns an array of the same length as the original array, with each element transformed based on the provided function.

Example:
```javascript
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.map((num) => num * 2);
console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

### 2. `filter`:
The `filter` method creates a new array containing elements from the original array that satisfy a given condition. It returns an array with elements for which the provided function returns `true`.

Example:
```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter((num) => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

### 3. `reduce`:
The `reduce` method applies a function to each element of the array, resulting in a single output value. It "reduces" the array to a single value by accumulating the result of each iteration.

Example:
```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // Output: 15
```

## Typed Arrays
Typed arrays in JavaScript provide a way to work with binary data in a specific format and are more memory-efficient compared to regular arrays. They are available in various types, such as `Int8Array`, `Uint8Array`, `Float32Array`, etc.

Example:
```javascript
const buffer = new ArrayBuffer(16); // Allocate a 16-byte buffer
const int32Array = new Int32Array(buffer); // Create a 4-element Int32Array
int32Array[0] = 42;
console.log(int32Array); // Output: Int32Array [42, 0, 0, 0]
```

Typed arrays allow you to perform efficient operations on binary data, such as bitwise operations, direct memory access, and interoperability with other systems.

## Set, Map, and WeakMap Data Structures
JavaScript provides three built-in data structures for handling collections of data: `Set`, `Map`, and `WeakMap`.

### 1. `Set`:
A `Set` is an ordered collection of unique values, where duplicates are automatically removed. It allows you to efficiently check for the presence of a value and iterate over its elements.

Example:
```javascript
const set = new Set();
set.add('apple');
set.add('banana');
set.add('apple'); // Duplicates are automatically removed
console.log(set.size); // Output: 2
console.log(set.has('banana')); // Output: true
```

### 2. `Map`:
A `Map` is a collection of key-value pairs, where each key is unique. It provides an efficient way to store and retrieve values based on a key.

Example:
```javascript
const map = new Map();
map.set('name', 'John');
map.set('age', 30);
console.log(map.get('name')); // Output: John
console.log(map.size); // Output: 2
```

### 3. `WeakMap`:
A `WeakMap` is similar to a `Map`, but it allows only objects as keys and has some differences in behavior. It is designed for scenarios where you want to associate additional data with objects without interfering with garbage collection.

Example:
```javascript
const weakMap = new WeakMap();
const obj1 = {};
const obj2 = {};
weakMap.set(obj1, 'value1');
weakMap.set(obj2, 'value2');
console.log(weakMap.get(obj1)); // Output: value1
```

`WeakMap` keys are weakly referenced, meaning that if the object used as a key is no longer referenced elsewhere, it may be garbage collected, and the corresponding entry in the `WeakMap` will be automatically removed.

