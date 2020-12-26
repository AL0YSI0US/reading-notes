CSS / RGB / HSL / Hex codes / Layout / Rule / Selector / Property & value / Curly braces

# Style Web Pages with CSS

:electron: [CSS MASTER CHEAT](https://overapi.com/css)

:mortar_board: [Beginner’s guide to CSS](https://friendlybit.com/css/beginners-guide-to-css-and-standards/)

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

| ***Term*** | Context |
|  :----: |  ----  |
|  **CSS**  | **Cascading Style Sheets** allows you to create rules that specify how the content of an element should appear *It reads from top to bottom*|
|  **RGB**  | These express colors in terms of how much res, green and blue are used to make it up. for example Rgb (100.100.90)  |
|  **HSL**  | **Hue.Saturation.Lightness**  |
|  **Hex codes**  | These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80  |
|  **Layout**  | how div elements appear / sections of the page all together make the layout of a web page  |
|  **Rule**  | opening and closing brackets is an example of rules they need to be performed in the right order to work as well  |
|  **Selector**  | indicate which element the rule applies to. The same rule can apply to more than one element if you seperate the element names with commas.  |
|  **Declarations**  | indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a proprty and a value), and are sepatated by a colon.  |
|  **Properties**  | indicate the aspects of the element you want to change. For example, color, font, width, height and border. |
|  **Values**  | specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be.  |
|  **Curly braces**  | Curly braces { } are special syntax in JSX. It is used to evaluate a JavaScript expression during compilation. A JavaScript expression can be a variable, function, an object, or any code that resolves into a value.  |

**Skim**
+ Duckett: HTML & CSS, Chapter 10: Introducing CSS
 
**Read**
+ Duckett: HTML & CSS, Chapter 11: Color

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](dynamic_web_pages_with_javascript.md)