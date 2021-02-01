# Code 201 Reading Notes

## Class 8

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-07.md) [Next Lesson ==>](class-09.md)

[<== Home](README.md) 

## CSS Layout

[CSS CHEATSHEET](https://overapi.com/css)

[HTML Wireframe Codefellows](https://codefellows.github.io/code-201-guide/curriculum/class-08/lab-a/)

[Lorem Ipsum](https://lipsum.com/)

`<img` `src="https://placehold.it/200x300/ddd"/>` produces the an image, with a width of 200 pixels, a height, of 300 pixels, and color of #DDD, which is a light gray.

[CSS NOTES](class-02.md)

**Refresher**

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

## Layout Duckett HTML book (pp.359-404)

+ `<div>` Elements are often used as containing elements to group together sections of a page [can create a grid with them]
+ Browsr displays the page in a normal flow unless you specify relative, absolute, or fixed positioning.
+ The float proprty moves content to the left or right and can be used to create milti column layouts. (*Floated layouts require a defined width*)
+ pages can be fixed width or *stretchy* layouts
+ 960-1000 pixles wide (*industry standard*)
+ Top 60% of the page is reserved for what the site is about (*to demonstrate relevance without scrolling*)
+ Grids helpp create professional and flexible designs
+ CSS frameworks provide rules for common tasks.
+ You can include multiple CSS files in one page (Helpful for styling each page or setting a baseline for each page like your top banner or logos appearing throughout the site.)

## Reading

**From the Duckett HTML book**:

+ Chapter 15: “Layout” (pp.359-404)

[<== Previous Lesson](class-07.md) [Next Lesson ==>](class-09.md)

[<== Home](README.md) 