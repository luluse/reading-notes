# SMACSS and Responsive Web Design

## Responsive Web Design

[link to article](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

> Practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

### 3 main components

1. Flexible Layouts

Flexible grids are built using relative length units, most commonly percentages or em units.

CSS3 introduced some new relative length units, specifically related to the viewport size of the browser or device. These new units include vw, vh, vmin, and vmax. 

**vw** Viewports width

**vh** Viewports height

**vmin** Minimum of the viewport’s height and width

**vmax** Maximum of the viewport’s height and width

> But support isn't great.

Other solution:take all of the fixed units of length and turn them into relative units.

Take the target width of an element and dividing it by the width of it’s parent element. The result is the relative width of the target element.

> target ÷ context = result

`width: 63.197026%;    /* 340px ÷ 538px = .63197026 */`  

For even more control within a flexible layout, you can also leverage the min-width, max-width, min-height, and max-height properties.

2.  Media Queries

Media queries provide the ability to specify different styles for individual browser and device circumstances. 

`/* @media Rule */
@media all and (max-width: 1024px) {...}`

3 logical operators: **and**, **not**, and **only**.

- Height and width features

`@media all and (min-width: 320px) and (max-width: 780px) {...}`

- Orientation Feature

`@media all and (orientation: landscape) {...}`

3.  Flexible Media

- Mobile First. This approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

> avoid CSS3 shadows, gradients, transforms, and animations within mobile styles. 

- Viewport

`<meta name="viewport" content="width=device-width">`

Will define the height or width of the viewport.

To control how a website is scaled on a mobile device, and how users can continue to scale a website, use the minimum-scale, maximum-scale, initial-scale, and user-scalable properties. Values should always be a positive integer between 0 and 10.

`<meta name="viewport" content="initial-scale=1">`

always have ability to scale on, allows accessibility and and desired usability for users.

`<meta name="viewport" content="user-scalable=yes">`

When combining multiple viewport properties, separate them by comma.Recommnded viewport values:

`<meta name="viewport" content="width=device-width, initial-scale=1">`

- Flexible Media

One quick way to make media scalable is by using the max-width property with a value of 100%. 

`img, video, canvas {
  max-width: 100%;
}`

Doesn't work for third party websites who use iframes. Solution: 
- the embedded element needs to be absolutely positioned within a parent element. 
- The parent element needs to have a width of 100% so that it may scale based on the width of the viewport. 

## All about Floats

[link to article](https://css-tricks.com/all-about-floats/)

- Four values: left, right, none, inherit
- clearing the float: use **clear** property.
    - both (clears floats coming from either direction)
    - left/right (clear the float from one direction respectively)
    - none (is the default)

- The great collapse. If this parent element contained nothing but floated elements, the height of it would literally collapse to nothing
    - We fix it by clearing the float after the floated elements in the container but before the close of the container
    - Empty Div method `<div style="clear: both;"></div>`
    - Overflow Method 
    - Easy Clearing Method uses a pseudo selector `:after`. apply an additional class to parent element and apply this to CSS. `.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}`

## Don't Overthink It Grids

[link to article](https://css-tricks.com/dont-overthink-it-grids/)

- Set columns width and float property

- Clearing context:

`.grid:after {
  content: "";
  display: table;
  clear: both;
}`

- Gutters:

  - When we set a width, that element stays that width, despite padding or borders being applied.
`box-sizing: border-box;`

  - apply a fixed padding to the right side of all columns except the last one.

## CSS Floats Explained By Riding An Escalator

[link to article](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)

> Floats create alternate flows.

## Scalable and Modular Architecture for CSS

[link to documentation](http://smacss.com/)

 > pronounced “smacks”

 SMACSS is a way to examine your design process and as a way to fit those rigid frameworks into a flexible thought process.