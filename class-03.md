# Code 201 Reading Notes

## Class 3 

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Home](README.md) [Next Lesson ==>](class-04.md)

[<== Previous Lesson](class-02.md)

## HTML Lists, Control Flow with JS, and the CSS Box Model

![lists](https://www.mactale.com/images/css-li-styling-techniques/list-markers.jpg)

## Lists 

+ There are three types of HTML lists: **ordered, unordered, and definition**.
+ **Ordered** lists use **numbers**
+ **Unordered** lists use **bullets**
+ **Definition** lists are used to define terminology
+  ***Lists can be nestled inside one another*** (jsBook pg. 72)
+ Browser automatically indents lists. 


[Lists CW3 Schools](https://www.w3schools.com/css/css_list.asp)

![box model](https://iq.opengenus.org/content/images/2020/03/css_box_model.png)

## Boxes

+ **Content** - The content of the box, where text and images appear
+ **Padding** - Clears an area around the content. The padding is transparent
+ **Border** - A border that goes around the padding and content
+ **Margin** - Clears an area outside the border. The margin is transparent
+ **The box model** allows us to add a border around elements, and to define space between elements. 
+ CSS treats Each 

[show every box with this code]

`* {`
   `border: 1px solid red !important;`
`}`

## Box Examples
`div {`

  `width: 320px;`

  `padding: 10px;`

  `border: 5px solid gray;`

  `margin: 0;`

`}`


 320px (width)

 20px (left + right padding)

 10px (left + right border)

 0px (left + right margin)

= **350px**

**The total width of an element should be calculated like this:**

Total element width = width + left padding + right padding + left border + right border + left margin + right margin

**The total height of an element should be calculated like this:**

Total element height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin

[Boxes CW3 Schools](https://www.w3schools.com/css/css_boxmodel.asp)]

![arrays](https://miro.medium.com/max/1006/1*HJY_2vNKkNkqRQhLZcYlyg.png)

## Array Properties

| ***Property*** | Description | 
|  :----: |  ----  |   
|  **constructor**  | Returns the function that created the Array object's prototype  | 
|  **length**  | Sets or returns the number of elements in an array  |
|  **prototype**  | Allows you to add properties and methods to an Array object  |

Values in an array are accessed if they are in a numbered list. It is important to know that the numbering of this list starts a\t zero (not one).

[Array Methods CW3 Schools](https://www.w3schools.com/jsref/jsref_obj_array.asp) 

[Boolean Practice Class 3](https://github.com/codefellows/seattle-201n21/blob/master/class-03/boolean-practice.md)

## Reading

**From the Duckett HTML book:**

- Chapter 3: “Lists” (pp.62-73)
- Chapter 13: “Boxes” (pp.300-329)

**From the Duckett JS book:**

- Review - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)
- Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

[<== Home](README.md) [Next Lesson ==>](class-04.md)

[<== Previous Lesson](class-02.md)