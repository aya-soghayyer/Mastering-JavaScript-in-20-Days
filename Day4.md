# Day4 : Events & handlers , Conditionals , Map & filter , Doggos Quiz Game


## Lesson Summary


## Coding Examples
```javascript
//When the "true" button is clicked, the button's text becomes "clicked true"
document.addEventListener("click", () => {document.querySelectorAll(".true")
    console.log("clicked true ")
});

//When the "false" button is clicked, the "explanation" div text becomes "clicked false"
document.addEventListener("click", () => {document.querySelectorAll(".false")
    console.log("clicked false")
});

// display the details of the code
document.addEventListener("click", (event) => {
    console.log(event);
});

//display where you clicked on the window
document.addEventListener("click", (event) => {
    console.log(event.target);
});

//capitalize the text btn when it is clicked 
optionButtons[0].addEventListener("click", (event)=>{optionButtons[0].textContent = optionButtons[0].textContent.toUpperCase();})

//
let h1 = document.getElementsByTagName("h1");
h1 = h1[0]
//the result: <h1>​Quiz.js​</h1>​
h1.addEventListener("mouseover" , ()=>{h1.textContent = "hovering"})
h1.addEventListener("mouseout" , ()=>{h1.textContent = "Quize.js"})

//Write a conditional that logs a message saying whether your first name or last name is longer
let fname = "aya"

let lname = "soghayyer"
if (fname.length > lname.length ){
console.log(fname +" is longer than "+lname) ; }
else{
    console.log(lname +" is longer than "+fname) ;}

//Write a function isEmpty(array) that returns whether a given array is empty or not
const isEmpty=(arr)=>{
if (arr.length===0 ) {console.log("array is empty");}
  else {console.log("array isn't empty");}}

//Is an empty array truthy or falsy? Write a conditional to find out
if ([])console.log("empty array is truthy")
else {console.log("empty array is Faley")}
//the result: empty array is truthy

```

## Coding Exercises

my solution:
```javascript

```
# Notes for me => 
- target will display where you clicked on browse.
- 
