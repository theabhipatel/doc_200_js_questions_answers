# doc_200_js_questions_answers
200 JavaScript questions and answers (basic to advanced)

---

### 1. What is JavaScript?
JavaScript is a high-level, dynamic programming language used to create interactive effects in web browsers. It is a key technology of the web along with HTML and CSS. JavaScript can be used for both front-end (client-side) and back-end (server-side) development. It supports different programming styles, making it a useful tool for building web applications, mobile apps, and more. Additionally, JavaScript can change the Document Object Model (DOM) to update content and respond to user actions in real-time.

### 2. What are the different data types in JavaScript?
In JavaScript, there are mainly two type of data types:

- 1. Premitive
- 2. Non Premtive (reference data type)

#### Premitives 
1. String: Used for text, e.g., "Hello, world!".
2. Number: For whole numbers and decimals, e.g., 42 and 3.14.
3. Boolean: Has two values: true and false.
4. Null: Represents "no value" or "empty," written as null.
5. Undefined: Indicates a variable that has been declared but not assigned a value.
6. Symbol: A unique value used as object property keys.
7. BigInt: For very large integers, e.g., 9007199254740991n.

#### Non Premitives 
1. Object: Stores collections of data as key-value pairs, e.g., { name: "John", age: 30 }.
2. Array: A special type of object for lists of values, e.g., [1, 2, 3, 4].
3. Functions
4. Date


### 3. What is the difference between let, const, and var?
var: The old way to declare variables. Variables declared with var are function-scoped and can be re-declared.
let: Introduced in newer versions, it is block-scoped and can be updated but not re-declared.
const: Also block-scoped but cannot be updated or re-declared after being assigned a value.

### 4. What is hoisting in JavaScript?
 Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their scope before the code executes. This means you can use a variable or function before you actually declare it in your code, but only with var (not let or const).
 
### 5. Explain the concept of closures.
A closure in JavaScript is a feature where an inner function can access variables from its own scope, the outer function's scope, and the global scope. This means the inner function "remembers" the variables from the outer function, even after the outer function has finished running. Closures allow functions to keep using data from the surrounding scope where they were created.

### 6. What is the difference between == and ===?
==: Checks if the values are the same, even if they are different types. For example, 5 == '5' is true because the values are the same.
===: Checks if the values and types are the same. So, 5 === '5' is false because one is a number and the other is a string.

### 7. What is the difference between null and undefined?
null: This means a variable is intentionally empty or has no value.
undefined: This means a variable has been declared but not yet given a value.

### 8. What are JavaScript arrow functions?
avaScript arrow functions are a shorter and more concise way to write functions, introduced in ES6. They don't have their own this context and instead inherit this from the surrounding code. Arrow functions are useful for simplifying function expressions, especially in callbacks or when using array methods. Their syntax is more compact compared to traditional functions.

### 9. How do you declare a function in JavaScript?
A function can be declared like this: using function keyword
```js
function sayHello() {
  console.log("Hello");
}
```
This creates a function named sayHello that prints "Hello" when it's called.

### 10. What is a callback function?
A callback function is a function that is passed into another function as an argument and is executed later. For example:

```js
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}
greet("John", function() {
  console.log("Welcome!");
});
```

---

### 11. What are promises in JavaScript?
A promise in JavaScript is a special object that represents the eventual completion or failure of an asynchronous operation. It can be in one of three states: pending, fulfilled, or rejected. Promises are used to handle asynchronous code, like making API calls or loading data, by allowing you to run code after an operation completes, rather than blocking other code from running.

### 12. What is async/await in JavaScript?
Async/await is a way to write asynchronous code in JavaScript more easily. It allows you to write code that looks like it runs in order, even though some tasks take time to complete. The async keyword is used before a function to make it asynchronous, and await is used inside that function to wait for a promise to complete before moving to the next line. This makes code easier to read and manage compared to promises alone.

