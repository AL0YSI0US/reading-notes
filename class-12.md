# Code 201 Reading Notes [![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](http://commonmark.org)

## Class 12

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-11.md) [Next Lesson ==>](class-13.md)

[<== Home](README.md)

## Docs for the HTML `<canvas>` Element & Chart.js

> Selected Readings

## [Easily create animated charts with chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

#### [Chart.js](https://www.chartjs.org/docs/latest/) // [js Samples](https://www.chartjs.org/samples/latest/)

```
FOR INSTALLATION:
npm install chart.js --save
```

````javascript
                 / Startup: Copy the Chart.min.js

            // Then create a new html page and import the script:

<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>

To draw a line chart create a canvas element in HTML in which  Chart.js can draw the chart. 

                              Add this to the body of our HTML page:

                             <canvas id="buyers" width="600" height="400"></canvas>

        Add this to the foot of the body element:

       <script>
            var buyers = document.getElementById('buyers').getContext('2d');
            new Chart(buyers).Line(buyerData);
        </script>

Inside the same script tags > create the data, in this instance it’s an object that contains 
labels for the base of the chart and datasets to describe the values on the chart. 
  
        Add this immediately above the line that begins ‘var buyers=’:

var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
````


## [Basic Usage of Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

#### [The `<canvas>` element](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage#the_%3Ccanvas%3E_element "Permalink to The  element")

```
<canvas id="tutorial" width="150" height="150"></canvas>
```

