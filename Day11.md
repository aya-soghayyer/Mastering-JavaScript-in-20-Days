# Day11: static typing, scope


## Lesson Summary
in this lesson, I've learned about many topics :
flow and typescript
- [ts vs flow](https://cdn-blog.scalablepath.com/uploads/2022/12/flow-vs-typscript-key-features.png)
- TypeScript and Flow are similar tools that focus on the same problem: JavaScript's lack of static types.
- js is not interpreted language.
- js is excute at compile time and run time.
- declare two variables with the same name and different scopes call shadowing.
- Undefined variable means a variable has been declared but does not have a value.
Undeclared variable means that the variable does not exist in the program at all.
- source reference : calling a stuff or function or variable or element in the globale scope.
- target reference : declare a variable in the globale scope.
- Benefits:
1. Catch type-related mistakes 
2. Communicate type intent
3. Provide IDE feedback

## Coding Examples
```javascript

```

## Coding Challenges :
## STATIC TYPING QUESTIONS:

### QUESTION #1

Given the following `promisesArray`, convert the array into an object using the
`convertToObj` function.

You should apply typescript types to every promise, the input of `convertToObj`,
and the output of `convertToObj`. 

Build interfaces and types as needed.

```javascript

const sayHelloWorld = new Promise(resolve, reject => {
  resolve("Hello world!");
});

const checkBoolean = (boolean) => new Promise(resolve, reject => {
  if (boolean) {
    resolve(boolean);
  } else {
    reject(`Input is false :(`)
  }
})

const returnObj = new Promise(resolve, reject => {
  resolve({
    x: "meow",
    y: 45,
  })
})

const promisesArray = [sayHeloWorld, checkBoolean, returnObj];

const convertToObj = (array) => {
  //write your code here;
  return obj;
}

```

-------------------------------------------------------------------

## SCOPE & HOISTING QUESTIONS:

### QUESTION #1:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();

```
**Choices:**

A) `undefined`, `undefined`, `undefined`   
B) `1`, `undefined`, `ReferenceError`  
C) `1`, `ReferenceError`, `ReferenceError`   
D) `1`, `ReferenceError`

sol: D becuase the variable declearation happen in the other scope and var has an access the variable decleration , but not the same in variable that declared by let and const .
-------------------------------------------------------------------

### QUESTION #2:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();

```

**Choices:**

A) `undefined`, `ReferenceError`   
B) `1`, `undefined`, `ReferenceError`   
C)`undefined`, `undefined`,`ReferenceError`  
D) `1`, `ReferenceError`

sol: A becuase js is cimpile at line by line so when it print a variable (a) the memory know that some declear for a but it still hidden cuz we print the variable out of the scope and before the declaretion, also in variable  (b) and (c). because they decleared by let and const the result will be referenceError for b and compiler will stop in it so there isn't any exist for variable (c).  
-------------------------------------------------------------------

### QUESTION #3:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript

function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();

```

**choices:**

A) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 36, 2, 3 ]`   
B) `[ 36, 100, 45 ]` | `[1, 2, 3 ]` | `[ 36, 100, 45 ]`   
C) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1,100, 45 ]`   
D) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1, 2, 3 ]`

sol: c because var can do redelearation on the variable, but let and const can't do that, also javascript compile line by line so when it finished from one, then put the result and go to other line and do the process of that line then put the result. 
here function testscope3 decleared in a global scope and have a nested scope in the function also it has console.log which will following the global scope, so the code will do the operations in the global function, then when you call the source reference of the function will apear the result 




#  Notes for me => 
- flow and typescript
- [ts vs flow](https://cdn-blog.scalablepath.com/uploads/2022/12/flow-vs-typscript-key-features.png)
- TypeScript and Flow are similar tools that focus on the same problem: JavaScript's lack of static types.
- js is not interpreted language.
- js is excute at compile time and run time.
- declare two variables with the same name and different scopes call shadowing.
- Undefined variable means a variable has been declared but does not have a value.
Undeclared variable means that the variable does not exist in the program at all.
- source reference : calling a stuff or function or variable or element in the globale scope.
- target reference : declare a variable in the globale scope.
- 