### 13. What are JavaScript template literals?
Template literals are a new way to work with strings in JavaScript, introduced in ES6. They allow you to embed variables and expressions inside a string without using concatenation (+). Template literals are written with backticks (`) instead of single or double quotes, and you can insert variables using ${}.

Example:
```js
const name = "John";
console.log(`Hello, ${name}!`);
```

### 14. What is event bubbling and event capturing?
Event bubbling and event capturing describe how events travel through the DOM. When an event happens on an element (like a button click), it first triggers event capturing, where the event travels from the top of the DOM tree to the target element. After that, event bubbling occurs, where the event moves back up the DOM tree from the target to the top. You can control whether you handle the event in the capture or bubble phase.

### 15. How do you handle errors in JavaScript?
In JavaScript, you handle errors using try...catch blocks. You put the code that might throw an error inside the try block, and if an error happens, the catch block runs to deal with it. You can also use the finally block to run code that should always execute, whether an error occurred or not.

Example:
```js
try {
  // Code that might throw an error
} catch (error) {
  // Handle the error
} finally {
  // Code that always runs
}
```

### 16. What is the difference between synchronous and asynchronous code?
Synchronous code runs in sequence, where each line of code waits for the previous one to finish before running. Asynchronous code allows some tasks to run in the background without waiting for others to finish. This is useful for tasks like fetching data from a server, so other code can keep running without delay.

### 17. What are JavaScript modules?
JavaScript modules are a way to organize and reuse code by splitting it into separate files. Each file is a module, and you can export parts of a module (like functions or variables) to use in other files. This helps make code easier to manage and avoids having everything in one large file.
Modules are typically imported using the import and export keywords.

### 18. What is the `this` keyword in JavaScript?
The **this** keyword in JavaScript refers to the object that is currently executing the function. What this refers to depends on how and where the function is called. In general, this helps functions access properties and methods within their own object, but it can change based on the context in which it's used.

### 19. What is the difference between call(), apply(), and bind()?
call(), apply(), and bind() are methods that allow you to set the value of this in a function.

call(): Calls a function with a given this value and arguments passed individually.
apply(): Calls a function with a given this value, but arguments are passed as an array.
bind(): Returns a new function with a specific this value, but doesn’t execute the function immediately.

### 20. What is a prototype in JavaScript?
In JavaScript, every object has a prototype. The prototype is like a blueprint or template for creating objects. It allows objects to share methods and properties, so you don't have to define them for each individual object. This is the basis of inheritance in JavaScript. When you try to access a property or method on an object, JavaScript looks for it in the object itself, and if it’s not found, it looks at the object’s prototype.

---

### 21. What is the difference between a function declaration and a function expression?
A function declaration is when you define a function with the function keyword, followed by a name. This type of function can be called before it’s defined, because it’s "hoisted" to the top.

Example:
```js
function greet() {
  console.log('Hello');
}
```
A function expression is when you define a function and assign it to a variable. It is not hoisted, so you can only call it after the definition.

Example:
```js
const greet = function() {
  console.log('Hello');
};
```

### 22. What are default parameters in JavaScript functions?
Default parameters allow you to set a default value for a function's parameter if no argument is provided. This helps avoid errors when a parameter is missing.

Example:
```js
function greet(name = 'Guest') {
  console.log('Hello, ' + name);
}
If you don’t pass a value for name, it will use the default value 'Guest'.
```

### 23. What is the difference between a for loop and a forEach loop?
A for loop is a general loop that you can use for any repetitive task. You control the start, end, and how it moves through items.

Example:
```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
A forEach loop is used specifically with arrays. It automatically goes through each item in the array and runs a function for each one.

Example:
```js
[1, 2, 3].forEach(function(item) {
  console.log(item);
});
```
The main difference is that forEach is only for arrays, while for is more general.

### 24. What is an IIFE (Immediately Invoked Function Expression)?
An IIFE (Immediately Invoked Function Expression) is a function that runs as soon as it’s defined. You write it as a function expression inside parentheses, and then add () to execute it immediately.

Example:
```js
(function() {
  console.log('This runs right away');
})();
```

### 25. What is the DOM in JavaScript?
The DOM (Document Object Model) is a way to represent the structure of a webpage. It treats the HTML of a page like a tree of objects that JavaScript can interact with. You can change, add, or remove elements on the page using the DOM.

### 26. How do you manipulate the DOM in JavaScript?
You can manipulate the DOM by selecting elements and changing them. You can use methods like document.getElementById, document.getElementsClassName or document.querySelector to find elements, then change their content, style, or attributes.

Example:
```js
const element = document.getElementById('myElement');
element.textContent = 'New Content';
```

### 27. What is the difference between document.getElementById and document.querySelector?
**document.getElementById()** is used to select an element by its ID. It only works with IDs and returns the first matching element.
Example:
```js
document.getElementById('myId');
**document.querySelector()** is more flexible. It can select elements using CSS selectors like class names, IDs, or tags. It returns the first matching element.
```

Example:
```js
document.querySelector('.myClass');
```

### 28. What are JavaScript events?
Events are actions that happen in a web page, like a mouse click, key press, or page load. JavaScript can "listen" for these events and respond when they happen.

Example: A button click is an event.

### 29. How do you add and remove event listeners in JavaScript?
You can add an event listener using the addEventListener method, which lets you run a function when an event occurs. To remove an event listener, you use removeEventListener.

Example of adding:
```js
document.getElementById('myButton').addEventListener('click', function() {
  console.log('Button clicked');
});
```
Example of removing:
```js
document.getElementById('myButton').removeEventListener('click', myFunction);
```

---

### 30. What is event delegation?
Event delegation is a way to manage events more efficiently. Instead of adding event listeners to many elements, you add one listener to a parent element, and it will handle events that bubble up from child elements.

Example:
```js
document.getElementById('parent').addEventListener('click', function(event) {
  if (event.target.matches('.child')) {
    console.log('Child element clicked');
  }
});
```
This method reduces the number of event listeners and makes your code simpler.

---

### 31. What is the difference between innerHTML and textContent?
innerHTML returns or sets the HTML content of an element, which can include HTML tags. It processes and renders HTML.
Example:
```js
element.innerHTML = '<strong>Hello</strong>'; // Renders bold "Hello"
```
textContent returns or sets the text inside an element, ignoring any HTML tags. It treats content as plain text.
Example:
```js
element.textContent = '<strong>Hello</strong>'; // Displays "<strong>Hello</strong>"
```

### 32. How do you prevent the default behavior of an event?
To prevent the default behavior (like submitting a form or following a link), you use event.preventDefault() inside the event handler.

Example:
```js
document.querySelector('form').addEventListener('submit', function(event) {
  event.preventDefault(); // Stops the form from submitting
});
```

### 33. How do you stop event propagation?
To stop an event from bubbling up to parent elements, you use event.stopPropagation() inside the event handler.

Example:
```js
document.querySelector('button').addEventListener('click', function(event) {
  event.stopPropagation(); // Stops the click event from reaching parent elements
});
```

### 34. What is local storage in JavaScript?
Local storage is a way to store data in the user's browser. It saves data as key-value pairs, and the data persists even after the browser is closed. It has no expiration time.

### 35. What is session storage?
Session storage is similar to local storage, but the data is only saved for the duration of the page session. When the browser or tab is closed, the data is cleared.

### 36. How do you set, get, and remove items in local storage?
You use the following methods to work with local storage:

setItem(): To store data.
getItem(): To retrieve data.
removeItem(): To delete data.
Example:
```js
// Set an item
localStorage.setItem('username', 'John');

// Get an item
const user = localStorage.getItem('username');

// Remove an item
localStorage.removeItem('username');
```

### 37. What are cookies in JavaScript?
Cookies are small pieces of data that websites store on a user's browser. They can be used to remember information like login sessions. Cookies have expiration dates and can be set to expire after a certain time.

### 38. How do you create and read cookies?
To create a cookie, you set the document.cookie property. To read cookies, you can access document.cookie, which returns all cookies in one string.

Example:
```js
// Create a cookie
document.cookie = "username=John; expires=Fri, 31 Dec 2024 12:00:00 UTC";

// Read cookies
const cookies = document.cookie;
```

### 39. What are JavaScript objects?
A JavaScript object is a collection of key-value pairs. Each key is a property, and the value can be any type of data. Objects let you group related data and functions.

Example:
```js
const person = {
  name: 'John',
  age: 30,
  greet: function() {
    console.log('Hello');
  }
};
```

### 40. What is object destructuring in JavaScript?
Object destructuring allows you to extract values from an object and assign them to variables in a simpler way.

Example:
```js
const person = { name: 'John', age: 30 };
const { name, age } = person;
console.log(name); // 'John'
console.log(age); // 30
```
This is a shorthand way to pull out object properties and assign them to variables.

---

### 41. What is array destructuring in JavaScript?
Array destructuring allows you to unpack values from an array into individual variables in a clean and simple way.

Example:
```js
const fruits = ['apple', 'banana', 'cherry'];
const [first, second] = fruits;
console.log(first);  // 'apple'
console.log(second); // 'banana'
```
This assigns apple to first and banana to second.

### 42. What is the spread operator in JavaScript?
The spread operator (...) allows you to expand or spread elements from arrays or objects into individual elements or properties.

Example (with arrays):
```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // [1, 2, 3, 4]
```
Example (with objects):
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 };
console.log(obj2); // { a: 1, b: 2, c: 3 }
```

### 43. What is the rest parameter in JavaScript?
The rest parameter (...) allows you to group the remaining function arguments into an array.

Example:
```js
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num);
}
console.log(sum(1, 2, 3)); // 6
```
Here, numbers becomes an array of all arguments passed to the function.

### 44. How do you clone an object in JavaScript?
To clone an object, you can use the spread operator (...) or Object.assign().

Example (spread operator):
```js
const original = { a: 1, b: 2 };
const clone = { ...original };
console.log(clone); // { a: 1, b: 2 }
```
Example (Object.assign()):
```js
const original = { a: 1, b: 2 };
const clone = Object.assign({}, original);
console.log(clone); // { a: 1, b: 2 }
```

### 45. How do you merge two objects in JavaScript?
To merge two objects, you can use the spread operator or Object.assign().

Example (spread operator):
```js
const obj1 = { a: 1 };
const obj2 = { b: 2 };
const merged = { ...obj1, ...obj2 };
console.log(merged); // { a: 1, b: 2 }
```
Example (Object.assign()):
```js
const obj1 = { a: 1 };
const obj2 = { b: 2 };
const merged = Object.assign({}, obj1, obj2);
console.log(merged); // { a: 1, b: 2 }
```

### 46. What are array methods like map(), filter(), and reduce()?
map() creates a new array by applying a function to each element.
```js
const nums = [1, 2, 3];
const doubled = nums.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```
filter() creates a new array with elements that pass a test.
```js
const nums = [1, 2, 3, 4];
const evens = nums.filter(num => num % 2 === 0);
console.log(evens); // [2, 4]
```
reduce() applies a function to each element to reduce the array to a single value.
```js
const nums = [1, 2, 3, 4];
const sum = nums.reduce((total, num) => total + num, 0);
console.log(sum); // 10
```

### 47. What is the difference between slice() and splice()?
slice() returns a new array containing selected elements from the original array. It doesn’t change the original array.
```js
const arr = [1, 2, 3, 4];
const sliced = arr.slice(1, 3);
console.log(sliced); // [2, 3]
```
splice() changes the original array by adding/removing elements.
```js
const arr = [1, 2, 3, 4];
arr.splice(1, 2); // removes 2 elements starting from index 1
console.log(arr); // [1, 4]
```

### 48. How do you check if a value is an array in JavaScript?
You can use Array.isArray() to check if a value is an array.

Example:
```js
const arr = [1, 2, 3];
console.log(Array.isArray(arr)); // true
```

### 49. What is the difference between for...of and for...in loops?
for...of iterates over the values of an iterable object (like an array).
```js
const arr = [1, 2, 3];
for (let value of arr) {
  console.log(value);
}
// Output: 1, 2, 3
```
for...in iterates over the keys (or indexes) of an object or array.
```js
const arr = [1, 2, 3];
for (let key in arr) {
  console.log(key);
}
// Output: 0, 1, 2 (indexes)
```

### 50. What is the difference between push() and unshift() methods in arrays?
push() adds an element to the end of the array.
```js
const arr = [1, 2];
arr.push(3);
console.log(arr); // [1, 2, 3]
```
unshift() adds an element to the beginning of the array.
```js
const arr = [1, 2];
arr.unshift(0);
console.log(arr); // [0, 1, 2]
```

---

### 51. What is the pop() and shift() methods in arrays?
pop() removes the last element from an array and returns that element. It changes the length of the array.
```js
const arr = [1, 2, 3];
const last = arr.pop();
console.log(last); // 3
console.log(arr);  // [1, 2]
```
shift() removes the first element from an array and returns that element. It also changes the length of the array.
```js
const arr = [1, 2, 3];
const first = arr.shift();
console.log(first); // 1
console.log(arr);   // [2, 3]
```

### 52. How do you check if an object has a specific property?
You can use the in operator or the hasOwnProperty() method to check if an object has a specific property.

Using the in operator:
```js
const obj = { name: 'Alice', age: 25 };
console.log('name' in obj); // true
```
Using hasOwnProperty():
```js
const obj = { name: 'Alice', age: 25 };
console.log(obj.hasOwnProperty('age')); // true
```

### 53. What is the typeof operator?
The typeof operator is used to determine the type of a variable or value. It returns a string that indicates the type.

Example:
```js
console.log(typeof 42);            // 'number'
console.log(typeof 'hello');       // 'string'
console.log(typeof true);          // 'boolean'
console.log(typeof {});            // 'object'
console.log(typeof undefined);     // 'undefined'
```

### 54. What is the instanceof operator?
The instanceof operator checks if an object is an instance of a specific constructor or class. It returns true or false.

Example:
```js
const arr = [1, 2, 3];
console.log(arr instanceof Array); // true
console.log(arr instanceof Object); // true
```

### 55. What is NaN in JavaScript?
NaN stands for "Not-a-Number." It is a special value used to represent a value that is not a valid number. It usually results from invalid mathematical operations.

Example:
```js
const result = 0 / 0; // results in NaN
console.log(result);   // NaN
```

### 56. How do you check if a value is NaN?
To check if a value is NaN, you can use the isNaN() function or compare it to itself (because NaN is the only value that is not equal to itself).

```js
console.log(isNaN(NaN));       // true
console.log(isNaN(42));        // false
```

### 57. What is the use of the isNaN() function?
The isNaN() function checks whether a value is NaN (Not-a-Number). It returns true if the value is NaN and false otherwise.

Example:
```js
console.log(isNaN('hello')); // true, because it's not a number
console.log(isNaN(123));     // false, because it is a number
```

### 58. How do you convert a string to a number in JavaScript?
You can convert a string to a number using several methods, such as Number(), parseInt(), or parseFloat().

Using Number():
```js
const str = '42';
const num = Number(str);
console.log(num); // 42
```
Using parseInt():
```js
const str = '42';
const num = parseInt(str);
console.log(num); // 42
```
Using parseFloat():
```js
const str = '42.5';
const num = parseFloat(str);
console.log(num); // 42.5
```

### 59. What is parseInt() and parseFloat()?
parseInt() converts a string to an integer. It takes two arguments: the string to convert and an optional base (radix).
```js
const num = parseInt('42', 10); // 42
```
parseFloat() converts a string to a floating-point number.
```js
const num = parseFloat('42.5'); // 42.5
```

### 60. What is the Number() function?
The Number() function converts a value to a number. It can handle strings, booleans, and other types.

Example:
```js
console.log(Number('42'));      // 42
console.log(Number('42.5'));    // 42.5
console.log(Number(true));       // 1
console.log(Number(false));      // 0
console.log(Number(undefined));  // NaN
```

---

### 61. What is JSON and how do you parse and stringify JSON in JavaScript?
JSON (JavaScript Object Notation) is a lightweight format for storing and exchanging data. It is easy for humans to read and write, and easy for machines to parse and generate.

Parsing JSON means converting a JSON string into a JavaScript object. You can do this using the JSON.parse() method:
```js
const jsonString = '{"name": "Alice", "age": 25}';
const jsonObject = JSON.parse(jsonString);
console.log(jsonObject); // { name: 'Alice', age: 25 }
```
Stringifying JSON means converting a JavaScript object into a JSON string. You can do this using the JSON.stringify() method:
```js
const jsonObject = { name: 'Alice', age: 25 };
const jsonString = JSON.stringify(jsonObject);
console.log(jsonString); // '{"name":"Alice","age":25}'
```

### 62. What is a higher-order function in JavaScript?
A higher-order function is a function that can take another function as an argument or return a function as a result. This allows for more flexible and reusable code.

Example:
```js
function greet(name) {
  return `Hello, ${name}!`;
}