At first sight a [`<canvas>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas) looks like the [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) element, with the only clear difference being that it doesn't have the `src` and `alt` attributes. Indeed, the `<canvas>` element has only two attributes, [`width`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas#attr-width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas#attr-height). These are both optional and can also be set using [DOM](https://developer.mozilla.org/en-US/docs/Glossary/DOM) [properties](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement). When no `width` and `height` attributes are specified, the canvas will initially be **300 pixels** wide and **150 pixels** high. The element can be sized arbitrarily by [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS), but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

**Note:** If your renderings seem distorted, try specifying your `width` and `height` attributes explicitly in the `<canvas>` attributes, and not using CSS.

The [`id`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id) attribute isn't specific to the `<canvas>` element but is one of the [global HTML attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes) which can be applied to any HTML element (like `<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class">class</a>` for instance). It is always a good idea to supply an `id` because this makes it much easier to identify it in a script.

The `<canvas>` element can be styled just like any normal image ([`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin), [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border), [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background)…). These rules, however, don't affect the actual drawing on the canvas. We'll see how this is done in a [dedicated chapter](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors) of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.

```
        Rendering:
 
              var canvas = document.getElementById('tutorial');
              var ctx = canvas.getContext('2d');

Note: it is not good practice to embed a script inside HTML. We do it here to keep the example concise.

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8"/>
    <title>Canvas tutorial</title>
    <script type="text/javascript">
      function draw() {
        var canvas = document.getElementById('tutorial');
        if (canvas.getContext) {
          var ctx = canvas.getContext('2d');
        }
      }
    </script>
    <style type="text/css">
      canvas { border: 1px solid black; }
    </style>
  </head>
  <body onload="draw();">
    <canvas id="tutorial" width="150" height="150"></canvas>
  </body>
</html>
```

## [Drawing shapes with canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

The grid

![](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes/canvas_default_grid.png)Before we can start drawing, we need to talk about the canvas grid or **coordinate space**. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the *top left* corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

````java
          There are three functions that draw rectangles on the canvas:

fillRect(x, y, width, height)
                Draws a filled rectangle.
strokeRect(x, y, width, height)
                Draws a rectangular outline.
clearRect(x, y, width, height)
                Clears the specified rectangular area, making it fully transparent.

Each of these three functions takes the same parameters. x and y specify the 
position on the canvas (relative to the origin) of the top-left corner of the rectangle. 
width and height provide the rectangle's size.
````


## [Applying styles and colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

````javascript
fillStyle = color
         // Sets the style used when filling shapes.
strokeStyle = color
           // Sets the style for shapes outlines.
          // color is a string representing a CSS <color>, a gradient object, or a pattern object.
         // By default, the stroke and fill color are set to black (CSS color value #000000).

      // Note: When you set the strokeStyle and/or fillStyle property, the new value becomes
     // the default for all shapes being drawn from then on. For every shape you want in a
    // different color, you will need to reassign the fillStyle or strokeStyle property.

  // The valid strings you can enter should, according to the specification,
 // be CSS <color> values. Each of the following examples describe the same color.

// these all set the fillStyle to 'orange'

ctx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
````

In this example, we once again use two `for` loops to draw a grid of rectangles, each in a different color. The resulting image should look something like the screenshot. There is nothing too spectacular happening here. We use the two variables `i` and `j` to generate a unique RGB color for each square, and only modify the red and green values. The blue channel has a fixed value. By modifying the channels, you can generate all kinds of palettes. By increasing the steps, you can achieve something that looks like the color palettes Photoshop uses.

````javascript
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  for (var i = 0; i < 6; i++) {
    for (var j = 0; j < 6; j++) {
      ctx.fillStyle = 'rgb(' + Math.floor(255 - 42.5 * i) + ', ' +
                       Math.floor(255 - 42.5 * j) + ', 0)';
      ctx.fillRect(j * 25, i * 25, 25, 25);
    }
  }
}
````


## [Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text#drawing_text "Permalink to Drawing text")

The canvas rendering context provides two methods to render text:

````javascript
fillText(text, x, y [, maxWidth])
// Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.


                             ....A fillText example.....

The text is filled using the current fillStyle.

function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}

            ....The text is filled using the current strokeStyle.....

function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.strokeText('Hello world', 10, 50);
}
````

There are some more properties which let you adjust the way the text gets displayed on the canvas:

`font = value`
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.

`textAlign = valu`
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

`textBaseline = value`
Baseline alignment setting. Possible values: `top`, `hanging`, `middle`, `alphabetic`, `ideographic`, `bottom`. The default value is `alphabetic`.[`direction = value`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/direction "direction = value")Directionality. Possible values: `ltr`, `rtl`, `inherit`. The default value is `inherit`.These properties might be familiar to you, if you have worked with CSS before.

The following diagram from the WHATWG demonstrates the various baselines supported by the textBaseline property.

![variousBaselines](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text/baselines.png)

[`font = value`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/font "font = value")The current text style being used when drawing text. This string uses the same syntax as the [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font) property. The default font is 10px sans-serif.[`textAlign = value`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textAlign "textAlign = value")Text alignment setting. Possible values: `start`, `end`, `left`, `right` or `center`. The default value is `start`.[`textBaseline = value`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/textBaseline "textBaseline = value")Baseline alignment setting. Possible values: `top`, `hanging`, `middle`, `alphabetic`, `ideographic`, `bottom`. The default value is `alphabetic`.[`direction = value`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/direction "direction = value")Directionality. Possible values: `ltr`, `rtl`, `inherit`. The default value is `inherit`.These properties might be familiar to you, if you have worked with CSS before.

The following diagram from the [WHATWG](https://www.whatwg.org/) demonstrates the various baselines supported by the `textBaseline` property.

## [HTML canvas lineTo( ) Method](https://www.w3schools.com/tags/canvas_lineto.asp)

The lineTo() method adds a new point and creates a line TO that point FROM the last specified point in the canvas (this method does not draw the line).

**Tip:** Use the [stroke()](https://www.w3schools.com/tags/canvas_stroke.asp) method to actually draw the path on the canvas.

````javascript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.moveTo(0, 0);     // Begin a path, move to position 0,0.
ctx.lineTo(300, 150); // Create a line to position 300,150:
ctx.stroke();
````

**Javascript  Syntax**

| **Parameter**|  Description

**x**  The x-coordinate of where to create the line to

**y**  The y-coordinate of where to create the line to

[<== Previous Lesson](class-11.md) [Next Lesson ==>](class-13.md)

[<== Home](README.md
)
