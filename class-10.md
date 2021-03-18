# Code 201 Reading Notes

## Class 10

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-09.md) [Next Lesson ==>](class-11.md)

[<== Home](README.md) 🏠

## Error Handling and Debugging

![debugger](https://www.elprocus.com/wp-content/uploads/Featured-image-2.png)

There are two stages for **Execution Contexts**

Debugging is all about refining the process of deduction

The console narrows down where the error can be found the rest is on you

> *hint: where does the code stop running?....*

## JavaScript Has 7 types of errors...

> . . . . . . . . . . . . . each can give you a line number and error message

1. **RangeError** This is thrown when a number is outside an allowable range of values.
2. **ReferenceError** This error is thrown when a reference made to a variable/item is broken. That is the variable/item doesn’t exist.
3. **ReferenceError** This error is thrown when a reference made to a variable/item is broken. That is the variable/item doesn’t exist.
4. **URIError** This indicates that one of the global URI handling functions was used in a way that is incompatible with its definition. URI (Uniform Resource Indicator) in JS has the functions: decodeURI, decodeURIComponent, etc. *If we call any of them with the wrong parameter we will get a URIError*
5. **EvalError** This is used to identify errors when using the global eval() function.
   According to EcmaSpec 2018 edition: This exception is not currently used within this specification. This object remains for compatibility with previous editions of this specification.
6. **InternalError** This error occurs internally in the JS engine, especially when it has too much data to handle and the stack grows way over its critical limit.
   This occurs when the JS engine is overwhelmed by too many recursions, too many switch cases, etc

7 Types of [Native Errors](https://blog.bitsrc.io/types-of-native-errors-in-javascript-you-must-know-b8238d40e492) in JavaScript You Should Know

## JavaScript Errors

> Throw and Try to Catch

The `try` statement lets you test a block of code for errors.

The `catch` statement lets you handle the error.

The `throw` statement lets you create custom errors.

The `finally` statement lets you execute code, after try and catch, regardless of the result.

> JavaScript catches **adddlert** as an error, and executes the catch code to handle it.

## JavaScript try and catch

The `try` statement allows you to define a block of code to be tested for errors while it is being executed.

The `catch` statement allows you to define a block of code to be executed, if an error occurs in the try block.

The JavaScript statements `try` and `catch` come in pairs:

try {

*Block of code to try*

}

catch(err) {

*Block of code to handle errors*

}

## JavaScript Throws Errors

When an error occurs, JavaScript will normally stop and generate an error message.

The technical term for this is: JavaScript will **throw an exception (throw an error).**

JavaScript will actually create an Error object with two properties: **name** and **message**.

## The throw Statement

The `throw` statement allows you to create a custom error.

Technically you can **throw an exception (throw an error)**.

The exception can be a JavaScript `String`, a `Number`, a `Boolean` or an `Object`.

If you use `throw` together with `try` and `catch`, you can control program flow and generate custom error messages.

## The finally Statement

The `finally` statement lets you execute code, after try and catch, regardless of the result

## The Error Object

JavaScript has a built in error object that provides error information when an error occurs.

The error object provides two useful properties: name and message.

### Error Object Properties

**Property**	| *Description*

**name**	*Sets or returns an error name*

message	Sets or returns an error message (a string)

### Error Name Values

Six different values can be returned by the error name property:

**Error Name**	| *Description*

**EvalError**	*An error has occurred in the eval() function*

**RangeError**	*A number "out of range" has occurred*

**ReferenceError**	*An illegal reference has occurred*

**SyntaxError**	*A syntax error has occurred*

**TypeError**	*A type error has occurred*

**URIError**	*An error in encodeURI() has occurred*

The six different values are described below.

**Eval Error**

An `EvalError` indicates an error in the eval() function.

Newer versions of JavaScript do not throw EvalError. Use SyntaxError instead.

**Range Error**

A `RangeError` is thrown if you use a number that is outside the range of legal values.

**Reference Error**

A `ReferenceError` is thrown if you use (reference) a variable that has not been declared.

**Syntax Error**

A `SyntaxError` is thrown if you try to evaluate code with a syntax error.

**Type Error**

A `TypeError` is thrown if you use a value that is outside the range of expected types.

**URI (Uniform Resource Identifier) Error**

A `URIError` is thrown if you use illegal characters in a URI function

## Non-Standard Error Object Properties

Mozilla and Microsoft defines some non-standard error object properties:

1. fileName (Mozilla)
2. lineNumber (Mozilla)
3. columnNumber (Mozilla)
4. stack (Mozilla)
5. description (Microsoft)
6. number (Microsoft)

**Do not use these properties in public web sites**. *They will not work in all browsers*.

[JavaScript Errors](https://www.w3schools.com/js/js_errors.asp) *w3schools.com*

[Complete Error Reference](https://www.w3schools.com/jsref/jsref_obj_error.asp) *w3schools.com*

## Reading

**From the Duckett JS book:**

- JavaScript book, Ch. 10, “Error Handling & Debugging”

[<== Previous Lesson](class-09.mdpm) [Next Lesson ==>](class-11.md)

[<== Home](README.md) 🏠