function executeGreeting(greetingFunction, name) {
  return greetingFunction(name);
}

console.log(executeGreeting(greet, 'Alice')); // 'Hello, Alice!'
```

### 63. What is the difference between Object.freeze() and Object.seal()?
Object.freeze() makes an object immutable, meaning you cannot change, add, or remove any properties from the object. Once frozen, the object cannot be modified.
```js
const obj = { name: 'Alice' };
Object.freeze(obj);
obj.name = 'Bob'; // This will not change the name
console.log(obj.name); // 'Alice'
```
Object.seal() allows you to prevent adding or removing properties from an object, but you can still change the existing properties. The object is not fully immutable.
```js
const obj = { name: 'Alice' };
Object.seal(obj);
obj.age = 25; // This will not add a new property
obj.name = 'Bob'; // This will change the existing property
console.log(obj.name); // 'Bob'
```

### 64. What is function currying in JavaScript?
Function currying is a technique where a function takes multiple arguments one at a time, instead of all at once. Each call to the function returns another function that takes the next argument. This allows for partial application of a function.

Example:
```js
function multiply(a) {
  return function(b) {
    return a * b;
  };
}

const double = multiply(2);
console.log(double(5)); // 10
```

### 65. What is the difference between mutable and immutable objects?
Mutable objects can be changed after they are created. You can add, remove, or modify properties without creating a new object. Examples include arrays and objects in JavaScript.
```js
const arr = [1, 2, 3];
arr.push(4); // This changes the original array
```
Immutable objects cannot be changed after they are created. Any changes result in a new object. Strings and numbers in JavaScript are examples of immutable objects.
```js
const str = 'hello';
const newStr = str.toUpperCase(); // This creates a new string
console.log(str); // 'hello'
console.log(newStr); // 'HELLO'
```

### 66. What is the event loop in JavaScript?
The event loop is a mechanism that allows JavaScript to handle asynchronous operations. It continuously checks the call stack and the message queue. If the call stack is empty, it takes the first event from the queue and executes its callback. This allows JavaScript to perform non-blocking operations.

Example:

A function is called.
If it has asynchronous operations (like a timer or an API call), it goes to the message queue.
When the call stack is empty, the event loop executes the next function from the queue.

### 67. What is a promise chain?
A promise chain is a series of promises that are linked together, where the output of one promise is the input to the next. Each promise in the chain can handle success and failure cases, making it easier to manage asynchronous operations.

Example:
```js
fetch('url')
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```
  
### 68. What are JavaScript generators?
Generators are special functions that can pause their execution and resume later. They allow you to define an iterative algorithm using the function* syntax and yield keyword. When you call a generator function, it returns an iterator that you can use to step through the values.

Example:
```js
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = numberGenerator();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
```

### 69. What is the difference between throw and return in JavaScript?
throw is used to create a custom error. When you throw an error, the normal flow of the program is stopped, and you can catch the error with a try-catch block.
```js
throw new Error('Something went wrong!');
```
return is used to exit a function and send a value back to the caller. It does not stop the whole program, just the current function.
```js
function add(a, b) {
  return a + b;
}
```

### 70. How do you handle promise rejection?
You can handle promise rejection using the catch() method or by providing a second argument to the then() method.

Example using catch():
```js
fetch('url')
  .then(response => response.json())
  .catch(error => {
    console.error('Error:', error);
  });
