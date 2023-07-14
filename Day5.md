# Day5 : Data Fetching & Promises , Destructuring Data , Async , Modules


## Lesson Summary


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

```

## Coding Exercises

my solution:
```javascript

```
# Notes for me => 
- Promises can be in 3 possible states:

pending: still waiting for the value, hang tight
fulfilled (aka "resolved"): finally got the value, all done
rejected: sorry couldn't get the value, all done
It takes time for Promises to resolve, so they are "asynchronous"

- [destructuring](https://raw.githubusercontent.com/SaraVieira/open-source-stickers/master/stickers/deconstructing-unicorn/unicorn.png)
