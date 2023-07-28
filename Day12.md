# Day12: scope and function expressions, advanced scope.


## Lesson Summary
In this lesson, I've learned about many topics :
- function expression: that a function who declared in a variable.
- function declaration: how to know that? if the function word is literally in the first thing of the statement.
- lexical scope:
- dynamic scope:
- (Named) Function Declaration > Named Function Expression > Anonymous Function Expression.
- IIFE pattern
- block scope: a scope with curly brackets.
- var or let?
- Global Scope: Any variable declared outside of a function is said to have Global Scope.
- Local Scope: Any variable that you declare inside a function is said to have Local Scope. You can access a local variable can within a function. If you try to access any variable defined inside a function from outside or another function, it throws an error.
- Block Scope: With the introduction of let and const keywords, it added a new type of Scope in JavaScript. You cannot access the variables declared inside a particular block (represented by {}) from outside the block. 
- Function Scope: With the creation of each new function, it creates a new scope in JavaScript. You cannot access variables defined inside a function from outside the function or from another function. Var, let, and const work similarly when used inside a function.
  ![image](https://github.com/aya-soghayyer/Mastering-JavaScript-in-20-Days/assets/128791822/af4a6b06-d05a-481b-90e0-564e7ea09a69)



## Coding Examples
```javascript
var t = 'aya'; 
{
  let t = 'yas'; 
  console.log(t);
}

console.log(t);
//the result:
// yas
//aya

var t = 'aya'; 
{
  var t = 'yas'; 
  console.log(t);
}

console.log(t);
//the result:
//yas
//yas
```

## Coding Challenges :
# Learning sprint (1), week (3), day (3) deliverables

## Scope & Function Expressions:

### QUESTION #1

Create a function called `arrowHOF` that takes an arrow function as input and
returns a new arrow function that enhances the behavior of the input function. 

The enhanced function should accept additional arguments and execute the input
function multiple times based on these arguments.


```javascript

const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
}

const exampleNormalFunc2 = (x, y) => {
  return x * y;
}

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
}


const arrowHOF = (normalFunc) => {
  // write your code here;
}

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1);
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3);

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 60 twice
console.log(hofNormalFunc2(20, 35))(4); // logs 700 four times
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once

```

-------------------------------------------------------------------
## Scope & Function Expressions:

### QUESTION #2

Build a function called `preserveThis` that takes a function as input and
returns a new arrow function that behaves the same way as the input function but
preserves the original this context when used as a method of an object.

```javascript

// Example object
const obj = {
  name: 'John',
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}!`);
  }
};

const preserveThis = (func) => {
  //Write your code here;
  return func;
}

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet('Hello'); // Output: "Hello, John!"

```

-------------------------------------------------------------------
## Scope & Function Expressions:

### QUESTION #3

Consider the 2 following examples and distinguish the different output in each
one with them with reasoning.

**Example 1:**

```javascript
function outer1() {
  var x = 10;

  var inner1 = function() {
    console.log(x);
  };

  inner1();
}

outer1(); // Output: 10
```

> **Reasoning for example 1's output:**
> because  
> .................................................................................

--------

**Example 2:**

```javascript
function outer2() {
  var x = 10;

  var inner2 = function() {
    var x = 20;
    console.log(x);
  };

  inner2();
}

outer2(); // Output: 20
```

> **Reasoning for example 2's output:**  
> .................................................................................


#  Notes for me => 