```
Example using then():
```js
fetch('url')
  .then(response => response.json(), error => {
    console.error('Error:', error);
  });
```

---

### 71. What is the use of Promise.all() in JavaScript?
Promise.all() is a method that takes an array of promises and returns a single promise that resolves when all the promises in the array have resolved or when one of them rejects. This is useful when you want to wait for multiple asynchronous operations to complete before proceeding.

Example:
```js
const promise1 = Promise.resolve(3);
const promise2 = new Promise((resolve) => setTimeout(resolve, 100, 'foo'));
const promise3 = 42;

Promise.all([promise1, promise2, promise3]).then((values) => {
  console.log(values); // [3, 'foo', 42]
});
```

### 72. What is the Promise.race() method?
Promise.race() is a method that takes an array of promises and returns a promise that resolves or rejects as soon as one of the promises in the array resolves or rejects. It’s useful when you want to take action based on the first promise to settle.

Example:
```js
const promise1 = new Promise((resolve) => setTimeout(resolve, 100, 'one'));
const promise2 = new Promise((resolve) => setTimeout(resolve, 50, 'two'));

Promise.race([promise1, promise2]).then((value) => {
  console.log(value); // 'two'
});
```

### 73. What is the difference between setTimeout and setInterval?
setTimeout is a method that allows you to run a function once after a specified delay. It takes two arguments: the function to execute and the time in milliseconds to wait before running it.
```js
setTimeout(() => {
  console.log('This runs after 2 seconds');
}, 2000);
```
setInterval is a method that allows you to run a function repeatedly at specified intervals. It also takes two arguments: the function to execute and the time in milliseconds between each execution.
```js
setInterval(() => {
  console.log('This runs every 2 seconds');
}, 2000);
```

### 74. How do you clear a timeout or an interval in JavaScript?
You can clear a timeout or an interval using the clearTimeout() and clearInterval() methods, respectively. You need to save the reference returned by setTimeout() or setInterval().

Example:
```js
const timeoutId = setTimeout(() => {
  console.log('This will not run');
}, 2000);
clearTimeout(timeoutId); // Cancels the timeout

