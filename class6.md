# Code 301 Reading Notes

## Class 06

[<== Previous Lesson](class5.md) [Next Lesson ==>](class7.md)

[<== Home](README.md) 🏠

# Readings: NODE.JS

### An Introduction to Node.js 

{ `sitepoint.com/an-introduction-to-node-js` }

### “Hello, World!” the Node.js Way

Check to see if Node is installed by opening a terminal and typing `node -v`

Next, create a new file `hello.js` and copy in the following code:

```javascript
console.log("Hello, World!");
```

This uses Node’s [built-in console module](https://nodejs.org/api/console.html#console_console) to display a message in a terminal window. To run the example, enter the following command:

```bash
node hello.js
```

If Node.js is configured properly, “Hello, World!” will be displayed.


### NPM : Installing a Package Globally

Open your terminal and type the following:

```bash
npm install -g jshint
```

This will install the [jshint package](https://www.npmjs.com/package/jshint) globally on your system. We can use it to lint the `index.js` file from the previous example:

```
jshint index.js
```

You should now see a number of ES6-related errors. If you want to fix them up, add `/* jshint esversion: 6 */` to the top of the `index.js` file, re-run the command and linting should pass.


### Installing a Package Locally

We can also install packages locally to a project, as opposed to globally, on our system. Create a `test` folder and open a terminal in that directory. Next type this:

```bash
npm init -y
```

This will create and auto-populate a `package.json` file in the same folder. Next, use npm to install the [lodash package](https://www.npmjs.com/package/lodash) and save it as a project dependency:

```bash
npm install lodash --save
```

Create a file named `test.js` and add the following:

```javascript
const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];
console.log(_.compact(arr));
```

Finally, run the script using `node test.js`. You should see `[ 1, 2, 3 ]` output to the terminal.

+ *F U R T H E R  . R E A D I N G*
+ [The Anatomy of a Modern JavaScript Application](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/)

### 6 Reasons for Pair Programming


## Pair Programming

{ `.codefellows.org/blog/6-reasons-for-pair-programming` }

The **Driver** is the programmer who is typing and the only one whose hands are on the keyboard. Handling the “mechanics” of coding, the **Driver** manages the text editor, switching files, version control, and—of course writing—code. The ***Navigator*** uses their words to guide the **Driver** but does not provide any direct input to the computer.

The **Navigator** thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The **Navigator** might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

## Reading

* [An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js)
* [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

### Bookmark/Skim

* [Geocoding API Docs](https://locationiq.com/)
* [Axios docs](https://www.npmjs.com/package/axios)
* [MDN async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)

[<== Home](README.md) 🏠
