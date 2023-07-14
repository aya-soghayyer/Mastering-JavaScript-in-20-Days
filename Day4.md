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
else {console.log("empty array is Falsy")}
//the result: empty array is truthy

//
if (undefined)console.log("undefined is truthy")
else {console.log("undefined is Falsy")}
//the result: undefined is Falsy

//
if (null)console.log("null is truthy")
else {console.log("null is Falsy")}
//the result:  null is Falsy

//
if ("")console.log("string is truthy")
else {console.log("string is Falsy")}
//the result:  string is Falsy

//first spread 
const skills = ["HTML", "CSS", "JS"];
const newSkills = ["React", "TypeScript", "Node"]
skills.push(...newSkills);
console.log(...skills);
//the result: HTML CSS JS React TypeScript Node

//second spread 
const skills = ["HTML", "CSS", "JS"];
const newSkills = ["React", "TypeScript", "Node"]
skills.push(...newSkills);
console.log(skills);
//the result: (6) ['HTML', 'CSS', 'JS', 'React', 'TypeScript', 'Node']

//From the spices array, use map and filter to:
//create a new array name with only the name of each girl
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const names = spices.map(n =>n.name);
//the result: (5) ['Emma', 'Geri', 'Mel B', 'Mel C', 'Victoria']

//create a new array endInY with just the girls whose nickname ends in "y"
const endInY = spices.filter(s=> s.nickname.endsWith("y"))
//the result:
{name: 'Emma', nickname: 'Baby'}
{name: 'Mel B', nickname: 'Scary'}
{name: 'Mel C', nickname: 'Sporty'}



// quiz.js start
<!DOCTYPE html>
<!-- saved from url=(0063)https://anjana.dev/javascript-first-steps/2-jsquiz-starter.html -->
<html lang="en-US"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    
    <title>Quiz.js</title>
    <style>
        body {
            margin: 1rem auto;
            padding: 3rem;
            font-family: sans-serif;
        }
        header {
            width: 50%;
            margin: 1em auto;
        }
        main {
            min-width: 25rem;
            max-width: 50%;
            margin: 0px auto;
            display:flex; 
            flex-direction: column;
        }
        #statement {
            border: 1px solid black;
            border-radius: 0.5rem;
            box-shadow: 5px 5px 5px gray;
            padding: 1rem;
            font-size: x-large;
            text-align: center;
            margin: 1rem 0px;
            min-height: 2em;
        }
        #explanation {
            padding: 1rem;
            text-align: center;
        }
        #options {
            width: 100%;
            display: flex;
            flex-direction: column;
        }
        button {
            padding: 0.5rem;
            font-size: medium;
            border-radius: 5px;
        }
        .correct {
            background-color: lightgreen;
        }
        .incorrect {
            background-color: lightpink;
        }
    </style>
  </head>
  <body data-new-gr-c-s-check-loaded="14.1114.0" data-gr-ext-installed="">
    <header>
    <h1>Quiz.js</h1>
    <p>Do you know JS? Find out!</p>
    </header>

    <main>
    <div id="statement">
        
    </div>

    <div id="options">
        <button name="true" value="true">true</button>
        <button name="false" value="false">false</button>
    </div>

    <div id="explanation">

    </div>

    </main>

  

  <script type="text/javascript">


    // TODO 1: Declare & assign variables pointing to the corresponding element(s)
    // statement should be the "statement" div
    const statement = document.getElementById("statement");
    // optionButtons should be all the elements within the "options" div
    const options = document.querySelector("#options").children;
    // explanation should be the "explanation" div
    const explanation = document.getElementById("explanation");

    // TODO 2: Declare & assign a variable called fact
    // Its value should be an object with a statement, true/false answer, and explanation 
    const fact = {
            statement : "mutable data can not be edited" , 
            answer : "false"    
             , 
            explanation : "mutable is data can be edited like array "
        }; 

    
    // TODO 3: Set the text of the statement element to the fact's statement
        statement.textContent = fact.statement; 
        

    // TODO 4: Declare disable & enable functions to set or remove the "disabled" attribute from a given button element
    // disable(button) should set the button element's attribute "disabled" to the value ""
        const disable = (button)=> button.setAttribute("disabled", "") 
    
    // enable(button) should remove the attribute "disabled" from the button element
        const enable = (button )=> button.removeAttribute("disabled")

    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
        let isCorrect = (guess)=> guess === fact.answer ; 


    // TODO 6A: Use a for loop to add a click event listener to each of the optionButtons
     // TODO 6B: Within the event handler function, display the fact's explanation by setting the text of the explanation element
     for (let b of options ){
                b.addEventListener("click", (event)=>{
                    explanation.textContent = fact.explanation;
                // for (let d of document.querySelectorAll("div")){
                // console.log(`<h1>${fact.explanation.textContent} </h1>`);
                //         b.classList.toggle("explanation");} 
                // });
            
           
                
            // TODO 7: Within the event handler function, 
            // Use a for loop to disable all the option buttons
            for (let b2 of options ){
            //     document.addEventListener("click", (event)=>{
                            disable(b2);
                            console.log(b2.value)
                            // console.log("tesst");
                            // if (b.getElementsByClassName('true'))
                            // console.log(options[0].setAttribute("style", "background-color:green;"));
                            // else{
                            //     console.log(options[0].setAttribute("style", "background-color:red;"));
                            // }
                            // consle.log(options);
                            // if (b.getElementsByClassName("true")){
                            //     b.getElementsByClassName("true").style.backgroundColor = "green";
                            // }
                        
                }

            // TODO 8: Within the event handler function,
            // Get the guessed value from the clicked button
            // Use a conditional to compare the guess to the fact's answer
            // and add the "correct"/"incorrect" class as appropriate
           
            if (isCorrect(b.value)){
                b.classList.add("correct");
                console.log("should green ")
                console.log()
            }
            else {
                console.log("shoudl red")
                console.log(b.value)
                b.classList.add("incorrect");
            }
           });}

      

  </script>

</body><grammarly-desktop-integration data-grammarly-shadow-root="true"><template shadowrootmode="open"><style>
  div.grammarly-desktop-integration {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select:none;
    user-select:none;
  }

  div.grammarly-desktop-integration:before {
    content: attr(data-content);
  }
</style><div aria-label="grammarly-integration" role="group" tabindex="-1" class="grammarly-desktop-integration" data-content="{&quot;mode&quot;:&quot;full&quot;,&quot;isActive&quot;:true,&quot;isUserDisabled&quot;:false}"></div></template></grammarly-desktop-integration></html>




```

## Coding Exercises

my solution:
```javascript

```
# Notes for me => 
- target will display where you clicked on browse.
- functions : endsWith(""), startsWith(""), includes("")
