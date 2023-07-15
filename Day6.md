# Day6 : Introduction, JavaScript Principles ,Functions & Callbacks

## Lesson Summary


## Coding Examples
```javascript
//Challenge 1
//Create a function addTwo that accepts one input and adds 2 to it.
function addTwo(num) {
  const output = num +2 ; 
  return output

}

// To check if you've completed it, uncomment these console.logs!
console.log(addTwo(3));
console.log(addTwo(10));

//Challenge 2
//Create a function addS that accepts one input and adds an "s" to it.
function addS(word) {
  return word + 's';

}

// uncomment these to check your work
console.log(addS('pizza'));
console.log(addS('bagel'));

/* Challenge 3
Create a function called map that takes two inputs:
an array of numbers (a list of numbers)
a 'callback' function - a function that is applied to each element of the array (inside of the function 'map')
Have map return a new array filled with numbers that are the result of using the 'callback' function on each element of the input array.
map([1,2,3,4,5], multiplyByTwo); //-> [2,4,6,8,10]
multiplyByTwo(1); //-> 2
multiplyByTwo(2); //-> 4
  */


```

## Coding Challenges from FreeCodeCamp
1. #### [Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)
 My Solution:
```javascript

```


2. #### [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

  My Solution:
```javascript

```

3. #### [Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)


 My Solution:
```javascript


```
#  Notes for me => 
- a function we insert in the higher order function is called the call back function.
- any function that takes in a function or returns one out  automatically is a higher-order function.
