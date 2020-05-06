# More CSS Layout

#### Containing elements

If one block-level element sits inside another block-level element, the outert box is known as the **containing** or **parent** element.

#### Controlling the position of elements

- **Normal flow**. Every block-level appears on a new line. Each item appears one after another vertically down the page. 
- **Relative positioning**. Moves an element from the position it would be in normal flow.
- **Absolute positioning**. Positions the element  in relation to its containing element.
- **Fixed positioninig**. Position the element in relation to the browser window. Elemeont do not move when the user scrolls up and down.
- **Floating elements**. Allows to take tha element out of normal flow and position it to the far left or far right of a containing box. Becomes a block-level element where other content can flow around. Always use the width property to indicate how wide the floated element should be.

If boxes overlap, `z-index` property allows you to control which box appears on top. 

To indicate where a box should be positioned, you can use **box offset** properties and tell the browser how far from top/bottom/left/right it should be placed. Properties are usually given in px, percentages or ems.

Using float to place elements side-by-side:
- Give width and float property to the selector

Clearing property:
- add clear class to yout element
- .clear allows you to say that no element shoud touch the side of a box. Values can be: left, right, both, none. 

#### Multi column
- create a div element for each column
- assign a class
- set properties: width, float, margin

#### Fixed width layout
Do not change size as the user increase or decrease the size of their browser window.

Width of boxes specified in pixels. create <div> an assign class or Id.

#### Liquid layout
Stretch and contract as the user increase or decrease the size of their browser window.

Width of boxes specified in percentages. (adding min-width and max-width properties can help create boundries)

#### 960 pixel grid

960 pixels wide made of 12 columns of 60 pixels wide.each column has a margin of 10 pixels and 10 pixels on left and right side of the page. 