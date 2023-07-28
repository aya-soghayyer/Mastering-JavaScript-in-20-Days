# Day5 : Data Fetching & Promises , Destructuring Data , Async , Modules


## Lesson Summary
I've learned how to do data fetching also promises, async functions and the keyword await and how to use them, then I learned how to use destructuring in js also modules type that we put it in <script> also via modules we can use await out of the function async furthermore import and export how to use them, in the last I learned about debugging and Error handling with try-catch.

## Coding Examples
```javascript
//on the console 
let response = await fetch("https://dog.ceo/api/breed/hound/list");
response
//the resutl: Response {type: 'cors', url: 'https://dog.ceo/api/breed/hound/list', redirected: false, status: 200, ok: true, …}

//with json method will apeare the data  
let body = await response.json();
body
message: Array(7), status: 'success'}message: (7) ['afghan', 'basset', 'blood', 'english', 'ibizan', 'plott', 'walker']status: "success"[[Prototype]]: Objectconstructor: ƒ Object()hasOwnProperty: ƒ hasOwnProperty()isPrototypeOf: ƒ isPrototypeOf()propertyIsEnumerable: ƒ propertyIsEnumerable()toLocaleString: ƒ toLocaleString()toString: ƒ toString()valueOf: ƒ valueOf()__defineGetter__: ƒ __defineGetter__()__defineSetter__: ƒ __defineSetter__()__lookupGetter__: ƒ __lookupGetter__()__lookupSetter__: ƒ __lookupSetter__()__proto__: (...)get __proto__: ƒ __proto__()set __proto__: ƒ __proto__()

//then() method
fetch("https://dog.ceo/api/breed/hound/list")
//the result: Promise {<pending>}[[Prototype]]: Promise[[PromiseState]]: "fulfilled"[[PromiseResult]]: Response
fetch("https://dog.ceo/api/breed/hound/list").then((value)=> console.log(value))
//the result1: Promise {<pending>}[[Prototype]]: Promise[[PromiseState]]: "fulfilled"[[PromiseResult]]: undefined
//the result2: VM397:1 Response {type: 'cors', url: 'https://dog.ceo/api/breed/hound/list', redirected: false, status: 200, ok: true, …}

//We can use ... to collect remaining values
let[one, ...others]= [1,2,4,5,6,]
one
//the result: 1
others
//the result: (4) [2, 4, 5, 6]

//We can use commas to "skip" values
let [one, two ,,, others ]= [1,2,3,4,5,6,6,6,7,7,8,8,]
one
//the result: 1
two
//the result: 2
others
//the result: 5


//project doggo fetch
<!DOCTYPE html>
<!-- saved from url=(0067)https://anjana.dev/javascript-first-steps/3-doggofetch-starter.html -->
<html lang="en-US">

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">

    <title>Doggo Fetch</title>
    <style>
        body {
            margin: 1rem auto;
            padding: 3rem;
            font-family: sans-serif;
        }

        header {
            width: 70%;
            margin: 1em auto;
        }

        main {
            max-width: 70%;
            margin: 0px auto;
            display: flex;
            flex-direction: column;
        }

        img {
            max-width: 100%;
        }

        #image-frame {
            font-size: x-large;
            text-align: center;
            margin: 1rem auto;
        }

        #explanation,
        #score {
            padding: 1rem;
            text-align: center;
        }

        #options {
            max-width: 100%;
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

        .hidden {
            display: none;
        }
    </style>
</head>

<body data-new-gr-c-s-check-loaded="14.1115.0" data-gr-ext-installed="">
    <header>
        <h1>Guess the Doggo</h1>
        <p>What breed is the dog in this image?</p>

    </header>

    <main>
        <div id="image-frame">
        </div>
        <div id="options">
        </div>

    </main>




    <script type="module">

        const RANDOM_IMG_ENDPOINT = "https://dog.ceo/api/breeds/image/random";

        const BREEDS = ["affenpinscher", "african", "airedale", "akita", "appenzeller", "shepherd australian", "basenji", "beagle", "bluetick", "borzoi", "bouvier", "boxer", "brabancon", "briard", "norwegian buhund", "boston bulldog", "english bulldog", "french bulldog", "staffordshire bullterrier", "australian cattledog", "chihuahua", "chow", "clumber", "cockapoo", "border collie", "coonhound", "cardigan corgi", "cotondetulear", "dachshund", "dalmatian", "great dane", "scottish deerhound", "dhole", "dingo", "doberman", "norwegian elkhound", "entlebucher", "eskimo", "lapphund finnish", "bichon frise", "germanshepherd", "italian greyhound", "groenendael", "havanese", "afghan hound", "basset hound", "blood hound", "english hound", "ibizan hound", "plott hound", "walker hound", "husky", "keeshond", "kelpie", "komondor", "kuvasz", "labradoodle", "labrador", "leonberg", "lhasa", "malamute", "malinois", "maltese", "bull mastiff", "english mastiff", "tibetan mastiff", "mexicanhairless", "mix", "bernese mountain", "swiss mountain", "newfoundland", "otterhound", "caucasian ovcharka", "papillon", "pekinese", "pembroke", "miniature pinscher", "pitbull", "german pointer", "germanlonghair pointer", "pomeranian", "medium poodle", "miniature poodle", "standard poodle", "toy poodle", "pug", "puggle", "pyrenees", "redbone", "chesapeake retriever", "curly retriever", "flatcoated retriever", "golden retriever", "rhodesian ridgeback", "rottweiler", "saluki", "samoyed", "schipperke", "giant schnauzer", "miniature schnauzer", "english setter", "gordon setter", "irish setter", "sharpei", "english sheepdog", "shetland sheepdog", "shiba", "shihtzu", "blenheim spaniel", "brittany spaniel", "cocker spaniel", "irish spaniel", "japanese spaniel", "sussex spaniel", "welsh spaniel", "english springer", "stbernard", "american terrier", "australian terrier", "bedlington terrier", "border terrier", "cairn terrier", "dandie terrier", "fox terrier", "irish terrier", "kerryblue terrier", "lakeland terrier", "norfolk terrier", "norwich terrier", "patterdale terrier", "russell terrier", "scottish terrier", "sealyham terrier", "silky terrier", "tibetan terrier", "toy terrier", "welsh terrier", "westhighland terrier", "wheaten terrier", "yorkshire terrier", "tervuren", "vizsla", "spanish waterdog", "weimaraner", "whippet", "irish wolfhound"];


        // Utility function to get a randomly selected item from an array
        function getRandomElement(array) {

            const i = Math.floor(Math.random() * array.length);
            return array[i];
        }

        // Utility function to shuffle the order of items in an array in-place
        function shuffleArray(array) {
            return array.sort((a, b) => Math.random() - 0.5);
        }


        // TODO 1
        // Given an array of possible answers, a correct answer value, and a number of choices to get,
        // return a list of that many choices, including the correct answer and others from the array
        function getMultipleChoices(n, correctAnswer, array) {
            // Use a while loop and the getRandomElement() function
            const choices = [];
            choices.push(correctAnswer)
            while (choices.length < n) {
                let candidates = getRandomElement(array)
                if (!choices.includes(candidates)) {
                    choices.push(candidates);
                }
            }
            return shuffleArray(choices);
            // Make sure there are no duplicates in the array


        }


        // TODO 2
        // Given a URL such as "https://images.dog.ceo/breeds/poodle-standard/n02113799_2280.jpg"
        //https://images.dog.ceo/breeds/akita/n02113799_2280.jpg
        // return the breed name string as formatted in the breed list, e.g. "standard poodle"
        function getBreedFromURL(url) {

            let unsplitBreed = url.split('/')[4];
            //    let joinsplitBreed = unsplitBreed.split('-').reverse().join(' ');
            let [breed, subbreed] = unsplitBreed.split('-');
            let newBreed = [subbreed, breed]

            return newBreed.join('').trim(' ');

            // The string method .split(char) may come in handy
            // Try to use destructuring as much as you can  
        }



        // TODO 3
        // Given a URL, fetch the resource at that URL, 
        // then parse the response as a JSON object,
        // finally return the "message" property of its body
        async function fetchMessage(url) {
                const response = await fetch(url) ; 
                const body = await response.json() ; 
                const {message}= body ; 
                return message; 
        }


        // Function to add the multiple-choice buttons to the page
        function renderButtons(choicesArray, correctAnswer) {

            // Event handler function to compare the clicked button's value to correctAnswer
            // and add "correct"/"incorrect" classes to the buttons as appropriate
            function buttonHandler(e) {
                if (e.target.value === correctAnswer) {
                    e.target.classList.add("correct");
                } else {
                    e.target.classList.add("incorrect");
                    document.querySelector(`button[value="${correctAnswer}"]`).classList.add("correct");
                }
            }

            const options = document.getElementById("options"); // Container for the multiple-choice buttons

            // TODO 4
            // For each of the choices in choicesArray,
            // Create a button element whose name, value, and textContent properties are the value of that choice,
            // attach a "click" event listener with the buttonHandler function,
            // and append the button as a child of the options element
                for(let choice of choicesArray){
                    let btn = document.createElement("button");
                    btn.textContent = choice;
                    btn.value = choice ; 
                    btn.name= choice ; 
                    btn.addEventListener('click', buttonHandler)
                    options.appendChild(btn)
                }



                    }


        // Function to add the quiz content to the page
        function renderQuiz(imgUrl, correctAnswer, choices) {
            const image = document.createElement("img");
            image.setAttribute("src", imgUrl);
            const frame = document.getElementById("image-frame");

            image.addEventListener("load", () => {
                // Wait until the image has finished loading before trying to add elements to the page
                frame.replaceChildren(image);
                renderButtons(choices, correctAnswer);
            })

        }

        // Function to load the data needed to display the quiz
        async function loadQuizData() {
            document.getElementById("image-frame").textContent = "Fetching doggo...";
            const doggoImgUrl = await fetchMessage(RANDOM_IMG_ENDPOINT);
            const correctBreed = getBreedFromURL(doggoImgUrl);
            const breedChoices = getMultipleChoices(3, correctBreed, BREEDS);

            return [doggoImgUrl, correctBreed, breedChoices];
        }

    // TODO 5
    // Asynchronously call the loadQuizData() function,
    // Then call renderQuiz() with the returned imageUrl, correctAnswer, and choices 
    const [imgurl, correctAnswer , choicess] = await loadQuizData();
    renderQuiz(imgurl , correctAnswer , choices)


    </script>

</body><grammarly-desktop-integration data-grammarly-shadow-root="true"><template shadowrootmode="open">
        <style>
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
                -ms-user-select: none;
                user-select: none;
            }

            div.grammarly-desktop-integration:before {
                content: attr(data-content);
            }
        </style>
        <div aria-label="grammarly-integration" role="group" tabindex="-1" class="grammarly-desktop-integration"
            data-content="{&quot;mode&quot;:&quot;full&quot;,&quot;isActive&quot;:true,&quot;isUserDisabled&quot;:false}">
        </div>
    </template></grammarly-desktop-integration>

</html>
```

