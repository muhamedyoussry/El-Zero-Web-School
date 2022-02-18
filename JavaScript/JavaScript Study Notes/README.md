<h1 align="center">JavaScript Study Notes</h1>


<h2 align="center">General Notes</h2>

- *HTML* and *CSS* are markup languages. Markup languages are used to describe and define elements within a document.*JavaScript* is a programming language. Programming languages are used to communicate instructions to a machine. Programming languages can be used to control the behavior of a machine and to express algorithms.
- you can see the effect of `javaScript` code using console tab from the web developer tools.


<h2 align="center">Data types and variables</h2>

- Defining a number in JavaScript is actually pretty simple. The **Number** data type includes any positive or negative integer, as well as decimals.
  - You can also perform calculations with numbers pretty easily.
  - You can compare two numbers to see if one’s greater than, less than, or equal to the other.
- You can use **comments** to help explain your code and make things clearer.
- **Strings** are number of any characters enclosed by single or double quotations.
  - **Concatenating** two strings together is mean to add strings together.
- **Variables** are used to store different data.
  - variables *naming convention*s such as: camelCase, snak_case, kabab-case, etc.

``` js
var variable_name = value; // creating variable iwht snak_case
```
- we can access the array character by entering the index inside a square brackets `name[0]`.
- we can escape special characters using backslash `\` before the target character.
- we can compare strings using comparios operators.
- you can use the function `.charCodeAt(string_index)` to return the ASCII value of a character.
- A boolean variable can take either of two values - `true` or `false`.
- JavaScript is known as a loosely typed language. Basically, this means that when you’re writing JavaScript code, *you do not need to specify data types*.
- `number.toFixed(decimal_points)` is used to round a number to the `decimal_points`.

<h2 align="center">Conditionals</h2>

- if...else statemetns, else if statement.

``` js
var weather = "sunny";

if (weather === "snow") {
  console.log("Bring a coat.");
} else if (weather === "rain") {
  console.log("Bring a rain jacket.");
} else {
  console.log("Wear what you have on.");
}
```
- logical operators: AND, OR, NOT.
- Advanced conditionals:
  - Truthy and Falsy: Every value in JavaScript has an inherent boolean value. When that value is evaluated in the context of a boolean expression, the value will be transformed into that inherent boolean value.
  - switch statement: A switch statement is an another way to chain multiple else if statements that are based on the same value without using conditional statements.The break statement can be used to terminate a switch statement and transfer control to the code following the terminated statement.
  - Ternary operator: The ternary operator provides you with a shortcut alternative for writing lengthy if...else statements.
  
  ```js
  var color = isGoing ? "green" : "red";
  // conditional ? (if condition is true) : (if condition is false)
  ```
<h2 align="center">Loops</h2>

- loops will let you iterate over values and repeat block of code.
  - when to start: initialization
  - when to stop: condition
  - how to get to the next item: update
- for loops *vs* while loops
  - the difference is in for loops you will define initialization, condition and update in begin of the loop.

``` js
for (var i = 0; i < 6; i = i + 1) {
  console.log("Printing out i = " + i);
}
```
- prefix and postfix increment and decrement operations.
```js
x++ ; // postfix increment
++x ; // prefix increment
```
- Scope in JavaScript types:
  - Global scope: can eb used anywhere in the code.
  - Funciton scope (local variable): can be used within a particular funciton.
  - Block scope: can be use in a pair of `{....}`
- Variable declaration types:
  - `let` It a new way to declare a variable in any scope - Global, Local, or Block. The value of this variable can be changed or reassigned anytime within its scope.
  - `const` It is also a way to declare constants in any scope - Global, Local, or Block. Once you are assigned a value to a `const` variable, the value of this variable **CANNOT** be changed or reassigned throughout the code.
  - `var` This is the old way of declaring variables in only two scope - Global, or Local. Variables declared with the `var` keyword can not have Block Scope. The value of this variable can be changed or reassigned anytime within its scope.

<h2 align="center">Functions</h2>

- Functions allow you to package up lines of code that you can use (and often reuse) in your programs.
- functions can have number of parameters or no parameters at all.

```js
function doubleGreeting(name, otherName) {
  // code to greet two people!
}
```
- A *parameter* is always going to be a *variable name* and appears in the function declaration. On the other hand, an *argument* is always going to be a *value*.
- scope overriding or shadowing, must be sure to make a new variable and not reassign the global variable

```js
var x = 1;

