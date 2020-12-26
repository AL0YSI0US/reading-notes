CSS / RGB / HSL / Hex codes / Layout / Rule / Selector / Property & value / Curly braces

# Style Web Pages with CSS

:electron: [CSS MASTER CHEAT](https://overapi.com/css)

:mortar_board: [Beginner’s guide to CSS](https://friendlybit.com/css/beginners-guide-to-css-and-standards/)

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

To select an element with a specific id, write a hash (#) character, followed by the id of the element.

**The CSS rule below will be applied to the HTML element with id="para1":**

#para1 {
  text-align: center;
  color: red;
}

## The CSS class Selector

The class selector selects HTML elements with a specific class attribute.

To select elements with a specific class, write a period (.) character, followed by the class name.

*In this example all HTML elements with class="center" will be red and center-aligned:*

.center {
  text-align: center;
  color: red;
}

*You can also specify that only specific HTML elements should be affected by a class.*

In this example only <p> elements with class="center" will be center-aligned:

p.center {
  text-align: center;
  color: red;
}
## The CSS Universal Selector

The universal selector **(*)** selects all HTML elements on the page.

* {
  text-align: center;
  color: blue;
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
- Makes troubleshooting easier (each issue lies in an individual file or section of rthe website be it html / js / css / etc)

## There are five important rules for coding with HTML tags.

1. Tags are always surrounded by angle brackets (less-than/greater-than characters), as in < HEAD >.

2. Most tags come in pairs and surround the material they affect. They work like a light switch: the first tag turns the action on, and the second turns it off. (There are some exceptions. For instance, the < BR > tag creates a blank line and doesn't have an "off switch." Once you've made a line break, you can't unmake it.)

3. The second tag--the "off switch"--always starts with a forward slash. For example, you turn on bold with < B >, shout your piece, and then go back to regular text with < /B >.

4. First tag on, last tag off. Tags are embedded, so when you start a tag within another tag, you have to close that inner tag before closing the outer tag. For instance, the page will not display properly with the tags in this order:

< HEAD >< TITLE >Your text< /HEAD >< /TITLE >.

The correct order is:

< HEAD >< TITLE >Your text< /TITLE >< /HEAD >.

5. Many tags have optional attributes that use values to modify the tag's behavior. The < P > (paragraph) tag's ALIGN attribute, for instance, lets you change the default (left) paragraph alignment. For example, < P ALIGN=CENTER > centers the next paragraph on the page.

## Opacity / Transparency

The opacity property specifies the opacity/transparency of an element. It can take a value from 0.0 - 1.0. The lower value, the more transparent.

| ***Term*** | Context |
|  :----: |  ----  |
|  **CSS**  | **Cascading Style Sheets** allows you to create rules that specify how the content of an element should appear *It reads from top to bottom*|
|  **RGB**  | **rgb(red, green, blue)** These express colors in terms of how much res, green and blue are used to make it up. for example Rgb (100.100.90) *Each parameter (red, green, and blue) defines the intensity of the color between 0 and 255.* |
|  **HSL**  | Hue, Saturation, Lightness: **Hue** is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue. **Saturation** is a percentage value, 0% means a shade of gray, and 100% is the full color. **Lightness** is also a percentage, 0% is black, 50% is neither light or dark, 100% is white |
|  **HSLA Value**  | **hsla(hue, saturation, lightness, alpha)** The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all):  |
|  **Hex codes**  | These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80 *In CSS, a color can be specified using a hexadecimal value in the form:* **#rrggbb** *Where rr (red), gg (green) and bb (blue) are hexadecimal values between 00 and ff (same as decimal 0-255).* |
|  **Layout**  | how div elements appear / sections of the page all together make the layout of a web page  |
|  **Rule**  | opening and closing brackets is an example of rules they need to be performed in the right order to work as well  |
|  **Selector**  | indicate which element the rule applies to. The same rule can apply to more than one element if you seperate the element names with commas.  |
|  **Declarations**  | indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a proprty and a value), and are sepatated by a colon.  |
|  **Properties**  | indicate the aspects of the element you want to change. For example, color, font, width, height and border. |
|  **Values**  | specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be.  |
|  **Curly braces**  | Curly braces { } are special syntax in JSX. It is used to evaluate a JavaScript expression during compilation. A JavaScript expression can be a variable, function, an object, or any code that resolves into a value.  |
|  **Comments**  | Comments are used to explain the code, and may help when you edit the source code at a later date. *Comments are ignored by browsers.* |
|  **Colors**  | Colors are specified using predefined color names, or RGB, HEX, HSL, RGBA, HSLA values.  |

**Skim**
+ Duckett: HTML & CSS, Chapter 10: Introducing CSS
 
**Read**
+ Duckett: HTML & CSS, Chapter 11: Color

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](dynamic_web_pages_with_javascript.md)