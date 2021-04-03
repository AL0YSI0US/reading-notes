# Code 301 Reading Notes

## Class 05

[<== Previous Lesson](class4.md) [Next Lesson ==>](class6.md)

[<== Home](README.md) 🏠

> Elements are what components are "made of”. . .
>
> The only method you *must* define in a `React.Component` subclass is called [`render()`](https://reactjs.org/docs/react-component.html#render) . . .

![lifecycleMethods](https://scontent.xx.fbcdn.net/v/t1.15752-0/s526x296/168443649_2902845933328871_5182715657245160561_n.png?_nc_cat=104&ccb=1-3&_nc_sid=58c789&_nc_ohc=8FCrcftofDAAX9sPp-F&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&_nc_tp=30&oh=b0b1079f3bb4981751b6c837ef027832&oe=608C8D7E)

+ [react-lifecycle-methods-diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

## React Docs

**The difference between state and props** [{ `Component State` }](https://reactjs.org/docs/faq-state.html#what-is-the-difference-between-state-and-props) - *React Docs*

`props` get passed to the c omponent (similar to function parameters)

whereas `state` is managed within the component (similar to variables declared within a function).

**Things to consider about data in regards to `state`** :

1. Is it passed in from a parent via `props`? If so, it probably isn't `state`.
2. Does it remain unchanged over time? If so, it probably isn't `state`.
3. Can you compute it based on any other `state` or `props` in your `component`? If so, it isn't state.

##### ✏️ RAW NOTES . . . r e p e t i t i o n . . .

What can I remember about rendering **Hello World**

**App.js** - default parent, Import React, App(css) and Header.js to the top of this page...then export.

````javascript
import React from 'react';
import './App.css';
import Header from './Header.js';

class App extends React.Component {
  render(){
    return(
    <div>
      <Header />
    </div>
    )
  }
}

export default App;

````

**Header.js** Import React, Header(css) to the top of this page, `return`: `<h1></h1>`...then export.

````javascript
import React from 'react';
import './Header.css';

class Header extends React.Component {
  render() {
    return(<h1>Aloysious remembers bits and pieces</h1>);
  }
}

export default Header; 
````

### Reading

* [React Docs - thinking in React](https://reactjs.org/docs/thinking-in-react.html)

[<== Home](README.md) 🏠
