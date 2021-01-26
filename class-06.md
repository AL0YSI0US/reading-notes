# Code 201 Reading Notes

## Class 6 

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-05.md) [Next Lesson ==>](class-07.md)

[<== Home](README.md) 

## The DOM, Domain Modeling, and Introduction to Objects

> In JavaScript, objects are king. If you understand objects, you understand JavaScript.

**In JavaScript, almost "everything" is an object.**

+ Booleans can be objects (if defined with the new keyword)
+ Numbers can be objects (if defined with the new keyword)
+ Strings can be objects (if defined with the new keyword)
+ Dates are always objects
+ Maths are always objects
+ Regular expressions are always objects
+ Arrays are always objects
+ Functions are always objects
+ Objects are always objects
+ All JavaScript values, except primitives, are objects.

**JavaScript Primitives**

> A primitive value is a value that has no properties or methods.

> A primitive data type is data that has a primitive value.

**JavaScript defines 5 types of primitive data types:**

+ string
+ number
+ boolean
+ null
+ undefined

> Primitive values are immutable (they are hardcoded and therefore cannot be changed).

if x = 3.14, you can change the value of x. But you cannot change the value of 3.14.

> JavaScript objects are containers for named values, called properties and methods.

**With JavaScript, you can define and create your own objects.**

There are different ways to create new objects:

+ Define and create a single object, using an object literal.
+ Define and create a single object, with the keyword new.
+ Define an object constructor, and then create objects of the constructed type.

[Bojects W3Schools](https://www.w3schools.com/js/js_object_definition.asp)

## Object Literals (pp.100-105) [Duckett JavaScript]

Using an object literal, you both define and create an object in one statement.

An object literal is a list of name:value pairs (like age:50) inside curly braces {}.

The following example creates a new JavaScript object with four properties:

**Example** 

`var` `person` `=` `{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};`

## Using the JavaScript Keyword new

The following example also creates a new JavaScript object with four properties:

**Example**

`var` `person` `=` `new Object();`

`person.firstName` `=` `"John";`

`person.lastName` `=` `"Doe";`

`person.age` `=` `50;`

`person.eyeColor` `=` `"blue";`

## Document Object Model (pp.183-242) [Duckett JavaScript]

## Reading 

**From the Duckett JavaScript book:**

+ Chapter 3: “Object Literals” (pp.100-105)
+ Chapter 5: “Document Object Model” (pp.183-242)

[<== Previous Lesson](class-05.md) [Next Lesson ==>](class-07.md)

[<== Home](README.md) 