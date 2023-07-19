# Day10: Introduction, Types


## Lesson Summary
in this lesson, I've learned about many topics like primitive type and object what they include also I learned about special values NaN, isNaN, and -0 and how to use it, also when we should put new keyword. 


## Coding Examples
```javascript
var v 
typeof v
//the result:'undefined'

v = '1'
typeof v
//the result:'string'

v = 1
typeof v
//the result:'number'

v = true
typeof v
//the result:'boolean'

v= {}
typeof v
//the result:'object'

v = Symbol()
typeof v
//the result: 'symbol'

v = 43n or bigint(43)
typeof v
//the result: 'bigint'

var yesterday = new Date("july 19, 2023");
console.log(yesterday);
console.log(yesterday.toUTCString());
//the reslutl:
//2023-07-18T21:00:00.000Z
// Tue, 18 Jul 2023 21:00:00 GMT

onsole.log(typeof doesnotExist) ; 

var v = null ; 
console.log(typeof v ); 

v = function(){}
console.log(typeof v)

v = [1,2,3]
console.log(typeof v );
//the resutl;
//undefined
//object
//function
//object

var myAge = Number("0o42")
console.log(myAge);

var myNextAge = Number('39');
console.log(myNextAge);

var myCatsAge = Number('n/a')
console.log(myCatsAge)

console.log(myAge - "my son's age");

console.log(myCatsAge === myCatsAge);

console.log(isNaN(myAge));
console.log(isNaN(myCatsAge))
console.log(isNaN("my son's age "))
//the result:
//34
//39
//NaN
//NaN
//false
//false
//true
//true

var trendRate= -0  ;
console.log(trendRate=== 0)
console.log(trendRate.toString());
console.log(trendRate === 0)
console.log(trendRate < 0 )
console.log(trendRate > 0 )
console.log(Object.is(trendRate, 0))
console.log(Object.is(trendRate, -0))
//the result:
//true
//0
//true
//false
//false
//false
//true

const formatTrend = (trendRate)=>{
    let direction = (trendRate<0 || Object.is(trendRate,-0)? '!': '^')
    return `${direction} ${Math.abs(trendRate)}`
}
console.log(formatTrend(3));
console.log(formatTrend(-3));
console.log(formatTrend(-0));
console.log(formatTrend(0));
//the result:
//^ 3
//! 3
//! 0
//^ 0
```

## Coding Challenges from FreeCodeCamp
## Question 1:

Write a function called `convertStringToNumber` that converts a string to a
number using the unary plus operator. 

If the input is not a string, return an object of the input's value and type.

```javascript
function convertStringToNumber(input) {
function convertStringToNumber(input) {
var v = (input !== String(input))? typeof input : Number(input)+1
return v ; 
}
console.log(convertStringToNumber("3"));
}
```

-------------------------------------------------------------------

## Question 2:

Write a function called `checkNaN` that takes a single argument and returns
`true` if the argument is `NaN` and `false` otherwise. 

```javascript
const checkNaN = (value) => {
  //write your own code here
}
```

-------------------------------------------------------------------

## Question 3: 

Write a function called `isEmptyValue` that checks if a given input is an empty value (undefined,
null, or empty string). 

```javascript
function isEmptyValue(value) {
  //write your own code here
}
```

-------------------------------------------------------------------

## Question 4: 

Write a function called `compareObjects` that takes 2 arguments of type
`"object"` and compares them. If both arguments are equal, return `true`. If
not, return `false`.

If either argument is not of type `"object"`, the function should return an
array of the arguments. 

```javascript
function compareObjects(input1, input2) {
  //write your own code here
}
```

-------------------------------------------------------------------

## Question 5: 

Write a function called `complexCoercion` that takes a single argument and
checks if its type is primitive, and if so returns a coerced value according to
the rules below.

coercion rules: 
- if input is primive and:
  - if input is a number, convert to string and then return a boolean. 
  - if input is a string, return a boolean.
  - if input is `null` or `undefined`, return `false`.

If input is not a primitive type, return the argument.

```javascript
const complexCoercion = (input) => {
  //write your own code here
}
```

```
#  Notes for me => 
- false not an object
- primitive type: undefined, string, number, object, symbol, boolean, null, bigint(large integer).
- objects: object, class, function, array. 
- symbols: obscure
- undefined vs undeclared VS uninitialized(aka TDZ)
- special values: NaN, isNaN, -0.
- Nan with any other operation is always NaN.
- NaN is not equal to itself.
- NaN is an invalid number.
- -0
- toUTCString() => Greenwich Mean Time (GMT)
- use new keyword with this obj : Object()
• Array()
• Function()
• Date()
• RegExp()
• Error()
- 


