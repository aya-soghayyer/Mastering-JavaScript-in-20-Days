# Day9: Classes & Prototypes, Wrapping up


## Lesson Summary
in this lesson, I've learned the following:
- object.create(null/ function)
- prototype
- the argument that we put in the object.create it is always a proto.
- this: While this is a valid way to access the object's property
-  the implicit parameter set in the execution context allows the function to work with individual objects despite being shared.
-  to use this in nested functions we put .call() with nested function.
-  new keyword When using a new keyword it allows to use .prototype.
-  function.prototype
-  Constructors are functions that create new objects.
- instance of:  allows you to compare an object to a constructor, returning true or false based on whether or not that object was created with the constructor
- hasOwnProperty(prop): for objects .
- there are  
- there are  two kinds of properties: own properties and prototype properties. Own properties are defined directly on the object instance itself. And prototype properties are defined on the prototype.,
-  IIFE : Immediately Invoked Function Expression

## Coding Examples
```javascript
function Bird(name) {
  this.name = name;  //own property
}

Bird.prototype.numLegs = 2; // prototype property

let duck = new Bird("Donald");


// code
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };

function Dog() { }

// Only change code below this line
Dog.prototype = Object.create(Animal.prototype); 
Dog.prototype.constructor = Dog; 
Dog.prototype.eat= function (){
conosle.log('nom nom nom')
}
Dog.prototype.bark = function (){
  console.log('Woof!');
}


// Only change code above this line

let beagle = new Dog();
beagle.eat();
beagle.bark();


// IIFE :
(function () {
  console.log("Chirp, chirp!");
})();
```
## freeCodeCamp profile: 
#### [profile](https://www.freecodecamp.org/aya22)


#  Notes for me => 

