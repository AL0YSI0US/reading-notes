JavaScript / Conditionals / Operators / Data Types / Variable

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) 🏠 [Forward ==>](programming_with_jacascript.md)

# Dynamic Web Pages with JavaScript

:mortar_board: [JAVASCRIPT MASTER CHEAT](https://overapi.com/javascript)

Every written "instruction" is called a statement. JavaScript **statements** are separated by **semicolons**.

## Comments in JavaScript.

**Statements**: are the instructions within our program that get "executed" when the program runs.
But! Not all JavaScript statements are "executed".
Any code after a double slash //, or between /* and */, is treated as a comment, and will be ignored, and not executed.

**To write a Single line comment we use double slashes ( // ). Like this:**

// This is a single line comment

alert("This is an alert box!");

**To create a multi-line comment, we write it between `/* and */` Like this:**

`/*`

The code below will change

the heading with `id = "myH"`

and the paragraph with `id = "myP"`

in my web page:

`*/`

document.getElementById("myH").innerHTML = "My First Page";

document.getElementById("myP").innerHTML = "My first paragraph.";

## This example uses a comment block to prevent execution of multiple lines:

`/*`

document.getElementById("myH").innerHTML = "My First Page";

document.getElementById("myP").innerHTML = "My first paragraph.";

`*/`

## In JavaScript we have the following conditional statements:

Use **if** to specify a block of code to be executed, if a specified condition is true

Use **else** to specify a block of code to be executed, if the same condition is false

Use **else if** to specify a new condition to test, if the first condition is false

Use **switch to** specify many alternative blocks of code to be executed

[W3Schools Condional Statements](https://www.w3schools.com/js/js_if_else.asp)

## The if Statement ( True )

Use the if statement to specify a block of JavaScript code to be executed if a condition is **true.**

**Syntax**

if (condition) {

//  *block of code to be executed if the condition is true*

}

## The else Statement ( False )

Use the else statement to specify a block of code to be executed if the condition is **false.**

**Syntax**

if (condition) {

//  *block of code to be executed if the condition is true*

} else {

//  *block of code to be executed if the condition is false*

}

## The else if Statement ( 1st condition is false )

Use the else if statement to specify a new condition if the first condition is false.

**Syntax**

if (condition1) {

//  *block of code to be executed if condition1 is true*

} else if (condition2) {

//  *block of code to be executed if the condition1 is false and condition2 is true*

} else {

//  *block of code to be executed if the condition1 is false and condition2 is false*

}

## The JavaScript Switch Statement

Use the switch statement to select one of many code blocks to be executed.

**Syntax**

switch(expression) {

case x:

// *code block*

break;
case y:

// *code block*

break;
default:

// *code block*
}

**This is how it works:**

+ The switch expression is evaluated once.
+ The value of the expression is compared with the values of each case.
+ If there is a match, the associated block of code is executed.
+ If there is no match, the default code block is executed.

## OPERATORS

[W3Schools Operators](https://www.w3schools.com/java/java_operators.asp)

Java divides the **operators** into the following groups:

+ Arithmetic operators
+ Assignment operators
+ Comparison operators
+ Logical operators
+ Bitwise operators
+ ***Operators are used to perform operations on variables and values.***

## Java Arithmetic Operators

Arithmetic operators are used to perform common mathematical operations.

## Java Assignment Operators

Assignment operators are used to assign values to variables.

In the example below, we use the **assignment** operator (=) to assign the value **10** to a variable called **x**:

**Example**

int x = 10;

The **addition assignment** operator (+=) adds a value to a variable:

**Example**

int x = 10;

x += 5;

## Java Comparison Operators

Comparison operators are used to compare two values:

## Java Logical Operators

Logical operators are used to determine the logic between variables or values:

## Java Bitwise Operators

Bitwise operators are used to perform binary logic with the bits of an integer or long integer.

## JavaScript Variables

[W3Schools Variables](https://www.w3schools.com/js/js_variables.asp)

JavaScript variables are containers for storing data values.

In this example, x, y, and z, are variables, declared with the var keyword:

Example

**var** x = **5**;

**var** y = **6**;

**var** z = x + y;

From the example above, you can expect:

x stores the value 5

y stores the value 6

z stores the value 11

## GEEK TALK

**Declare a varialble called x, assign the value
42 to it and output it to the colsole:**

`x = ___;`

`______.log(_____);`

**EXAMPLE**

`x = 42;`

`console.log(x);`

## DATA TYPES

[W3Schools Data Types](https://www.w3schools.com/java/java_data_types.asp)

> A variable in Java must be a specified data type.

**Data types are divided into two groups:**

+ Primitive data types - includes byte, short, int, long, float, double, boolean and char
+ Non-primitive data types - such as String, Arrays and Classes

## Primitive Data Types

A primitive data type specifies the size and type of variable values, and it has no additional methods.

There are ***eight primitive data types*** in Java:


| **Data Type** | **Size** | **Description** |
| :-: | :-: | - |
| byte | 1 byte | Stores whole numbers from -128 to 127 |
| short | 2 bytes | Stores whole numbers from -32,768 to 32,767 |
| int | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
| long | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| float | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits |
| double | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits |
| boolean | 1 bit | Stores true or false values |
| char | 2 bytes | Stores a single character/letter or ASCII values |

## Non-Primitive Data Types

Non-primitive data types are called reference types because they refer to objects.

**The main difference between primitive and non-primitive data types are:**

+ Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).
+ Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
+ A primitive type has always a value, while non-primitive types can be null.
+ A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
+ The size of a primitive type depends on the data type, while non-primitive types have all the same size.
+ *Examples of non-primitive types are Strings, Arrays, Classes, Interface*

[How computers work - Youtube](https://www.youtube.com/playlist?list=PLzdnOPI1iJNcsRwJhvksEo1tJqjIqWbN-)

[How computers work-notes](How_computers_work.md)


| ***Term*** | Context |
| :-: | - |
| **JavaScript** | JavaScript is the Programming Language for the Web. JavaScript can update and change both HTML and CSS. JavaScript can calculate, manipulate and validate data. |
| **conditionals** | Conditional statements are used to perform different actions based on different conditions. |
| **operators** | Operators are used to perform operations on variables and values. |
| **data types** | a variable in Java must be a specified data type (two types: Primitive/ Non-Primitive) |
| **variable** | JavaScript variables are containers for storing data values. |

**Read**

1. Duckett: JavaScript & jQuery, ***Pages 43 - 69.***
2. DO ALONG: ***pages 46 - 49***
3. Create a new repo on GitHub for the files you’ll be working with. Clone it locally.
4. Copy all the contents of the Class 6 starter-code directory into your new repo.
5. Look for the steps to follow, numbered in green circles.
6. Do steps: 1, 3 - 8 on your own computer.
7. Test it locally, to ensure it’s working as expected. Troubleshoot as needed.
8. Commit the result, and push it to your remote repo.

[How computers work-notes](How_computers_work.md)

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) 🏠 [Forward ==>](programming_with_jacascript.md)
