## HTML Lists

-  **Ordered lists**. Created with the `<ol>` element. Each item in the list is placed between `<li></li>`.

-  **Unordered lists**. Created with the `<ul>` element. Each item in the list is placed between `<li></li>`.

- **Definition lists**. Created with the `<dl>` element. Inside you will see pairs of `<dt>`(contains the term being defined- *definition term*) and `<dd>` (contains the *definition*). 

- **Nested lists**. To create a nested list you can put a `<ul>` element inside a `<li>` element.

## CSS Boxes

#### Box dimensions

By default a box is sized just big enough to hold its content. To set your own dimensions, use **width** and **height** properties. 

Ways to specify size of a box: 
- pixels (most popular)
- percentages
- ems


#### Limiting width

Some pages design shrink and expand the fit the size of the user screen. **mid-width** and **max-width** properties specify the smallest or maximum size the box can be displayed. Very helpful to ensure that the content of pages are legible. 

#### Limiting height

Use **mid-height** and **max-height** properties.

#### Overflowing content

If the box is not big enough to hold the content. The content expands outside the box and becomes messy. The **overflow** property tells the browser what to do with the content.
- `overflow: hidden;` Simply hides extra content that does not fit in the box
- `overflow: scroll;` Adds a scroll bar to the box

### Border, Margin, Padding

Every box has 3 properties that can be ajusted to control its appearance.

- The border separates the edge of one box from another.
- Margin sits outside the edge of the border. Creates gaps between borders
- Padding is the space between the content of a box and its border

#### Border

- border-width property. Value can be given in pixel or using one of these values: **thin**, **medium**, **thick**.

- border-style property. solid, dotted, dashed, double, groove, ridge, inset, outset, hidden/none. 

- border-color property. RGB values, hex codes, css color names. 

- border property allows you to specify width, style and color in one property. Values must be coded in that specific order.

#### Padding

- padding property. most often specified in pixels.

#### Margin

- margin property. commmonly given in pixels. 

#### Centering content

If you want to center a box on the page: 
- set a width for the box
- set the margin-left and margin-right to **auto**
- add a text-align property

#### Change inline/block

**display** property allows to turn an inline element into block level element. The values can be:
- `display: inline;` causes a block element to act like an inline element.
- `display: block;` causes an inline element to act like a block element.
- `display: inline-block;` causes a block level element to flow like an inline element while retaining other features of block level element.
- `display: none;` Hides an element from the page.

#### Hiding boxes

visibility property allows you to hide boxes from users but leaves a space where the element would have been. This property takes two values:
- `visibility: hidden;` A blank space will appear in its place
- `visibility: visible;` 

## CSS3

#### Border images

border-image property applies an image to the border of a box. It needs:
- The url of the image
- Where to slice the image
- What to do with the straight edges: **stretch** the image, **repeat** the image. 

The box must havea border width for the image to be shown.

#### Box Shadows

box shadow property allows you to add drop shadow around the box. It must use:
- horizontal offset in px
- vertical offset in px
- blur distance in px
- color 

#### Rounded corners

border-radius property. The value indicates the size of the radius in pixels.
`border-radius: 10px;`


## Js Control Flow - Decisions and Loops

#### If else statements

Check a condition:
- If it resolves to **true** the first code block is executed
- If it resolves to **false** the second code block is run instead

#### Switch Statement

A switch statement sstarts with a variable called the switch value. Each case indicates a possible value for thsi variable and the code that should run if the variable matches tha value.
At the end of each case there is a **break** keyword. Tells the browers it is done with this statement and can run next block.

#### Type coercion

JS can convert data behind the scenes to complete an operation. It is called type coercion.

#### Loops

Loops check a condition. If it returns true, a code block will run. It repeats until the condition returns false.

3 types of loops:

- FOR if you need to run code a specific number of times.
- WHILE code will continue the loop for as long as the condition is true.
- DO WHILE will run the statements inside the curly brackets at least once even if the condition evaluates false.
`for (var i = 0; i < 10; i++) { document.write(i); }`

`(var i = 0; i < 10; i++) is the condition counter document.write(i);` is the code to execute during loop (between the curly brackets).

#### Loop counter

A **for** loop uses a counter as a condition. This instructs the code to run a specified amount of times.

Condition is made of 3 statements:

- **initialization**. Create a variable and set it to 0 `var i = 0;`
- **condition**. The loop should continue until the counter reaches a specified number `i < 10;`
- **update**. Everytime the loop runs, it adds one to the counter `i++`

A while loop will continue to run as long as the condition in the parenthesis are true. `while (i < 10)`