const intervalId = setInterval(() => {
  console.log('This will not run either');
}, 2000);
clearInterval(intervalId); // Cancels the interval
```

### 75. What are function constructors?
Function constructors are functions used to create objects. You can define a function that acts like a blueprint for creating multiple objects with the same properties and methods. You use the new keyword to create an instance of the object.

Example:
```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const person1 = new Person('Alice', 25);
const person2 = new Person('Bob', 30);
console.log(person1.name); // 'Alice'
console.log(person2.age); // 30
```

### 76. What are template literals and how do you use them?
Template literals are a way to create strings in JavaScript that can contain placeholders. They are enclosed by backticks (`) instead of quotes. You can use ${} to insert variables or expressions into the string.

Example:
```js
const name = 'Alice';
const age = 25;
const message = `My name is ${name} and I am ${age} years old.`;
console.log(message); // 'My name is Alice and I am 25 years old.'
```

### 77. How do you work with dates and times in JavaScript?
You can work with dates and times using the built-in Date object in JavaScript. You can create a new date object, get the current date and time, and perform operations like getting the year, month, day, etc.

Example:
```js
const now = new Date();
console.log(now); // Current date and time
console.log(now.getFullYear()); // Get the current year
console.log(now.getMonth() + 1); // Get the current month (0-11, so add 1)
console.log(now.getDate()); // Get the current day of the month
```

### 78. What are JavaScript classes?
JavaScript classes are a way to create objects using a more structured syntax. They allow you to define a blueprint for creating objects with properties and methods. Classes can also use inheritance.

Example:
```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

const dog = new Animal('Dog');
dog.speak(); // 'Dog makes a noise.'
```

### 79. What is the extends keyword in JavaScript?
The extends keyword is used in class declarations to create a subclass. A subclass inherits properties and methods from a parent class (or superclass). This allows for code reuse and the creation of more specific classes.

Example:
```js
class Animal {
  constructor(name) {
    this.name = name;
  }
}

class Dog extends Animal {
  bark() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Buddy');
dog.bark(); // 'Buddy barks.'
```

### 80. What is inheritance in JavaScript?
Inheritance is a feature in JavaScript that allows one class (the child or subclass) to inherit properties and methods from another class (the parent or superclass). This promotes code reuse and makes it easier to create related classes.

Example:
```js
class Vehicle {
  constructor(brand) {
    this.brand = brand;
  }

  honk() {
    console.log('Beep!');
  }
}

class Car extends Vehicle {
  drive() {
    console.log(`${this.brand} is driving.`);
  }
}

const car = new Car('Toyota');
car.honk(); // 'Beep!'
car.drive(); // 'Toyota is driving.'
```

---

### 81. How do you create private variables in JavaScript?
You can create private variables in JavaScript using closures or by using the # syntax in class fields. Private variables can only be accessed within the function or class where they are defined.

Using closures:
```js
function createCounter() {
  let count = 0; // Private variable

  return {
    increment: function() {
      count++;
      return count;
    },
    getCount: function() {
      return count;
    }
  };
}

const counter = createCounter();
console.log(counter.increment()); // 1
console.log(counter.getCount()); // 1
// console.log(counter.count); // Undefined
```

Using class fields:
```js
class Counter {
  #count = 0; // Private field

  increment() {
    this.#count++;
    return this.#count;
  }

  getCount() {
    return this.#count;
  }
}

const counter = new Counter();
console.log(counter.increment()); // 1
console.log(counter.getCount()); // 1
// console.log(counter.#count); // Syntax error
```

### 82. What is the Object.assign() method?
The Object.assign() method is used to copy the values of all enumerable properties from one or more source objects to a target object. It returns the target object. This method is useful for merging objects or creating copies.

Example:
```js
const target = { a: 1 };
const source = { b: 2, c: 3 };

Object.assign(target, source);
console.log(target); // { a: 1, b: 2, c: 3 }
```

### 83. What is the difference between deep copy and shallow copy?
Shallow copy creates a new object but only copies the references to the original object's properties. If the property is an object, changes to that object in the copied object will affect the original object.

Deep copy creates a new object and recursively copies all properties and nested objects. Changes to the copied object do not affect the original object.

Example:
```js
const original = { a: 1, b: { c: 2 } };

// Shallow copy
const shallowCopy = Object.assign({}, original);
shallowCopy.b.c = 3;
console.log(original.b.c); // 3 (changed)

// Deep copy using JSON
const deepCopy = JSON.parse(JSON.stringify(original));
deepCopy.b.c = 4;
console.log(original.b.c); // 2 (unchanged)
```

### 84. How do you implement memoization in JavaScript?
Memoization is a technique used to optimize functions by caching their results based on their input arguments. When the function is called again with the same arguments, it returns the cached result instead of recalculating.

Example:
```js
function memoize(fn) {
  const cache = {};

  return function(arg) {
    if (cache[arg]) {
      return cache[arg]; // Return cached result
    }
    const result = fn(arg);
    cache[arg] = result; // Store result in cache
    return result;
  };
}

// Example function to memoize
function expensiveCalculation(n) {
  // Simulating a costly computation
  return n * 2;
}

const memoizedCalculation = memoize(expensiveCalculation);
console.log(memoizedCalculation(5)); // 10
console.log(memoizedCalculation(5)); // 10 (cached result)
```

### 85. How do you debounce or throttle functions in JavaScript?
Debouncing and throttling are techniques to control the rate at which a function is executed:

