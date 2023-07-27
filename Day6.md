# Day6: Introduction, JavaScript Principles,Functions & Callbacks

## Lesson Summary
I've learned :
- a function we insert in the higher order function is called the call back function.
- any function that takes in a function or returns one out  automatically is a higher-order function.
   ![image](https://github.com/aya-soghayyer/Mastering-JavaScript-in-20-Days/assets/128791822/7be19b51-66b8-490d-9171-58ba45e2a982)



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
1. #### [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)
 My Solution:
```javascript
const squareList = arr => {
  // Only change code below this line
 let newarr= arr.filter(n => {
    return (n >0) && (n%parseInt(n)===0);
  })
 newarr= newarr.map( arr => {return arr*arr});
  return newarr;
  // Only change code above this line
}
const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);
```


2. #### [Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)

  My Solution:
```javascript
// Only change code below this line
function urlSlug(title) {
 return title
      .toLowerCase()
      .trim()
      .split(/\s+/)
      .join("-");
}
// Only change code above this line
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");
```

3. ####
# Learning sprint (1), week (2), day (1) deliverables

## Question 1: Functions and Callbacks

Implement a JavaScript function called mapAsync that takes an array and a callback function. 
The function should map each element of the array to a new value using the callback function 
asynchronously. 
The final result should be returned as a Promise.

my Solution:
```javascript

```

-------------------------------------------------------------------
## Question 2: Call Stack and Recursion

Write a JavaScript function called sumRange that calculates the sum of all integers in a given range. 
The function should use recursion to handle the calculation and demonstrate an understanding of the call stack.

 My Solution:
```javascript
const sumRange = (a, b )=>{
 if (a<b )
  return a + sumRange(a+1,b);
  else return a ; 
}

console.log(sumRange(1,5));


```
#  Notes for me => 
- some functions: reduce, map, filter, trim, split, join, replace(  ,   ).
