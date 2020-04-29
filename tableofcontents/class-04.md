## HTML Links

Links are created using the `<a href=""></a>` element. The text between the opening and closing tag is called **link text**.

Linking to other websites: the value of the href attribute will be the full web address for the site. it is known as **absolute** URL.

Linking to other pages on the same site: use the **relative** URL. The href attribute is just the name of the file if all the pages are in the same folder.
- same folder: use fileName.html
- child folder: use nameOfTheChildFolder/fileName.html
- grandchild folder: use childFolder/grandChildFolder/fileNAme.html
- parent folder: use ../FileName.html
- grandparent folder: use ../../fileName.html

Email links:
- `<a href="mailto:lulu@gmail.com">Email Lulu</a>`

opening links to a new window:
- add attribute `target=_blank` in the `<a>` tag.

Linking to a specific part of same page:
- add list of contents at the top of page
- add an Id attribute to sections you want to link.

## CSS Layout

### Positionnning elements

#### Building blocks

CSS treats each HTML element as if it is in its on box:

- block level box: start on a new line and acts like the main builing block. `<h1>` `<p>` `<ul>` `<li>`
- inline box: flow between surrounding text. `<img>` `<i>` `<b>`

#### Containing elements

If one block-level element sits inside another block-level element, the outert box is known as the **containing** or **parent** element.
It is common to group a number of elements together inside a `<div>` element

#### Controlling the position of elements

- **Normal flow**. Every block-level appears on a new line. Each item appears one after another vertically down the page. 
- **Relative positioning**. Moves an element from the position it would be in normal flow.
- **Absolute positioning**. Positions the element  in relation to its containing element.
- **Fixed positioninig**. Position the element in relation to the browser window. Elemeont do not move when the user scrolls up and down.
- **Floating elements**. Allows to take tha element out of normal flow and position it to the far left or far right of a containing box. Becomes a block-level element where other content can flow around. Always use the width property to indicate how wide the floated element should be.

If boxes overlap, `z-index` property allows you to control which box appears on top. 

To indicate where a box should be positioned, you can use **box offset** properties and tell the browser how far from top/bottom/left/right it should be placed. Properties are usually given in px, percentages or ems.

## JS Functions


Functions let you group a series of statements together to perform a specific task, they’re packed in a **code block**.

When you ask a function to perform its task, it is known as **calling** the function.

Pieces of information passed to a function are called **parameters**.

When you write a function, you expect an answer, the response is called a **return value**.

#### Declaring a function

`function sayHello() { Document.write(‘Hello!’); }`

- **function** is the function keyword
- **sayHello()** is the function name
- The code block is between the curly brackets

#### Calling a function

When a function is declared, you can use it several times in your code to perform the same task by typing the **function name** where you need it. `sayHello();`

> Declare the function before calling it.

#### Declaring a function that needs information

When you declare a function you give it **parameters**. Inside the function, the parameters act like **variables**.

`function getArea(width,height) { Return width * height; }`

Each time you call the function, the values could be different.

When you call a function that has parameters, you specify the values it should use in the parentheses that follow the name. The values are called **arguments**. They can be values or variables.

arguments as values: `getArea(3, 5);`
arguments as variables: `wallWidth = 3; wallHeight = 5; getArea(wallWidth, wallHeight);`

#### Getting a single value out of a function