Debouncing ensures that a function is only called after a certain amount of time has passed since the last time it was called. It's useful for events like resizing or typing.
Example:
```js
function debounce(func, delay) {
  let timeout;
  return function(...args) {
    clearTimeout(timeout);
    timeout = setTimeout(() => func.apply(this, args), delay);
  };
}

// Usage
const saveInput = debounce(() => {
  console.log('Input saved');
}, 1000);
```
Throttling ensures that a function is called at most once in a specified time period. It's useful for events like scrolling.
Example:
```js
function throttle(func, limit) {
  let lastFunc;
  let lastRan;

  return function(...args) {
    if (!lastRan) {
      func.apply(this, args);
      lastRan = Date.now();
    } else {
      clearTimeout(lastFunc);
      lastFunc = setTimeout(() => {
        if (Date.now() - lastRan >= limit) {
          func.apply(this, args);
          lastRan = Date.now();
        }
      }, limit - (Date.now() - lastRan));
    }
  };
}

// Usage
const logScroll = throttle(() => {
  console.log('Scroll event fired');
}, 1000);
```

### 86. What is the difference between var, let, and const in terms of scope?
var: Declares a variable that is function-scoped or globally-scoped. It can be re-declared and updated.
```js
var x = 10;
if (true) {
  var x = 20; // Same variable
}
console.log(x); // 20
```
let: Declares a block-scoped variable that can be updated but not re-declared in the same block.
```js
let y = 10;
if (true) {
  let y = 20; // Different variable
}
console.log(y); // 10
```
const: Declares a block-scoped variable that cannot be updated or re-declared. It must be initialized when declared.
```js
const z = 10;
if (true) {
  const z = 20; // Different variable
}
console.log(z); // 10
```

### 87. What is lexical scoping in JavaScript?
Lexical scoping refers to the way variable scopes are determined in JavaScript based on the location in the source code. A function can access variables defined in its own scope, the scope of its parent, and the global scope.

Example:
```js
function outerFunction() {
  const outerVariable = 'I am from outer scope';

  function innerFunction() {
    console.log(outerVariable); // Accessing outerVariable
  }
  
  innerFunction(); // 'I am from outer scope'
}
outerFunction();
```

### 88. What is function hoisting?
unction hoisting is a JavaScript behavior where function declarations are moved to the top of their containing scope during the compilation phase. This allows you to call a function before it is defined in the code.

Example:
```js
console.log(myFunction()); // 'Hello!'

function myFunction() {
  return 'Hello!';
}
```

### 89. What is the eval() function and why is it discouraged?
The eval() function takes a string as an argument and executes it as JavaScript code. It is discouraged because it can introduce security risks, such as executing malicious code, and it can make code harder to understand and debug.

Example:
```js
eval('console.log("Hello from eval!")'); // Executes the code inside the string
```

### 90. What is the difference between strict mode and non-strict mode in JavaScript?
Strict mode is a way to opt into a restricted variant of JavaScript. It helps catch common coding errors and prevents the use of certain features that can lead to problems. Non-strict mode is the default mode in which all JavaScript code runs.

Differences include:

In strict mode, you cannot use undeclared variables.
Assignments to read-only properties throw errors.
You cannot delete variables, functions, or arguments.
To enable strict mode, add 'use strict'; at the beginning of a script or function.

```js
'use strict';
x = 10; // ReferenceError: x is not defined
```

---

### 91. How do you enable strict mode in JavaScript?
You can enable strict mode by adding 'use strict'; at the beginning of your JavaScript file or inside a function. This tells the JavaScript engine to enforce stricter parsing and error handling.

Example:
```js
'use strict'; // Enable strict mode

function myFunction() {
  // This function runs in strict mode
}
```

### 92. What are JavaScript symbols?
Symbols are a special data type in JavaScript that are unique and immutable. They are often used as property keys to avoid name collisions. Each symbol is created using the Symbol() function, and no two symbols are the same, even if they have the same description.

Example:
```js
const mySymbol = Symbol('description');
const obj = {
  [mySymbol]: 'value'
};
console.log(obj[mySymbol]); // 'value'
```

### 93. What are regular expressions in JavaScript?
Regular expressions (regex) are patterns used to match character combinations in strings. They are useful for searching, replacing, or validating strings. In JavaScript, regular expressions are created using the RegExp object or by using a regex literal.

Example of a regex literal:
```js
const regex = /abc/; // Matches the string 'abc'
```

### 94. How do you create and use a regular expression?
You can create a regular expression using either a regex literal or the RegExp constructor. You can then use methods like .test(), .exec(), or string methods like .match() to work with it.

Example:
```js
const regex = /hello/; // Regex literal

console.log(regex.test('hello world')); // true
console.log('hello world'.match(regex)); // ['hello']
```
Using the RegExp constructor:
```js
const regex = new RegExp('hello');
console.log(regex.test('hello world')); // true
```

### 95. What is the difference between deep equality and strict equality?
Strict equality (===) checks if two values are the same in value and type. It does not perform type conversion. Example:

```js
console.log(1 === '1'); // false (different types)
```
Deep equality checks if two objects are equal by comparing their properties and values recursively. Libraries like Lodash provide deep equality checks. Example:
```js
const obj1 = { a: 1, b: { c: 2 } };
const obj2 = { a: 1, b: { c: 2 } };
console.log(JSON.stringify(obj1) === JSON.stringify(obj2)); // true (deep equality)
```

### 96. How do you create an asynchronous function in JavaScript?
You can create an asynchronous function using the async keyword before a function declaration. Inside this function, you can use the await keyword to wait for promises to resolve.

Example:
```js
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  return data;
}

fetchData().then(data => console.log(data));
```

### 97. What is the difference between DOMContentLoaded and load events?
DOMContentLoaded: This event fires when the initial HTML document has been completely loaded and parsed. It does not wait for stylesheets, images, and subframes to finish loading.
Example:
```js
document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM fully loaded and parsed');
});
```
load: This event fires when the whole page, including all dependent resources like images and stylesheets, has finished loading.
Example:
```js
window.addEventListener('load', function() {
  console.log('All resources finished loading!');
});
```

### 98. What are WeakMap and WeakSet in JavaScript?
WeakMap: A collection of key-value pairs where the keys are objects and the values can be any value. The keys are weakly held, meaning if there are no other references to the key object, it can be garbage collected.
Example:
```js
const weakMap = new WeakMap();
const obj = {};
weakMap.set(obj, 'value');
console.log(weakMap.get(obj)); // 'value'
```
WeakSet: A collection of objects where each object is weakly held. Like WeakMap, if there are no other references to the object, it can be garbage collected.
Example:
```js
const weakSet = new WeakSet();
const obj = {};
weakSet.add(obj);
console.log(weakSet.has(obj)); // true
```

### 99. How do you check if an object is empty in JavaScript?
To check if an object is empty (i.e., it has no own properties), you can use Object.keys() to get an array of the object's keys and check if the length is zero.

