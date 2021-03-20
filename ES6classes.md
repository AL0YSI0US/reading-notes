[<== Home](README.md) 🏠

# ES6 Classes

💎 [Aloysious ES6 Classes Repl](https://replit.com/join/zetjdxpz-al0ysi0us) 🎬 [ES6 Classes & Data Modeling](https://www.youtube.com/watch?v=9Yc5J3Ap9-4) 🚧 [Demo Code](https://codefellows.github.io/code-301-guide-react/curriculum/prework/classes/DEMO.html)

### [Class declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes#class_declarations "Permalink to Class declarations")

One way to define a class is using a **class declaration**. To declare a class, you use the `class` keyword with the name of the class ("Aloysious" here).

```
class Aloysious {
  constructor(height, width) {
    this.age = age;
    this.hobby = hobby;
  }
}
```

### [Class expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes#class_expressions "Permalink to Class expressions")

A **class expression** is another way to define a class. Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body. (it can be retrieved through the class's (not an instance's) [`name`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/name) property, though).

```
// unnamed
let Aloysious = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Aloysious.name);
// output: "Aloysious"

// named
let Aloysious = class Aloysious2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Aloysious.name);
// output: "Aloysious2"
```

#### Hoisting

An important difference between **function declarations** and **class declarations** is that function declarations are [hoisted](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting) and class declarations are not. You first need to declare your class and then access it, otherwise code like the following will throw a [`ReferenceError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError):

```
const p = new Rectangle(); // ReferenceError

class Rectangle {}
```

### Class body and methods

+ A class body can only contain methods, but not data properties. [source](https://2ality.com/2015/02/es6-classes-final.html)

**Strict mode**

+ code written this way is subject to stricter syntax for increased performance.

**Constructor**

+ Special method used to create and initialze an object created with a `class`.
+ There can be only one method named "constructor" in a class.

**Prototype Methods**

```
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  // Getter
  get area() {
    return this.calcArea();
  }
  // Method
  calcArea() {
    return this.height * this.width;
  }
}

const square = new Rectangle(10, 10);

console.log(square.area); // 100
```

**Generator Methods**

```
  constructor(...sides) {
    this.sides = sides;
  }
  // Method
  *getSides() {
    for(const side of this.sides){
      yield side;
    }
  }
}

const pentagon = new Polygon(1,2,3,4,5);

console.log([...pentagon.getSides()]); // [1,2,3,4,5]
```

**Static methods and properties**

Static members (properties and methods) are called without instantiating: An example of class instance is `var john = new Person();` their class and **cannot** be called through a class instance. Static methods are often used to create utility functions for an application, whereas static properties are useful for caches, fixed-configuration, or any other data you don't need to be replicated across instances.

**Getters and Setters** - [Source : 2ality](https://2ality.com/2015/02/es6-classes-final.html)

The syntax for getters and setters is just like [in ECMAScript 5 object literals](http://speakingjs.com/es5/ch17.html#getters_setters):

```
class MyClass {
    get prop() {
        return 'getter';
    }
    set prop(value) {
        console.log('setter: '+value);
    }
}
```

You use `MyClass` as follows.

````javascript
let inst = new MyClass();
 inst.prop = 123;
setter: 123
 inst.prop
'getter'
````

> ES6 Classes according to Code Fellows :

### Objects and Inheritance

JavaScript objects use prototype-based inheritance. Its design is logically similar (but different in implementation) from class inheritance in strictly Object Oriented Programming languages like Java and C#.

It can be loosely described by saying that when methods or properties are attached to object’s prototype they become available for use on that object and its descendants, but not directly attached to them.

When you use class and extends keywords internally JavaScript will still use prototype-based inheritance. It just simplifies the syntax (this is often called “Syntactic Sugar”). While classes are easier to use, it’s still very important to understand how prototype-based inheritance works. It’s still at the core of the language design.

### ES6 Classes

* `function()` becomes `class {}`
* `call()` becomes `extends`
* Classes are standalone, self-contained object (instance) factories
  * Ultimately, they result in a prototype

### Additional Resources

* [Notes on ES6 obtained from](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes) - *developer.mozilla.org*
* [Classes (ES6) Sample](https://googlechrome.github.io/samples/classes-es6/) - *googlechrome.github.io*


[<== Home](README.md) 🏠
