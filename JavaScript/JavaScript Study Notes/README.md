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
- 