function addTwo() {
  var x = x + 2; // shadowing or scope overriding
}

addTwo();
x = x + 1;
console.log(x);
```
- If an identifier is declared in global scope, it's available everywhere.
- If an identifier is declared in function scope, it's available in the function it was declared in (even in functions declared inside the function).
- before any JavaScript is executed, all functions are **hoisted** to the top of their current scope.
- JavaScript **hoists** function declarations and variable declarations to the to/p of the current scope.
- Variable assignments are *not hoisted*.
- Declare functions and variables at the top of your scripts, so the syntax and behavior are consistent with each other.
- you can also store functions in variables. When a function is stored inside a variable it's called a **function expression**.
  - All function declarations are hoisted and loaded before the script is actually run. Function expressions are not hoisted, since they involve variable assignment, and only variable declarations are hoisted. 
```js
// anonymous function expression
var doSomething = function(y) {
  return y + 1;
};

// named function expression
var doSomething = function addOne(y) {
  return y + 1;
};
```
- example of inline funcitons
```js

// emotions() function definition
function emotions(myString, myFunc) {
    console.log("I am " + myString + ", " + myFunc(2));
}

// Call the emotions() function with two arguments
// Argument 1 - "happy" string
// Argument 2 - an inline function expression
emotions ("happy", function(num) {
    var sound = ""; // Local variable
    //Iterate
    for (var i = 0 ; i < num ; i++) {
        sound = sound + "ha" ;  
    }
    sound = sound +"!"; 
    return sound; 
});
```

<h2 align="center">Arrays</h2>

- an Array is a data structure that we can use to store multiple values in one container.
- You can store any data types in an array, even an array in an array to create a nested array!
- 
```js
// write nested arrays in single lines to maek it easy to read them
var arraysInArrays = [
  [1, 2, 3], 
  ["Julia", "James"], 
  [true, false, true, false]
];
```
- index is the location or the poisition of the array element and starts from 0.
- built-in properties and methods in array:
  - *property*: length
  - *methods*: push, pop, splice,shift, unshift, join, toUpperCase [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- the forEach() loop method iterates over the array without the need of an explicitly defined index.

```js
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

donuts.forEach(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  console.log(donut);
});
```
- creating a new array from an existing array is simple with the powerful `map()` method.
```js
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

var improvedDonuts = donuts.map(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  return donut;
});
```
- 2d Array
```js
for (var row = 0; row < donutBox.length; row++) {
  // here, donutBox[row].length refers to the length of the donut array currently being looped over
  for (var column = 0; column < donutBox[row].length; column++) {
    console.log(donutBox[row][column]);
  }
}
```
<h2 align="center">Objects</h2>

- objects wrap/group data members and data functions in one user defined data type. (Encabsulation)
```js
// the entire object is wrapped insed {...}
var sister = {
  name: "Sarah", // key: value
  age: 23, // don't forget the comma after each decleration except the last line
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true
};
```
- you can access object data members by two ways:
  - *bracket notation* `sister["parents"]`
  - *dot notation* sister.parents
- naming conventions in objects:
  - do not use quotation marks to name the property (data Member)
  - do not start your property name with number
  - do not use hiphens or spaces in your property names


<h2 align="center">ES6: the future of JavaScript</h2>

- Hoisting is a result of how JavaScript is interpreted by your browser. Essentially, before any JavaScript code is executed, all variables declared with `var` are "hoisted", which means they're raised to the top of the function scope.
- Variables declared with `let` and `const` eliminate the issue of hoisting because they’re scoped to the block, not to the function.
  - Variables declared with `let` can be reassigned, but can’t be redeclared in the same scope.
  - Variables declared with `const` must be assigned an initial value, but can’t be redeclared in the same scope, and can’t be reassigned.
- The big question is when should you use let and const? The general rule of thumb is as follows:
  - use `let` when you plan to reassign new values to a variable, and
  - use `const` when you don’t plan on reassigning new values to a variable.
- we will not need to use `var` anymore, because it will be a bad practise.
- **Template literals** are essentially string literals that include embedded expressions.

```js
let message = `${student.name} please see ${teacher.name} in ${teacher.room} to pick up your report card.`;
```
- Here’s where *template literals* really shine. In the code animation above, the quotes and string concatenation operator have been dropped, as well as the newline characters `\n`. That's because template literals also preserve newlines as part of the string!

```js
let message = `${student.name}
please see ${teacher.name} in ${teacher.room} to pick up your report card.
Thank You`;
```
- **Destructuring** borrows inspiration from languages like Perl and Python by allowing you to specify the elements you want to extract from an array or object on the left side of an assignment.
  - Destructuring from an array.

```js
const point = [10, 25, -34];

