# Code 301 Reading Notes

## Class 02

[<== Previous Lesson](class1.md) [Next Lesson ==>](class3.md)

[<== Home](README.md) 🏠

# States and Props

## React Docs - State and Lifecycle

+ State is similar to props, but it is private and fully controlled by the component.

#### Converting a Function to a Class

You can convert a function component like `Clock` to a class in five steps:

1. Create an [ES6 class](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes), with the same name, that extends `React.Component`.
2. Add a single empty method to it called `render()`.
3. Move the body of the function into the `render()` method.
4. Replace `props` with `this.props` in the `render()` body.
5. Delete the remaining empty function declaration.

#### Adding Lifecycle Methods to a Class

In applications with many components, it's very important to free up resources taken by the components when they are destroyed.

+ Setting up a clock that is rendered to the DOM for the first time is an example of“mounting” in React.
+ Clearing a clock timer would be considered“unmounting” in React.

> Before you can access the **files** on a **file system**, you need to **mount** the **file system**. **Mounting** a **file system** attaches that **file system** to a directory (**mount** point) and makes it available to the **system**. The root ( / ) **file system** is always **mounted**. [source](https://www.google.com/search?q=mounting+and+unmounting+file+system+in+unix&rlz=1C1CHBD_enUS773US773&oq=mounting+and+unmounting+&aqs=chrome.0.0l3j69i57j0l3j0i390l2.4850j1j7&sourceid=chrome&ie=UTF-8)


## React Docs - handling events

+ React events are named using camelCase, rather than lowercase.
+ With JSX you pass a function as the event handler, rather than a string.
+ you cannot return `false` to prevent default behavior in React.
+ You must call `preventDefault` explicitly.

**For example, with plain HTML, to prevent the default link behavior of opening a new page, you can write:**

````html
<a href="#" onclick="console.log('The link was clicked.'); return false">
  Click me
</a>
````

**In React this could instead be:**

````javascript
function ActionLink() {
---------------------------------------------
  function handleClick(e) {
    e.preventDefault();                         <=========   Function
    console.log('The link was clicked.');
  }
---------------------------------------------
  return (
---------------------------------------------
    <a href="#" onClick={handleClick}>           <=========   Return
---------------------------------------------
      Click me
    </a>
  );
}
````

## React Docs - conditional rendering

> Determining When to Re-Render in React

The main benefit of immutability is that it helps you build *pure components* in React. Immutable data can easily determine if changes have been made, which helps to determine when a component requires re-rendering.

+ In React, **function components** are a simpler way to write components that only contain a `render` method and don’t have their own state. Instead of defining a class which extends `React.Component`, we can write a function that takes `props` as input and returns what should be rendered. Function components are less tedious to write than classes, and many components can be expressed this way.

## React Tutorial through Developer Tools

> Note:
>
> In [JavaScript classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes), you need to always call `super` when defining the constructor of a subclass. All React component classes that have a `constructor` should start with a `super(props)` call.

+ To collect data from multiple children, or to have two child components communicate with each other, you need to declare the shared state in their parent component instead. The parent component can pass the state back down to the children by using props; this keeps the child components in sync with each other and with the parent component.

Lifting state into a parent component is common when React components are refactore

## React Bootstrat Documentation

## Netlify

### Reading

* [React Docs - State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
* [React Docs - handling events](https://reactjs.org/docs/handling-events.html)
* [React Docs - conditional rendering](ttps://reactjs.org/docs/conditional-rendering.html)
* [React Tutorial through Developer Tools](https://reactjs.org/tutorial/tutorial.html)

### Bookmark/Skim

* [React Bootstrap Documentation](https://react-bootstrap.github.io/)
* [Netlify](https://www.netlify.com/)

[<== Home](README.md) 🏠
