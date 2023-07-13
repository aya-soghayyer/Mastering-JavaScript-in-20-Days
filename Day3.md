# Day3 : quize project , quize project function 


## Lesson Summary
I've learned about functions and how can I declare a normal function and an arrow function also I had knowledge about scopes and how they impact the value of variables.

## Coding Examples
```javascript
// fucntion mutlti
function multiply(a,b){return a*b} multiply(3,4)
//the result: 12

// function convert sentence to uppercase
const yell = sentence =>  sentence.toUpperCase(); yell("hello world")
//the result: 'HELLO WORLD'

//function longerthan return that the first variable longer than the second
const longerThan = (a,b )=>  a.length > b.length ; longerThan([1,3,4],[3,4])
//the result: true

//function divide
const divide = (x,y ) => x/y ; 
divide(72,8)
//the result: 9

// function convert sentence to lowercase
const whisper = sentence =>  sentence.toLowerCase(); whisper("HELLOW WORLD !")
//the result: 'hellow world !'
```

## Coding Exercises
1. ### [Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)
my solution:
```javascript
const timesFive= val => val*5 ; 
```
2. ### [Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)
my solution:
```javascript
// Declare the myGlobal variable below this line
const myGlobal = 10 ; 

function fun1() {
  // Assign 5 to oopsGlobal here
oopsGlobal= 5 ; 
}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```
3. ### [Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)
my solution:
```javascript
function myLocalScope() {
  // Only change code below this line
   let myVar ; 
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```
4. ### [Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)
my solution:
```javascript
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
   var outerWear = "sweater";
  // Only change code above this line
  return outerWear;
}

myOutfit();
```
5. ### [Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)
my solution:
```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item)
  // let arr1 = arr.reverse();
  // arr1.pop();
  // arr1.reverse();
  return  arr.shift();
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```

# Notes for me => 
- Dom functions: document.getElementByName(true or btn or any value in {name}  ) e.g : <button> name: "btn" value="true"></button>, setAttribute("value", "true"), removeAttribute("value"), toString() to convert the variable to string .
- wider scope e.g. global scope, narrower scope e.g. function scope.
- function shift() removes the first item from an array.