const [x, y, z] = point;

console.log(x, y, z);
```
- Destructuring from an object. you can't access methods

```js
const gemstone = {
  type: 'quartz',
  color: 'rose',
  carat: 21.29
};

const {type, color, carat} = gemstone;

console.log(type, color, carat);
```

- **Object literal shorthand**
```js
let type = 'quartz';
let color = 'rose';
let carat = 21.29;

const gemstone = {
  type, // without reduntant `type: type,`
  color,
  carat,
  calculateWorth:() { // without the word function
    // will calculate worth of gemstone based on type, color, and carat
  }
};
```

- the for loop, for..in loop, and the for..of loop.
  - the for loop problems are indexing and exit condition; too many details
  - the for..in loop problem is indexing
  - the for..of loop is the easiest.

```js
// the for loop
const digits = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];

for (let i = 0; i < digits.length; i++) {
  console.log(digits[i]);
}

// the for.. in loop
const digits = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];

for (const index in digits) {
  console.log(digits[index]);
}

// the for..of loop
const digits = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];

for (const digit of digits) {
  console.log(digit);
}
```
- The **spread operator**, written with three consecutive dots `( ... )`, is new in ES6 and gives you the ability to expand, or spread, iterable objects into multiple elements.
```js
const books = ["Don Quixote", "The Hobbit", "Alice in Wonderland", "Tale of Two Cities"];
console.log(...books);
// result: Don Quixote The Hobbit Alice in Wonderland Tale of Two Cities
```
- you can use the spread operator to concatinate number of arrays in an iterable way.

```js
const produce = [...Arr1, ... Arr2];
```

- The **rest parameter**, also written with three consecutive dots `( ... )`, allows you to represent an indefinite number of elements as an array.
```js
const order = [20.17, 18.67, 1.50, "cheese", "eggs", "milk", "bread"];
const [total, subtotal, tax, ...items] = order;
console.log(total, subtotal, tax, items);
```
- one of the use cases for the **rest parameter** is when you’re working with variadic functions. Variadic functions are functions that take an indefinite number of arguments.
```js
function sum(...nums) {
  let total = 0;  
  for(const num of nums) {
    total += num;
  }
  return total;
}
```

```js
/*
 * Programming Quiz: Using the Rest Parameter (1-5)
 */

// your code goes here

function average(...nums) {
    let avg = 0;
    let sum = 0;
    for (const num of nums){
        sum = sum + num;
    }
    if (sum === 0){
        return avg;
    }
    avg = sum/nums.length;
    return avg;
}

console.log(average(2, 6));
console.log(average(2, 3, 3, 5, 7, 10));
console.log(average(7, 1432, 12, 13, 100));
console.log(average());
```

<h2 align="center">JavaScript & the DOM </h2>

<h3 align="center">The Document Object Model</h3>

- The DOM stands for "Document Object Model" and is a tree-like structure that is a representation of the HTML document, the relationship between elements, and contains the content and properties of the elements.
- The DOM is not:
  - part of the JavaScript language
- The DOM is:
- constructed from the browser
- is globally accessible by JavaScript code using the document object
- HTML document object methods
  - we can select page element by id using the document object method `document.getElementById('footer');`
  - we can select page element by class using the document object method `document.getElementsByClassName();` - take care of the `s`
  - we can select page element by its tag using the document object method `document.getElementsByTagName('p');` - take care of the `s`
  - they all return a live HTMLCollection of found elements.
- We can use the `.querySelector()` method to select elements just like we do with CSS. We use the `.querySelector()` method and pass it a string that's just like a CSS selector. But, it only returns one element.

```js
// find and return the element with an ID of "header"
document.querySelector('#header');

// find and return the first element with the class "header"
document.querySelector('.header');

// find and return the first <header> element
document.querySelector('header');
```
- we can use `.querySelectorAll()` to return multiple elements.

<h3 align="center">Creating Content with JavaScript</h3>


