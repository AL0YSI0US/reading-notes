# Code 301 Reading Notes

## Class 10

[<== Previous Lesson](class9.md) [Next Lesson ==>](class11.md)

[<== Home](README.md) 🏠

# In memory storage

## Understanding the JavaScript Call Stack

+ The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
+ In Asynchronous JavaScript, we have a **callback function**, an **event loop**, and a **task queue**. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

````javascript
//                   Last In, First Out = L I F O 

// The last function that gets pushed into the stack is the first 
// to be pop out, when the function returns.

function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();

// the arrangement of the functions as a stack begins with the 
// firstFunction() (which is the last function that got into the stack, 
// and is popped out to throw the error), 

// followed by the secondFunction(), 

// and then the thirdFunction() (which is the first function that 
// gets pushed into the stack when the code is executed).
````

#### The key takeaways from the call stack are:

1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

## JavaScript error messages

> Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

Try to manipulate an object with some kind of length and give it an invalid length and `Range Errors` will show up.

**EXAMPLE :**

````javascript
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
````

+ `console.log();` is a great tool for debugging.

## JavaScript errors reference on MDN

+ List of errors : [developer.mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

### Reading

* [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)
* [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

### Additional Resources

* [JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)


[<== Home](README.md) 🏠
