# Code 201 Reading Notes

## Class 9

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-08.md) [Next Lesson ==>](class-10.md)

[<== Home](README.md) 🏠

## HTML Forms and JS Events

![JSevents](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/JavaScript-Event-Types.jpg)

## Forms HTML book (p.144-175)

> Adding text...Making choices...Submitting forms

+ **Form Structure** (pp.151-162)
+ **Labeling Form Controls** (pp.163)
+ **Grouping Form Elements** (pp.164)
+ **Form Validation** (pp.165)
+ **Date input** (pp.066)
+ **Email and URL input** (pp.167)
+ **Search input** (pp.168)

> *Radio buttons cannot be deselected, when agreeing to things like terms and conditions use a checkbox instead.*

> The `<label>` element makes a form more accessible to vision impaired users.

> Information from a form is sent in **name/value** pairs.

**The HTML `<input>` element is the most used form element.**

An `<input>` element can be displayed in many ways, depending on the `type` attribute.

`Type` =	Description

`<input type="text">`	Displays a single-line text input field

`<input type="radio">`	Displays a radio button (for selecting one of many choices)

`<input type="checkbox">`	Displays a checkbox (for selecting zero or more of many choices)

`<input type="submit">`	Displays a submit button (for submitting the form)

`<input type="button">`	Displays a clickable button

[Forms](https://www.w3schools.com/html/html_forms.asp) W3Schools

## Lists, Tables & Forms HTML book (pp.330-357)

> Forms are easier to use if the form controls are vertically alinged using CSS

List markers can be given different appearances using the `list-style-type` and `list-style` image properties.

[Web-Developer Tool](https://chrispederick.com/work/web-developer/) < Chris Pederick

`tr:hover {background-color: #f5f5f5;}` for `<tr>` makes table rows color change when the user scrolls over it.

Lookup "Zebra" to alternate row colors for increased visibility. I'ts an nth thang.

## Events JS book (pp.243-292)

When an event occurs, the **event** object tells you information about the event, and the element it happened upon.

![eventpropogation](https://dmitripavlutin.com/static/9a8fc772a94452ca819295094c99b1a9/7c84e/javascript-event-propagation-5.webp)

[Event Delegation](https://dmitripavlutin.com/javascript-event-delegation/) < Dmitri Pavlutin

**Event Delegation**

Creating event listeners for a lot of elements cal slow down a page, but event flow allows you to listen for an event on a parent element.

**Changing Default Behavior**

The event object has methods that change: the default behavior of an element and how the element's ancestors respond to the event.

[jQuery Events](https://www.w3schools.com/jquery/jquery_events.asp) W3Schools

## Reading

**From the Duckett HTML book**:

+ Chapter 7: **“Forms”** (p.144-175)
+ Chapter 14: **“Lists, Tables & Forms”** (pp.330-357)

**From the Duckett JS book**:

+ Chapter 6: “Events” (pp.243-292)

[<== Previous Lesson](class-08.md) [Next Lesson ==>](class-10.md)

[<== Home](README.md) 🏠
