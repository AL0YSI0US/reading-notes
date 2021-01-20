# Code 201 Reading Notes

## Class 4 

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Home](README.md) [Next Lesson ==>](class-05.md)

[<== Previous Lesson](class-03.md)

## HTML Links, JS Functions, and Intro to CSS Layout

1. [CSS MASTER CHEAT](https://overapi.com/css)
2. [learnlayout.com](http://learnlayout.com) practical entry point into layout
3. [CSS Zen Garden](http://www.csszengarden.com/) allows you to practice CSS styling and see how others have styled the same HTML code.
4. [Centering in CSS](https://css-tricks.com/centering-css-complete-guide/) has some helpful tips for centering content horizontally and vertically.
5. [Floats in CSS](https://medium.freecodecamp.org/css-floats-explained-by-riding-an-escalator-57fa55232333) as explained by riding an escalator.
6. [CSS Snapshot 2020](https://www.w3.org/TR/CSS/#css)
7. [CSS EXAMPLES - JavaTpoint](https://www.javatpoint.com/css-tutorial)

## URL | Uniform Resource Locator | Relative URL

![url photo codecamp images](https://cdn-media-1.freecodecamp.org/images/1*YunI3ChUVMlpmFzo75FczQ.png)

> **Uniform Resource Locator** navigates to a website outside of your own

> **Relative URL** navigates user to anothe page within your websites directory

## Links [Duckett HTML] (pp.74-93)

+ Links are created using the `<a>` **Element**
+ The `<a>` tag uses the ``href` **Attribute** to indicate the page you are linking to
+ Linking to pages within your own site = Relative url with specified file path included in the url

1. You can create links to open email programs. 
2. You can create links to open a new window. (It is a good measure to include a disclaimer which informs the user that they will be directed elsewhere or may need pop up blocker to be disabled)
3. You can use the **id** *attribute* to target *elements* within a page that can e linked to. 

1. **emailto:** `<a href="mailto:aloysious@example.org">`Email Aloysious`</a>`
2. **target** `<a href="http://imdb.com" target="_blank">`Internet Movie Database`</a>` (Opens in a new window)
3. **id** (Link at **top** of page)`<h1 id="top>`Film Making Terms`</h1>`
4.  **id** (Link at **bottom** of page)`<p>``<a href="#top">`Film Making Terms`</a>``</p>`

## Layout [Duckett HTML] (pp.358-404)

+ `<div>` Elements are often used as containing elements to group together sections of a page [can create a grid with them]
+ Browsr displays the page in a normal flow unless you specify relative, absolute, or fixed positioning.
+ The float proprty moves content to the left or right and can be used to create milti column layouts. (*Floated layouts require a defined width*)
+ pages can be fixed width or *stretchy* layouts
+ 960-1000 pixles wide (*industry standard*)
+ Top 60% of the page is reserved for what the site is about (*to demonstrate relevance without scrolling*)
+ Grids helpp create professional and flexible designs
+ CSS frameworks provide rules for common tasks.
+ You can include multiple CSS files in one page (Helpful for styling each page or setting a baseline for each page like your top banner or logos appearing throughout the site.)

## Positioning Schemes

+ **NORMAL FLOW** Boxes in the normal flow belong to a formatting context, which may be block or inline, but not both simultaneously. Block-level boxes participate in a block formatting context. Inline-level boxes participate in an inline formatting context.
+ **RELATIVE POSITIONING** The box's position is calculated according to the normal flow (this is called the position in normal flow). Then the box is offset relative to its normal position. When a box B is relatively positioned, the position of the following box is calculated as though B were not offset. The effect of 'position:relative' on table-row-group, table-header-group, table-footer-group, table-row, table-column-group, table-column, table-cell, and table-caption elements is undefined.
+ **ABSOLUTE POSITIONING** The box's position (and possibly size) is specified with the 'top', 'right', 'bottom', and 'left' properties. These properties specify offsets with respect to the box's containing block. Absolutely positioned boxes are taken out of the normal flow. This means they have no impact on the layout of later siblings. Also, though absolutely positioned boxes have margins, they do not collapse with any other margins.
+ **FIXED POSITIONING** The box's position is calculated according to the 'absolute' model, but in addition, the box is fixed with respect to some reference. As with the 'absolute' model, the box's margins do not collapse with any other margins. In the case of handheld, projection, screen, tty, and tv media types, the box is fixed with respect to the viewport and does not move when scrolled. In the case of the print media type, the box is rendered on every page, and is fixed with respect to the page box, even if the page is seen through a viewport (in the case of a print-preview, for example). For other media types, the presentation is undefined. Authors may wish to specify 'fixed' in a media-dependent way. For instance, an author may want a box to remain at the top of the viewport on the screen, but not at the top of each printed page. The two specifications may be separated by using an @media rule, as in:
+ **STATIC** The box is a normal box, laid out according to the normal flow. The 'top', 'right', 'bottom', and 'left' properties do not apply.
+ **FLOATING ELEMENTS** The float CSS property places an element on the left or right side of its container, allowing text and inline elements to wrap around it. The element is removed from the normal flow of the page, though still remaining a part of the flow (in contrast to absolute positioning).

[Visual formatting model](https://www.w3.org/TR/CSS2/visuren.html#normal-flow)

[SELECTORS](https://www.w3.org/TR/CSS/#selectors)

[PROPERTIES](https://www.w3.org/TR/CSS/#properties)

## Functions, Methods, and Objects [Duckett JS] (pp.86-99 ONLY)

**JavaScript Function Syntax**

+ A JavaScript function is defined with the function keyword, followed by a **name**, followed by parentheses **()**.
+ Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).
+ The parentheses may include parameter names separated by commas: (parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: **{}**

function name(parameter1, parameter2, parameter3) `{`
 
  // code to be executed

`}`

Function **parameters** are listed inside the parentheses () in the function definition.

Function **arguments** are the **values** received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

> A Function is much the same as a Procedure or a Subroutine, in other programming languages.

**Function Invocation**

The code inside the function will execute when "something" **invokes** (calls) the function:

- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)


Function Return
When JavaScript reaches a `return` statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.

Functions often compute a **return value**. The return value is "returned" back to the "caller":

**EXAMPLE**

Calculate the product of two numbers, and return the result:

`var` `x` `=` `myFunction``(4, 3)``;`   // Function is called, return value will end up in **x**

`function` `myFunction``(a, b)` `{`
  `return` `a *b;`             // Function returns the product of `a` and `b`
`}`
The result in **x** will be:

**12**  [Notes above W3Schools Functions](https://www.w3schools.com/js/js_functions.asp)

## The JavaScript this Keyword

The JavaScript `this` keyword refers to the object it belongs to.

> It has different values depending on where it is used:

> In a method, `this` refers to the **owner object**.

> Alone, `this` refers to the **global object**.

> In a function, `this` refers to the **global object**.

> In a function, in strict mode, `this` is `undefined`.

> In an event, `this` refers to the element that received the event.

> Methods like `call()`, and `apply()` can refer `this` to **any object**. [this W3Schools](https://www.w3schools.com/js/js_this.asp)

## Pair Programming 

The **Driver** is the programmer who is typing and the only one whose hands are on the keyboard. Handling the “mechanics” of coding, the **Driver** manages the text editor, switching files, version control, and—of course writing—code. The ***Navigator*** uses their words to guide the **Driver** but does not provide any direct input to the computer. 

The **Navigator** thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The **Navigator** might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

## Reading 

**From the Duckett HTML book:**
+ Chapter 4: Ch.4 “Links” (pp.74-93)
+ Chapter 15: “Layout” (pp.358-404)

**From the Duckett JS book:**
+ Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)
+ Article: [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

[layout of webpages](http://htmlandcssbook.com/code-samples/chapter-15/)

[<== Home](README.md) [Next Lesson ==>](class-05.md)

[<== Previous Lesson](class-03.md)