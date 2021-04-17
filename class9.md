# Code 301 Reading Notes

## Class 09

[<== Previous Lesson](class8.md) [Next Lesson ==>](class10.md)

[<== Home](README.md) 🏠

![](https://hackr.io/blog/functional-programming/thumbnail/large)

📷 Image: [Source](https://hackr.io/blog/functional-programming) 

## Functional Programming Concepts
> Functional programming is a programming paradigm :
> 
> a style of building the structure and elements of computer programs 
> 
> that treats computation as the evaluation of mathematical functions 
> 
> and avoids changing-state and mutable data — [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)

## Pure functions

+ They return the same result if given the same arguments (it is also referred as `deterministic`)
+ also does not cause any observable side effects.
+ It returns the same result if given the same arguments

## Immutability

When data is immutable, its state cannot change after it’s created. 

If you want to change an immutable object, you can’t. 

Instead, you create a new object with the new value.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--axNtCB_Z--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://thepracticaldev.s3.amazonaws.com/i/3f7gqqfk3v7h3tuymjqb.png)

📷 Image: [Source](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

### Refactoring Javascript for Readability [source](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

**Strategies**:

Here are some straightforward to implement methods that can lead to easier to read code. 

There are no absolutes when it comes to clean code — there's always an edge case!

### Return early from functions:
````javascript
function showProfile(user) {
  if (user.authenticated === true) {
    // ..
  }
}

// Refactor into ->

function showProfile(user) {
  // People often inline such checks
  if (user.authenticated === false) { return; }
  // Stay at the function indentation level, plus less brackets
}
````

## Cache variables so functions can be read like sentences:
````javascript
function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    for (let j = 0; j < continents[i].length; j++) {
      for (let k = 0; k < continents[i][j].tags.length; k++) {
        if (continents[i][j].tags[k] === name) {
          return continents[i][j].id;
        }
      }
    }
  }
}

// Refactor into ->

function searchGroups(name) {
  for (let i = 0; i < continents.length; i++) {
    const group = continents[i]; // This code becomes self-documenting
    for (let j = 0; j < group.length; j++) {
      const tags = group[j].tags;
      for (let k = 0; k < tags.length; k++) {
        if (tags[k] === name) {
          return group[j].id; // The core of this nasty loop is clearer to read
        }
      }
    }
  }
}
````

## Check for Web APIs before implementing your own functionality:
````javascript
function cacheBust(url) {
  return url.includes('?') === true ?
    `${url}&time=${Date.now()}` :
    `${url}?time=${Date.now()}`
}

// Refactor into ->

function cacheBust(url) {
  // This throws an error on invalid URL which stops undefined behaviour
  const urlObj = new URL(url);
  urlObj.searchParams.append('time', Date.now); // Easier to skim read
  return url.toString();
}
````


**Reading**
+ [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
+ [Refactoring Javascript for Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)


[<== Home](README.md) 🏠