## Coding Exercises
1. [Task requirements](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week1-day5-task/task.md)
   
my solution:

```javascript
<!DOCTYPE html>
<html>
<head>
  <title>Alive Character List</title>
  <link rel="stylesheet" href="./styles.css">
</head>
<body>
  <h1>Alive Character List</h1>
  <ul id="characterList"></ul>

  <script src="./dy5.js"></script>
</body>
</html>
const characterList = document.getElementById('characterList');

async function fetchCharacters() {
  try {
    const response = await fetch('https://rickandmortyapi.com/api/character?status=alive');
    const data = await response.json();
    const characters = data.results.slice(0, 50);

    characters.forEach((character) => {
      const li = document.createElement('li');
      const img = document.createElement('img');
      const name = document.createElement('h2');
      const location = document.createElement('p');
      const species = document.createElement('p');
      const gender = document.createElement('p');

      img.src = character.image;
      name.textContent = character.name;
      location.textContent = `Location: ${character.location.name}`;
      species.textContent = `Species: ${character.species}`;
      gender.textContent = `Gender: ${character.gender}`;

      li.appendChild(img);
      li.appendChild(name);
      li.appendChild(location);
      li.appendChild(species);
      li.appendChild(gender);

      characterList.appendChild(li);
    });
  } catch (error) {
    console.error(error);
    characterList.innerHTML = '<li>Error fetching characters</li>';
  }
}

fetchCharacters();


```
# Notes for me => 
- Promises can be in 3 possible states:

pending: still waiting for the value, hang tight
fulfilled (aka "resolved"): finally got the value, all done
rejected: sorry couldn't get the value, all done
It takes time for Promises to resolve, so they are "asynchronous"
- [destructuring img](https://raw.githubusercontent.com/SaraVieira/open-source-stickers/master/stickers/deconstructing-unicorn/unicorn.png)
- Destructuring is a fancy way of declaring multiple variables at once
- We can use commas to "skip" values
- putting the keyword async in front of the function, tells js that this is gonna be a function that's carrying out some potentially long-running asynchronous operation
- functions: parseInt, parseFloat, split(), trim()
- [modules img](https://media0.giphy.com/media/l0JMrPWRQkTeg3jjO/giphy.gif?cid=ecf05e47pagiiw3sbae054ux0xw1q1i81rt4youv25pzuit2&rid=giphy.gif&ct=g)
  Modules let us split big codebases across multiple files
- export lets us expose variables from our module's scope to the outside world
- import lets us use an exposed variable from another module
- dom function: createelement("")
- function in promise: then(),
