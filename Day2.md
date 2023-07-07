# Day2: Expressions, Arrays, objects


## Lesson Summary


## Coding Examples
```javascript
// in Tic Tac Toe project :
//declare my name :
const aya = "Aya";

//The combined age of your parents
let combainedParentsAge = 45 + 56;

//The #board element on the page
let board = document.querySelector("#board");

["c," "a", "d", "b"].sort()
//the result : (4) ['a', 'b', 'c', 'd']

[1, 2, 3].concat([4, 5, 6])
//the result : (6) [1, 2, 3, 4, 5, 6]

//when I push one number in the push function vs push more than one number in push function
let a = [1,2,3]
a
//the result : (3) [1, 2, 3]0: 11: 22: 3length: 3[[Prototype]]: Array(0)
a.push(4)
a
//the result : (4) [1, 2, 3, 4]
a.push([5,6,7])
a
//the result : (5) [1, 2, 3, 4, Array (3)]0: 11: 22: 33: 44: (3) [5, 6, 7]length: 5[[Prototype]]: Array(0)

// new exercise 
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const spiceGirls = {
    albums: ["Spice", "Spiceworld", "Forever"],
    motto: "Girl Power",
    members: spices
};


spiceGirls.motto
//The result: 'Girl Power'

spiceGirls.albums[1]
//the result: 'Spiceworld'
spiceGirls.members[4].name
//the result: 'Victoria'
spiceGirls.members[1].nickname
//the result: 'Ginger'

```

## Coding Exercises
1. ### [Profile Lockup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

My solution:
```javascript

```
# Notes for me => 
-Arrays can hold any type of items or mix and match.
-when I push some of the numbers in an array using function push like this format push([]),  it will make a nested array.
-"Mutable" data can be edited (e.g. Arrays, objects)
"Immutable" data always stays the same (e.g. strings & other primitives).
-concat() did not change the original Array. It changed the new Array.
-Using immutable data & variables is usually best
-if I use mutable value in immutable, we'll break the rule of immutable (I can make some edits in ). 
-jects collect multiple values together to describe more complex data.
Arrays are just a special kind of object.
-Properties can point to functions, too. We call function-properties "methods" on objects



