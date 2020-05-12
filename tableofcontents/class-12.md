# Docs for the HTML `<canvas>` Element & Chart.js

## Create animated charts with chat.js

> chart.js is a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.

- Download chart.js
- copy the Chart.min.js into your directory
- In the head tag, link `<script src='Chart.min.js'></script>`

Drawing a line chart:
- add this to the body of your HTML `<canvas id="buyers" width="600" height="400"></canvas>`
- add to foot of your body: `<script>`

    `var buyers = document.getElementById('buyers').getContext('2d');`

    `new Chart(buyers).Line(buyerData);`

`</script>`

You can also draw:
- a pie chart
- a bar chart

[link to webdesignerdeport.com](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

[char.js docs](https://www.chartjs.org/docs/latest/)

## Basic usage of `<canvas>`

`<canvas>` element has only two attributes, width and height.they're optional. It requires a closing tag.

The `<canvas>` element can be styled just like any normal image (margin, border, background…)

 

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it.

> The `<canvas>` element has a method called **getContext()**, used to obtain the rendering context and its drawing functions. getContext() takes one parameter: the type of context.

## Drawing shapes with canvas

> function draw(){}

Drawing rectangles:
- fillRect(x, y, width, height) filled rectangle
- strokeRect(x, y, width, height) rectangular outline
- clearRect(x, y, width, height) clears the specified rectangular area, making it fully transparent

x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.

Drawing paths:
- beginPath() Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
- Path methods. Methods to set different paths for objects.
- closePath() Adds a straight line to the path, going to the start of the current sub-path.
- stroke() Draws the shape by stroking its outline.
- fill() Draws a solid shape by filling the path's content area.

1. First step: create a path is to call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.

2. Second step: call the methods that actually specify the paths to be drawn.

3. Third step (optional): call closePath(). This method tries to close the shape by drawing a straight line from the current point to the start. If the shape has already been closed or there's only one point in the list, this function does nothing.

Moving the pen:
- moveTo(x, y) doesn't draw anything. think as lifting the pen to a new location.
- lineTo(x, y) draws a line
- arc(x, y, radius, startAngle, endAngle, anticlockwise) Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise)
- arcTo(x1, y1, x2, y2, radius) Draws an arc with the given control points and radius, connected to the previous point by a straight line.

## Applying styles and colors

- `fillStyle = color`
Sets the style used when filling shapes.
- `strokeStyle = color`
Sets the style for shapes' outlines.

 strokeStyle and fillStyle properties accept CSS rgba color values, we can use the following notation to assign a transparent color to them.

 `ctx.strokeStyle = 'rgba(255, 0, 0, 0.5)';`

`ctx.fillStyle = 'rgba(255, 0, 0, 0.5)';`

Line Styles:

- `lineWidth = value`
Sets the width of lines drawn in the future.
- `lineCap = type`
Sets the appearance of the ends of lines.
- `lineJoin = type`
Sets the appearance of the "corners" where lines meet.
- `miterLimit = value`
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
- `getLineDash()`
Returns the current line dash pattern array containing an even number of non-negative numbers.
- `setLineDash(segments)`
Sets the current line dash pattern.

- `lineDashOffset = value`
Specifies where to start a dash array on a line.

## Drawing text

- `fillText(text, x, y [, maxWidth])`
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
- `strokeText(text, x, y [, maxWidth])`
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

Styling text:

- `font = value`
The default font is 10px sans-serif.
- `textAlign = value`
Possible values: start, end, left, right or center.
- `textBaseline = value`
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. 
- `direction = value`
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.