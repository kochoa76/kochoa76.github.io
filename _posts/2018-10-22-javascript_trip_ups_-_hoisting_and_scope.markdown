---
layout: post
title:      "Javascript Trip Ups - Hoisting and Scope"
date:       2018-10-22 15:11:13 -0400
permalink:  javascript_trip_ups_-_hoisting_and_scope
---


Javascript has been awesome. I'm enjoying learning more languages specific to front-end, and as I get deeper into learning React I'm getting more and more excited to see where Javascript takes me. 

There were a couple key concepts  I wanted to go back and review specific to vanilla Javascript prior to moving on, these are hoisting and scope. 

At first I thought I could avoid all hoisting and scope issues by not using var and only utilizing const and let for variables but now I'm seeing how important it is to understand these key concepts as I dive deeper into JS. 


**Scope **

At a high level Scope is where something is available. In Javascript, where your code goes, *matters*. 

Global scope means you can access that function or variable anywhere in your code, for example: 

```
 function myFunc () {
		return 42;
	}

	const myVar = myFunc() * 2;

	 myVar // => Will return 84 (42 * 2) 
```
		 
`myFunc()` is declared in the global execution context and thus, is in the global scope and can be accessed within the `myVar` variable. 

**Block Scope** - also creates it's own scope --but here is the tricky part, Javascript treats var differently than `const` and `let`. So let's dive into these variables some more: 

	`		if (true) {
				 var myVar = 42;
			}

			myVar;
			// => 42 `
				
variables declared with var are accessabile outside its scope. 
				
				`if (true) {
        const myVar = 42;
 
        let myOtherVar = 9001;
       }
 
       myVar;
       // Uncaught ReferenceError: myVar is not defined
 
       myOtherVar;
       // Uncaught ReferenceError: myOtherVar is not defined `
			
As you can see from these examples a variable declared with `var` is accessible while those declared with `const` and `let` are not. This is why I thought I could avoid scoping issues by solely utilizing `const` and `let`. 

** Scope Chain**

We've discussed global scope so now lets discuss functions defined with their own scope and how they relate to outer scope ( or functions declared outside of an inner function). 

  ```
 const globalVar = 1;     //=> this is in global scope 
 
   function firstFunc () {   //=> firstFunc() has access to firstVar and globalVar
       const firstVar = 2;
 
      function secondFunc () {       //=> secondFunc() has access to firstVar and secondVar and globalVar
          const secondVar = 3;
 
          return secondVar + firstVar + globalVar;
      }
 
    const resultFromSecondFunc = secondFunc();
 
    return resultFromSecondFunc;
 }
 
firstFunc();
// => 6
```

I helps me to think of Scope Chain as a friendly ally -- it *wants* to find the answer for you. In the line below Scope Chain sees return `secondVar` which is easily accessible within the `secondFunc()` function and then it sees `firstVar`, since Scope Chain can't find the variable declared with `secondFunc()` it will search upwards into the scope chain or outerscope. Immediately, it sees `firstFunc()` with a `firstVar` variable declaration and the Chain is satisfied. Once it encounters `globalVar` it repeats the same process. 

```
 function secondFunc () {     
          const secondVar = 3;
 
          return secondVar + firstVar + globalVar;
	}
```
	
*Note: Scope Chain cannot seek for your answers down the scope Chain, only upwards *


**Javascript Engine phases **

 The Javascript engine encounters two phases when reading code:  

* Compilation Phase - *Think Overview and Scope *

This phase doesn't take action but rather stores memory and scope 
The engine will review your code and store all of your variables/functions into memory (but not their values, just the variable or function names) and their scope or execution context and any outerscope that's relevant to the function or variable. 

* Execution Phase - *Think Action*

This phase actually runs our code, assigning values to variables and invoking functions.
It assigns the value to your variable or function and calls any functions. 

```
   const myVar = 42;
 
   function myFunc () {
     const myVar = 9001;
 
   return myVar;
  }
 
myFunc(); 

//=> 9001 
```

During the compilation phase, the engine recognizes `myFunc()`'s innerscope with a declared `myVar`
During the execution phase, the engine matches `myVar` to 9001 and returns 9001. It does not see `myVar=42 ` because it did not need to go up the Scope Chain it found the answer inside the `myFunc()` function. 

**Lexical Scope**

   ```
const myVar = 'Foo';
 
   function first () {
     console.log('Inside first()');
 
     console.log('myVar is currently equal to:', myVar);
   }
 
   function second () {
     const myVar = 'Bar';
 
     first();
   }
```
	 
