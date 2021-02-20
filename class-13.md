# Code 201 Reading Notes

## Class 13

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-12.md) [Next Lesson ==>](class-14.md)

[<== Home](README.md)



## [HTML5 and Local Storage](https://www.dummies.com/web-design-development/site-development/html5-and-local-storage/) | dummies.com

> By Andy Harris

The local storage mechanism is a nice replacement for cookies, and with HTML5, you can write up to 5MB of data to a special file on the client. This file is not executable and cannot hold binary data (only strings), so it’s reasonably safe.

All the pages that come from your domain share the same storage area, so you can use this mechanism to keep data persistent between multiple pages. The data also stays on the client machine (until you remove it), so it can be used to keep track of information over time.

The localStorage attribute is an example of a very simple (but powerful) type of data structure called a *dictionary.* You’ve already used dictionaries many times as a Web developer. Each piece of data is stored in a *key/value* pair. The key identifies the name of the information (say ‘firstName’), and the value is the value associated with that key (‘Herbert’).

HTML attributes are dictionaries (in <a href = “http://www.google.com“>, href is the key, and http://www.google.com is the value). CSS rules are also dictionaries. (In the style rule color: red;, color is the key, and red is the value.) Some programming languages use different names for dictionaries, including associative arrays and hash tables.

Access to the local storage is through a special built-in object called localStorage(). This class has a relatively small number of methods, but they are extremely powerful and easy to use:

* **localStorage.setItem(key, value)**: Stores a value associated with a key. Essentially, key is like a variable name, and value is the value associated with that key. You can store any type of value you want, but it will be stored as string data.
* **localStorage.getItem(key):** Retrieves the value associated with the key. Again, you can think of the key as a variable name. Note that this method always returns a string value, so you might need to convert the data to another type. If the key does not exist, you will get the special value null.
* **localStorage.removeItem(key)**: Removes an item from storage. The key and the value will both be removed. This can be useful if you are running out of space. You are allotted only 5MB of space, and once it’s full, you can’t add anything else.
* **localStorage.length**: Returns the number of key/value pairs in the database. Usually used in a loop with the key() method to work with every key/value pair.
* **localStorage.key(i)** Given an integer i, this method finds the corresponding key. Note that the order of the keys is not guaranteed. Normally, this method is used in a loop to retrieve all the keys in the database. Then each key is used to look up the corresponding value.
* **localStorage.clear()**: Clears all key/value pairs from localStorage. This is a potentially destructive command, so think carefully before you use it. By definition, localStorage data is not backed up on the server (or anywhere else). Once it’s gone, it’s really gone.

Of course, any time a Web page can write data to the client machine, there is some concern for privacy and safety. However, the data is stored on the client machine, so it is never transmitted to the server (unlike cookie data). The data is stored on the client machine and belongs to the client. The 5MB limit gives a fair amount of space to Web applications, but even if it is filled, it won’t clog up modern machines. Finally, the data is stored in a plain-text format, and it can’t be put in a separate file — so it would be difficult to use this technology to create viruses and other troublesome code pests.

It may seem limiting to store data in these simple name/value pairs, but you can actually store very complex data using this mechanism. The value can be any type, including the very rich XML and JSON data storage mechanisms.

### [Window.localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) | developer.mozilla

The read-only `localStorage` property allows you to access a `Storage` object for the `Document's` origin; the stored data is saved across browser sessions. `localStorage` is similar to sessionStorage, except that while data stored in `localStorage` has no expiration time, data stored in `sessionStorage` gets cleared when the page session ends — that is, when the page is closed. (Data in a `localStorage` object created in a "private browsing" or "incognito" session is cleared when the last "private" tab is closed.)

Data stored in either `localStorage` **is specific to the protocol of the page.** In particular, data stored by a script on a site accessed with HTTP (e.g., http://example.com) is put in a different `localStorage` object from the same site accessed with HTTPS (e.g., https://example.com).

The keys and the values are always in the UTF-16 `DOMString` format, which uses two bytes per character. As with objects, integer keys are automatically converted to strings.

**Syntax**

````javascript
myStorage = window.localStorage;
````

**Example**

The following snippet accesses the current domain's local [`Storage`](https://developer.mozilla.org/en-US/docs/Web/API/Storage) object and adds a data item to it using [`Storage.setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem).

````javascript
localStorage.setItem('myCat', 'Tom');
````

The syntax for reading the `localStorage` item is as follows:

````javascript
const cat = localStorage.getItem('myCat');
````

The syntax for removing the `localStorage` item is as follows:

````javascript
localStorage.removeItem('myCat');
````

The syntax for removing **all** the `localStorage` items is as follows:

```javascript
localStorage.clear();
```

#### Bonus Reading....Potential grabber? > [typeof](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof) *mozilla.developer*

```javascript
// Objects
typeof {a: 1} === 'object';

// use Array.isArray or Object.prototype.toString.call
// to differentiate regular objects from arrays
typeof [1, 2, 4] === 'object';

typeof new Date() === 'object';
typeof /regex/ === 'object'; // See Regular expressions section for historical results

// The following are confusing, dangerous, and wasteful. Avoid them.
typeof new Boolean(true) === 'object';
typeof new Number(1) === 'object';
typeof new String('abc') === 'object';

// Functions
typeof function() {} === 'function';
typeof class C {} === 'function';
typeof Math.sin === 'function';
```

### Reading

[The past, present & future of local storage for web applications](http://diveinto.html5doctor.com/storage.html) *dive into html doctor*

[<== Previous Lesson](class-12.md) [Next Lesson ==>](class-14.md)

[<== Home](README.md)
