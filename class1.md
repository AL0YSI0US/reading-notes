# Code 301 Reading Notes

## Class 01

[Next Lesson ==>](class2.md)

[<== Home](README.md) 🏠

# Introduction to React and Components

## React Tutorial through Passing Data Through Props

+ React is a flexible JavaScript library for creating user interfaces.
+ Each React component is encapsulated and can operate independently.
+ The React Devtools extension for Chrome and Firefox lets you inspect a React component tree with your browser's developer tools.
+ **To collect data from multiple children, or to have two child components communicate with each other**, one must declare the shared state in their parent component instead. The parent component can pass the state back down to the children by using props; this keeps the child components in sync with each other and with the parent component.
+ [Tic Tac Toe - Codepen](https://codepen.io/gaearon/pen/gWWZgR?editors=0010)

## React Docs - hello world

The smallest React example looks like this:

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

It displays a heading saying “Hello, world!” on the page.

> **Things to consider when reading React documentation:**

* We define variables with [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) and [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) statements. For the purposes of the React documentation, you can consider them equivalent to [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).
* We use the `class` keyword to define [JavaScript classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes). There are two things worth remembering about them. Firstly, unlike with objects, you *don't* need to put commas between class method definitions. Secondly, unlike many other languages with classes, in JavaScript the value of `this` in a method [depends on how it is called](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes#Boxing_with_prototype_and_static_methods).
* We sometimes use `=>` to define [&#34;arrow functions&#34;](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions). They're like regular functions, but shorter. For example, `x => x * 2` is roughly equivalent to `function(x) { return x * 2; }`. Importantly, arrow functions [don&#39;t have their own `this` value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#No_separate_this) so they're handy when you want to preserve the `this` value from an outer method definition.


## React Docs - introducing JSX

to be continued...

## React Docs - rendering elements

to be continued...

## React Docs - Components and props

to be continued...

#### Reading

* [React Tutorial through Passing Data Through Props](https://reactjs.org/tutorial/tutorial.html)
* [React Docs - hello world](https://reactjs.org/docs/hello-world.html)
* [React Docs - introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
* [React Docs - rendering elements](https://reactjs.org/docs/rendering-elements.html)
* [React Docs - Components and props](https://reactjs.org/docs/components-and-props.html)

[<== Home](README.md) 🏠
