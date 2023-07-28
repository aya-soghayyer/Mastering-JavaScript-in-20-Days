# Day7: Closures


## Lesson Summary
I've learned :
- create a brand new via execution context.
- scope rule: what's called lexical or static scoping t.
- backpack 
- closure: is a function having access to the parent scope, even after the parent function has closed.
- Helper functions are JavaScript functions that you can call from your template.
- Memoization is a top-down, depth-first, optimization technique of storing previously executed computations. Whenever the program needs the result of these computations, the program will not have to execute that computation again. Instead, it will reuse the result of the previously executed computation. This way the program will not have to repeat expensive computations. An expensive function is a function that takes some time to execute.
- Execution context is an abstract concept used by the ECMAScript specification to track the runtime evaluation of code. 
  

## Coding Examples
```javascript

```

## Coding Challenges from FreeCodeCamp
# Learning sprint (1), week (2), day (2) deliverables

## Question 1:

Write a closure named createCounter that takes an initial value start and returns a function. 
The returned function, when invoked, should increment the counter by 1 and return the updated value.
```javascript
const createCounter =() => {
  let start = 0 ;
  function counterincreament(){
    start++ ; 
    return start; 
  }
  return counterincreament;
}
const count = createCounter();
console.log(count());
console.log(count());
console.log(count());
console.log(count());
```
-------------------------------------------------------------------
## Question 2:

Write a closure named calculateAverage that takes an array of numbers, nums, and returns a function. 
The returned function, when invoked, should calculate and return the average of the numbers in the array.
```javascript
const calculateAverage = (nums )=> {
  let sum = 0 ; 
    let avg ;
  function Avg(nums){
     sum  =  nums.reduce((e1,e2)=>{
      console.log (e1,e2)
      return e1+e2;
    })
    // console.log('the sum '+ sum)
    avg = sum / nums.length ; 
    return avg ;

  }
  // console.log('the average ' + avg)
  return Avg;
 }


 const arr = [1,2,3,4,5,]
 const averageCalculator = calculateAverage(arr);
 console.log('the result is : '+averageCalculator(arr))
```
-------------------------------------------------------------------
## Question 3: 

Write a closure named powerOf that takes a base number base and returns a function. 
The returned function, when invoked with an exponent exp, should calculate and return the result of base raised to the power of exp.
```javascript
const powerOf  = (num)=> {
    let exp = 4 ; 
    let expo ;
    function pow(num, exp){
      expo = num *num *num *num ;
      return expo ; 

    }
    return pow;  


}
const powfun = powerOf(2)
console.log(powfun(2));
```
-------------------------------------------------------------------
## Question 4: 

Write a closure named compose that takes multiple functions as arguments and returns a new function. 
The returned function should apply the provided functions in reverse order, passing the result of each function as an argument to the next function.

```javascript
const one = ()=> {
  return 1 ; 
}
const two = ()=> {
  return 2 ; 
}
const three = ()=> {
  return 3 ; 
}
const compose = (fun1, fun2, fun3)=>{
    
  function rev(fun3){
    return `${three()} ${two()} ${one()}` 
  }
  return rev(fun3);
}
const res = compose(one , two, three );
console.log(res);
```
#  Notes for me => 
