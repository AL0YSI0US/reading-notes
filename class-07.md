# Code 201 Reading Notes

## Class 7

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-06.md) [Next Lesson ==>](class-08.md)

[<== Home](README.md)

## Intro to Object-Oriented Programming with Constructor Functions; HTML Tables

[DomainModeling](https://github.com/codefellows/domain_modeling#domain-modeling)

## Tables HTML book (pp.126-145)

+ The `<table>` element is used to add tables to a web page.
+ A table is drawn out row by row. Each row is created with a `<tr>` element.
+ Inside each row there are a number of cells represented by the `<td>` element(or `<th>` if it is a header).
+ You can make cells of a table span more than one row or column uing the **rowspan** and **columnspan** attributes.
+ For long tables you can split the table into a `<thead>` [table head] `<tbody>` and `<tfoot>`.

## Functions JS Book (pp.86-99 review)

+ Allow you to group a set of related statements together that represent a single statement.
+ Can take paramaters (information required for them to do thier job)

## Objects JS Book (pp.100-128)

+ An **object** is a series of varibles and functions that represent the world around you.
+ In an object, variables are known as ***properties*** of the object; functions are known as ***methods*** of the  object. 

In real life, a car is an object.

A car has properties like weight and color, and methods like start and stop:

**Object	Properties	Methods**
	
car.name = Fiat

car.model = 500

car.weight = 850kg

car.color = white	

car.start()

car.drive()

car.brake()

car.stop()

All cars have the same properties, but the property values differ from car to car.

All cars have the same methods, but the methods are performed at different times.

> JavaScript variables are containers for data values.

This code assigns a simple value (Fiat) to a variable named car:

`var` `car` = `"Fiat";`

Objects are variables too. But objects can contain many values.

This code assigns many values (Fiat, 500, white) to a variable named car:

`var` `car` = `{type:"Fiat", model:"500", color:"white"};`

The values are written as **name:value pairs** (*name and value separated by a colon*).

JavaScript objects are containers for named values called properties or methods.

Object Definition

You define (and create) a JavaScript object with an **object literal**:

Example

`var` `person` = `{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};`

Spaces and line breaks are not important. An object definition can span multiple lines:

Example

var person = {

  firstName: "John",

  lastName: "Doe",

  age: 50,

  eyeColor: "blue"

};

Object Properties

The name:values pairs in JavaScript objects are called properties:

Property	Property Value

firstName	John

lastName	Doe

age	50

eyeColor	blue

Accessing Object Properties

You can access object properties in two ways:

`objectName.propertyName` or `objectName["propertyName"]`

[Objects CW3 Schools](https://www.w3schools.com/js/js_objects.asp)

## Methods JS Book  (pp.106-144)

[this tutorial JavaScript](https://javascript.info/object-methods)

> In a function definition, this refers to the "owner" of the function.

In the example above, this is the person object that "owns" the fullName function.

In other words, `this.firstName` means the firstName property of this object.

JavaScript methods are actions that can be performed on objects.

A JavaScript method is a property containing a function definition.

[Methods CW3 Schools](https://www.w3schools.com/js/js_object_methods.asp)




**From the Duckett HTML book**:

+ Chapter 6: “Tables” (pp.126-145)

**From the Duckett JS Book**:

+ Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

[<== Previous Lesson](class-06.md) [Next Lesson ==>](class-08.md)

[<== Home](README.md)

