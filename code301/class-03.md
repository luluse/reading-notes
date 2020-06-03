# Flexbox and Templating

## Mustache

[link to article](https://medium.com/@1sherlynn/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)

Mustache is a logic-less template syntax. It works by expanding tags in a template using values provided in a hash or object.(no if statements, else clauses, or for loops)

`Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });`

`// returns: Hello, Sherlynn`


## Flexbox

### Properties for the Parent/ flex container

- `display: flex;` enables flex context for direct children. 
- `flex-direction: row | row-reverse | column | column-reverse;` 
- `flex-wrap: nowrap | wrap | wrap-reverse;` by default, flex items will try to fit onto one line.
- `flex-flow: column wrap;` shorthand for the flex-direction and flex-wrap properties,
- `justify-content:` aligns items horizontally
    - `flex-start` (default): items are packed toward the start of the flex-direction.
    - `flex-end:` items are packed toward the end of the flex-direction.
    - `start:` items are packed toward the start of the writing-mode direction.
   - `end:` items are packed toward the end of the writing-mode direction.
   - `left:` 
    - `right:`
    - `center:` items are centered along the line
    - `space-between:`
    items are evenly distributed in the line; first item is on the start line, last item on the end line
    - `space-around:` items are evenly distributed in the line with equal space around them. 
    - `space-evenly:` items are distributed so that the spacing between any two items (and the space to the edges) is equal.

- `align-items: stretch | flex-start | flex-end | center | baseline`. aligns items vertically 

- `align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline` this property has no effect when there is only one line of flex items.

### Properties for the CHILDREN/ flex items

- `flex-grow: 4; /* default 0 */` defines the ability for a flex item to grow if necessary.

- `flex-shrink: 3; /* default 1 */` ability for a flex item to shrink if necessary.

- `flex-basis:  | auto; /* default auto */`

- `align-self: auto | flex-start | flex-end | center | baseline | stretch;` allows the default alignment (or the one specified by align-items) to be overridden for individual flex items