Example:
```js
const obj = {};
console.log(Object.keys(obj).length === 0); // true (empty object)

const obj2 = { a: 1 };
console.log(Object.keys(obj2).length === 0); // false (not empty)
```

### 100. What is garbage collection in JavaScript?
Garbage collection is the automatic process of identifying and freeing up memory that is no longer being used by the program. This helps to prevent memory leaks and optimize memory usage. JavaScript uses algorithms like mark-and-sweep to manage memory automatically.

---

### 101. What is the purpose of the JavaScript debugger statement?
The debugger statement is used to pause the code right where you want, like placing a bookmark. It allows you to inspect what’s happening in your code, such as checking the values of variables or seeing the flow of the program. When the debugger is triggered, you can step through your code line by line to find issues.

### 102. What is the difference between window and document in JavaScript?
Window is the global object that represents the browser window. It contains things like browser settings, window size, and can access methods like alert() or setTimeout().
Document is a part of the window and represents the web page itself. It allows you to interact with the HTML structure, like finding elements or changing text on the page.

### 103. What is an anonymous function in JavaScript?
An anonymous function is a function that doesn’t have a name. It’s often used when you only need a function temporarily or want to pass it around without bothering to give it a name.

Example:
```js
const greet = function() {
  console.log('Hello!');
};
greet(); // 'Hello!'
```
Here, the function has no name, but it still works.

### 104. What are getter and setter methods in JavaScript?
Getter and setter methods are special functions used to control how a property of an object is accessed or changed. A getter fetches the value, and a setter updates it. It’s like having a gatekeeper for your object’s properties.

Example:
```js
const person = {
  firstName: 'John',
  lastName: 'Doe',
  get fullName() {
    return this.firstName + ' ' + this.lastName;
  },
  set fullName(name) {
    [this.firstName, this.lastName] = name.split(' ');
  }
};

console.log(person.fullName); // 'John Doe'
person.fullName = 'Jane Smith';
console.log(person.fullName); // 'Jane Smith'
```

### 105. How do you create an object in JavaScript?
There are many ways, but the simplest one is using curly braces {}. Inside the braces, you define properties for the object, like this:
```js
const car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2020
};
```
This creates an object called car with properties make, model, and year.

### 106. What is the difference between const and Object.freeze()?
const is used to declare variables that can’t be reassigned. However, the contents of an object declared with const can still be changed.
Object.freeze() makes sure that no changes can be made to the object at all. It locks the object so no properties can be added, removed, or modified.
Example:
```js
const obj = { name: 'Alice' };
Object.freeze(obj);
obj.name = 'Bob'; // This won’t work, the object is frozen
```

### 107. What is the difference between a shallow copy and a deep copy in JavaScript?
A shallow copy copies an object’s top-level properties, but if those properties are objects themselves, only the references are copied, not the actual objects.
A deep copy creates a copy of the object and all of its nested objects, ensuring that everything is fully duplicated.
Shallow copy:
```js
const original = { a: 1, b: { c: 2 } };
const copy = { ...original };
copy.b.c = 3; // This will also change original.b.c because it’s a shallow copy
```
Deep copy:
```js
const deepCopy = JSON.parse(JSON.stringify(original)); // Full independent copy
```
### 108. How do you compare objects in JavaScript?
To compare objects, you can’t just use === because that checks if they are the same reference (not the content). Instead, you usually compare their properties manually, or use a library to do a deep equality check.

Example:
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { a: 1, b: 2 };

console.log(JSON.stringify(obj1) === JSON.stringify(obj2)); // true (same content)
```

### 109. What is the arguments object in JavaScript?
The arguments object is like a built-in array for functions. It holds all the arguments passed to the function, even if you didn’t define parameters. This is useful when you don’t know in advance how many arguments will be passed. also it only works in traditonal functions.

Example:
```js
function showArguments() {
  console.log(arguments);
}