This example is tricky but it reviews what we've recently learned. If you call `second()` the engine will return:
	 
```
 Inside first()
 myVar is currently equal to: Foo
```
	 
 This is because the function `first()` does not see `const myVar= "Bar"` in `second()` this is because the global scope is the parent scope of the function `first()` not the function `second()`. *Remember the Scope Chain goes up.* Additionally, the JS doesn't care *where* the function is invoked but instead where it's *declared*. So when `first()` is called, and `console.log('myVar is currently equal to: myVar)` is run it goes up the scope chain to find myVar and prints `'Foo'`. 

 Lexical scope has to do with where your code is declared. 
	 
	 
**Hoisting**

Definition on MDN:   

> suggests that variable and function declarations are physically moved to the top of your code, but this is not in fact what happens. Instead, the variable and function declarations are put into memory during the compile phase, but stay exactly where you typed them in your code.

Hoisting has to do with the two phases of the JS engine: compilation and execution. 

To help clear up hoisting I've utilized a series of quiz questions from [](http://www.thamizhchelvan.com/javascript/javascript-variable-hoisting-quiz/.   )Let's see a series of examples to clear up this topic: 


Example 1 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/js-hoisting-quiz.png)
 
Compilation Phase: recognizing scope and storing var a to memory *but* at this moment in time `var a= undefined` (because it has not yet been defined, that step happens in the execution phase) 

Execution Phase: the engine reads `console.log(a)` and calls it but at that point in time var a has not been defined 

As a result `test()` results in undefined 

Example 2 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/js-hoisting-quiz-technology.png)

Compilation Phase: recognizes var technology is in the global scope, and assigns the variable to memory 

Execution Phase: This question is specifically asking what would the variable technology print when called. Since this variable was initially declared in the global scope, the variable will return Java. You can test this by typing this problem into your console and then typing window which will show you a series of methods available to window (if you scroll to 'T' you will see technology--pretty cool!)

Example 3 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/javascript-hoisting-quiz.png)

Compilation phase: recognizes scope and sets to memory `var x`, `var y` and `var fruit` -- all undefined 

Execution phase: the engine reads `console.log(fruit)` and the engine prints out undefined, as fruit has not yet been assigned.

Example 4 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/javascript-hoisting-quiz-function.png)

Compilation Phase: recognizes scope of `var sayHai` and sets the variable to memory (in this moment `var sayHai` is *not* a function but a variable  

Execution Phase: calls `sayHai()` but since the variable has not yet been assigned a value (or in this case, function), `sayHai()` will return a reference error `'sayHai is not a function'`. 

Another piece to note on this problem, if you try this out in console and call the variable `sayHai`, the response is undefined. The reason for this is once the function calls `sayHai()` and the response is `"sayHai() is not a function"`, the code stops running and sayHai will never be defined. This may seem obvious but can be helpful in understanding how the engine works. 

Example 5 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/javascript-hoisting-quiz-es6.png)

*Note: this problem is similar to our previous problem reviewed in scope above* 

`const` and `let` are treated differently than var when it comes to hoisting. Variables declared with `const` and `let` do technically get 'hoisted', but the JavaScript engine doesn't allow them to be referenced before they've been initialized.

Compilation Phase: `let number` is not recognized in this phase

Execution Phase: when `console.log(number)` is called the response is: Uncaught ReferenceError: number is not defined

Example 6 

![](http://www.thamizhchelvan.com/wp-content/uploads/2017/12/javascript-quiz-variable-hoisting.png)

Compilation Phase: recognizes scope and sets to memory `var x`,  it does not recognize y or tree since they do not have `var`. If a variable is not given `var`, `const` or `let` it is only recognized upon assignment, or the execution phase. 

Execution Phase: `x = 15` and `y = 17` and when the engine reads `console.log(tree)` it doesn't recognize this variable as it hasn't yet been declared or assigned, so it will print out `Uncaught ReferenceError: tree is not defined`. However if you type `y` into your console, it will return `17`, as this variable has been recognized and assigned at the time `console.log(tree)` is run. 

As you can see a lot of these problems can be avoided by using `const` or `let` rather than var especially when it comes to hoisting. However, I learned it is helpful to understand how these concepts work as it will be helpful in reading legacy code utilizing var in previous JS versions. 


**
