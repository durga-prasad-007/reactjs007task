1. Arrow Functions (=>)
A concise way to write functions.
Example:
const multiply = (x, y) => x * y;
-------------------------------------------------------------------------
2. Block-Scoped Variables (let and const)
let and const provide block-level scoping, unlike var.
const is used for variables that shouldn't be reassigned.
Example:
let name = "John";
const PI = 3.14;
-------------------------------------------------------------------------
3. Template Literals
Allows for multi-line strings and string interpolation.
Example:
const name = "Alice";
const greeting = `Hello, ${name}!`;
-------------------------------------------------------------------------
4. Destructuring Assignment
Extract values from arrays or properties from objects into distinct variables.
Example:
const [a, b] = [1, 2];
const { name, age } = { name: "John", age: 30 };
-------------------------------------------------------------------------
5. Default Parameters
Function parameters can have default values if no argument is provided.
Example:
function greet(name = "Guest") {
  return `Hello, ${name}`;
}
-------------------------------------------------------------------------
6. Rest and Spread Operators (...)
The rest operator collects all remaining elements into an array.
The spread operator allows an array or object to be expanded.
Example:
function sum(...numbers) {
  return numbers.reduce((a, b) => a + b, 0);
}

const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
-------------------------------------------------------------------------
7. Classes
A new syntax for creating objects and dealing with inheritance.
Example:
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  
  greet() {
    return `Hello, my name is ${this.name}`;
  }
}
-------------------------------------------------------------------------
8. Enhanced Object Literals
Shortened syntax for defining properties and methods in objects.
Example:
const name = "John";
const person = {
  name,
  greet() {
    return `Hello, ${this.name}`;
  }
};
-------------------------------------------------------------------------
9. Promises
A way to handle asynchronous operations more easily.
Example:
const fetchData = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve("Data"), 1000);
  });
};
-------------------------------------------------------------------------
10. Modules (import and export)
Allows code to be divided into separate files and modules.
Example:
// math.js
export const add = (a, b) => a + b;

// main.js
import { add } from './math';
-------------------------------------------------------------------------
11. Iterators and Generators
Iterators provide a way to iterate over collections like arrays.
Generators (function*) allow functions to pause and resume execution.
Example:
function* generator() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = generator();
console.log(gen.next().value); // 1
-------------------------------------------------------------------------
12. Symbols
A new primitive data type for creating unique identifiers.
Example:
const sym1 = Symbol('description');
-------------------------------------------------------------------------
13. Map, Set, WeakMap, and WeakSet
New data structures to store collections of data.
Example:
const map = new Map();
map.set('key', 'value');

const set = new Set([1, 2, 3]);
-------------------------------------------------------------------------
14. for...of Loop
Iterates over iterable objects like arrays, strings, etc.
Example:
const arr = [1, 2, 3];
for (const value of arr) {
  console.log(value);
}
-------------------------------------------------------------------------
15. Number, Math, String, and Array Extensions
New methods added to built-in objects.
Example:
Number.isNaN(NaN);          // true
Array.from('hello');        // ['h', 'e', 'l', 'l', 'o']
-------------------------------------------------------------------------
16. Proxy and Reflect
Proxies allow you to intercept and customize operations on objects.
Reflect provides methods for interceptable JavaScript operations.
Example:
const target = {};
const handler = {
  get: (obj, prop) => (prop in obj ? obj[prop] : 42)
};
const proxy = new Proxy(target, handler);
-------------------------------------------------------------------------
17. Tail Call Optimization
Optimization that allows for certain types of recursion to avoid growing the call stack.
These features collectively bring more power, flexibility, and readability to JavaScript, making it easier to develop complex applications.