# Day1 : Introduction , DOM , Values & Data Types , Operators

## Lesson Summary

I've learned in this lesson about many topics I'll mention below:

Dom: document object model, And I know new functions and document objects like document.title, document.body, document.body.children, document.title, document.getElementById("board), document.querySelector("#board"), clear(), document.getElementsByTagName("h1"), etc.., then I learned about values and how to declare them via date type, and there are two types of data type: 1. Primitive type: null, undefined, number, string, symbol, boolean. 2. Object / References type: object, array, function, class, etc. Also, now I know some operators that use to execute the operations on the js elements or variables.

## Coding Examples
```javascript
// tic tac toe project :
document.getElementsByTagName("p")
// the result : HTMLCollection(2) [p#p1.player, p#p2.player, p1: p#p1.player, p2: p#p2.player]

document.getElementsByClassName("square").length
//The result: 9

document.getElementById("p1-symbol").textContent
// the result : 'x'

document.querySelector("h2").textContent
//The result: 'A game you know'

// add (and love) to h2 
document.querySelector("header h2").append(" and love")

//swap the symbols x & o  :
document.getElementById("p2-symbol").textContent= "X"
//the result: 'X'

document.getElementById("p1-symbol").textContent = document.getElementById("p2-symbol").textContent
//the result: 'O'

// put my last name in the player's  name
document.getElementById("p1-name").append(" soghayyer")

//convert Tic Tac Toe to upper case
document.querySelector("h1").textContent.toLocaleUpperCase()
//the result: 'TIC TAC TOE'

//test if this substring is in the title of the page 
document.title.includes("JavaScript")
//the result: false

//Retrieve the first "T" in the page title
document.title[9]
//the result: 'T'

```

## Coding Challenges from FreeCodeCamp
1. #### [Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)
 My Solution:
```javascript
//Challenge 1

let a = 5;
let b = 12;
let c = 4.6;

b *= 3;
a *= 5;
c *= 10;
```


2. #### [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

  My Solution:
```javascript
//Challenge 2

let myStr= "This is the first sentence. ";
myStr += "This is the second sentence."
```

3. #### [Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)


 My Solution:
```javascript

//Challenge 3 :

const lastName = "Lovelace";
const secondToLastLetterOfLastName = lastName[lastName.length-2]; 

```
#  Notes for me => 
- js: interact programming language and used to modify websites with HTML language.
- use js as a compilation target: it means some other language that then gets translated to js to run in the web browser  like typeScript and ClojureScript.
- creator's name  is Brendan Eich.
- js's birth year: 1995.
- HTML for content structure.
- HTML is like a noun, CSS is like an adjective, and js is like a verb and that is a pure and good analogy.
- the console is kind of a live dynamic sort interpreter for js that we can use.
- js is a browser's js console, local txt file in editor e.g: TextEdit, VS code .online playground e.g: CodePen, CodeSandbox.
- dom: document object model.
- The top level element in the HTML page is attribute <html></html>.
- how to find the elements in js: document.title, document.body, document.body.children, document.title, document.getElementById("board),   
 document.querySelector("#board"), clear(),document.getElementsByTagName("h1"), 
 document.querySelectorAll("h1"),document.getElementsByClassName("player"),document.querySelectorAll(".player").
-the difference between undefined and null =>
 undefined it suppose that sth here is like a value but there is nothing cause have a mistake.
 null: it is usually there is nothing.
-Functions in js :) => typeof , indexof(""), includes(""), startsWith(""),toLowerCase(), append("").
- ** it's equivalent with Math.pow(),  for example 3**4 = math.pow(3,4)= 81 .


