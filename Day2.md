# Day2: Expressions, Arrays, objects


## Lesson Summary
In this session, I learned new three essential topics: 
1. Expressions: the main difference between expressions and statements is expression is some operation or sentence in js without containing a (=) sign in it, and a statement is vice versa, the sentence to be a statement should contain a (=) sign.
2. Arrays: a set of multiple values that keep them together in one variable which helps to save the storage, also we have functions that are used in arrays I mentioned below
3. Objects: collect multiple values together to describe data or complex data, also we'd token about built-in objects like math, console, strings, and documents, for more details go to  Notes for me.
4. Mutable: data can be edited like arrays.
5. Immutable: date stays the same.


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

// array can contain a mix of values in one variable
let mixedArray = ["pop", 6, "squish", false, document];


//this in a method lets us reference other properties on the object
anjana.speak = function () {
    console.log("Hi my name is", this.name);
}
anjana.speak();
```

## Coding Exercises
1. ### [Profile Lockup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

My solution:
```javascript
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
 for(var i = contacts.length-1 ; i>=0 ; i--){
    
     if ( contacts[i].firstName === name ){
      if ( prop ==="lastName"  ){return contacts[i][prop] ;}
      else if ( prop ==="number"  ){return contacts[i][prop] ;}
       else if ( prop ==="likes"  ){return contacts[i][prop]; }
       else {
         return "No such property";
       }
    }
  }
 
    return "No such contact";
  
  // Only change code above this line
}

lookUpProfile("Akira", "likes")
```

2. ### [Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

My solution:
```javascript
function forecast(arr) {
  // Only change code below this line

  return arr.slice(2,4);
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

3. ### [Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

My solution:
```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment , 'is', 'fun']; // Change this line
  return sentence;
}

console.log(spreadOut());
```
# Notes for me => 

- Arrays can hold any type of item or mix and match.
- when I push some of the numbers in an array using function push like this format push([]),  it will make a nested array.
- "Mutable" data can be edited (e.g. Arrays, objects). "Immutable" data always stays the same (e.g. strings & other primitives).
- concat() did not change the original Array. It changed the new Array.
- Using immutable data & variables is usually best.
- if I use mutable value in immutable, we'll break the rule of immutable (I can make some edits in ). 
- jects collect multiple values together to describe more complex data.
  Arrays are just a special kind of object.
- Properties can point to functions, too. We call function-properties "methods" on objects
- Functions in js :) => typeof , indexof(""), includes(""), startsWith(""),toLowerCase(), append("").
- Functions that can used in array: sort() , Join(''),pop(), push(), concat([]).
- Console's functions:  warn(""), error(""), log() , clear()
- Math Functions: math.random(), math.pi, math.aps(number)



