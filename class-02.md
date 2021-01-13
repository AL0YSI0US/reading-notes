# Code 201 Reading Notes

## Class 2

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

## Introducing CSS / Basic JavaScript Instructions / Decisions and Loops

[CSS MASTER CHEAT](https://overapi.com/css)

[Beginner’s guide to CSS](https://friendlybit.com/css/beginners-guide-to-css-and-standards/)

[https://chris.beams.io/posts/git-commit/](https://chris.beams.io/posts/git-commit/)

> The seven rules of a great Git commit message 

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters 
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

> **Structural Markup** the elements you can use to describe both the headings and paragraphs.

> **Semantic Markup** provides different informtion; such as where the mphasis is placed in a sentence, that something you have written is a quotation (and who said it), the meaning of acronyms, and so on. 

> HTML elements (*semantic information*) are used to describe the structures of the page. (e.g. headings, subheadings, paragraphs).

> They also provide semantic information (e.g. where emphasis should be placed, the definition of any acronynms used, when given text is a quotation).

## Semantic Markup

* `<h1>`-`<h6>` : `<h1>`main `<h2>`subheading `<h3>`-`<h6>`sections beyond subheading 
* `<strong>` element has **strong** importance, will be in ***bold*** 
* `<em>` emphasis has subtly changed, will be in *italics*  
* `<blockquote>` pg. 52 : element is used for longer qoutes that take up an entie paragraph. (*no lazy inenting, use CSS for page indents*)
* `<q>` shorter quotes that sit between the paragraph 
* `<abbr>` If you use an abbreviation or an acronym, the the `<abbr>` element can be used. A ***Title Attribute*** on the opening tag is used to fully specify the full term
* `<cite>`  when referencing  
* `<dfn>`  is used to indicate the defining instance of a new term. The first time you explain tome new terminology (perhaps an acedemic concept or some jargon) in a document, it is known as the defining instance of it  
* `<adress>` SPECIFIC PURPOSE: Contains contact details for the author of a page.  
* `<ins>`  *underline* content has been inserted into a document 
* `<del>` *line through* element can show that text has been deleted from it 
* `<s>` : `<p><s>`Price was 999.99`</s></p>` Indicates something is no longer accurate or relavant (but that it should not be deleted). Creates a strike through content, old HTML placed an underline 
* `<hCard>`   ``<a` `class="h-card"` `href="http://waterpigs.co.uk">`
`<img` `src="/photo.png" alt="" /> Barnaby Walters</a>`  



## CSS Syntax

A CSS rule-set consists of a selector and a declaration block:

![css syntax](https://www.w3schools.com/css/selector.gif)

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.


**There are three ways of inserting a style sheet:**
+ External CSS
+ Internal CSS
+ Inline CSS

## Cascading Order

All the styles in a page will "cascade" into a new "virtual" style sheet by the following rules, where number one has the highest priority:

1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

So, an inline style has the highest priority, and will override external and internal styles and browser defaults.

## The CSS id Selector

The id selector uses the id attribute of an HTML element to select a specific element.

The id of an element is unique within a page, so the id selector is used to select one unique element!

To select an element with a specific id, write a hash **(#)** character, followed by the id of the element.

> The CSS rule below will be applied to the HTML element with `id="para1"`: (view in raw mode to view propper formatting)

#para1 {
  text-align: center;
  color: red;
}

## The CSS class Selector

The class selector selects HTML elements with a specific class attribute.

To select elements with a specific class, write a period **(.)** character, followed by ***the class name***.

*In this example all HTML elements with* `class="center"` will be `red` and `center-aligned:`*

.center {
  text-align: center;
  color: red;
}

*You can also specify that only specific HTML elements should be affected by a class.*

In this example only `<p>` elements with class="center" will be center-aligned:

p.center {
  text-align: center;
  color: red;
}
## The CSS Universal Selector

The universal selector **(*)** selects all HTML elements on the page.

`*` {
  text-align: center;
  color: blue;
}

> **UNIVERSAL BORDERS**

`*` {
  border: solid: black; 1px
}

## The CSS Grouping Selector
The grouping selector selects all the HTML elements with the same style definitions.

h1, h2, p {
  text-align: center;
  color: red;
}

## Cascading Style Sheets
- The style portion of the website
- How does HTML differ from CSS?
- comes after HTML
- uses different language /  vocabulary
- Reads from top to bottom
- Include values like size of text or images
- can add directly into HTML document of have its own page
- scalibility
- Makes troubleshooting easier (each issue lies in an individual file or section of the website be it html / js / css / etc)

## There are five important rules for coding with HTML tags.

1. Tags are always surrounded by angle brackets (less-than/greater-than characters), as in `<HEAD>`.

2. Most tags come in pairs and surround the material they affect. They work like a light switch: the first tag turns the action on, and the second turns it off. (There are some exceptions. For instance, the < BR > tag creates a blank line and doesn't have an "off switch." Once you've made a line break, you can't unmake it.)

3. The second tag--the "off switch"--always starts with a forward slash. For example, you turn on bold with `<B>`, shout your piece, and then go back to regular text with `</B>`.

4. First tag on, last tag off. Tags are embedded, so when you start a tag within another tag, you have to close that inner tag before closing the outer tag. For instance, the page will not display properly with the tags in this order:

`<HEAD><TITLE>`Your text`</HEAD></TITLE>`

The correct order is:

`**<HEAD><TITLE>`Your text`</TITLE></HEAD>**`

5. Many tags have optional attributes that use values to modify the tag's behavior. The `<P>` (paragraph) tag's ALIGN attribute, for instance, lets you change the default (left) paragraph alignment. For example, `<P` `ALIGN=CENTER>` centers the next paragraph on the page.

## JavaScript Variables

[W3Schools Variables](https://www.w3schools.com/js/js_variables.asp)

JavaScript variables are containers for storing data values.

In this example, x, y, and z, are **variables**, ***declared*** with the **var** keyword:

Example

**var** x = **5**;

**var** y = **6**;

**var** z = x + y;

From the example above, you can expect:

**x** stores the value **5**

**y** stores the value **6**

**z** stores the value **11**

## DATA TYPES

[W3Schools Data Types](https://www.w3schools.com/java/java_data_types.asp)

> A variable in Java must be a specified data type.

**Data types are divided into two groups:**

+ Primitive data types - includes byte, short, int, long, float, double, boolean and char
+ Non-primitive data types - such as String, Arrays and Classes

## Primitive Data Types

A primitive data type specifies the size and type of variable values, and it has no additional methods.

## Non-Primitive Data Types

Non-primitive data types are called reference types because they refer to objects.

**The main difference between primitive and non-primitive data types are:**

+ Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).
+ Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
+ A primitive type has always a value, while non-primitive types can be null.
+ A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
+ The size of a primitive type depends on the data type, while non-primitive types have all the same size.
+ *Examples of non-primitive types are Strings, Arrays, Classes, Interface*

[Storing data in variables - Khanacademy](https://www.khanacademy.org/computing/ap-computer-science-principles/programming-101/storing-variables/a/assigning-variables)

[Storing strings in variables - Khanacademy](https://www.khanacademy.org/computing/ap-computer-science-principles/programming-101/strings/a/storing-strings-in-variables)

[JavaScript Strings](https://www.javascript.com/learn/strings)

## Enclosing quotation marks

Let’s say you’re trying to use quotation marks inside a string. You’ll need to 

use opposite quotation marks inside and outside. That means strings containing 

single quotes need to use double quotes and strings containing double quotes need 

to use single quotes.

**EXAMPLE**

"It's six o'clock.";

'Remember to say "please" and "thank you."';

Alternatively, you can use a backslash \ to escape the quotation marks. This lets 

JavaScript know in advance that you want to use a special character.

Here’s what that looks like reusing the examples above:

**EXAMPLE**

'It\'s six o\'clock.';

"Remember to say \"please\" and \"thank you.\"";

## Using a Variable to store a boolean

**JavaScript Boolean**

Boolean is a primitive data type in JavaScript. Boolean can have only two values, 

**true** or **false**. It is useful in controlling program flow using conditional 

statements like ***if..else, switch, while, do..while.***

**Boolean object**

JavaScript includes Boolean object to represent true or false. It can be 

initialized using new keyword.

**Example:** Boolean object

1. JavaScript Boolean data type can store one of two values, true or false.
2. Boolean objects can be created using new keyword. e.g. var YES = new Boolean(true);
3. JavaScript treats an empty string (""), 0, undefined and null as false. Everything else is true.
4. Boolean methods are used to perform different tasks on Boolean values.

**Boolean Methods**

Primitive or Boolean object includes following methods.

toLocaleString()	Returns string of boolean value in local browser environment.

**Example:** var result = (1 > 2); result.toLocaleString(); // returns "false"

toString()	Returns a string of Boolean.

**Example:** var result = (1 > 2); result.toString(); // returns "false"

valueOf()	Returns the value of the Boolean object.

**Example:** var result = (1 > 2); result.valueOf(); // returns false

[Boolean - tutorialsteacher](https://www.tutorialsteacher.com/javascript/javascript-boolean)

[Naming conventions W3Schools](https://www.w3schools.com/js/js_conventions.asp)

## Reading

From the Duckett HTML book:

- Chapter 2: “Text” (pp.40-61)
- Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)

From the Duckett JS book:

- Chapter 2: “Basic JavaScript Instructions” (pp.53-84)
- Chapter 4: “Decisions and Loops” (pp.145-162)

[<== Home](README.md) [Next Lesson ==>](class-03.md)

[<== Previous Lesson](201_class_1.md)