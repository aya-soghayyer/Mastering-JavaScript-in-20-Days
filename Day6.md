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
function map(array, callback) {
   const output = []; 
   for(let i = 0 ;i< array.length ; i++){
     output.push(callback(array[i]));
   }
   return output ; 

 }

  console.log(map([1, 2, 3], addTwo));

/*Challenge 4
Create a function called forEach that takes an array and a callback, and runs the callback on each element of the array. forEach does not return anything.
let alphabet = '';
const letters = ['a', 'b', 'c', 'd'];
forEach(letters, function(char) {
  alphabet += char;
});
console.log(alphabet);   //prints 'abcd'*/
function forEach(array, callback) {
  const output = []
  for(let i=0  ; i<array.length ; i++)
output.push(callback(array[i]));
  return output;
}

// see for yourself if your forEach works!
console.log(forEach([1,2,3], addTwo));

/*Challenge 5
In challenge 3, you've created a function called map. In this challenge, you're going to rebuild the map function by creating a function called mapWith. This time you're going to use forEach inside of mapWith instead of using a for loop.*/

function mapWith(array, callback) {
  let output = [];
 output= forEach(array , callback );
 
    return output;
}
console.log(mapWith([1,2,3], addTwo));

```

## Coding Challenges from FreeCodeCamp
1. #### [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem
](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)
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
