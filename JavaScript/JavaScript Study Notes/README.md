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

- 