showArguments(1, 2, 3); // Outputs: { '0': 1, '1': 2, '2': 3 }
```

### 110. What is a pure function in JavaScript?
A pure function is a function that always returns the same result if given the same inputs and doesn’t change anything outside its scope (no side effects). Pure functions are predictable and easier to test.

Example:
```js
function add(a, b) {
  return a + b; // Always the same result for the same inputs
}
```
Pure functions don't rely on external variables and don’t modify external states.

---

### 111. What is memoization in JavaScript?
Memoization is a way to speed up functions by saving (caching) the results of expensive operations. If the function is called again with the same arguments, it returns the cached result instead of recalculating it.

### 112. How do you perform deep cloning of an object in JavaScript?
To create a full copy (deep clone) of an object, you can use JSON.parse(JSON.stringify(object)) or libraries like Lodash. This copies everything, including nested objects.

### 113. What is the difference between synchronous and asynchronous iteration in JavaScript?
Synchronous iteration happens one step at a time, blocking the code until each step is done.
Asynchronous iteration allows the code to continue while waiting for operations (like fetching data) to complete without blocking.

### 114. What is a symbol in JavaScript, and why would you use it?
A symbol is a unique value that you can use as a key for object properties. It helps avoid property name conflicts because each symbol is different, even if they seem similar.

### 115. What is the hasOwnProperty() method?
hasOwnProperty() checks if an object has a specific property, ensuring that it’s not inherited from its prototype chain.

### 116. How do you merge arrays in JavaScript?
You can merge arrays using the spread operator [...] or Array.concat() method. Example:
```js
const merged = [...array1, ...array2];
```

### 117. What is the purpose of the reduce() method in arrays?
reduce() is used to go through all the elements of an array and combine them into a single value, like summing numbers or flattening arrays.

### 118. What is the difference between Array.from() and Array.of()?
Array.from() creates an array from something like a string or a list-like object.
Array.of() creates an array from the arguments you give it.

### 119. What is the difference between map() and forEach() in arrays?
map() returns a new array after applying a function to each element.
forEach() just runs a function for each element but doesn’t return anything.

### 120. What is the use of the every() and some() methods in arrays?
every() checks if all elements in an array pass a test.
some() checks if at least one element passes a test.

---

### 121. How do you convert a string to an array in JavaScript?
You can use the split() method to turn a string into an array. For example:
```js
let str = "hello world";
let arr = str.split(" ");  // ["hello", "world"]
```

### 122. How do you reverse a string in JavaScript?
To reverse a string, you can split it into an array, reverse the array, and then join it back into a string:
```js
let reversed = str.split("").reverse().join("");
```

### 123. How do you remove duplicates from an array in JavaScript?
You can remove duplicates using a Set, which only keeps unique values:
```js
let uniqueArr = [...new Set(array)];
```

### 124. How do you flatten an array in JavaScript?
To flatten an array, you can use flat():
```js
let flatArr = array.flat();
You can also specify depth like array.flat(2) to flatten more levels.
```

### 125. What is the difference between Array.prototype.sort() and Array.prototype.reverse()?
sort() arranges the elements in a specific order (like alphabetical or numerical).
reverse() simply flips the order of the elements in the array.

### 126. What is the Math.random() method, and how do you generate a random number in JavaScript?
Math.random() generates a random number between 0 and 1. To get a number in a specific range, you can multiply it:
```js
let randomNum = Math.random() * 10; // Random number between 0 and 10
```

### 127. How do you round a number to a specific number of decimal places in JavaScript?
You can use toFixed() to round a number to a certain number of decimals:
```js
let rounded = num.toFixed(2);  // Rounds to 2 decimal places
```

### 128. What is the Math.floor(), Math.ceil(), and Math.round() methods?
Math.floor() rounds down to the nearest whole number.
Math.ceil() rounds up to the nearest whole number.
Math.round() rounds to the nearest whole number based on standard rounding rules.

### 129. How do you format a number as a currency string in JavaScript?
You can use toLocaleString() to format a number as currency:
```js
let currency = num.toLocaleString('en-US', { style: 'currency', currency: 'USD' });
```

### 130. How do you find the maximum or minimum value in an array of numbers in JavaScript?
You can use Math.max() and Math.min() with the spread operator:
```js
let max = Math.max(...array);
let min = Math.min(...array);
```

---

### 131. What are setTimeout() and setInterval() methods?
setTimeout() runs a function after waiting for a certain amount of time. For example, you can delay something by 2 seconds.
setInterval() keeps running a function repeatedly at fixed intervals. For example, you can run a function every 3 seconds until you stop it.

### 132. How do you convert a date to a string in a specific format in JavaScript?
ou can use toLocaleDateString() or toISOString() to format a date:
```js
let date = new Date();
let formattedDate = date.toLocaleDateString("en-US");  // MM/DD/YYYY
```
Or use toISOString() for a standard format.

### 133. How do you calculate the difference between two dates in JavaScript?
You can subtract two Date objects to get the difference in milliseconds, then convert that into days or hours:
```js
let diff = (date2 - date1) / (1000 * 60 * 60 * 24); // Difference in days
```

### 134. What is a Date object in JavaScript, and how do you create it?
The Date object represents a specific point in time. You can create it by:
```js
let today = new Date();
```
You can also pass a specific date like:
```js
let myBirthday = new Date('1990-01-01');
```

### 135. How do you compare two dates in JavaScript?
You can compare two dates using getTime() to get their millisecond values:
```js
if (date1.getTime() > date2.getTime()) {
  console.log("date1 is after date2");
}
```

### 136. How do you convert a JavaScript date to UTC format?
### 137. What is the difference between encodeURI() and encodeURIComponent()?
### 138. How do you decode a URL in JavaScript?
### 139. What is the use of the new keyword in JavaScript?
### 140. How do you define a constructor function in JavaScript?
### 141. How do you inherit properties from another object in JavaScript?
### 142. What is the purpose of the prototype property in JavaScript?
### 143. How do you create an instance of an object using a constructor function?
### 144. What is prototypal inheritance in JavaScript?
### 145. How do you use the Object.create() method for inheritance?
### 146. What is the purpose of the super() keyword in JavaScript?
### 147. How do you create a subclass in JavaScript using the extends keyword?
### 148. What is the constructor property in JavaScript?
### 149. How do you add methods to a JavaScript class?
### 150. What is a static method in JavaScript?
### 151. How do you check if an object is an instance of a class in JavaScript?
### 152. What is the difference between a class and an object in JavaScript?
### 153. How do you define a method in a JavaScript class?
### 154. What is the use of the constructor method in a JavaScript class?
### 155. How do you override a method in JavaScript?
### 156. How do you implement method chaining in JavaScript?
### 157. What is the difference between the function keyword and an arrow function in JavaScript?
### 158. How do you handle exceptions in JavaScript using try...catch?
### 159. How do you rethrow an error in JavaScript?
### 160. What is the use of the finally block in exception handling?
### 161. What are JavaScript built-in errors?
### 162. What is a custom error in JavaScript?
### 163. How do you define and throw a custom error in JavaScript?
### 164. What is the purpose of the stack trace in error handling?
### 165. How do you catch multiple types of errors in JavaScript?
### 166. What is the purpose of the throw statement in JavaScript?
### 167. How do you define a module in JavaScript?
### 168. What is the export and import syntax in JavaScript modules?
### 169. How do you export multiple values from a JavaScript module?
### 170. How do you import only specific parts of a module in JavaScript?
### 171. What is the default export in JavaScript?
### 172. How do you rename imports or exports in JavaScript?
### 173. What is the difference between named and default exports in JavaScript?
### 174. How do you import a module dynamically in JavaScript?
### 175. What is tree shaking in JavaScript?
### 176. What are CommonJS modules in JavaScript?
### 177. How do you convert a CommonJS module to an ES module?
### 178. How do you handle circular dependencies in JavaScript modules?
### 179. What is a module bundler in JavaScript?
### 180. What is Webpack, and how does it work?
### 181. How do you configure Webpack for a JavaScript project?
### 182. What are entry and output properties in a Webpack configuration?
### 183. How do you define loaders in a Webpack configuration?
### 184. What is the purpose of plugins in Webpack?
### 185. What is the difference between a loader and a plugin in Webpack?
### 186. How do you configure Babel with Webpack?
### 187. What is code splitting in Webpack?
### 188. How do you optimize Webpack build performance?
### 189. What is hot module replacement (HMR) in Webpack?
### 190. How do you use Webpack with React?
### 191. How do you configure Webpack for production and development environments?
### 192. What are source maps in JavaScript, and how do they work?
### 193. How do you enable source maps in Webpack?
### 194. What is lazy loading in JavaScript?
### 195. How do you implement lazy loading in a React application?
### 196. What is code splitting in React?
### 197. How do you use React.lazy() for dynamic imports?
### 198. How do you handle errors in dynamically loaded components in React?
### 199. What is the Suspense component in React?
### 200. How do you use the Suspense component for code splitting in React?
