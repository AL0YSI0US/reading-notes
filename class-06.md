# Code 201 Reading Notes

## Class 6 

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-05.md) [Next Lesson ==>](class-07.md)

[<== Home](README.md) 

## The DOM, Domain Modeling, and Introduction to Objects

![betterDom](https://lh3.googleusercontent.com/proxy/gLZLhsTgDcP6RtqcuB5BNUUvq0q2tQ7YeXcjuQTFfKuJs_jzt45og3zos6qX0J0iMCdlS7nk2mANN0J_XGoEwk_4Ug-EpPfYGpjA0zhXAVr9SH3islbd8UmL8ySImMbgcnCa2XPWDg)


## Object Literals (pp.100-105) [Duckett JavaScript]

Using an object literal, you both define and create an object in one statement.

An object literal is a list of name:value pairs (like `age:50`) inside curly braces `{}`.

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

if **x = 3.14**, you ***can*** change the value of **x**. 

- But you **cannot** change the value of **3.14**.

> JavaScript objects are containers for named values, called properties and methods.

**With JavaScript, you can define and create your own objects.**

There are different ways to create new objects:

+ Define and create a single object, using an object literal.
+ Define and create a single object, with the keyword new.
+ Define an object constructor, and then create objects of the constructed type.

[Objects W3Schools](https://www.w3schools.com/js/js_object_definition.asp)

## Document Object Model (pp.183-242) [Duckett JavaScript]

> refer to book, it has the best visuals

+ Working with the DOM Tree (pp.188-189)
+ Caching DOM Queries (pp.190-191)
+ Accessing Elements (pp.192-193)
+ Methods that select individual elements (pp.194)
+ Selecting elements using ID attributes (pp.195)
+ Nodelists / DOM queries that return more than one element (pp.196)
+ Selecting an element from a nodelist (pp.198-199)
+ Selecting an element using CLASS name (pp.200)
+ Selecting an element by TAG name (pp.201)
+ Selecting an element using CSS selectors (pp.202-203)

>This topic is huuuuuuuuge oOf.  `<(^.^)>` refer to (pp.239)

[What is the DOM? - Medium Article](https://medium.com/@ReaganCuthbert/what-is-the-document-object-model-dom-87d552e27305)

## Reading 

**From the Duckett JavaScript book:**

+ Chapter 3: “Object Literals” (pp.100-105)
+ Chapter 5: “Document Object Model” (pp.183-242)

[<== Previous Lesson](class-05.md) [Next Lesson ==>](class-07.md)

[<== Home](README.md) 